Hàm cần kiểm thử là: 
1.   public int total_isosceles_triangle(ArrayList<Triangle> arrayListTriangle) {
2.        if (arrayListTriangle.size() == 0) {
3.           return 0;
4.        }
5.        int index = 0;
6.        int length = arrayListTriangle.size();
7.        int total_isosceles_triangle = 0;
8.        while (index < length) {
9.            Triangle triangle = arrayListTriangle.get(index);
10.            int edge1 = triangle.getEdge1();
11.            int edge2 = triangle.getEdge2();
12.            int edge3 = triangle.getEdge3();
13.            if ((edge1 > 0 && edge2 > 0 && edge3 > 0) && ((edge1 + edge2 > edge3) && (edge1 + edge3 > edge2) && (edge3 + edge2 > edge1)) 
                    && ((edge1 == edge3) || (edge1 == edge2) || (edge3 == edge2))){
14.                total_isosceles_triangle += 1;
15.            }            
16.            index++;
17.        }
18.        return total_isosceles_triangle;
19.    }


All-DU-Paths của biến arrayListTriangle:
+ Đường 1: 1-2-3
+ Đường 2: 1-2-6-8-18:
+ Đường 3: 1-2-6-8-9-13-8-9-13...8-9-13-18
+ Đường 4: 1-5-7-8-9-13-14...8-9-13-14-18

All-DU-Paths của biến total_isosceles_triangle:
+ Đường 1: 7-18
+ Đường 2: 7-8-8....8-18
+ Đường 3: 7-8-14...8-14-18

Các ca kiểm thử xây dựng:
+ Ca 1: arrayListTriangle = null - Đường 1
+ Ca 2: arrayListTriangle rỗng - Đường 2
+ Ca 3: arrayListTriangle là mảng, trong đó không có một bộ ba giá trị thỏa mãn điều kiện
+ Ca 4: arrayListTriangle là mảng, trong đó tồn tại ít nhất một bộ ba giá trị thỏa mãn điều kiện.


So sánh với MCDC:






