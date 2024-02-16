# algorithm
Bài toán của NAL

import java.util.Scanner;
public class DemChuCaiTiengViet {
   
    public static void main(String[] args) {
       
        Scanner scanner = new Scanner(System.in);

        // Nhập chuỗi từ người dùng
        System.out.print("Nhập vào chuỗi chữ cái latin: ");
        String chuoiNhapVao = scanner.nextLine();

        // Đếm số lượng chữ cái Tiếng Việt trong chuỗi nhập vào
        int soLuongChuVietTat = demSoLuongChuVietTat(chuoiNhapVao);

        // Hiển thị số lượng chữ cái Tiếng Việt đã được tạo ra
        System.out.println("Số lượng chữ cái Tiếng Việt có thể được tạo ra là: " + soLuongChuVietTat);

        scanner.close();
    }

    // Phương thức để đếm số lượng chữ cái Tiếng Việt có thể được tạo ra từ chuỗi chữ cái Latin
    public static int demSoLuongChuVietTat(String chuoi) {
        int soLuong = 0;
        char[] chuVietTat = {'ă', 'â', 'đ', 'ê', 'ô', 'ơ', 'ư'};

        // Duyệt qua từng ký tự trong chuỗi
        for (int i = 0; i < chuoi.length(); i++) {
            char kyTu = chuoi.charAt(i);

            // Kiểm tra xem ký tự có trong danh sách các chữ cái Tiếng Việt không
            if (kyTu == 'ă' || kyTu == 'â' || kyTu == 'đ' || kyTu == 'ê' || kyTu == 'ô' || kyTu == 'ơ' || kyTu == 'ư') {
                soLuong++;
            }
        }

        return soLuong;
    }
}

