# Reader Book Lite

Trình đọc sách điện tử tinh gọn cho SiYuan Notes, được fork từ [SiReader](https://github.com/mika-si/siyuan-sireader).

Hỗ trợ các định dạng PDF, EPUB, MOBI và TXT với chú thích, đánh dấu trang, từ điển, dịch thuật, TTS và giao diện chủ đề đọc sách.

## Tính năng

- Tất cả tính năng của SiReader — không bị chặn (không có cổng giấy phép/kích hoạt)
- Giao diện hoàn toàn bằng tiếng Việt
- Mục tiêu dịch thuật mặc định: Tiếng Việt — có thể chuyển đổi theo phiên
- Fork được bảo trì bởi cộng đồng

## Cài đặt

1. Tải bản phát hành mới nhất từ [Releases](https://github.com/DatTran0105/reader-book-lite/releases)
2. Trong SiYuan, vào `Cài đặt → Plugin → Import plugin` và chọn tệp `.zip` đã tải
3. Kích hoạt plugin

## Sử dụng

Mở bất kỳ tệp sách điện tử nào được hỗ trợ (PDF, EPUB, MOBI, TXT) từ cây tệp của SiYuan. Thanh công cụ đọc sách cung cấp:

- **Tô sáng/gạch chân/viền** chú thích văn bản
- **Tra từ điển** (nhấn giữ hoặc chọn văn bản)
- **Dịch thuật** — mục tiêu mặc định là Tiếng Việt, có thể thay đổi trong bảng dịch
- **Đánh dấu trang** và **điều hướng** qua mục lục
- **TTS** đọc to
- **Chủ đề đọc sách** (ngày/đêm/nâu)

## Thay đổi từ SiReader

| Thay đổi | Chi tiết |
|--------|--------|
| Cổng giấy phép | Đã loại bỏ — tất cả tính năng miễn phí |
| Lời nhắc kích hoạt/nâng cấp | Đã loại bỏ |
| Phần cài đặt thành viên | Đã ẩn (giữ nguyên liên kết template) |
| Ngôn ngữ giao diện | Tiếng Việt (~637 thay thế chuỗi) |
| Dịch thuật mặc định | Tiếng Việt (`vi`) thay vì tiếng Trung (`zh-CN`) |
| Tên plugin/phiên bản | `reader-book-lite` v1.0.0 |

## Từ điển ngoại tuyến

Reader Book Lite hỗ trợ từ điển ngoại tuyến **StarDict**. Bạn có thể tải xuống và nhập từ điển của riêng mình để tra từ mà không cần internet.

### Nguồn từ điển tương thích

Các nguồn này cung cấp tệp StarDict `.ifo`/`.idx`/`.dict.dz` hoạt động với plugin:

| Nguồn | Ngôn ngữ | Ghi chú |
|--------|-----------|-------|
| [tudien](https://github.com/redphx/tudien) | Anh ↔ Việt | Từ điển hiện đại, định nghĩa HTML |
| [OVDP stardict-dict](https://github.com/lpdevs/stardict-dict) | Việt ↔ Anh, Việt ↔ Trung, Anh ↔ Trung | Định dạng văn bản thuần, số lượng từ lớn |
| [StarDict archive](https://web.archive.org/web/20231001000000/http://abloz.com/huzheng/stardict-dic/) | Nhiều cặp ngôn ngữ | Bộ sưu tập StarDict cổ điển |
| [FreeDict](https://freedict.org/) | Nhiều cặp ngôn ngữ | Bộ sưu tập từ điển mã nguồn mở |
| [Book Reader Dict](https://github.com/BoboTiG/ebook-reader-dict) | Dựa trên Wiktionary, nhiều ngôn ngữ | Định dạng XML (chuyển đổi sang StarDict) |

> Đối với người dùng Việt Nam, các từ điển được khuyên dùng là:
> - **tudien-en-vi** (EN→VI, 235K từ) — chất lượng tốt nhất
> - **stardict_en_vi** (EN→VI, 387K từ) — số lượng từ lớn hơn
> - **stardict_vi_en** (VI→EN, 42K từ) — tra ngược

### Cách nhập

1. **Tải xuống** một từ điển StarDict. Nó phải chứa 3 tệp có cùng tên cơ sở:
   - `your-dict.ifo` — siêu dữ liệu (bắt buộc)
   - `your-dict.idx` — chỉ mục từ (bắt buộc)
   - `your-dict.dict.dz` — dữ liệu định nghĩa đã nén (bắt buộc)

   > Một số từ điển có dạng `.dict` (không nén). Plugin **không** chấp nhận tệp `.dict` trực tiếp. Nếu từ điển của bạn chỉ có `.dict`, bạn cần chuyển đổi trước (xem phần Khắc phục sự cố bên dưới).

2. **Mở** SiYuan → Reader Book Lite → chọn bất kỳ văn bản nào → nhấp vào nút Từ điển → nhấp vào **bánh răng cài đặt** trong bảng từ điển, hoặc vào **Cài đặt plugin → Reader Book Lite → Từ điển**.

3. Nhấp vào **Thêm từ điển**.

4. Trong trình chọn tệp, **chọn cả 3 tệp cùng lúc** (giữ Ctrl hoặc Shift và nhấp vào từng tệp). Bạn phải chọn đồng thời `.ifo`, `.idx` và `.dict.dz`.

5. Từ điển đã được nhập và sẵn sàng sử dụng ngay lập tức — không cần khởi động lại. Nó sẽ xuất hiện trong thanh tab từ điển khi bạn tra từ tiếp theo.

### Thứ tự từ điển

Các từ điển được truy vấn theo thứ tự xuất hiện trong danh sách. Từ điển đầu tiên trả về kết quả sẽ thắng. Bạn có thể sắp xếp lại chúng bằng cách nhấp vào **Sắp xếp** trong bảng cài đặt từ điển.

### Khắc phục sự cố

| Vấn đề | Nguyên nhân | Khắc phục |
|---------|-------|-----|
| "Không tìm thấy nhóm từ điển hoàn chỉnh" | Bạn không chọn đủ 3 tệp, hoặc tên tệp không khớp | Chọn `.ifo`, `.idx` và `.dict.dz` **cùng lúc** — tất cả phải có cùng tên cơ sở |
| "Subfield ID should be RA" | Tệp `.dict.dz` là gzip thông thường, không phải định dạng DictZip | Sử dụng từ điển có sẵn `.dict.dz` (không phải `.dict`), hoặc chuyển đổi bằng script bên dưới |
| "Không tìm thấy tệp" | Đường dẫn tệp trong cấu hình không đúng | Sử dụng giao diện **Thêm từ điển** để nhập — không đặt tệp thủ công |
| Từ điển không hiển thị khi tra | Từ điển bị tắt hoặc không có kết quả | Kiểm tra từ điển đã được bật (công tắc bật/tắt) và từ đó có tồn tại trong từ điển đó |

### Chuyển đổi .dict sang .dict.dz (Nâng cao)

Nếu từ điển của bạn ở dạng `.dict` (không nén), bạn cần mã hóa nó thành tệp **DictZip** (không phải gzip thông thường). Sử dụng script Node.js này:

```javascript
const fs = require('fs');
const zlib = require('zlib');

function makeDictZip(inputPath, outputPath) {
    const raw = fs.readFileSync(inputPath);
    const CHLEN = 8192;
    const chunks = [];
    for (let offset = 0; offset < raw.length; offset += CHLEN) {
        const chunk = raw.subarray(offset, Math.min(offset + CHLEN, raw.length));
        chunks.push(zlib.deflateRawSync(chunk, { level: 9 }));
    }
    const subfieldDataLen = 6 + 2 * chunks.length;
    const xlen = 4 + subfieldDataLen;
    const extra = Buffer.alloc(xlen);
    let off = 0;
    extra[off++] = 0x52; extra[off++] = 0x41; // "RA"
    extra.writeUInt16LE(subfieldDataLen, off); off += 2;
    extra.writeUInt16LE(1, off); off += 2;     // version
    extra.writeUInt16LE(CHLEN, off); off += 2; // chunk length
    extra.writeUInt16LE(chunks.length, off); off += 2; // chunk count
    for (const c of chunks) extra.writeUInt16LE(c.length, off); off += 2;

    const name = outputPath.split(/[\\/]/).pop().replace(/\.dz$/, '') || 'dict';
    const fname = Buffer.from(name, 'utf-8');
    const header = Buffer.alloc(12 + xlen + fname.length + 1);
    off = 0;
    header[off++] = 0x1F; header[off++] = 0x8B; header[off++] = 0x08;
    header[off++] = 0x0C; // FEXTRA | FNAME
    off += 4; // mtime = 0
    header[off++] = 0; header[off++] = 0; // xfl, os
    header.writeUInt16LE(xlen, off); off += 2;
    extra.copy(header, off); off += extra.length;
    fname.copy(header, off); off += fname.length;
    header[off] = 0;
    fs.writeFileSync(outputPath, Buffer.concat([header, ...chunks]));
}

makeDictZip('input.dict', 'output.dict.dz');
```

Chạy: `node convert.js`

## Ghi công

Plugin gốc: [SiReader](https://github.com/mika-si/siyuan-sireader) bởi mika-si.
