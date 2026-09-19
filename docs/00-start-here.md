# Writing System: Bắt đầu từ đây

> Hướng dẫn cài đặt và dùng bộ Writing System. Đọc file này trước.

---

## Bộ này có gì

Writing System là bộ 13 skill cho Claude, biến quá trình viết content thành một hệ thống
chạy lại được nhiều lần. Chia 2 lớp.

**Lớp Foundation (5 skill): setup một lần cho mỗi mảng viết**

- **about-me-hn**: bạn là ai, viết cho ai.
- **work-context-hn**: công việc hiện tại của bạn.
- **project-context-hn**: một dự án cụ thể.
- **defi-audience-hn**: người đọc của một kênh nội dung.
- **voice-profile-builder-hn**: giọng văn của bạn, học từ bài cũ.

Cộng **tài liệu tham chiếu** cấp sẵn (không phải skill):
- **anti-ai-rulebook**: 2 file quy tắc bắt giọng AI (tiếng Việt + tiếng Anh).
- **storytelling-kit**: 12 khuôn chuyện + 10 kỹ thuật kể, tra được cả khi không chạy skill nào.

**Lớp Writing Flow (8 skill): chạy mỗi bài, qua 3 giai đoạn**

- **Think:** topic-researcher-hn -> angle-finder-hn -> outline-builder-hn
- **Write:** long-form-writer-hn / short-form-writer-hn / atomic-post-writer-hn
- **Refine:** voice-ai-auditor-hn -> repurposer-hn

---

## Mô hình dùng: Project theo từng mảng viết của bạn

Đây là phần quan trọng nhất. Bộ này hoạt động tốt nhất khi bạn tạo **Claude Project theo
từng mảng nội dung bạn viết**: mỗi Project chứa bộ file Foundation riêng phù hợp mảng đó.

Ví dụ một người có thể có 3 Project:

**Project "Branding cá nhân"**
```
- about-me.md
- personal-voice-profile.md
- audience-blog.md, audience-linkedin.md  (nhiều kênh, nhiều audience)
- anti-ai-patterns-vn.md, anti-ai-patterns-en.md, storytelling-kit.md
```

**Project "Freelance"**
```
- about-me.md
- project-context.md          (dự án client)
- client-voice-profile.md     (giọng viết cho client)
- audience-client.md
- anti-ai-patterns-vn.md, anti-ai-patterns-en.md, storytelling-kit.md
```

**Project "Công ty"**
```
- about-me.md
- work-context.md
- project-context.md
- company-voice-profile.md    (giọng công ty)
- audience-company-blog.md
- anti-ai-patterns-vn.md, anti-ai-patterns-en.md, storytelling-kit.md
```

Mỗi mảng có giọng khác, audience khác, context khác. Tách Project giữ chúng không lẫn,
viết cho công ty không vô tình lấy giọng cá nhân.

---

## Quy ước đặt tên file

Skill nhận diện file Foundation theo **từ khóa vai trò trong tên**, nên bạn đặt prefix tự do
để phân biệt giữa các Project:

| Loại | Pattern tên | Vi du |
|---|---|---|
| Voice profile | `*voice-profile.md` | `personal-voice-profile.md`, `company-voice-profile.md` |
| Audience | `audience-*.md` | `audience-blog.md`, `audience-mym.md` |
| About me | `about-me.md` | |
| Work context | `work-context.md` | |
| Project context | `*project-context.md` | `acme-project-context.md` |
| Anti-AI rulebook | `anti-ai-patterns-*.md` | (cấp sẵn) |
| Storytelling kit | `storytelling-kit.md` | (cấp sẵn) |

Điểm chính: giữ từ khóa vai trò (`voice-profile`, `audience`, `work-context`...) trong tên;
prefix thì tự do. Skill tìm file theo từ khóa đó.

---

## Cài đặt: 3 bước

### Bước 1: Cài 13 skill vào Claude

Mỗi skill là một file `.skill`. Cài lần lượt cả 13 (5 Foundation + 8 Writing Flow) vào phần
quản lý Skill của Claude. Skill cài một lần, dùng được trong mọi Project.

### Bước 2: Tạo Project cho mảng viết đầu tiên

Tạo một Claude Project (vd "Branding cá nhân"). Đây là nơi bạn sẽ viết cho mảng đó.

### Bước 3: Tạo và nạp Foundation file cho Project

Trong Project, chạy các Foundation skill để tạo file, rồi upload file vào **Project knowledge**:

1. "setup about me" -> `about-me.md`
2. "tạo voice profile" (cần 3-10 bài cũ của mảng này) -> đặt tên rõ, vd `personal-voice-profile.md`
3. "define audience cho [kênh]" -> `audience-[kênh].md` (làm cho từng kênh bạn viết)
4. work-context / project-context nếu mảng này cần
5. Bỏ 3 file tham chiếu cấp sẵn vào Project knowledge: `anti-ai-patterns-vn.md`, `anti-ai-patterns-en.md`, `storytelling-kit.md`

Xong. Project sẵn sàng. Lặp lại bước 2-3 cho mỗi mảng viết khác.

**Tối thiểu để bắt đầu:** chỉ cần `voice-profile` + rulebook là Writing Flow chạy được. about-me,
audience, context làm bài cá nhân hóa hơn nhưng không bắt buộc.

---

## Viết bài đầu tiên

Mở chat mới **trong Project** của mảng bạn muốn viết. Writing Flow đầy đủ cho bài dài:

1. "research topic [chủ đề]" -> topic-researcher chạy -> `research-brief.md`
2. "tìm angle" -> angle-finder đọc audience trong Project (hỏi nếu nhiều audience), ra `angle-brief.md`
3. "dựng outline" -> `outline.md`
4. "viết bài" -> long-form-writer đọc voice-profile trong Project, ra draft
5. "soát bài" -> voice-ai-auditor soát giọng + anti-AI, ra bản sẵn đăng

Skill tự đọc file Foundation từ Project knowledge, bạn không cần upload lại mỗi chat. Nếu
Project có nhiều audience, skill hỏi bài này viết cho audience nào (hoặc bạn nói luôn: "viết
bài blog cho [kênh]").

Xem `recipes.md` để biết các cách dùng khác, post ngắn, atomic post, repurpose.

---

## Lưu ý

- **Foundation setup một lần cho mỗi Project.** Dùng lại cho mọi bài trong Project đó.
- **Mỗi mảng viết một Project.** Giọng, audience, context khác nhau giữa các mảng.
- **Mỗi bài một chat** trong Project. Tránh lẫn context giữa các bài.
- **Skill đọc file từ Project knowledge**: để file ở đó, skill tự thấy, không cần upload lại.
- **Cập nhật voice/audience** khi chúng đổi, chạy lại skill chế độ update, thay file trong Project.
- **Tài liệu tham chiếu được cập nhật theo thời gian.** Khi có bản mới của rulebook hoặc storytelling-kit, thay file trong Project knowledge.
- **storytelling-kit tra trực tiếp được.** Không cần chạy skill nào, hỏi thẳng trong chat của Project là Claude đọc được.

---

*Built by Hoang Nguyen (@hoangthoughts). Please do not share without permission.*
