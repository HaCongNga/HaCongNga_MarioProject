# Mario

A small 2D, SDL2 Game written in C++ featuring move, jump, collision and more!


Dự án game Mario cuối khóa Lập trình nâng cao

## 1. Hướng dẫn cài đặt: cách lấy chương trình về, tất cả các câu lệnh, cài đặt để có thể chạy được chương trình:

+ Clone từ github về máy. Tạo 1 project tên MarioProject.cbp, trong CodeBlocks sau đó add file recursively từ Folders: MarioProjectFinal. (Trong quá trình làm trên

Codeblocks em làm code và lưu trong MarioProjectFinal, sau đó tạo MarioVersion1.cbp để nộp băng cách add files nhưng đẩy lên git chỉ có file.o ạ)

+ Vào MarioProject.cbp\Build options\Linker settings\ sau đó add link libraries: mingw32, SDL2main, SDL2, SDL2_image, SDL2_mixer, SDL2_ttf

+ Vào MarioProject.cbp\Build options\Search directorries\ Thêm các include vào Compiler, thêm các lib vào linker.

## 2. Mô tả chung về trò chơi, các ý tưởng chính:

+ Mô tả chung về trò chơi: Trò chơi có ý tưởng như game Mario truyền thống, người chơi cố gắng đạt càng nhiều điểm càng tốt trong khi chưa kết thúc. Trò chơi kết thúc 

khi cả hai người chơi đều thua.

+ Ý tưởng chính: 

. Người chơi thua khi chạm vào Koopa (Enemy) khi chúng đang còn sống. Cả hai người chơi thua thì game kết thúc_Game Over.

. Người chơi giành được điểm trong hai trường hợp: Chạm vào rùa khi rùa bị thương ( + 200đ), hoặc là ăn đồng tiền vàng (+500đ)

. Rùa bị thương trong các trường hợp: Mario or Luigi va chạm vào nút Pow, hoặc là khi hai nhân vật trên va chạm vào tường đúng lúc rùa đi qua vị trí đó, 

trong trường hợp này đồng xu(Coin) mới xuất hiện.

##3. Mô tả các chức năng đã cài đặt, kèm video minh họa (chèn link video youtube)

+ Mô tả chức năng đã cài đặt: 

. Chức năng DI CHUYỂN: Mario dùng A,D để di chuyển trái phải, Luigi dùng nút mũi tên trái phải để di chuyển. Enemy Koopa di chuyển bằng hàm DoAIMove.

. Chức năng NHẢY: Hai người chơi dùng W, mũi tên lên để nhảy, khi nhảy tối đa 2 lần (nếu không chạm tường), chạm tường sẽ bị rơi xuống.

. Chức năng VA CHẠM: 
    
    * Va chạm với rùa lúc rùa bị thương
    
    * Va chạm với rùa lúc rùa còn sống
    
    * Va chạm với bức tường
    
    * Va chạm với nút Pow.
    
 . Chức năng TÍNH ĐIỂM: Điểm được hiện thị dưới góc trái màn hình, +200 sau khi va chạm rùa bị thương, +500 khi ăn được đồng xu trong thời gian lifetime của nó

+ Link Youtube: https://youtu.be/w7ehYYT0pbE

##4. Các kỹ thuật lập trình được sử dụng: 

+ Sử dụng mamg 2 chiều để đọc ma trận từ 1.txt (Map của Level 1) (trong LevelMap.cpp)

+ Sử dụng con trỏ: Cấp phát động để nâng cao hiệu quả chương trình: VD: m_pow_block  trong Collision.cpp

+ Sử dụng Lớp: Định nghĩa lớp được định nghĩa khái quát để các lớp con có thể kế thừa từ nó. VD: Enemy Koopa kế thừa từ Enemy, Player Mario kế thừa từ Player.

Sử dụng hàm ảo trong Lớp để tự định nghĩa lại trong hàm dẫn xuất để kiểm soát tốt logic game, tiết kiệm thời gian code.

+ Đồ họa : Sử dụng SDL_image: load file ảnh, SDL_ttf: xử lý font, SDL_mixer: xử lý âm thanh

##5. Kết luận, hướng phát triển và các điều tâm đắc rút ra được sau khi hoàn thiện chương trình

+ Kết luận: Thư viện SDL2 và  ngôn ngữ C++ hỗ trợ khá tốt cho lập trình game 2D. Việc khai báo tên theo kiểu kể chuyện giúp kiểm soát được logic game tốt hơn trong quá 

trình code nhiều ngày. Việc khai báo các const vào const.h giúp chương trình đẹp hơn, tiện lợi hơn. 

+ Hướng phát triển: Làm thêm Level 2 cho game : Tính thời gian (2p) (Sử dụng SDL_gettick), thêm Enemy để người chơi khó chơi hơn trong 2p, thêm công chúa để giải cứu

+ Các điều tâm đăc nhất:

. Biết một game được hoạt động như thế nào, xây dựng ra sao, từ đó có thêm ý tưởng cho riêng mình từ bây giờ.

. Học cách kiểm soát việc code project trong thời gian dài.

. Bước đầu lập trình theo Hướng đối tượng hơn: Sử dụng protected để lớp kế thừa trỏ đến được các biến thành viên. Sử dụng hàm ảo tạo tính đa hình hơn, giúp tăng hiệu 

quả.









