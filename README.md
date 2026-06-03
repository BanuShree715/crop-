# crop-
from pathlib import Path

import cv2


def main() -> None:
    image_path = Path(__file__).resolve().parent / "leaf.jpg"
    image = cv2.imread(str(image_path))

    if image is None:
        print(f"Error: Image not found or unreadable at {image_path}")
        return

    h, w, c = image.shape
    print(f"Image loaded successfully: {image_path}")
    print(f"Dimensions: {w}x{h}, Channels: {c}")


if __name__ == "__main__":
    main()
