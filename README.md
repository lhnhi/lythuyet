# Ly Thuyet

## Python 

LISTE (DANH SÁCH)

Có thể thay đổi được (mutable), sắp xếp theo thứ tự (thứ tự này sẽ không thay đổi trừ khi mình thay đổi thủ công), cho phép các phần tử trùng lặp (có thể lặp lại), kí hiệu: dấu [ ] , và cũng có các chỉ mục bắt đầu từ 0, 1,... phần tử mới thêm vào sẽ luôn đặt ở cuối danh sách. 

Phần tử trong list có thể là các kiểu dữ liệu khác nhau. Có thể dùng làm list( ) để tạo ra một list mới. 

```python
x = list((‘orange’, ‘pomme’))     #output: [‘orange’, ‘pomme’] 
my_list = [10, 20, 30]    # Thay đổi phần tử tại chỉ mục 1
my_list[1] = 25
print(my_list)  # Output: [10, 25, 30]
```

Thay đổi nhiều phần tử cùng lúc 
thislist = ["apple", "banana", "cherry", "orange", "kiwi", "mango"]
thislist[1:3] = ["blackcurrant", "watermelon"]
print(thislist)
Độ dài của list có thể bị thay đổi nếu những phần tử của chúng ta muốn thay thế không đủ. VD muốn thay thế 2 phần tử nhưng chúng ta chỉ đưa một phần tử duy nhất, vậy len list đã bị thay đổi. 

liste = [ ] #liste rỗng 
liste = [1,2,3,4,5] 
print (liste[1]) 		#result: 2 
liste[1] = 20 		#thay đổi phần tử         #output: [1,20,3,4,5] 
liste.append(5) 	#thêm phần tử vào trong liste
liste.remove(3) 	#xoá các phần tử có giá trị là 3 

List dùng để lưu trữ các giá trị có thể thay đổi và cần tuân theo thứ tự. 

* Phép toán + : 
list1 = [1,2,3] 
list2 = [4,5,6]
combine = list1 + list2 	#result = [1,2,3,4,5,6] 
* Phép nhân * : 
list1 = [1,2,3] 
repetition = list1 * 3 		#result = [1,2,3,1,2,3,1,2,3] 
* Kiểm tra phần tử (True - False): 
list1 = [1, 2, 3]
print(2 in list1)  		# Output: True
print(4 in list1)  		# Output: False
* Lấy độ dài ( len() ): 
list1 = [1, 2, 3]
print(len(list1)) 		 # Output: 3
 * Lấy phần tử MIN, MAX: 
list1 = [1, 2, 3]
print(max(list1))  		# Output: 3
print(min(list1))  		# Output: 1

Hàm .pop (chỉ mục) 
Dùng để xóa phần tử tại vị trí chỉ mục (x.pop(1)), còn nếu KHÔNG CÓ CHỈ MỤC, .pop() sẽ xóa đi phần tử cuối cùng trong list.

Hàm .del (chỉ mục) 
 Dùng để xóa phần tử tại vị trí chỉ mục (del x[1]) hoặc xóa vĩnh viễn list đó. 

Hàm .clear () 
Dùng để xoá hết tất cả các phần tử có trong list và trả về list rỗng. 
thislist = ["apple", "banana", "cherry"]
thislist.clear()
print(thislist)    #output: [] 

Hàm .remove (phần tử) 
Dùng để xóa phần tử đầu tiên có giá trị cụ thể (trong trường hợp có nhiều phần tử giống nhau trong list). 

thislist = ["apple", "banana", "cherry"]
thislist.remove("banana")
print(thislist)    #output:['apple', 'cherry']

hoặc 

thislist = ["apple", "banana", "cherry", "banana", "kiwi"]
thislist.remove("banana")
print(thislist)    #output: ['apple', 'cherry', 'banana', 'kiwi']

Hàm .sort():  
Dùng để phân loại danh sách theo thứ tự mà không làm thay đổi list ban đầu. 
thislist = [100, 50, 65, 82, 23]
thislist.sort()
print(thislist)

Hàm .index():  chỉ mục 
Dùng để chỉ ra vị trị chỉ mục của phần tử cần tìm, nếu có nhiều phần tử lặp, nó trả về vị trí đầu tiên của phần tử đó. 

fruits = [4, 55, 64, 32, 16, 32]
x = fruits.index(32)    #output : 3


Dùng vòng lặp for để duyệt qua tất cả các phần tử trong list. 

Liste de compréhension : ngắn gọn hơn phần code, logic hơn. 

fruits = ["apple", "banana", "cherry", "kiwi", "mango"]

newlist = [x for x in fruits if "a" in x]

print(newlist)   #output: [‘apple’, ‘banana’, ‘mango’] 

Cấu trúc: 
newlist = [expression for item in iterable if condition == True]

**Lưu ý: Nếu không đặt điều kiện if ở cuối, Python sẽ trả về list gốc. 

fruits = ["apple", "banana", "cherry", "kiwi", "mango"]
newlist = [x.upper() for x in fruits]
print(newlist)   
#output: ["apple", "banana", "cherry", "kiwi", "mango"]



nouvelleliste = []
for i in fruits: 
    nouvelleliste.append(i.upper()) 
print (nouvelleliste) 
#output: ["apple", "banana", "cherry", "kiwi", "mango"]


TUPLE ()
Không thể thay đổi (immutable): không thể thêm, bớt, hay xoá các phần tử, có thứ tự, cho phép các phần tử trùng lặp, kí hiệu: dấu ( ) 

tuple = ( ) 			#tuple rỗng 
tuple = (1,2,3,4,5) 		#không thể thay đổi giá trị của phần tử sau khi tạo

Sử dụng khi chúng ta cần một danh sách các giá trị không thể thay đổi
Tuple có thể sử dụng làm khoá trong từ điển nhờ tính bất biến. 
Tuple là không thay đổi, nên nếu muốn thêm phần tử vào trong tuple, có thể dùng phép tính cộng. 

* Phép toán + : 
tuple1 = (1, 2, 3)
tuple2 = (4, 5, 6)
combined = tuple1 + tuple2
print(combined) 		 # Output: (1, 2, 3, 4, 5, 6)

* Phép nhân * : 
tuple1 = (1, 2, 3)
repeated = tuple1 * 3
print(repeated) 		 # Output: (1, 2, 3, 1, 2, 3, 1, 2, 3)

* Kiểm tra phần tử (True - False): 
tuple1 = (1, 2, 3)
print(2 in tuple1)  		# Output: True
print(4 in tuple1)  		# Output: False

* Lấy độ dài ( len() ): 
tuple1 = (1, 2, 3)
print(len(tuple1))  		# Output: 3

 * Lấy phần tử MIN, MAX: 
tuple1 = (1, 2, 3)
print(max(tuple1))  		# Output: 3
print(min(tuple1))  		# Output: 1

SET (ENSEMBLE)
Thay đổi được (mutable), không có thứ tự (các biến có thể sắp xếp lung tung), KHÔNG ACCEPT phần tử trùng lặp, kí hiệu: dấu { } 
Một set chỉ có thể chứa những kiểu dữ liệu IMMUTABLE, nên sẽ không bao giờ có trường hợp set trong set. Có thể thay thế bằng giải pháp: frozenset trong set. 
s = set ( )				#set rỗng 
set = {1,2,3,4,5} 
set.add(5) 				#thêm phần tử vào set 
set.remove(3) 				#xóa phần tử 
print (1 in set)				#result: True

Dùng set khi ta cần những giá trị duy nhất (không lặp) và không quan tâm đến thứ tự. 
* Tính HỢP (kết hợp các phần tử của hai tập hợp, không lấy phần tử LẶP): 
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union_set = set1 | set2
print(union_set)  			# Output: {1, 2, 3, 4, 5}

* Tính GIAO (lấy các phần tử chung của hai tập hợp): 
set1 = {1, 2, 3}
set2 = {3, 4, 5}
intersection_set = set1 & set2
print(intersection_set)  		# Output: {3}

* Hiệu (phép TRỪ - lấy những phần tử có trong set1 nhưng không có ở trong set2): 
set1 = {1, 2, 3}
set2 = {3, 4, 5}
difference_set = set1 - set2
print(difference_set)  			# Output: {1, 2}

* Phép khác biệt đối xứng (lấy các phần tử không CHUNG của cả hai tập hợp): 
set1 = {1, 2, 3}
set2 = {3, 4, 5}
sym_diff_set = set1 ^ set2
print(sym_diff_set)  			# Output: {1, 2, 4, 5}




* Kiểm tra phần tử (True - False): 
set1 = {1, 2, 3}
print(2 in set1)  			# Output: True
print(4 in set1)  			# Output: False

* Lấy độ dài ( len() ): 
set1 = {1, 2, 3}
print(len(set1)) 			 # Output: 3

KHAI BÁO VÀ GỌI HÀM (FONCTION): 
Để gọi hàm, ta sử dụng từ khoá def + tên hàm + dấu ( ), nhớ phải THỤT LỀ. 
Mục đích: để sử dụng được nhiều lần mà không cần phải viết lại. 
Sử dụng từ khóa return để trả lại về 1 giá trị của hàm.

def say_hello():
    print("Hello, world!")
say_hello()  # Output: Hello, world!  => Để gọi hàm, chỉ cần sử dụng tên hàm + dấu ngoặc tròn. 

Tham số và đối số: 
Tham số: các biến được định nghĩa trong phần khai báo hàm, ta có thể truyền giá trị cho các tham số khi gọi hàm. 
def greet(name):
    print(f"Hello, {name}!")
Đối số: các giá trị được truyền cho hàm khi ta gọi nó. 
greet("Alice")  # Output: Hello, Alice!

def add(a, b):
    return a + b
result = add(2, 3)
print(result)  # Output: 5

Giá trị mặc định của tham số: Ta có thể gắn giá trị mặc định cho các tham số trong hàm, nếu không có đối số nào được truyền vào, các giá trị mặc định sẽ đc sử dụng. 
def greet(name="world"):
    print(f"Hello, {name}!")
greet()       		 # Output: Hello, world! (không truyền đối số)
greet("Bob") 		 # Output: Hello, Bob! (truyền đối số Bob) 

Biến cục bộ: là biến được gọi ở bên TRONG hàm, chỉ có thể truy cập ở bên trong hàm đó, ngược lại với biến toàn cục. 

Lệnh assert: 
Là một lệnh dùng để kiểm tra điều kiện, với cú pháp assert condition, message. 
Nếu điều kiện kiểm tra là True, hàm fonction sẽ được khởi chạy, nếu False sẽ báo lỗi. 
Thường để dùng để phát hiện lỗi. 

MODULE: 
Mục đích: tổ chức và tái sử dụng mã lệnh
Ta có thể sử dụng các hàm và biến từ một module bằng cách sử dụng lệnh import 
# fichier mymodule.py (tự tạo file)
def greet(name):
    return f"Hello, {name}!"
def add(a, b):
    return a + b
#fichier main.py
import mymodule
print(mymodule.greet("Alice"))  # Output: Hello, Alice!
print(mymodule.add(5, 3))       # Output: 8

from…import… (xem sau) 
import…as…(xem sau) 

Những module tiêu chuẩn trong Python: 
import math
import random
random.randint(): trả về một số nguyên ngẫu nhiên trong khoảng [a,b] - bao gồm cả 2 đầu a,b
random.randrange(): trả về một số nguyên bất kì từ một dải số [start, end, step] 

SỐ NHỊ PHÂN: 
Số nhị phân là số chỉ sử dụng hai chữ số là 0 và 1, biểu diễn số nhị phân bằng cách thêm kí hiệu “0b" ở đằng trước số.
Mỗi vị trí trong số nhị phân đại diện cho một số luỹ thừa của 2, bắt đầu từ 2^0 bắt đầu từ phía ngoài cùng bên phải. 
VD: số 1010

1 * 2^3 = 1 * 8 = 8 / 0 * 2^2 = 0 * 4 = 0 / 1 * 2^1 = 1 * 2 = 2 / 0 * 2^0 = 0 * 1 = 0 (tổng = 10) 
Hàm bin( ): nhận một số nguyên và trả về một số nhị phân.
Khi in kết quả ra, cấu trúc sẽ là “0b + kết quả"  VD: 0b1010. Nếu ta muốn cắt phần “0b", có thể sử dụng vd: binary = bin(3)[2: ] 
Nhớ: chia lấy phần dư

SỐ THẬP LỤC PHÂN:
Là số khi in kết quả ra, cấu trúc là “0x + kết quả". 

* Hàm int( ) có thể nhận 2 đối số, vd: int(binary_str, 2) 
* Nếu làm trong số thập phân với hàm int( ), sẽ làm tròn đến số nguyên và bỏ đi phần thập phân, vd: int(3.2) = 3
* math.floor( ) làm tròn một số thực tới số nguyên lớn nhất nhỏ hơn tham số. LƯU Ý: làm tròn XUỐNG không làm tròn lên. 
VD: math.floor (-3.2) = -4 

SỐ PHỨC: 
Có dạng : a + bj (j là đơn vị ảo i: a + bi) 
z.real : in ra phần thực - z.imag: in ra phần ảo 
Hàm complexe( ) dùng để tạo ra số phức từ hai số thực. VD: complexe(3,4) -> 3 + 4j 

DICTIONNAIRE: 
Là kiểu dữ liệu lưu trữ các cặp khóa - giá trị (clé - valeur), kí hiệu: dấu { } 
Dictionnaire không có thứ tự, mỗi mục trong từ điển bao gồm một khoá và giá trị, được viết dưới dạng clé: valeur
La clé est unique, nếu ta gán valeur mới cho valeur cũ đã tồn tại một clé, valeur cũ sẽ bị ghi đè lên. 
La clé có thể là bất kỳ kiểu dữ liệu nào. 
empty_dic = { } 	#dictionnaire rỗng 
person = {"name": "Alice",  "age": 30, "city": "New York"}
Cách truy cập vào giá trị trong từ điển, cú pháp: dict [key] : 
name = person["name"] 	print(name)  		# Output: Alice
age = person["age"]		print(age)  		# Output: 30

Cách để thêm một valeur mới hoặc update vào từ điển: 
person["email"] = "alice@example.com" 	#thêm 
person["age"] = 31				#update
print(person)
# Output: {'name': 'Alice', 'age': 31, 'city': 'New York', 'email': 'alice@example.com'}

Xoá mục ở từ điển: sử dụng khoá del( ) hoặc pop ( ): 
del person["city"]			print(person)  # Output: {'name': 'Alice', 'age': 31}
email = person.pop("email")		print(email)  # Output: alice@example.com

Kiểm tra sự tồn tại của clé: 
if “name” in person: 
if “name” not in person: 

Duyệt qua các mục trong từ điển: sử dụng phương thức keys(), values (), items(): 
for key in person.keys():
    print(key)
# Output:
# name
# age

for value in person.values():
    print(value)
# Output:
# Alice
# 31

for key, value in person.items():
    print(f"{key}: {value}")
# Output:
# name: Alice
# age: 31
dic.clear ( ): xoá toàn bộ từ điển 
dic.update( ): thêm vào các cặp khoá và giá trị vào từ điển từ một từ điển khác 

TOÁN TỬ SO SÁNH ( > , < , <= , >= ) : 
SET: Phần tử A được gọi là tập hợp con của B nếu tất cả các phần tử của A đều là các phần tử của B.
set1 = {1, 2, 3}
set2 = {1, 2, 3, 4}
print(set1 < set2)  # True, set1 là tập hợp con của set2
print(set2 > set1)  # True, set2 là tập hợp cha của set1
print(set1 > set2)  # False, set1 không phải là tập hợp cha của set2
print(set1 < set1)  # False, set1 không phải là tập hợp con của chính nó
print(set1 <= set1)  # True, set1 là tập hợp con hoặc bằng chính nó

TUPLE và LIST: thực hiện so sánh phần tử từ đầu đến cuối từ trái sang phải. 
list1 = [1, 2, 3]
list2 = [1, 2, 4]
print(list1 < list2)  # True, vì 3 < 4
print(list1 > list2)  # False, vì 3 < 4
print(list1 == list1)  # True, vì hai list giống nhau

tuple1 = (1, 2, 3)
tuple2 = (1, 2, 4)
print(tuple1 < tuple2)  # True, vì 3 < 4
print(tuple1 > tuple2)  # False, vì 3 < 4
print(tuple1 == tuple1)  # True, vì hai tuple giống nhau

DICTIONARY: Từ điển không hỗ trợ toán tử so sánh, sẽ gây ra lỗi TypeError. 

CÁCH TẠO LIST, TUPLE, SET, DICTIONARY TỪ KIỂU DỮ LIỆU: 
… = set(kiểu dữ liệu) 

… = list(kiểu dữ liệu) 
* tạo list từ một từ điển, chỉ lấy được phần khoá
d = {'a': 1, 'b': 2, 'c': 3}
list_from_dict_keys = list(d)
print(list_from_dict_keys)  			# Output: ['a', 'b', 'c']

… = tuple(kiểu dữ liệu) 

… = dict (kiểu dữ liệu) 
* Tạo dict( ) từ hai list khác nhau: dùng hàm zip( )
keys = ['a', 'b', 'c']
values = [1, 2, 3]
dict_from_keys_values = dict(zip(keys, values))
print(dict_from_keys_values)  		# Output: {'a': 1, 'b': 2, 'c': 3}

ARGUMENTS OPTIONNELS - Tham số chỉ định: 
Tham số tuỳ chọn: tức là các tham số có giá trị mặc định, khi gọi hàm ta có thể bỏ qua các tham số này, chúng sẽ sử dụng các giá trị mặc định đã định nghĩa. 
Tham số tuỳ chọn được nhận dạng bằng cách có dấu “=”. 

def greet(name, greeting="Hello"):
    print(f"{greeting}, {name}!")
greet("Alice")               # Output: Hello, Alice!
greet("Bob", "Hi")       # Output: Hi, Bob!

def greet(name, age):
    print(f"Chào bạn {name}, bạn đã {age} tuổi.")
greet(name="Alice", age=25)		
greet(age=30, name="Bob")

L'argument obligatoire: thường được gọi theo thứ tự theo như định nghĩa của hàm, tuy nhiên, nếu ta chỉ định chính xác tên gọi của chúng (gọi theo cú pháp key = value), ta có thể gọi theo bất kỳ thứ tự nào, kể cả ta để key cần phải chỉ định đằng sau cũng được. 
L'argument nommé: không cần quan tâm đến thứ tự tham số trong hàm, Python vẫn có thể nhận dạng đc nhờ tên, vd: name, age.
#argument nommé: name=“Alice”, age = 25
L’argument positionnel: các đối số được truyền vào hàm theo thứ tự vị trí của chúng trong danh sách đối số của hàm, không cần chỉ định tên của tham số. 
#Alice và 25 là argument positionnel của name và age. 

Lưu ý: Các arguments positionnels KHÔNG THỂ ĐẶT SAU các arguments nommés. 

Tham số bắt buộc: là giá trị BẮT BUỘC phải được cung cấp khi gọi hàm, nó sẽ gây ra lỗi ‘TypeError’ nếu không được cung cấp giá trị. 
Luôn phải xuất hiện TRƯỚC tham số tuỳ chọn. 

FROZENSET: 
Tương tự như set, nhưng IMMUTABLE - bất biến, ta không thể thay đổi một frozenset. 
Cách tạo frozenset: dùng lệnh frozenset( ) và truyền vào đó một iterable (list, tuple, set,...).
Giống set, nó KHÔNG CHỨA phần tử trùng lặp và KHÔNG CÓ THỨ TỰ.
frozenset( ) có thể sử dụng làm khoá trong từ điển, vì nó là bất biến, còn set thì không vì set là khả biết (mutable).
fs = frozenset([1, 2, 3])
d = {fs: "value"}
print(d)  # Kết quả: {frozenset({1, 2, 3}): 'value'}

HÀM LAMBDA: 
Là hàm ẩn danh, sử dụng chính từ khoá: lambda argument : expression (argument là tham số mà lambda sẽ nhận, expression là biểu thức mà nó trả về). 
Hàm lambda chỉ chứa một biểu thức duy nhất, không thể chứa đc nhiều dòng lệnh. 
square = lambda x:  x**2
print(square(5))  			# Output: 25


FONCTION RÉCURSIVE - NON RÉCURSIVE (Hàm đệ quy): 
Hàm đệ quy: tự gọi chính nó, cần điều kiện để dừng đệ quy.
Hàm không đệ quy: sử dụng vòng lặp, không cần điều kiện.
* Nếu trong bài có sin, cos, phải gọi from math import sin, cos. 
Các chức năng:
set.update ( ) : cách thêm nhiều phần tử vào một tập hợp, có thể là list, tuple, str, set
my_set = {1, 2}
my_set.update([3, 4], {5, 6}, "78")
print(my_set)  				# Output: {1, 2, 3, 4, 5, 6, '7', '8'}

z = {'a': 1, 'b': 2, 'c': 3}  ;  a = 3
z[a] = 2 					#update phần tử 
* tức z[3] = 2, lúc này z =  {'a': 1, 'b': 2, 'c': 3, 3 : 2} 

set/list.clear ( ) : xoá all các phần tử trong set, list (tuple không có) 

Chú ý: Nếu muốn tìm cái gì đó, nên nghĩ đến việc đặt biến True/False

tuple/list.count(a): đếm số lần a xuất hiện trong tuple/list

set/list.pop(): xoá phần tử cuối cùng trong set/list
List: có thể chỉ định phần tử để xoá, list.pop(1): tức là xoá phần tử ở vị trí thứ 1 nhất trong list. 
Set: không thể chỉ định phần tử xoá vì set không theo thứ tự. 

tuple/list.index(a): trả về chỉ số đầu tiên của giá trị a
my_list = [1, 2, 3, 4, 2]
print(my_list.index(2))  	# Output: 1 (chỉ số của phần tử đầu tiên có giá trị 2)

tuple/list.remove(a): loại bỏ phần tử đầu tiên có giá trị a. 
my_list = [1, 2, 3, 4, 2]
my_list.remove(2)
print(my_list)  			# Output: [1, 3, 4, 2] (loại bỏ phần tử đầu tiên có giá trị 2)

del list: được sử dụng để xóa các biến, phần tử trong list, và các chỉ mục từ của dictionnaire. Đối với set chỉ dùng del set để XOÁ TOÀN BỘ set, còn nếu muốn xoá biến thì dùng set.remove( ) 
my_list = [1, 2, 3, 4]
del my_list[1] 			 # Xóa phần tử tại chỉ mục 1
print(my_list)  			 # Output: [1, 3, 4]

Đối với sort( ), list gốc sẽ bị thay đổi (ảnh hưởng trực tiếp). 
list.sort() hoặc sorted(L): chỉ dùng với list, sắp xếp theo thứ tự từ bé đến lớn.
list.sort(reverse=True): sắp xếp theo thứ tự giảm dần. 

* reverse = boolean cho biết có sắp xếp theo thứ tự giảm dần hay không, mặc định reverse = False. 
Hàm sorted ( ): là hàm có thể dùng với bất kì các kiểu dữ liệu nào, nó sẽ trả về một danh sách mới với các phần tử được sắp xếp mà không làm thay đổi danh sách gốc.
my_set = {3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5} 				#set không chứa phần tử lặp
sorted_set = sorted(my_set) print(sorted_set) 			# Output: [1, 2, 3, 4, 5, 6, 9]

my_dict = {'banana': 3, 'apple': 4, 'pear': 1, 'orange': 2} 
sorted_keys = sorted(my_dict) 
print(sorted_keys) 			# Output: ['apple', 'banana', 'orange', 'pear']

len( ) : được dùng để trả về độ dài phần tử của tuple, list,, hay dict, len( ) không thể sử dụng cho kiểu dữ liệu số như int hoặc float. 

set.add( ): lệnh add( ) chỉ sử dụng được cho set, dùng để thêm một phần tử vào tập hợp
my_set = {1, 2, 3}
my_set.add(4)
print(my_set)  				# Kết quả: {1, 2, 3, 4}

set.discard( ): loại bỏ phần tử được chỉ định khỏi set, chỉ dùng được cho set. 
s = {1, 2, 3}
s.discard(2) 				 # Loại bỏ phần tử 2 khỏi tập hợp
print(s)  				# Kết quả: {1, 3}

220125
B = (A<=C) : kiểm tra xem A có phải là tập con của C hay không, tức là các phần tử của A có nằm trong C không, nếu có kết quả trả về True, nếu không trả về False. 

B = C - A : Trả về một (tập hợp - nếu đang là set) các phần tử thuộc tập hợp C nhưng không thuộc tập hợp A. 

VD: 
A = {1, 'n'}
C = {'p', 'y', 't', 'h', 'o', 'n'}
B = C - A
print(B)   #  {'p', 'y', 't', 'h', 'o’}

số phức: real (z) : không đúng cú pháp 
cần viết: z.real 

GÉNÉRATEUR : 
Đối tượng sinh ra giá trị một cách lười biếng, chỉ tạo giá trị khi cần thiết, thay vì lưu trữ toàn bộ danh sách trong bộ nhớ. 
Nó dùng dấu ngoặc tròn (...) thay cho ngoặc vuông [...] 
Dùng trong vòng lặp for, sum, any, all…

Để phân biệt với Tuple: Tuple trong đó có 2 thành phần trở lên, VD: (abc, ) kể cả không cần tồn tại giá trị thứ 2. Còn générateur, chỉ dùng dấu ngoặc tròn và bên trong chỉ có một phép tình hoặc yêu cầu nào đó. 

Khi chạy x =(1/a for a in range (1,101)
Nó sẽ trả về dạng <generator object <genexpr> at 0x100f86900>

LISTE DE COMPRÉHENSION 



% có nghĩa là chia lấy phần dư

LƯU Ý: 

Cần phải cách ít nhất 4 khoảng trắng để mã có thể hoạt động, tuy nhiên phải số khoảng trắng phải đồng đều, nếu không sẽ có lỗi. 

Dùng dấu nháy để đặt chú thích 

Cách chuyển đổi kiểu dữ liệu: 

str( ) : chuyển đổi thành chuỗi 
int( ) : chuyển đổi thành số nguyên
float ( ) : chuyển đổi thành số thực (thập phân: dấu chấm)

Dùng lệnh type ( ) nếu muốn biết kiểu dữ liệu của biến. Python sẽ trả về dạng <class 'int'>, <class 'float'>,...
x = “HaNi”
print (type(x))

Hoặc ta có thể chỉ định, biến đổi một kiểu dữ liệu thành một kiểu dữ liệu: set( ), list( ), tuple( ), dict( ), int( ), float( ), complex ( ), bool( ),  



VD: x = str(5) (5 vốn là thuộc kiểu int, nhưng ta đang biến nó thành kiểu str, khi xuất ra sẽ đc “5”) 

VARIABLE 
Quy tắc đặt tên biến: 
Tên biến phải bắt đầu bằng 1 chữ cái hoặc kí tự gạch dưới 
Tên biến không thể bắt đầu bằng số 
Tên biến chỉ có thể chứa chữ cái, số, dấu gạch dưới, các tên phải nối với nhau bằng dấu gạch dưới nếu không muốn viết dính liền ( VD: x, _age, car_name)
Tên biến phân biệt chữ hoa và chữ thường (VD: age, Age, AGE,...) 
Tên biến KHÔNG THỂ là từ khoá của Python (VD: type,...) 

Gán biến: Python sẽ tự phân biệt kiểu dữ liệu mà không cần chúng ta phải làm rõ. Ngoài việc gán một biến, chúng ta có thể gán nhiều biến cùng một lúc (trên cùng một dòng) 

VD:
x, y, z = ‘orange’, ‘pomme’, ‘banane’ 
print (x)
print (y) 
print (z) 

hoặc : 
x = y = z = 50 
print (x)
print (y) 
print (z) 

Cách giải nén một tập (une collection) và gán biến: 
fruits = ["apple", "banana", "cherry"]
x, y, z = fruits
print(x)
print(y)
print(z)

hoặc có thể in nhiều biến cùng một lúc: print(x, y, z)
hoặc: 
x = "Python "
y = "is "
z = "awesome"
print(x + y + z)

** Cần có khoảng trắng đằng sau mỗi từ vd như “Python ” vì nếu không sẽ bị VIẾT DÍNH LIỀN. 
** Không thể print ( ) cộng hai kiểu dữ liệu khác nhau, vd như str + int sẽ gây ra lỗi, nếu muốn in hai kiểu dữ liệu khác nhau, dùng dấu phẩy print(x, y, z)

x = “awesome” - x được gọi là biến ngoài cục, có thể sử dụng cả ở trong lẫn ngoài hàm def 

VD: 
y = “Hani” 
def mylove () : 
	print (‘Hyunjin love ‘ + y ) 
mylove() #Hyunjin love Hani 

or: print("Python is " + x)

** Nếu khai hai biến có tên giống nhau, ở cả trong và ngoài hàm, hàm sẽ chọn biến ở trong làm dữ liệu chứ không chọn biến ở ngoài, và biến đó cũng chỉ có thể sử dụng được ở trong hàm đó. 

Kiểu String : 
Để truy cập vào từng phần tử trong chuỗi, dùng dấu ngoặc [ ] , phần tử đầu tiên là 0 

VD: x = “Hyunjin” 
print (x[4])   - - -  sẽ in ra phần tử thứ 4 trong chuỗi là ký tự “j” 

Để duyệt từng phần tử trong chuỗi, dùng từ khoá nào cũng đc (char, c, i, k): 
VD: for char in “Hyunjin” : 
	print (char) 
#H y u n j i n (trên code sẽ xuất theo hàng dọc)
Để lấy một phần của chuỗi, dùng [ start : end : step (nếu có)] trong ngoặc dùng số từ 0 đến end - 1 để biểu thị vị trí muốn lấy. 
[2: ] có nghĩa là lấy hết kể từ vị trí thứ 2 
[ :4] có nghĩa là lấy từ đầu đến vị trí (4-1) 

** START phải BÉ hơn END, nếu không sẽ trả về chuỗi rỗng**

Hoặc dùng chỉ số âm để đếm ngược từ cuối lên, bắt đầu từ -1, tuy nhiên, vẫn bắt đầu đếm từ bên trái sang. 

x = “Hyunjin” 
print (x[2:4]) #un 
print (x[2:])
print (x[-3:-1])

Không thể cộng hai kiểu dữ liệu khác nhau, phải cùng loại. Nếu muốn, dùng dạng f“...” + { biến } để cộng hai kiểu dữ liệu khác nhau. Hoặc nếu không, phải đổi hết về cùng một kiểu dữ liệu. 

VD: 
age = 25 
txt = f“Hyunjin a {age} ans.” 
print (txt) 
Hàm len ( ) 
Dùng hàm len ( ) để tính số phần tử của chuỗi. Hàm len( ) sẽ tính cả khoảng trắng và coi nó là một kí tự. Hàm này cũng dùng để tính số phần tử của các kiểu dữ liệu khác, tuple, list, dict,... 
VD: 
x = “Hyunjin” 
longueur = len(x) 
print (longueur) hoặc print (len(x)) 

Check chuỗi 
muốn check một ký tự, một từ có trong chuỗi hoặc các kiểu dữ liệu hay không, dùng lệnh in hoặc not in, nếu có sẽ trả về True, không sẽ trả về False. 

VD: print (“jin” in “Hyunjin”) 

Hàm .upper ( ) 
Dùng để viết in hoa hết các kí tự trong chuỗi, nhớ phải viết cả dấu ( ).

VD: x = “Hyunjin” 
print (x.upper( ))     #HYUNJIN

Hàm .lower ( ) 
Dùng để viết thường tất cả các kí tự trong chuỗi, nhớ phải viết cả dấu ( ).

VD:  x = “Hyunjin” 
print (x.lower( ))     #hyunjin

Hàm .capitalize( ) 
Dùng để viết hoa ký tự đầu tiên của chuỗi, nhớ phải viết cả dấu ( ). Kể cả trong chuỗi có những kí tự viết hoa cũng sẽ biến thành viết thường, chữ được viết hoa chỉ có duy nhất kí tự đầu tiên. 

VD: x = “hwang hyunjin” 
print (x.capitalize( ))     #Hwang hyunjin

MODULE RANDOM 
Python không có hàm random, nhưng sẽ có module random để tạo ra số ngẫu nhiên. 
import random
VD: 
import random
print(random.randrange(1, 10))
random.randint(a, b) → Tạo số nguyên ngẫu nhiên trong khoảng [a, b].
random.random () → Tạo số thực ngẫu nhiên từ 0.0 đến 1.0.
random.choice(list) → Chọn một phần tử ngẫu nhiên từ danh sách.
random.shuffle(list) → Xáo trộn danh sách.
Giá trị BOOLEAN
Kiểu dữ liệu này chỉ trả về hai giá trị duy nhất là True hoặc False. 
bool( ) : bất kỳ số nào khác 0 (dương hoặc âm), mọi chuỗi, khi chuyển sang bool đều có giá trị True.  Chỉ có “0”, None, ”...”(chuỗi rỗng), [...] (danh sách rỗng), {...} (từ điển rỗng), set() (tập hợp rỗng) và False mới cho giá trị False 
VD: print (10 == 9)        #False - trả về giá trị đúng hoặc sai chứ không in ra 10 == 9 
print (bool(“Hyunjin”))     #True 

Đối với những hàm không nhận tham số, nó sẽ được trả về giá trị True hoặc False (tuỳ vào điều kiện) khi được gọi. 

def myFunction() :   #hàm không nhận tham số 
 	return True
print (myFunction())   #được gọi nên sẽ trả về True 

TOÁN TỬ PYTHON : CỘNG TRỪ NHÂN CHIA 
: cộng 
: trừ 
      *     : nhân 

/ : chia số thực (10 / 3 = 3.33333…) 
// : chia làm tròn đến số nguyên gần nhất ( 10// 3 = 3) 
% : chia lấy phần dư (10 % 3 = 1) 

** : luỹ thừa 

Toán tử and or not 
and: trả về True nếu cả hai điều kiện đều đúng (10 > 5 and 5 < 7) 
or : trả về True nếu có ít nhất điều kiện đúng (x > 5 or y < 4)
not: đảo ngược kết quả của một điều kiện not (x<5 and x < 10)  

PILE (Ngăn xếp) 
Loại dữ liệu trừu tượng, hđ theo nguyên tắc LIFO (Last In First Out) - phần tử đc lấy vào sau cùng sẽ lấy đc ra đầu tiên (quyển sách đặt trên cùng sẽ là quyển đầu tiên được lấy ra). 

FILE (Hàng đợi) 
Loại dữ liệu trừu tượng khác , hđ theo nguyên tắc FIFO (First In First Out) - phần tử đc thêm vào đầu tiên sẽ là phần tử đc lấy ra đầu tiên (người xếp hàng mua vé, xếp hàng trước sẽ mua đc vé trước). 
Các thao tác cơ bản: enfiler (thêm vào hàng chờ), défiler (xóa và lấy phần tử ở đầu hàng đợi), tête (xem phần tử ở đầu hàng đợi nhưng không lấy), est vide (kiểm tra xem có rỗng không) 

CLASS 
Định nghĩa 1 lớp, khuôn mẫu tạo ra các đối tượng, một class có thể chứa nhiều hàm, ta gọi là méthode. 
Nếu tên def thấy có dấu gạch dưới _ _ … _ _ thì có nghĩa là “các phương thức đặc biệt” - dunder methods 
VD: __init__ (self, tên): 

Vòng lặp - BOUCLE
WHILE 
Đối với vòng lặp while, ta có thể thực hiện một tập hợp các câu lệnh MIỄN là điều kiện vẫn đúng. Vòng lặp này cần ta tạo sẵn biến i (biến bước nhảy), thường là sẽ định nghĩa 1 biến theo chỉ mục i, và bắt đầu với i = 0 hoặc i = 1 
i = 1
while i < 6:   #chỉ cần i vẫn nhỏ hơn 6 vòng lặp sẽ vẫn chạy
  print(i)
  i += 1       #biến i cần tăng lên thì vòng lặp mới chạy hết đk 

CHÚ Ý: Phải dừng i nếu không vòng lặp sẽ chạy mãi không ngừng. 

FOR 
Được dùng để lặp qua một dãy, có thể là một danh sách, tuple, set, string, dict… cũng giống như While, dùng để thực hiện những câu lệnh. 
Vòng lặp này không yêu cầu biến số trước như While. Có thể dùng else làm điều kiện dừng vòng lặp (cả với while), nếu vòng lặp có break (bước trước else), else sẽ không chạy. 

** Range là loại đối tượng itérable, nó thể lặp lại, tạo ra giá trị nhưng không cần lưu trữ hết chúng trong bộ nhớ. nó sẽ tính toán để trả về giá trị tiếp theo chứ không lưu hết. 
Nhưng nếu đưa list vào, vd: list(range(10**1000)) thì sẽ gây MemoryError vì tính chất của range không lưu hết giá trị nhưng list thì khác, nó sẽ tạo ra và lưu lại toàn bộ các giá trị. 
générateur cũng là một itérable 

yield cho phép hàm dừng lại và trả về ngay giá trị yêu cầu (trả về một générateur) và nó sẽ tiếp tục đc gọi TỪ ĐIỂM ĐÓ nếu gọi nó bằng next() hoặc dùng vòng lặp. 
Một générateur chỉ có thể ĐƯỢC DUYỆT 1 LẦN, NẾU ĐÃ TỪNG ĐƯỢC DUYỆT QUA RỒI, NÓ SẼ KHÔNG CÒN GIÁ TRỊ NÀO NỮA. 
