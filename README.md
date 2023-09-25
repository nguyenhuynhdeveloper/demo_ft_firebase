https://firebase.google.com/docs/flutter/setup?platform=android
Buổi 13 : học về firebase 13/9/2022
Phải cài được cái Firebase CLI
npm install -g firebase-tools
firebase login

dart pub global activate flutterfire_cli

export PATH="$PATH":"$HOME/.pub-cache/bin" Cứ chạy k báo gì cả
flutterfire configure
di chuyển lên xuống đúng dự án của mình đúng hệ điều hành

Platform Firebase App Id
web 1:658114513459:web:0dd104dc777b03b5073146
android 1:658114513459:android:5332b658030638ff073146
ios 1:658114513459:ios:d77593ade05bfa29073146
macos 1:658114513459:ios:d77593ade05bfa29073146

Sau đó ở lib phải có được

// Cài đặt thư viện firebase
flutter pub add firebase_core

khởi tạo firebase ở
void main() async {
WidgetsFlutterBinding.ensureInitialized();
await Firebase.initializeApp(
options: DefaultFirebaseOptions.currentPlatform,
);
runApp(const MyApp());
}

authentication là tính năng đăng ký đăng nhập bằng firebase

lên console firebase enable phần

storage gửi và nhận file giữa các máy
cơ chế ảnh lưu ở firebase storage

Buổi 14 : Học tiếp về firebase ngày 15/9/2022
Cloud fileStore là update của realtime database
realtime chỉ là file json , chứa các chuỗi Json

chọn chế độ test mode 1 tháng sẽ hết

chọn nơi lưu server , cứ để nguyên mặc định

Chỉ cần pull code về và ghi đè file google service .json

echo "# demo_ft_firebase" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/nguyenhuynhdeveloper/demo_ft_firebase.git
git push -u origin main
