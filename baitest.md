# Bài Test Thuật Toán

**Yêu cầu:** Viết code bằng ngôn ngữ lập trình tùy chọn (ưu tiên JavaScript, TypeScript, Dart)

***Ưu tiên ghi rõ giải thích***

---

## Bài 1: Two Sum

**Đề bài:**
Cho một mảng số nguyên `nums` và một số nguyên `target`. Tìm hai số trong mảng sao cho tổng của chúng bằng `target`.

**Input:**
- `nums = [2, 7, 11, 15]`
- `target = 9`

**Output:**
- Trả về chỉ số của hai phần tử (ví dụ: `[0, 1]`)

**Yêu cầu:**
- Độ phức tạp thời gian: O(n)
- Giải thích cách tiếp cận và tại sao lại hiệu quả

**Test cases:**
```javascript
Test 1: nums = [2, 7, 11, 15], target = 9 → Expected: [0, 1]
Test 2: nums = [3, 2, 4], target = 6 → Expected: [1, 2]
Test 3: nums = [3, 3], target = 6 → Expected: [0, 1]
```

--- 

## Bài 2: Sort với Phần tử Cố định

**Đề bài:**
Cho một mảng số nguyên và một mảng boolean `fixed`. Sắp xếp mảng theo thứ tự tăng dần, nhưng các phần tử có `fixed[i] = true` không được di chuyển khỏi vị trí ban đầu.

**Input:**
- `nums = [1, 0, 2, 3, 0, 4, 0, 4, 1]`
- `fixed = [false, true, false, false, true, false, true, false, false]`

**Output:**
- `[1, 0, 1, 2, 0, 3, 0, 4, 4]`

**Giải thích:** Các phần tử tại vị trí 1, 4, 6 (có giá trị 0, 0, 0) không được di chuyển.

**Yêu cầu:**
- Giữ nguyên vị trí các phần tử cố định
- Sắp xếp các phần tử còn lại theo thứ tự tăng dần

**Test cases:**
```javascript
Test 1: nums = [1, 0, 2, 3, 0, 4, 0, 4, 1], fixed = [false, true, false, false, true, false, true, false, false]
        → Expected: [1, 0, 1, 2, 0, 3, 0, 4, 4]
        
Test 2: nums = [5, 3, 2, 4, 1], fixed = [false, true, false, true, false]
        → Expected: [1, 3, 2, 4, 5]
```

---

## Bài 3: Tìm Min Max

**Đề bài:**
Viết hàm tìm giá trị nhỏ nhất và lớn nhất trong mảng với số lần so sánh tối thiểu.

**Input:**
- `nums = [3, 5, 1, 8, -2, 7, 4]`

**Output:**
- `{min: -2, max: 8, comparisons: X}` (trong đó X là số lần so sánh đã thực hiện)

**Yêu cầu:**
- Tối ưu hóa số lần so sánh
- Độ phức tạp thời gian: O(n)
- So sánh với phương pháp naive (2n-2 so sánh)
- Mục tiêu: 3n/2 - 2 so sánh

**Test cases:**
```javascript
Test 1: nums = [3, 5, 1, 8, -2, 7, 4] → min: -2, max: 8
Test 2: nums = [10] → min: 10, max: 10
Test 3: nums = [1, 2] → min: 1, max: 2
```

---

## Bài 4: Subarray Target Sum

**Đề bài:**
Cho một mảng số nguyên dương và một số `target`. Tìm subarray liên tiếp có tổng bằng `target`.

**Input:**
- `nums = [1, 4, 2, 3, 5, 7, 8, 9]`
- `target = 12`

**Output:**
- Chỉ số bắt đầu và kết thúc của subarray (ví dụ: `[1, 3]` cho subarray `[4, 2, 3]`)
- Nếu không tìm thấy: trả về `[-1, -1]`

**Yêu cầu:**
- Sử dụng kỹ thuật sliding window
- Độ phức tạp thời gian: O(n)
- Độ phức tạp không gian: O(1)

**Test cases:**
```javascript
Test 1: nums = [1, 4, 2, 3, 5, 7, 8, 9], target = 12 → Expected: [3, 5] (subarray [3, 5, 4])
Test 2: nums = [1, 2, 3, 4, 5], target = 9 → Expected: [1, 3] (subarray [2, 3, 4])
Test 3: nums = [1, 2, 3], target = 10 → Expected: [-1, -1]
```

---

## Bài 5: Delete Duplicates

**Đề bài:**
Cho một mảng đã được sắp xếp, xóa các phần tử trùng lặp sao cho mỗi phần tử chỉ xuất hiện một lần. Trả về độ dài mới của mảng.

**Input:**
- `nums = [0, 0, 1, 1, 1, 2, 2, 3, 3, 4]`

**Output:**
- Độ dài mới: `5`
- Mảng sau khi xử lý: `[0, 1, 2, 3, 4, _, _, _, _, _]` (các vị trí _ có thể chứa giá trị bất kỳ)

**Yêu cầu:**
- Không sử dụng thêm không gian (in-place)
- Độ phức tạp thời gian: O(n)
- Độ phức tạp không gian: O(1)
- Sử dụng kỹ thuật two pointers

**Test cases:**
```javascript
Test 1: nums = [0, 0, 1, 1, 1, 2, 2, 3, 3, 4] → Length: 5, Array: [0, 1, 2, 3, 4, ...]
Test 2: nums = [1, 1, 2] → Length: 2, Array: [1, 2, ...]
Test 3: nums = [1, 2, 3] → Length: 3, Array: [1, 2, 3]
```
