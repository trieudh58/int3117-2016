      0.	public boolean ham(int n) {                                                                 
      1.		int tong = 0;
      2.		int i = 0;
      3.		while (n > 0) {
      4.			tong += n % 10;
			n = n / 10;
			i++;
		}
      5.		boolean result = false;
      6.		if (i < 5)
      7.			return result;
      8.		if ((tong % 3 == 0 || tong % 4 == 0) && tong % 2 == 0) {
      9.			result = true;
		}
     10.		return result;
	  }


 
All-DU-Paths vo�i bi�n trong:
0-1-2-3-4-5-6-7-8-9-10
All-DU-Paths vo�i bi�n result:
0-1-2-3-4-5-6-7-8-9-10
All-DU-Paths vo�i bi�n i:
0-1-2-3-4-5-6-7-8-9-10

So s�nh v?i �p d?ng MCDC:

All-DU-Path:	
-Bao ph? lu?ng d? li?u	
-Quan tr?ng t?i vi?c l?a ch?n du?ng di v?i
MCDC:
-Bao phu? lu�`ng di�`u khi�?n	
 m?c ti�u bao ph? c�c c?p g�n (definition) 
 v� d�ng (use) d? li?u.
 S? d?ng th�ng tin def-use v� ti�u chu?n 
 c? th? d? nh?n du?c c�c du?ng di c? th? 
 trong d? th? CFG,t? d� x�c d?nh c�c ca 
 ki?m th?  |X�t m?i t? h?p c� d? c�c ca ki?m th?
 d? ki?m tra m?i di?u ki?n c� 
 th? ?nh hu?ng d?n k?t qu? c?a bi?u th?c di?u ki?n 
 ch?a n� ,Bao ph? du?ng di t?t nhung c� nhi?u du th?a.
 X�c d?nh s? ca ki?m th? d?a v�o du?ng di th?a m�n 
 ti�u chu?n l?a ch?n,y�u c?u s? ca ki?m th? gi?ng bao
 ph? di?u ki?n/quy?t d?nh

K?t lu?n

MCDC c� d? bao ph? cao, du?c �p d?ng cho Unit testing, 
ch? y?u ch? s? d?ng cho c�c d? �n quy m� r?t l?n ho?c 
d?c bi?t quan tr?ng, d�i h?i d? ch�nh x�c tuy?t d?i 
nhu c�ng nghi?p � t�, h�ng kh�ng, vu tr?... 
All-DU-Path kh� ph?c t?p n?u b�i to�n c� nhi?u bi?n
