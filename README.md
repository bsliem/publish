# Pháp tụng hằng ngày

Bộ ba trang HTML độc lập để tụng kinh/chú từng câu trên máy tính, iPhone và GitHub Pages. Không cần cài Node.js, R hay máy chủ web.

## Mở trên GitHub Pages

Sau khi đẩy thư mục này lên repository GitHub:

1. Vào repository → **Settings** → **Pages**.
2. Ở mục **Build and deployment**, chọn **Deploy from a branch**.
3. Chọn branch chứa các tệp HTML (thường là `main`) và thư mục `/(root)`.
4. Nhấn **Save**, chờ GitHub Pages hoàn tất triển khai.
5. Mở một trong các đường dẫn sau (thay `bsliem` bằng tên tài khoản/repository của bạn nếu khác):

   - `https://bsliem.github.io/publish/leng_yan_jing.html`
   - `https://bsliem.github.io/publish/di_zang_jing.html`
   - `https://bsliem.github.io/publish/ri_zong.html`

Nếu repository không tên là `publish`, thay phần `/publish/` trong URL bằng tên repository thực tế.

## Các trang

| Tệp | Nội dung |
| --- | --- |
| `leng_yan_jing.html` | Đại Phật Đỉnh Thủ Lăng Nghiêm Kinh |
| `di_zang_jing.html` | Địa Tạng Bồ Tát Bổn Nguyện Kinh |
| `ri_zong.html` | Nhật tụng: tiền hành, Lăng Nghiêm Chú, Đại Bi Chú, thập tiểu chú, Tâm Kinh, hồi hướng |

## Cách tụng và điều hướng

- Mỗi màn hình hiển thị câu chính ở giữa, chữ lớn; câu trước/sau hiện nhỏ và mờ để theo dõi.
- Nhấn `←` / `→` trên bàn phím để về câu trước / sang câu sau.
- Nhấn `Space` để sang câu sau khi không đặt con trỏ trong ô nhập.
- Nhấn `↑` / `↓` để cuộn trang.
- Chạm nửa trái của khung kinh để về câu trước; chạm nửa phải để sang câu sau.
- Vuốt ngang để đổi câu. Kéo lên/xuống chỉ cuộn trang, không đổi câu.
- Dùng thanh kéo hoặc ô số `第 … / … 句` để nhảy đến câu bất kỳ trong phần đang chọn.
- `A−` / `A+` thay đổi cỡ chữ.
- `搜尋` chỉ tìm trong quyển/phẩm/phần đang chọn.

## Riêng trang Nhật tụng

Các câu chú có dạng:

```text
南無薩怛他 # 如來
```

Khi đến câu đó, nút `註解` xuất hiện dưới khung câu tụng. Nhấn nút để xem nội dung ở sau dấu `#`.

## Sao chép và ghi chú

- Nút `複製` sao chép câu trước, câu chính và câu sau để dán sang ứng dụng khác.
- Mục `筆記` lưu ngày giờ, phần/câu hiện tại, câu kinh, mốc MP3 và nội dung ghi chú.
- Mỗi ghi chú có `前往` để trở về đúng câu đã ghi, `編輯` để sửa và `刪除` để xóa.
- Tiến độ và ghi chú được tự lưu trong trình duyệt trên thiết bị đang dùng.

## Đồng bộ giữa nhiều thiết bị

Git chỉ đồng bộ **tệp HTML**, không đồng bộ dữ liệu tiến độ/ghi chú đã lưu trong trình duyệt.

Để chuyển tiến độ và ghi chú sang iPhone hoặc máy khác:

1. Mở `進度備份`.
2. Nhấn `匯出進度` để tải tệp JSON.
3. Chuyển tệp JSON sang thiết bị kia.
4. Trên thiết bị kia, mở cùng trang HTML → `進度備份` → `匯入進度`.

> Khi nhập, tiến độ và ghi chú hiện có trên thiết bị đích sẽ được thay bằng dữ liệu trong tệp sao lưu.

## Cập nhật trang web

Sau khi sửa HTML:

```bash
git add leng_yan_jing.html di_zang_jing.html ri_zong.html README.md
git commit -m "Cập nhật trang tụng"
git push
```

GitHub Pages thường cập nhật sau ít phút. Nếu vẫn thấy giao diện cũ, tải lại mạnh trang (`Cmd + Shift + R` trên macOS) hoặc mở lại trang trong trình duyệt.

