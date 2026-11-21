# IELTS Coach

Plugin gia sư IELTS cá nhân hóa, giao tiếp bằng tiếng Việt. Mục tiêu mặc định: band 7.0 trong 12 tháng kể từ 22/11/2026.

## Làm được gì

- Kiểm tra đầu vào (ngữ pháp/từ vựng, Listening khi có audio, Reading, Writing Task 2, Speaking và Pronunciation khi có bản ghi âm) và ước lượng band.
- Lập lộ trình theo khoảng cách giữa band hiện tại và mục tiêu của từng kỹ năng.
- Luyện và chấm Listening, Reading, Writing, Speaking theo tiêu chí khi có đủ dữ liệu; Speaking có thể kèm Pronunciation từ bản ghi âm.
- Theo dõi lỗi lặp lại và từ vựng cần ôn trong file `ielts-progress.md`.

## Giới hạn

- Listening cần audio bài nghe và giao diện có khả năng phân tích audio. Pronunciation cần bản ghi âm và giao diện có khả năng phân tích giọng nói. Nếu thiếu audio hoặc giao diện không đọc được tệp, tiêu chí tương ứng được ghi là “chưa đánh giá”.
- Band chỉ là ước lượng của AI để định hướng, không thay thế bài thi thật.

## Cấu trúc

```
ielts-coach/
├── .claude-plugin/plugin.json
└── skills/ielts-coach/
    ├── SKILL.md
    └── references/
        ├── placement-test.md
        ├── rubrics.md
        ├── audio-assessment.md
        └── roadmap.md
```

## Cài đặt (Claude Code)

```
/plugin marketplace add sinhdao/my-english-quizz
/plugin install ielts-coach@my-english-quizz
```

Hoặc copy thư mục `ielts-coach/skills/ielts-coach/` vào `~/.claude/skills/` để dùng như một skill cá nhân.

## Cách dùng

Mở cuộc trò chuyện mới và nhắn, ví dụ:

- "Cho tôi làm bài kiểm tra đầu vào IELTS."
- "Lập lộ trình tuần này cho tôi."
- "Chấm bài Writing này theo band." (dán bài viết)
- "Chấm Listening này." (gửi audio và câu trả lời sau khi làm)
- "Đánh giá phát âm trong bản ghi Speaking này." (gửi file ghi âm)
- "Luyện Speaking Part 2 với tôi." (gửi bản ghi âm nếu muốn nhận xét Pronunciation)

Cuối mỗi buổi, lưu bản tóm tắt tiến độ để buổi sau dán lại nếu không có file.
