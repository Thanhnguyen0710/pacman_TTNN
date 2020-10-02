# pacman_TTNN
Câu 1
Thuật toán DFS:
Tạo 1 mảng lưu các vị trí đã đi qua
Push vị trí bắt đầu và 1 mảng để lưu các action vào stack
Bắt đầu chạy vòng lặp while với điều kiện stack khác rỗng
Lấy trạng thái và mảng các action trên cùng của stack, nếu trạng thái này là trạng thái đích thì trả về mảng các action
Nếu trạng thái không nằm trong mảng lưu các vị trí đã đi qua thì thêm trạng thái vào mảng lưu các vị trí đã đi qua
Lấy các trang thái có thể đi tiếp
Tạo 1 mảng mới sao chép mảng lưu các action vào và thêm từng trạng thái này (Vì mỗi 
trạng thái có các action khác nhau)
Push các trạng thái và mảng lưu các action của từng trạng thái vào stack

Câu 2
Thuật toán BFS:
Tạo 1 mảng lưu các vị trí đã đi qua
Push vị trí bắt đầu và 1 mảng để lưu các action vào queue
Bắt đầu chạy vòng lặp while với điều kiện queue khác rỗng
Lấy trạng thái và mảng các action đầu tiên của queue, nếu trạng thái này là trạng thái đích thì trả về mảng các action
Nếu trạng thái không nằm trong mảng lưu các vị trí đã đi qua thì thêm trạng thái vào mảng lưu các vị trí đã đi qua
Lấy các trang thái có thể đi tiếp
Tạo 1 mảng mới sao chép mảng lưu các action vào và thêm từng trạng thái này (Vì mỗi 
trạng thái có các action khác nhau)
Push các trạng thái và mảng lưu các action của từng trạng thái vào queue

Câu 3
Thuật toán UCS:
Tạo 1 mảng lưu các vị trí đã đi qua
Push vị trí bắt đầu và 1 mảng để lưu các action và 1 giá trị để lưu chi phí đó là 1 phần tử và thêm 1 phần tử giá trị số nguyên để đánh giá trị ưu tiên chính bằng chi phí của trạng thái vào priority queue
Bắt đầu chạy vòng lặp while với điều kiện priority queue khác rỗng
Lấy trạng thái và mảng các action và chi phí đầu tiên của priority queue, nếu trạng thái này là trạng thái đích thì trả về mảng các action
Nếu trạng thái không nằm trong mảng lưu các vị trí đã đi qua thì thêm trạng thái vào mảng lưu các vị trí đã đi qua
Lấy các trang thái có thể đi tiếp
Tạo 1 mảng mới sao chép mảng lưu các action vào và thêm từng trạng thái này (Vì mỗi 
trạng thái có các action khác nhau)
Update các trạng thái và mảng lưu các action và chi phí  và số đánh giá trị ưu tiên của từng trạng thái vào priority queue

Câu 4
Thuật toán Astar:
Tạo 1 mảng lưu các vị trí đã đi qua
Push vị trí bắt đầu và 1 mảng để lưu các action và 1 giá trị để lưu chi phí đó là 1 phần tử và thêm 1 phần tử giá trị số nguyên để đánh giá trị ưu tiên chính bằng chi phí + kinh nghiệm của trạng thái vào priority queue
Bắt đầu chạy vòng lặp while với điều kiện priority queue khác rỗng
Lấy trạng thái và mảng các action và chi phí đầu tiên của priority queue, nếu trạng thái này là trạng thái đích thì trả về mảng các action
Nếu trạng thái không nằm trong mảng lưu các vị trí đã đi qua thì thêm trạng thái vào mảng lưu các vị trí đã đi qua
Lấy các trang thái có thể đi tiếp
Tạo 1 mảng mới sao chép mảng lưu các action vào và thêm từng trạng thái này (Vì mỗi 
trạng thái có các action khác nhau)
Update các trạng thái và mảng lưu các action và chi phí  và số đánh giá trị ưu tiên của từng trạng thái vào priority queue

Câu 5
Hàm getStartState sẽ trả về trạng thái bắt đầu của qacman và 1 mảng rỗng để chứa các góc đã đi qua

Hàm isGoalState sẽ trả về True nếu số phần tử của mảng corners bằng số phần tử của mảng chứa các góc đã đi qua

Hàm getSuccessors tạo mảng successors chứa các phần tử trạng thái tiếp theo có thể đi của state, sét các action kiểm tra xem các action nếu đi thì co gặp tường không
Nếu không và trạng thái đó là góc thì tạo mảng mới thì sao chép từ mảng lưu chứa các góc đã đi qua thêm trạng thái đó vào mảng và thêm trang thái , mảng lưu chứa các góc đã đi qua, chi phí vào mảng successors
Nếu không phải ở góc thì thêm trang thái , mảng lưu chứa các góc đã đi qua, chi phí vào mảng successors
Trả về mảng successors

Câu 6

cornersHeuristic:
Sẽ tính chi phí đi từ trạng thái bắt đầu đến góc gần nhất mà không có wall và từ góc đó đi đến góc tiếp theo gần nhất và cứ thế cho đến khi đi hết các góc(bỏ qua các góc mà pacman đã đi qua)

Câu 7

foodHeuristic:
tìm khoảng các giữa 2 nút xa nhau nhất và cộng thêm chi phí đi từ pacman đến nút có dấu chấm gần nhất

Câu 8
Hàm isGoalState sẽ trả về giá trị True nếu state nằm trong mảng tọa độ các food

Hàm findPathToClosestDot trả về list các action dựa trên thuật toán BFS vì thuật toán tìm kiếm theo chiều rộng nên sẽ tìm xung quanh con pacman trước nên 
tỉ lệ có thể tìm nút có dấu chấm gần nhất cao hơn DFS 