_B�i to�n: kiem tra xem 1 nam c� phai nam nhuan kh�ng

	+ Nam nhuan l� nam chia het cho 4 v� kh�ng chia het cho 100 hoac chia het cho 400.
	+ H�m test: 
public int getNumber(int year) {
        int result = -1;

        if (year < 0) {
            return result;
        }

        result = 0;
        if (year % 4 == 0 && year % 100 != 0
                || year % 400 == 0) {
            while (year != 0) {
                result = result * 10 + year % 10;
                year /= 10;
            }
        }
        return result;

	+)h�m intgetNumber(intyear): nhap v�o 1 nam bat ki 
