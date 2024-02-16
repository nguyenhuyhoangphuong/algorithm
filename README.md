# algorithm
Bài toán của NAL
import java.util.Scanner;

public class DemChuCaiTiengViet {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Nhập vào chuỗi chữ cái latin: ");
        String chuoiNhapVao = scanner.nextLine();
        int soLuongChuVietTat = demSoLuongChuVietTat(chuoiNhapVao);
        System.out.println("Số lượng chữ cái Tiếng Việt có thể được tạo ra là: " + soLuongChuVietTat);
        scanner.close();
    }
    public static int demSoLuongChuVietTat(String chuoi) {
        int soLuong = 0;
        char[] chuVietTat = {'ă', 'â', 'đ', 'ê', 'ô', 'ơ', 'ư'};
        for (int i = 0; i < chuoi.length(); i++) {
            char kyTu = chuoi.charAt(i);
            if (kyTu == 'ă' || kyTu == 'â' || kyTu == 'đ' || kyTu == 'ê' || kyTu == 'ô' || kyTu == 'ơ' || kyTu == 'ư') {
                soLuong++;
            }
        }
        return soLuong;
    }
}
