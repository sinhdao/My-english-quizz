# IELTS Coach

Plugin gia sư IELTS cá nhân hóa, giao tiếp bằng tiếng Việt. Mục tiêu mặc định: band 7.0 trong 12 tháng kể từ 22/11/2026.

## Làm được gì

- Kiểm tra đầu vào (ngữ pháp/từ vựng, Reading, Writing Task 2, Speaking bằng văn bản) và ước lượng band.
- Lập lộ trình theo khoảng cách giữa band hiện tại và mục tiêu của từng kỹ năng.
- Luyện và chấm Writing, Speaking, Reading theo tiêu chí, kèm bản viết lại cao hơn khoảng 1 band.
- Theo dõi lỗi lặp lại và từ vựng cần ôn trong file `ielts-progress.md`.

## Giới hạn

- Không đánh giá được Listening (không có audio) và Pronunciation (không nghe được giọng).
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
- "Luyện Speaking Part 2 với tôi."

Cuối mỗi buổi, lưu bản tóm tắt tiến độ để buổi sau dán lại nếu không có file.
