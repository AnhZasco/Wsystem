# ANTI-AI WRITING PATTERNS — Tiếng Việt

> Tổng hợp các pattern AI writing cần tránh khi viết content tiếng Việt.
> Rút từ nhiều session diff giữa bản AI draft và bản người viết edit lại.
> Part of the Writing System bundle. Skill `voice-ai-auditor-hn` đọc file này runtime.
> Cũng dùng được standalone như một checklist edit.

---

## NGUYÊN TẮC GỐC — STACKED SIGNALS

**1 dấu hiệu lẻ = YẾU. Chỉ flag mạnh khi nhiều dấu hiệu CHỒNG NHAU qua structure + stance + rhythm.**

AI-origin detection là probabilistic, không forensic. 1 từ off-brand, 1 câu parallel lẻ → yếu, đừng over-flag. Dấu hiệu mạnh khi stack: mở bài generic + transition templated + nhịp câu đều đều competent + nominalized/impersonal + thiếu epistemic individuality + stylistic uniformity quá đều.

Hệ quả khi audit:
- Nghi 1 cụm lẻ → ĐỀ XUẤT, không tự thay (false positive cao, "AI words" đang diffuse vào văn người thật).
- Flag mạnh + tự sửa → chỉ khi nhiều dấu hiệu cùng xuất hiện.
- **"Polished ≠ voiced"**: bài trơn tru từng câu vẫn có thể thiếu messy variability của con người (variation ở openings, transitions, intensifiers). Đây là dấu hiệu AI khó thấy nhất.

**3 tầng audit:** Macro (argument architecture, cách mở/đóng) → Meso (paragraph logic, transition, over/under-explain) → Micro (nhịp câu, hedging, dấu câu, function words). Fix structure TRƯỚC sentence polish — voice problem thường nằm upstream.

**GỐC CHUNG CỦA NHIỀU LỖI: AI thích sự CÂN ĐỐI.** Anaphora, phản đề, cặp đối xứng, seal punch 2 câu cụt — đều là biến thể của cùng một xu hướng làm câu "đẹp." Giọng người thật chấp nhận LỆCH, CỤT, PHẲNG. Khi phân vân giữa câu cân đối và câu lệch nhịp → chọn lệch.

---

## 1. CẤU TRÚC CÂU KIỂU ANH

### 1a. Parallel structure đối xứng
- Sai: "Đau mà không hiểu thì chỉ là đau. Đau mà hiểu thì thành nền."
- Đúng: "Ai cũng đau, nhưng người hiểu được mình đau vì cái gì thì sẽ đứng lại được, còn người chỉ chịu mà không hiểu thì cứ lặp lại hoài."
- Test: 2 vế đối xứng cả structure + length + predicate → cắt. Single comparison "thay vì" = OK.

### 1b. Staccato fragments
- Sai: "phải được xây dựng. Mỗi ngày. Có chủ đích."
- Đúng: "phải được xây dựng mỗi ngày một cách có chủ đích, không ai làm thay bạn được."
- Tiếng Việt chảy bằng phẩy, không chẻ bằng chấm.

### 1c. "Nhịp 3 câu ngắn" seal đoạn
- Sai: "Không gọi tên được. Không kể cho ai được. Vì nó không có hình."
- Đúng: "Nhưng khi ra về, ở trong họ luôn có một khoảng trống không thể gọi tên."
- 3 câu ngắn liên tiếp = AI showing off rhythm. 1 câu prose chảy đủ rồi.
- Exception: OK nếu MỖI câu add observation MỚI, không restate.

### 1d. "Không phải X, mà là/để/vì Y"
- CÓ ĐIỀU KIỆN, không cấm tuyệt đối. Cấm khi: đối xứng cứng, lặp 2+ lần, dịch nguyên aphorism English.
- OK khi: nhấn một tương phản thật, 1 lần, nhịp Việt tự nhiên.
- "Không chỉ X, mà còn Y" gần như luôn OK — tách riêng khỏi lệnh cấm.

### 1e. Nghịch lý "X nhất lại là Y nhất"
- Calque "hardest = simplest." Sai: "bước khó nhất lại nằm ngay chỗ tưởng đơn giản nhất."
- Đúng: "bước này khó nhất, cũng là bước quan trọng nhất." Khẳng định trực tiếp.

### 1f. Symmetric contrast tách thành 2 câu cụt
- Sai: "Sự thật của bạn vẫn có thật. Nó chỉ không phải là sự thật duy nhất." (nhịp staccato lấy punch = cadence AI)
- Đúng: "dù sự thật của bạn vẫn là thật, nhưng nó không phải là sự thật duy nhất." (nối dù/nhưng/mà trong 1 câu chảy)
- Cùng nhóm: seal 2 câu cụt punch "Bận thì ai cũng bận. Chỉ cần biết mình đang bận trong chế độ nào." → gộp 1 câu liền có trục so sánh: "Ai cũng bận, chỉ hơn nhau ở chỗ bận trong chế độ nào."

### 1g. Cặp 2 vế cắt gọn đối xứng → NỚI ra
- Sai: "chẳng ai giao, chẳng ai nhắc" (cú pháp ngắn giống hệt = AI-crisp)
- Đúng: "chẳng ai giao cho, cũng chẳng ai nhắc nhở"
- Cách chữa không chỉ là tránh, mà là NỚI: thêm liên từ (cũng/mà/lại), dùng động từ đủ chữ thay cụt ("nhắc" → "nhắc nhở").

### 1h. Anaphora hai nhịp
- Sai: "chỉ mình biết cách làm thì mình còn cần thiết, chỉ mình chạy được cái này thì công ty còn cần mình" (2 vế cùng mở đầu, nói CÙNG 1 ý = dư thừa)
- Đúng: "nếu chỉ mình biết cách làm việc gì đó, thì mình sẽ trở nên cần thiết và khó bị thay thế" (gộp 1)
- Exception: 2 vế cùng mở đầu nhưng đưa 2 VÍ DỤ KHÁC nhau ("mỗi lần bạn nghỉ phép... mỗi lần một việc bị pending...") = OK.

---

## 2. CỤM DỊCH THẲNG TỪ TIẾNG ANH

| English pattern | Vietnamese dịch (SAI) | Vietnamese tự nhiên (ĐÚNG) |
|---|---|---|
| "doesn't come from X. It comes from Y" | "không đến từ việc X. Nó đến từ việc Y" | "Lý do thật ra ở chỗ khác..." |
| "Although X, it still Y" | "Dù X, nó vẫn Y" | "Dù X tới đâu, Y cũng..." |
| "the first... the second..." | "cái thứ nhất... cái thứ hai..." | "câu trước... câu sau..." / "cái này... cái kia..." |
| "When that's gone" | "Khi cái đó không còn nữa" | "Tới lúc không còn..." |
| "on this spectrum" | "trên cái phổ này" | "trong tình trạng này" |
| "you're not alone" | "bạn không cô đơn" | "không phải mình bạn đang vậy đâu" |
| "answer the question of who you are" | "trả lời câu hỏi mình là ai" | "biết mình là ai" |
| "packaged as" | "được gói lại thành" | "lâu dần thành" |
| "a room full of people" | "một phòng đầy người" | "ngoài kia" / "xung quanh" |
| "set of X" | "bộ X" | "danh sách X" hoặc bỏ luôn |
| "live with it" | "sống cùng nó" | "đã là vậy rồi" / "không thể đổi được nữa" |
| "I'm building" | "đang xây [community/brand]" | "lập ra," "dẫn dắt," "tạo ra" |
| "it is what it is" | "A là A" (tautology) | Câu có content mới để đóng |
| "pretty real / quite true" | "khá thật / khá đúng" | "khá gần / khá sát" (adj cụ thể) |
| "silently + verb" | "thầm + verb process" | "thầm" chỉ đi với verb nói/cảm xúc |
| "if you look around" | "nếu nhìn quanh một chút" | "ngoài kia bạn vẫn sẽ thấy" |
| "ignore" | "bỏ qua / phớt lờ" | "mặc kệ" (giữ thái độ) |
| "friction / resistance" | "ma sát" | "sức ỳ" |
| "carry a feeling" | "mang theo cảm giác" | "dễ cảm giác" / "dễ thấy" |
| "becomes invisible" | "thành vô hình" | "thành chuyện đương nhiên" / "không còn thấy nó nữa" |
| "a point on the path" | "một điểm trên đường" | "chuyện dọc đường" |
| "bad day" | "ngày tệ" | "hôm mệt" / "hôm oải" / "hôm bận" |
| "one thing in common" | "có một thứ chung" | "có một điểm chung" |
| "overrated" | "bị đánh giá cao quá mức" | "được xem là toàn bộ câu chuyện" / "được tung hô quá" |
| "running in your head" | "(giọng nói) chạy trong đầu" | "câu mình đang tự nói trong đầu" |
| "the feeling of X is real" | "cảm giác X có thật" | "cái cảm giác mình đang X là có thật" |

---

## 3. BUILDUP GIẢ (câu mở không tự nhiên)

Người Việt không mở câu bằng buildup tạo kịch tính giả:
- Tránh: "Có một thực tế mà ít người chia sẻ:"
- Tránh: "Mình từng nghe một câu mà cứ theo mình mãi:"
- Tránh: "Có một nỗi sợ ít ai nói ra nhưng..."
- Tránh: "Và đây là điểm đáng lưu ý." / "Điều thú vị là" / "Điểm quan trọng ở đây là"
- Tránh: "Trong bối cảnh [X] phát triển không ngừng..." — mở bài dịch máy điển hình. Thay bằng "Khi [X] ngày càng phát triển..." hoặc vào thẳng.
- Tránh câu dẫn lấy đà khi kể: "mình để ý một chuyện," "mình nhận ra một điều," "có một chuyện thế này" → vào thẳng nội dung, chấp nhận cả câu cụt ("Theo kinh nghiệm cá nhân ở vị trí giao việc.")

Test: "Người Việt bình thường có mở câu kiểu này không?"

---

## 4. DRAMATIC LABELING

Nội dung tự nặng, không cần setup dramatic:
- Tránh: "bài học đau đớn / khá đau", "điều đáng sợ là", "điều nguy hiểm là", "điều trớ trêu là", "Đây là dấu hiệu tinh tế mà ít ai nói"
- Lưu ý: "sự thật phũ phàng" KHÔNG mặc định là sáo AI — chấp nhận trong nhiều giọng. Đề xuất, đừng tự cắt.

---

## 5. CLAIM RARITY / SECRET

- Tránh: "ít ai gọi tên thẳng", "không ai nói thẳng", "hiếm khi được nhắc tới", "hiếm ai nhận ra", "ít ai để ý"
- Tất cả variants "[ít/không] + ai/người + [verb nói/biết]"
- Self-importance ngầm, Medium thought leader tone.
- Test: xóa phrase → observation còn đứng không? Nếu có → mạnh hơn khi xóa.

---

## 6. RULE OF THREE (gom 3 synonym)

- Tránh: "sự kiên trì, bền bỉ và quyết tâm", "rõ ràng, cụ thể và thực tế", "lắng nghe, thấu hiểu và đồng hành"
- 3 từ/cụm cùng nghĩa đứng cạnh nhau → cắt còn 1-2, hoặc viết thành câu chảy.
- 3 thứ thật sự KHÁC nhau → OK.

---

## 7. SYNONYM CYCLING (elegant variation)

- Tránh: "công việc... nghề nghiệp... sự nghiệp..." xoay vòng trong cùng đoạn
- Người Việt viết tự nhiên lặp từ khi cần. "Công việc" đúng thì cứ "công việc" 3 lần.

---

## 8. PHÂN TÍCH HỜI HỢT CUỐI CÂU

- Tránh: "...góp phần tạo nên sự thay đổi tích cực", "...phản ánh sự trưởng thành trong tư duy", "...thể hiện tinh thần không ngừng phát triển"
- Test: bỏ cụm cuối mà câu vẫn đủ ý → đó là filler, cắt.

---

## 9. FORCED CONTRAST THỪA

- Tránh: "Nghe thì X nhưng thực ra Y" khi X là điều ai cũng biết
- Tránh: "Ba câu hỏi này nghe đơn giản, nhưng để trả lời trung thực thì không dễ chút nào."
- Nguyên tắc: nếu "nghe thì X" là điều hiển nhiên → bỏ, vào thẳng Y.

---

## 10. ABSTRACT NOUN LÀM CHỦ THỂ

- Tránh: "đề cao kinh nghiệm giải quyết vấn đề"
- Đúng: "đề cao những người có kinh nghiệm giải quyết vấn đề"
- Abstract noun làm chủ thể nghe AI-flavored. Concrete subject (người, nhóm cụ thể) = cách người Việt nói.

---

## 11. COMPRESSION ĐỂ PUNCH

- Tránh: "Feedback lúc đó chỉ là cú chốt."
- Đúng: "Feedback lúc đó chỉ là giúp họ điều chỉnh nhanh hơn mà thôi."
- Test: compound mới không tồn tại trong tiếng Việt → restore full phrase + softener "mà thôi."

---

## 12. NEGATIVE-AVOIDANCE ENDING

- Tránh: "bạn sẽ không thấy hoảng hay nản mỗi khi trượt một ngày"
- Đúng: "bạn sẽ thấy tự chủ hơn khi gặp ngày khó khăn"
- AI default nói cái reader TRÁNH. Viết tự nhiên nói cái reader CÓ.

---

## 13. HẬU QUẢ WORKFLOW THAY VÌ TÂM LÝ

- Tránh: "không giải quyết được gì lâu dài" (workflow, reader đã biết)
- Đúng: "tư duy nạn nhân trở nên lì lợm hơn, khó gỡ" (psychological, chạm identity)
- Tránh: "một nếp xấu bắt đầu hình thành" (label trừu tượng)
- Đúng: "tiếng nói cản trở mạnh hơn trong đầu" (trải nghiệm nội tâm)

---

## 14. PROSE ENUMERATION (thay numbered list)

- Tránh: "Phần chọn mục tiêu giúp bạn... Phần đặt mục tiêu... Còn phần dựng thói quen..."
- Đúng: "01. Chọn mục tiêu... / 02. Lập kế hoạch... / 03. Biến hành động..."
- Framework synthesis đa-phần → numbered list gọn, không prose.

---

## 15. RHYTHM FILLER BỊ CẮT

AI hay cắt "lại/thì/đang/có" để punch, đây là English writing instinct. Tiếng Việt CẦN filler cho flow:
- Tránh: "gốc của nó nằm ngoài bạn" → Đúng: "gốc rễ của nó **lại** đến từ bên ngoài"
- Tránh: "Phần đầu họ làm qua loa" → Đúng: "Phần đầu **thì** làm qua loa"

---

## 16. OVER-CORRECT "NÓ"

- AI hay thay "nó" bằng "chính tầm nhìn đó" — over-formal.
- "Nó" = đại từ tiếng Việt bình thường. Chỉ thay khi referent thật sự mơ hồ.

---

## 17. OVER-CORRECT ENGLISH CASUAL

AI Việt hóa hết mọi English term = quá cứng:
- **GIỮ** (đã internalize trong workplace VN): fix, break, build, routine, ship, launch, commit, sprint, deadline
- **CẮT** (calque cấu trúc câu): script, set of X, packaged as
- Test: "Dân đi làm VN tech có nói từ này hàng ngày không?" Có → giữ.

---

## 18. 2+ CÂU HỎI RHETORICAL LIÊN TIẾP

- Tránh: "Họ có thấy đúng cái bạn đang thấy không? Họ có nhận ra... Hay đang ở một cái bản đồ hoàn toàn khác?"
- Đúng: "Câu trả lời của họ sẽ cho bạn thấy họ có đang tự mình nhìn thấy được vấn đề hay không."
- 2+ rhetorical questions liên tiếp = AI padding → chuyển thành 1 câu declarative.

---

## 19. LẶP CẤU TRÚC CÂU TRONG CÙNG BÀI

5 dạng lặp cần scan:
1. Motif câu: "Nghe thì X nhưng Y" x2
2. Mở đầu đoạn: "Mình từng..." mở 2 đoạn
3. Parallel ẩn: 3 lần "cần" trong 3 câu liên tiếp
4. Liệt kê lặp khuôn: "Sếp X thì bạn cần Y" x3
5. Cụm từ nguyên văn: cùng 1 cụm xuất hiện ở 2 vị trí

Ngoại lệ: backbone motif có chủ đích ("Hãy đổi tư duy từ X sang Y" lặp mỗi mục).

---

## 20. LẶP CẤU TRÚC GIỮA CÁC BÀI LIÊN TIẾP

Reader đọc nhiều bài liên tiếp cảm thấy "AI viết" nếu signature move lặp y chang giữa các bài:
- Closer ("viết bài này để tự nhắc"), opener, aside, vulnerable disclosure, transition, seal.
- Function lặp được (bài nào cũng có closer), nhưng CÁCH THỰC HIỆN phải khác bài trước.
- Detection: so với closer/opener 1-2 bài gần nhất → đổi variant cùng function.

---

## 21. HEDGE NUANCE — 2 RULES NGƯỢC NHAU

AI hay apply 1 direction cho cả 2 context:
- **Heading/thesis = dứt khoát.** Cắt "có thể." Sai: "Mục tiêu có thể hỏng..." → Đúng: "Mục tiêu 'chết' ngay từ lúc..."
- **Câu quan sát đời thường = mềm.** Sai: "Đời không bao giờ chạy đúng kế hoạch" → Đúng: "Kế hoạch thường ít khi nào chuẩn"

---

## 22. LIÊN TỪ KẾT NỐI CỨNG

AI hay nối câu bằng liên từ trang trọng, nghe như văn bản hành chính:
- Tránh: "Hơn nữa", "Thêm vào đó", "Bên cạnh đó", "Đáng chú ý là", "Không những vậy"
- Người Việt nói chuyện nối ý bằng: "Mà", "Rồi", "Ngoài ra" (nhẹ), hoặc xuống dòng không cần liên từ.
- Test: bỏ liên từ ra, hai câu đặt cạnh nhau có tự hiểu quan hệ không? Nếu có → bỏ liên từ.

---

## 23. TỪ SÁO RỖNG TIẾNG VIỆT

Danh sách từ AI Việt lạm dụng, nghe sang nhưng rỗng:
- "đa chiều", "toàn diện", "giải pháp toàn diện"
- "chuyên sâu", "khám phá sâu", "đào sâu"
- "đồng bộ hoá", "thỏa mãn nhu cầu", "đáp ứng nhu cầu"
- "không ngừng", "vượt trội", "đột phá", "tối ưu" (khi dùng làm tính từ marketing)
- "nâng tầm", "kiến tạo", "lan toả", "trải nghiệm" (lạm dụng)

**Không cấm cứng:** nhiều từ trên là từ thật khi dùng đúng nghĩa cụ thể ("tối ưu database", "đồng bộ data giữa 2 hệ thống"). Chỉ flag khi dùng theo nghĩa marketing rỗng, không trỏ tới cái gì cụ thể.

Test: từ này có trỏ tới một cái cụ thể, đo được không? Có → giữ. Chỉ để nghe sang → cắt.

---

## 24. SO SÁNH NHẤT KHI KHÔNG KHỚP Ý

- Tránh: "kết nối sâu nhất" (với tới superlative để tăng sức nặng)
- Đúng: "kết nối sâu sắc" (khi ý không thật sự là "nhất")
- Đừng mặc định superlative. Chỉ dùng "nhất" khi thật sự là nhất.

---

## 25. CÂU GIẢI THÍCH TRỪU TƯỢNG THAY PROVENANCE THẬT

- Tránh: "Mình thấy nó đáng để biết, vì gọi được tên chỗ mình đang đứng thì mới chủ động dịch chuyển được." (lý do trừu tượng đóng gói gọn = mùi AI)
- Đúng: "Mình đã mất khá nhiều thời gian với ChatGPT để ra được sơ đồ này." (provenance thật)
- Khi giới thiệu thứ mình làm/tìm ra, dùng chi tiết khâu sản xuất thật thay câu lý do trừu tượng.

---

## 26. TỪ ĐƠN THAY VÌ TỪ GHÉP (tiếng Việt ưu tiên từ ghép)

AI hay dùng từ đơn nghe cộc; tiếng Việt thuần ưu tiên từ ghép hai âm tiết:
- chăm → chăm chỉ, nền → nền tảng, kém → kém cỏi, chai → chai sạn, mềm → mềm mại
- né → né tránh, bận → bận rộn, đau → đau đớn, sâu → sâu sắc, lạnh → lạnh lùng, lệch → lệch lạc
- nối → kết nối, rộng → mở rộng, biết → nhận biết, cảm → cảm nhận, tỉnh → tỉnh táo, giữ → kiên trì, mệt → mệt mỏi

Rule: khi có từ ghép sạch tương đương, LUÔN chọn ghép. Enforce nhất quán — đây là pattern bị miss nhiều nhất.
Exception: từ đơn đã đủ tự nhiên trong văn cảnh (đi, đến, nói, viết) → không ép ghép.

---

## 27. NHÃN PHẨM CHẤT TRỪU TƯỢNG ĐỨNG TRẦN (abstraction / self-help register)

Nhãn phẩm chất gắn tên một đức tính mà không nói ra nó là gì: vững, mạnh, bền, trưởng thành, kiên cường, bình tĩnh...
- **Delete test**: xóa nhãn → câu vẫn đứng nhờ mô tả hành vi cụ thể → bỏ nhãn. Câu rỗng → chưa viết ra hành vi, viết hành vi trước. Muốn giữ → định nghĩa bằng cơ chế cụ thể.
- Sai: "Vững là mỗi lần lại nhận ra sớm hơn, dựng lại nhanh hơn." → Đúng: "Chỉ là mỗi lần lại nhận ra sớm hơn, dựng lại nhanh hơn."
- Pattern tốt: "Bình tĩnh giữa lúc loạn không phải tính cách trời cho, nó là cái nhịp đó được tập đủ nhiều thành quen."
- Adapt English: đừng mirror sự lặp từ-phẩm-chất gốc (strong/strength/resilience → 1 từ Việt lặp lại).
- Ranh giới: chỉ cấm nhãn đứng trần làm payoff khi cạnh đã có mô tả cụ thể. Ưu tiên gỡ nhãn positive trước.

---

## 28. PHẢN ĐỀ CÂN ĐỐI ĐÓNG BÀI

- Sai: kết bài bằng cặp đối xứng gọn gàng "Công sức bỏ ra thì chỉ mình biết... còn cái để lại thì người khác mới đếm" (khung X thì A, Y thì B)
- Đúng: kết bằng hình ảnh hoặc hành động cụ thể, lệch nhịp: "Hãy vỗ tay cho người khác, và chờ đến lượt của mình."
- AI hay cài khung phản đề ở cả mở lẫn kết. Câu/đoạn kết không được là cặp đối xứng.

---

## 29. MOTIF ENGINEERED (chữ writerly lặp làm keo + keyword threading + callback neo xa)

- Sai: chọn 1 chữ writerly ("nhịp," "chạy," "canh," "để lại") rồi lặp xuyên đoạn làm chất keo — đọc ra giọng có dụng công. "Nhịp đó an toàn" (ngay sau "nhịp này") → "Làm theo kiểu này thì an toàn."
- Sai: cố thread 1 keyword thành motif xuyên bài ("hẹp" lặp nhiều lần khắp bài) — engineered, không tự nhiên.
- Sai: callback "như vậy / như thế" neo vào từ khóa cách đó nhiều đoạn — reader mất mạch, phải cuộn ngược. "cái hôm nay bạn tin chắc có khi cũng hẹp như vậy" → "cái hôm nay bạn tin nhiều khi đã tự nó lỗi thời." (gọi thẳng ý mới bằng ngôn ngữ của chính câu đó)
- Phân biệt: backbone motif CÓ CHỦ ĐÍCH được phép (chữ khẩu ngữ đời thường "chán/chờ/làm," motif đã chốt với người viết) — cấm là motif tự phát sinh khi draft để làm văn.

---

## 30. ĐỘNG TỪ THỔI PHỒNG

- Sai: "sự phát triển cá nhân của bạn đang bị đe dọa" (AI leo thang mức độ)
- Đúng: "sự phát triển cá nhân của bạn đang bị chậm lại" (đúng thực tế)
- Tránh động từ đao to (đe dọa, hủy hoại, đánh mất) khi hiện tượng thật chỉ ở mức nhẹ hơn. Chọn động từ đúng cường độ.

---

## 31. SÁO TRẤN AN "[TÍNH TỪ] HƠN BẠN NGHĨ"

Khuôn tổng quát: **[tính từ] + hơn + bạn nghĩ / bạn tưởng / tưởng tượng**. Áp cho MỌI tính từ, không chỉ vài cụm quen.

- Sai: "nhỏ hơn nhiều so với bạn nghĩ" / "dễ hơn bạn tưởng" / "đơn giản hơn tưởng tượng" / "mỏng hơn bạn tưởng" / "gần hơn bạn nghĩ"
- Đúng: nói thẳng mức độ, bỏ vế so sánh. "Để bắt đầu thì đơn giản." / "Cái ranh giới đó mỏng lắm."
- Vì sao lọt: bản trước chỉ list vài cụm cố định nên tính từ khác trượt qua. Nhận diện bằng KHUÔN, không bằng danh sách.

---

## 32. LẶP INTENSIFIER TRONG CÙNG CÂU

- Sai: "luôn có những tháng dài mình luôn ở trong chế độ phản ứng"
- Đúng: "luôn có những tháng dài mình ở trong chế độ phản ứng"
- Không lặp cùng một intensifier (luôn, rất, cứ) trong cùng câu — giữ lần đầu.

---

## 33. SEAL LƯỢC CHỮ CHO "ĐẮT" + CỤM HAI NGHĨA Ở VỊ TRÍ CHỐT

- Sai: "Ai cũng đang nói thật, từ chỗ của họ." (lược chữ nghe gọn-đắt = thẩm mỹ AI; "nói thật" 2 nghĩa)
- Đúng: "Ai cũng đang nói sự thật, từ góc nhìn họ đang đứng." (đủ chữ, câu vẫn mạnh, hết mơ hồ)
- Câu seal/câu chốt không cần cụt chữ để mạnh. Viết đủ. Tránh cụm hai nghĩa ở vị trí chốt — đó là chỗ reader mang theo.

---

## 34. ĐOẠN ĐUÔI RESTATE META

- Sai: dựng đoạn riêng "Điều mình tự nhắc bây giờ không còn là..." / "Chỉ cần vậy thôi đã đủ để..." — restate insight vừa nêu bằng khung meta, không thêm ý mới.
- Đúng: gộp ý tự nhắc vào 1 câu trong đoạn có sẵn ("Nhưng phải luôn tự nhắc mình điều này: ...").
- Nếu đoạn mới không đẩy ý tiến thêm → cắt.

---

## 35. TITLE TRỪU TƯỢNG LỚN

- Sai: "Hai chế độ cuộc đời" (AI với tay lên chữ hoành tráng life-scale)
- Đúng: "Hai chế độ bận rộn" (neo vào triệu chứng cụ thể người đọc đang cảm)
- Title ưu tiên neo cụ thể vào cái reader đang cảm, tránh chữ to (cuộc đời, số phận, hành phúc).

---

## LƯU Ý — KHÔNG PHẢI LÚC NÀO CŨNG LỖI (false positive cao)

Đề xuất, đừng tự thay:
- **"Sự thật phũ phàng"** — chấp nhận trong nhiều giọng, KHÔNG mặc định sáo AI.
- **Nominal hóa nhẹ** ("nhận được sự giúp đỡ cần thiết") — có thể là chủ ý làm nhẹ, không tự cắt thành dạng cộc ("được đỡ thật").
- Khi nghi 1 cụm là sáo/AI → đề xuất cho người viết, đừng tự thay.

---

## 36. "MỘT CÁCH + TÍNH TỪ" (adverb of manner tiếng Anh)

- Sai: "dễ chịu một cách nguy hiểm" (dangerously comfortable)
- Đúng: tách thành mệnh đề, "nguy hiểm ở chỗ nó dễ chịu"
- Chỉ flag khi hai tính từ NGHỊCH nhau bị ép chồng theo khuôn adverb Anh, tức adj₂ đang đánh giá adj₁.
- Hợp lệ, không flag: "một cách có chủ đích", "một cách tự nhiên", "một cách bài bản". Đây là tiếng Việt sạch.

---

## 37. DANH TỪ TRỪU TƯỢNG LÀM CHỦ THỂ CỦA ĐỘNG TỪ NÓI (personification calque)

Khuôn: **danh từ trừu tượng + động từ giao tiếp** (nói, cho biết, cho thấy, kể, chỉ cho). Dịch thẳng từ "X tells you / X shows you".

- Sai: "quyết tâm không nói cho bạn biết mình sẽ trụ được bao lâu" / "dữ liệu cho bạn thấy" / "con số nói lên"
- Đúng: "quyết tâm không trả lời được câu mình trụ được bao lâu" / đưa người làm chủ thể, "nhìn số liệu thì thấy"
- Họ hàng với lỗi danh từ trừu tượng làm chủ thể nói chung, nhưng cụ thể hơn ở chỗ động từ là động từ giao tiếp.

---

## 38. ĐỘNG TỪ ĐỨNG TRẦN THIẾU TÂN NGỮ (intransitive kiểu Anh)

Tiếng Anh nhiều động từ tự đứng được không cần tân ngữ (to defend, to adapt, to grow). Dịch sang tiếng Việt giữ nguyên thì câu hụt.

- Sai: "phản xạ đầu tiên là bảo vệ" (to defend)
- Đúng: chọn động từ Việt tự thân đủ nghĩa, "phản xạ đầu tiên là chống chế". Hoặc thêm tân ngữ, "bảo vệ mình".
- Test: động từ đứng cuối câu không có tân ngữ thì hỏi động từ này tiếng Việt có tự đứng được không.

---

## 39. CHUỖI DANH TỪ HÓA "CÁI GIÁ CỦA VIỆC + ĐỘNG TỪ"

Khuôn: **[danh từ đo lường] + của việc + [động từ]**. Dịch thẳng từ "the cost of X-ing".

- Sai: "cái giá của việc giữ nguyên trở nên cụ thể hơn cái giá của việc đổi"
- Đúng: chuyển thành mệnh đề có chủ thể, "cứ giữ nguyên thì mình sẽ mất gì, và cái mất đó rõ hơn cái cực phải chịu khi đổi"
- Xuất hiện hai lần trong cùng một câu thì chắc chắn là dịch.

---

## 40. BỊ ĐỘNG DANH TỪ HÓA "ĐƯỢC/BỊ + ĐỘNG TỪ + BẰNG VIỆC"

Dịch thẳng từ "is maintained by / is achieved by".

- Sai: "nó được duy trì bằng việc bạn nhận ra..."
- Đúng: đưa người làm chủ thể, động từ chủ động, "bạn giữ được là nhờ nhìn ra..."

---

## 41. ĐỘNG TỪ ẨN DỤ DỊCH THẲNG

Động từ ẩn dụ tiếng Anh dịch sang thì cặp động từ và danh từ không còn có thật trong tiếng Việt.

- Sai: "giọng nói chạy trong đầu" / "suy nghĩ chạy trong đầu" / "câu hỏi chạy trong đầu" (running in your head)
- Đúng: "câu mình đang tự nói trong đầu" / "câu hỏi cứ lởn vởn"
- "Chạy" hợp lệ chỉ với: máy, chương trình, script, chân người.
- Rộng hơn: cặp động từ + danh từ phải verify có thật ngoài đời, KỂ CẢ khi động từ là từ thuần Việt. Động từ Việt vẫn có thể bị ghép với danh từ không ai ghép.
  - Sai: "cái đà gãy" (đà thì "đứt" hoặc "mất", không "gãy")
  - Sai: "bỏ qua sạch" (nói "nhảy cóc qua")
- Test: nói riêng cặp động từ + danh từ này ở quán cà phê, tách khỏi ngữ cảnh bài, có tự nhiên không.

---

## CHECKLIST NHANH — SCAN SAU DRAFT

- [ ] Parallel đối xứng 2 vế?
- [ ] 3 câu ngắn liên tiếp không add observation mới?
- [ ] "Không phải X mà Y" lặp 2+ lần? Nghịch lý "X nhất lại Y nhất"?
- [ ] Rule of Three (3 synonym gom lại)?
- [ ] Synonym cycling trong cùng đoạn?
- [ ] Cụm filler cuối câu bỏ đi vẫn đủ ý?
- [ ] Claim rarity ("ít ai," "hiếm khi")?
- [ ] Dramatic labeling ("điều đáng sợ", "điều nguy hiểm")?
- [ ] Buildup giả mở câu? Mở bài "Trong bối cảnh..."?
- [ ] Cấu trúc câu lặp 2+ lần trong bài?
- [ ] Signature move lặp với bài trước?
- [ ] Cụm dịch thẳng từ tiếng Anh?
- [ ] Abstract noun làm chủ thể?
- [ ] Compound mới compress để punch?
- [ ] Kết bullet negative-avoidance thay positive state?
- [ ] Hậu quả workflow thay hậu quả tâm lý?
- [ ] Prose enumeration thay numbered list?
- [ ] Rhythm filler bị cắt (lại/thì/đang/có)?
- [ ] "Nó" bị over-correct?
- [ ] English casual bị Việt hóa quá mức (fix, break, build)?
- [ ] 2+ câu hỏi rhetorical liên tiếp?
- [ ] Heading hedge "có thể" thay dứt khoát?
- [ ] Liên từ kết nối cứng ("Hơn nữa", "Thêm vào đó")?
- [ ] Từ sáo rỗng ("đa chiều", "toàn diện", "không ngừng")?
- [ ] So sánh nhất khi không chính xác?
- [ ] Từ đơn chỗ nên dùng từ ghép (chăm→chăm chỉ, nền→nền tảng)?
- [ ] Nhãn phẩm chất trần (vững/mạnh/bền/trưởng thành) — chạy delete test?
- [ ] Kết bài "Tóm lại", "Kết luận là"?
- [ ] Symmetric contrast tách 2 câu cụt ("X. Nó chỉ Y.")?
- [ ] Cặp 2 vế cắt gọn đối xứng chưa nới ("chẳng ai giao, chẳng ai nhắc")?
- [ ] Anaphora 2 nhịp cùng ý ("chỉ mình X... chỉ mình Y...")?
- [ ] Kết bài bằng phản đề cân đối?
- [ ] Motif engineered (chữ writerly lặp làm keo, callback neo từ khóa xa)?
- [ ] Động từ thổi phồng (đe dọa/hủy hoại khi thực tế nhẹ hơn)?
- [ ] Sáo trấn an "nhỏ hơn bạn nghĩ / dễ hơn bạn tưởng"?
- [ ] Lặp intensifier trong 1 câu (luôn... luôn)?
- [ ] Seal lược chữ / cụm 2 nghĩa ở vị trí chốt?
- [ ] Đoạn đuôi restate meta ("điều mình tự nhắc là...")?
- [ ] Câu dẫn lấy đà ("mình để ý một chuyện")?
- [ ] Title chữ to trừu tượng (cuộc đời) thay neo cụ thể?
- [ ] Sáo "[tính từ] hơn bạn nghĩ/tưởng" (mọi tính từ, không chỉ nhỏ/dễ)?
- [ ] "một cách + tính từ" với 2 tính từ nghịch nhau ép chồng?
- [ ] Danh từ trừu tượng làm chủ thể động từ nói (X cho bạn thấy, con số nói lên)?
- [ ] Động từ đứng trần thiếu tân ngữ (phản xạ là bảo vệ)?
- [ ] "cái giá của việc + động từ" và họ hàng danh từ hóa?
- [ ] "được/bị + động từ + bằng việc"?
- [ ] Cặp động từ ẩn dụ + danh từ chưa verify (chạy trong đầu, đà gãy, bỏ qua sạch)?
- [ ] Danh từ trục của bài là từ dịch từ framework gốc (thước đo ← metric)?

---

*Part of the Writing System bundle. Built by Hoang Nguyen (@hoangthoughts). Please do not share without permission.*
