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
_Ti�u chuan MDCD X�t dieu kien if (year%4 == 0 && year%100 != 0) || (year%400 == 0)

No.	year%400	year%4	year%100	K?t qu?
1	T	-	-	T
2	F	T	F	T
3	F	T	T	F
4	F	F	-	F
_ �o bao phu: 72,8%
