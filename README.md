import os
import shutil
import requests

# آدرس URL فایل‌های صوتی و عکس
audio_url = "https://example.com/path/to/audio/file.mp3"
image_url = "https://example.com/path/to/image/file.jpg"

# مسیر ذخیره فایل‌ها بر روی فلش
flash_drive_path = os.path.join(os.getcwd(), "downloaded_files")

# ایجاد پوشه برای ذخیره فایل‌ها
if not os.path.exists(flash_drive_path):
    os.makedirs(flash_drive_path)

# دانلود فایل صوتی
audio_file_path = os.path.join(flash_drive_path, "audio_file.mp3")
response = requests.get(audio_url)
with open(audio_file_path, 'wb') as file:
    file.write(response.content)
print(f"فایل صوتی دانلود شده و در {audio_file_path} ذخیره شد.")

# دانلود فایل عکس
image_file_path = os.path.join(flash_drive_path, "image_file.jpg")
response = requests.get(image_url)
with open(image_file_path, 'wb') as file:
    file.write(response.content)
print(f"فایل عکس دانلود شده و در {image_file_path} ذخیره شد.")
