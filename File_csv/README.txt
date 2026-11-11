DU LIEU MAU - QUAN LY SAN GIAO DICH BAT DONG SAN
=================================================

Thu muc nay gom 13 file CSV:
- 12 bang chinh theo thiet ke: PhongKinhDoanh, MoiGioi, ChuSoHuu,
  KhachHang, BatDongSan, HopDongKyGui, LichXemNha, HopDongDatCoc,
  GiaoDich, HoaHong, HopDongMuaBan, HopDongThue.
- TinDang.csv la bang phu tro de kiem thu Business Rule ky gui doc quyen.

DINH DANG
- CSV ma hoa UTF-8 with BOM (UTF-8-SIG), phu hop mo bang Excel.
- Ngay: YYYY-MM-DD.
- Thoi gian: YYYY-MM-DD HH:MM:SS.
- Tien: so nguyen VND, khong co dau phay phan tach hang nghin.
- Mot so truong khong ap dung duoc de trong.

THU TU IMPORT DE TRANH LOI KHOA NGOAI
1. PhongKinhDoanh.csv
2. ChuSoHuu.csv
3. KhachHang.csv
4. MoiGioi.csv
5. BatDongSan.csv
6. HopDongKyGui.csv
7. LichXemNha.csv
8. HopDongDatCoc.csv
9. GiaoDich.csv
10. HoaHong.csv
11. HopDongMuaBan.csv
12. HopDongThue.csv
13. TinDang.csv (neu tao bang TinDang)

LUU Y QUAN TRONG
- CSV chi chua du lieu, khong tao bang va khong tao khoa/rang buoc.
  Hay tao database va cac bang trong SQL Server truoc khi import.
- Trong SQL Server, cot NgayHetHan co the la computed column:
  khong import cot nay neu ban khai bao AS DATEADD(...).
  Neu muon import truc tiep CSV, hay khai bao NgayHetHan la cot DATE,
  hoac bo cot nay va tinh tu NgayDatCoc khi truy van.
- GiaoDich.MaHDDC co gia tri rong o mot so dong; khi import, can chuyen
  chuoi rong thanh NULL.
- Cac gia tri LoaiBDS, LoaiKyGui, LoaiGiaoDich va TrangThai dang dung
  khong dau de de dong bo voi cac lenh SQL mau.
- Du lieu duoc tao de minh hoa va kiem thu 8 truy van; khong phai du lieu
  bat dong san that.
