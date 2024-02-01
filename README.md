# Git-Github
The common git/github command

### Contents
#### 1. Initalize project
#### 2. Git basic (regularly)
<a name="GitReset"></a>
#### 3. Git reset
    - 3.1. Git reset
      - Đầu tiên, sử dụng lệnh git reset để đặt HEAD của bạn về commit commit_id:
        ```
          git reset --hard [commit_id]
        ```
        OR
        ```
          git reset --soft [commit_id]
        ```
       - Lệnh này sẽ loại bỏ các commit trước của commit_id và đặt HEAD tại commit_id
       - Sự khác nhau giữa --hard và --soft
        - --hard: Nó sẽ đặt lại HEAD về commit cụ thể và loại bỏ tất cả các thay đổi trong Index và thư mục làm việc. Các thay đổi chưa commit sẽ mất đi mà không có cơ hội khôi phục. Điều này có nghĩa là tất cả các thay đổi chưa commit (các commit ở trạng thái "Unstaged" và "Staged") sẽ mất đi và lịch sử sẽ được làm mới.
        - --soft: Ngược lại, với --soft, HEAD được đặt lại vào commit cụ thể, nhưng thay đổi chưa commit vẫn được giữ nguyên trong Index. Điều này có nghĩa là bạn có thể thực hiện lại commit ngay lập tức nếu bạn muốn, và tất cả các thay đổi sẽ được thêm vào commit mới.
    - 3.2. Git Push
      - Nếu dùng --hard:
      ```
        git push --force origin your_branch
      ```
      - Nếu dùng --soft
       ```
        git push origin your_branch
      ```
#### 4. Git amend
  - 4.1. Giữ nguyên comment log của commit
    ```
      git commit --amend --no-edit
    ```
  - 4.2. Thay đổi comment mới
    ```
      git commit --amend -m "A new comment"
    ```
#### 5. Git revert
#### 6. Git merge (regularly)
#### 7. git debase
