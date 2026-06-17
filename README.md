# Awesome QR Codes [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of QR code resources, libraries, tools, and best practices.

QR codes are ISO-standardized two-dimensional barcodes capable of encoding URLs, contact data, WiFi credentials, and arbitrary binary data. This list covers open-source libraries, online generators, scanning tools, design guidance, the underlying standard, and security considerations.

## Contents

- [QR Code Generators](#qr-code-generators)
- [JavaScript Libraries](#javascript-libraries)
- [Python Libraries](#python-libraries)
- [Other Languages](#other-languages)
- [QR Code Readers and Scanners](#qr-code-readers-and-scanners)
- [Design and Customization](#design-and-customization)
- [Standards and Specifications](#standards-and-specifications)
- [QR Code Types](#qr-code-types)
- [Use Cases and Best Practices](#use-cases-and-best-practices)
- [Statistics and Market Data](#statistics-and-market-data)
- [Articles and Guides](#articles-and-guides)
- [Security](#security)
- [Contributing](#contributing)
- [License](#license)

---

## QR Code Generators

Web-based tools for generating QR codes without writing code. Most offer both static and dynamic codes; dynamic codes require a paid account and route scans through a redirect URL that can be updated after printing.

- [QR Code Monkey](https://www.qrcode-monkey.com/) - Free generator with high-resolution PNG/SVG output, custom colors, and logo embedding.
- [QR Tiger](https://www.qrcode-tiger.com/) - Dynamic QR codes with detailed scan analytics, bulk generation, and extensive design templates.
- [Flowcode](https://www.flowcode.com/) - Generator focused on branded, custom-shape codes with real-time conversion analytics.
- [Bitly](https://bitly.com/pages/products/qr-codes) - QR codes built on top of Bitly short links; integrates with Bitly's existing link management and analytics dashboard.
- [QR Nova](https://qrcodenova.com/) - Free QR code generator with permanent redirects and scan analytics. Codes never expire.
- [ME-QR](https://me-qr.com/) - Free generator supporting dynamic codes, Google Analytics integration, and a digital menu builder.
- [Scanova](https://scanova.io/) - Business-oriented platform with 16+ QR code types, white-label options, and API access.
- [GoQR.me](https://goqr.me/) - Simple generator and REST API (`api.qrserver.com`) for programmatic PNG/SVG/EPS generation; no account required.
- [Mini-Tools.uk QR Generator](https://mini-tools.uk/qr) - Self-recommending a browser QR code generator for URL, Wi-Fi, email and vCard/contact QR codes, with error correction options and PNG download.

---

## JavaScript Libraries

### Generation

- [node-qrcode](https://github.com/soldair/node-qrcode) - Widely used Node.js and browser library; outputs to canvas, SVG, and terminal.
- [qr-code-styling](https://github.com/kozakdenys/qr-code-styling) - Generates styled QR codes with custom dot shapes, gradients, and embedded images.
- [qrcodejs](https://github.com/davidshimjs/qrcodejs) - Dependency-free browser library using HTML5 Canvas or a DOM table fallback.
- [qrious](https://github.com/neocotic/qrious) - Pure JavaScript QR code generation via HTML5 Canvas.
- [react-qr-code](https://github.com/rosskhanas/react-qr-code) - SVG-based React and React Native component; encodes in UTF-8 byte mode.
- [angularx-qrcode](https://github.com/Cordobo/angularx-qrcode) - Angular standalone component (Angular 4-21) with Ivy support, based on node-qrcode.
- [vue-qrcode](https://github.com/fengyuanchen/vue-qrcode) - Vue 3 component wrapping node-qrcode.
- [nayuki/QR-Code-generator](https://github.com/nayuki/QR-Code-generator) - Correctness-focused implementation available in JavaScript, Java, Python, Rust, C++, and C.

### Reading

- [jsQR](https://github.com/cozmo/jsQR) - Pure JavaScript QR decoder that operates on raw image data; works in browser and Node.js.

---

## Python Libraries

- [qrcode](https://github.com/lincolnloop/python-qrcode) - The standard `pip install qrcode` library; outputs PNG, SVG, and terminal art. Depends on Pillow for raster images.
- [segno](https://github.com/heuer/segno) - Pure Python encoder with no dependencies; produces QR and Micro QR codes in SVG, EPS, PNG, PDF, PAM, and LaTeX formats. Implements ISO/IEC 18004:2015.
- [amazing-qr](https://github.com/x-hw/amazing-qr) - Generates standard, artistic (image-blended), and animated GIF QR codes.
- [MyQR](https://github.com/sylnsfar/qrcode) - Artistic QR code generator supporting colorized and animated GIF output.

---

## Other Languages

### Go

- [skip2/go-qrcode](https://github.com/skip2/go-qrcode) - Pure Go encoder implementing QR Code 2005 (ISO/IEC 18004:2006); supports all four error correction levels and PNG output.

### Rust

- [qrcode-rust](https://github.com/kennytm/qrcode-rust) - QR and Micro QR code encoder for Rust; renders to PNG, SVG, Unicode, and EPS via the `image` crate.

### Java

- [ZXing](https://github.com/zxing/zxing) - "Zebra Crossing" -- the canonical multi-format 1D/2D barcode library for Java and Android. Supports reading and writing QR codes.
- [QRGen](https://github.com/kenglxn/QRGen) - Fluent Java API built on top of ZXing, simplifying QR code generation with a builder pattern.

### Swift

- [EFQRCode](https://github.com/EFPrefix/EFQRCode) - iOS, macOS, watchOS, tvOS, and visionOS library for generating stylized QR codes with watermarks. Built on CoreGraphics and CoreImage.

### PHP

- [endroid/qr-code](https://github.com/endroid/qr-code) - Feature-rich PHP library with a builder API; outputs PNG, WebP, SVG, EPS, and binary.
- [chillerlan/php-qrcode](https://github.com/chillerlan/php-qrcode) - PHP 8.2+ generator and reader with GD, ImageMagick, and SVG output; includes a ZXing-based decoder.

### Ruby

- [rqrcode](https://github.com/whomwah/rqrcode) - Ruby library for encoding QR codes; renders to SVG, PNG, and ANSI terminal output.

### C#

- [QRCoder](https://github.com/codebude/QRCoder) - Pure C# implementation with no external dependencies; supports standard and Micro QR codes.

---

## QR Code Readers and Scanners

- [ZXing](https://github.com/zxing/zxing) - The reference Java/Android barcode scanning library; handles QR, DataMatrix, Aztec, PDF417, and many 1D formats.
- [jsQR](https://github.com/cozmo/jsQR) - Client-side JavaScript decoder; locates and decodes QR codes from pixel arrays or video frames.
- [zbar](https://github.com/mchehab/zbar) - C library and command-line tool for reading barcodes from images and video streams; supports QR codes among many symbologies.
- [quirc](https://github.com/dlbeer/quirc) - Small, embeddable C decoder with no dependencies beyond libc; processes a VGA frame in approximately 50 ms on a modern x86 core.
- [html5-qrcode](https://github.com/mebjas/html5-qrcode) - Cross-platform browser library for continuous webcam scanning and single-image decoding; wraps ZXing-js and other engines.

---

## Design and Customization

### Principles

A QR code will scan reliably only when its structural and visual constraints are respected. The following guidelines apply regardless of what tool or library generated the code.

**Minimum size.** The practical minimum for close-range scanning (arm's length) is 2 cm x 2 cm. A rough rule: the scanning distance should not exceed 10x the code's physical width. For a billboard readable at 3 m, the code should be at least 30 cm wide.

**Quiet zone.** Every QR code requires a border of blank space equal to four module widths on all four sides. Without it, most decoders fail to locate the finder patterns.

**Color contrast.** The dark modules must contrast strongly against the light background. Dark-on-light is more reliable than light-on-dark because most cameras are tuned for the former. Avoid low-contrast combinations like dark blue on black.

**Error correction level.** Four levels are defined in the standard:

| Level | Data recovery | Common use |
|-------|--------------|------------|
| L | ~7% | Clean digital displays |
| M | ~15% | General print use |
| Q | ~25% | Print with potential wear |
| H | ~30% | Logo/image overlay, outdoor signage |

Use level Q or H whenever you embed a logo. A logo that covers more than roughly 30% of the code area will cause decode failures even at level H.

**Logo placement.** Center the logo over the timing and alignment patterns, not over the three finder patterns in the corners. Keep it proportional and ensure the underlying module grid remains parseable.

**Testing.** Print at the final intended size before committing to production. Test with at minimum three different scanning apps and two operating systems. Scan from multiple angles and under varied lighting.

### Reference

- [Nielsen Norman Group -- 13 QR-Code Usability Guidelines](https://www.nngroup.com/articles/qr-code-guidelines/) - Research-backed UX guidelines on contextual labeling, mobile destination requirements, and placement.
- [QR code - Wikipedia](https://en.wikipedia.org/wiki/QR_code) - Comprehensive reference on history, symbol structure, encoding modes, and version/size tables.

---

## Standards and Specifications

### ISO/IEC 18004

QR code is defined by ISO/IEC 18004. The current edition is the fourth (2024); the previous widely implemented edition is 2015.

- [ISO/IEC 18004:2024](https://www.iso.org/standard/83389.html) - Current normative specification covering symbol structure, encoding, error correction, and production quality requirements.
- [ANSI Blog -- ISO/IEC 18004:2024 overview](https://blog.ansi.org/ansi/iso-iec-18004-2024-qr-code-bar-code-symbology/) - Plain-language summary of what changed in the 2024 revision.

### Error Correction

QR codes use Reed-Solomon error correction. The four levels (L, M, Q, H) represent the proportion of codewords that can be restored if damaged. Increasing the level increases the physical size of a code encoding the same data.

### Encoding Modes

The standard defines four primary encoding modes; the encoder should automatically select the most compact mode for the given data:

- **Numeric** -- digits 0-9 only; most compact (up to 7,089 characters at version 40-L).
- **Alphanumeric** -- digits, uppercase letters, and nine special characters (`$`, `%`, `*`, `+`, `-`, `.`, `/`, `:`, space).
- **Byte** -- arbitrary 8-bit data, typically UTF-8 text.
- **Kanji** -- double-byte Shift JIS encoding for Japanese characters.

### Versions and Capacity

Symbol sizes run from version 1 (21x21 modules) to version 40 (177x177 modules). Maximum data capacity at version 40-L is 7,089 numeric digits, 4,296 alphanumeric characters, or 2,953 bytes.

---

## QR Code Types

### Static vs. Dynamic

A **static** QR code encodes data directly in the module pattern. The destination cannot be changed after printing; replacing it requires generating and printing a new code.

A **dynamic** QR code encodes a short redirect URL. The destination can be changed at any time in the generator platform without reprinting. Dynamic codes also enable scan analytics (count, location, device type) and are typically provided through paid SaaS platforms.

### Common Data Types

| Type | Encoded payload example |
|------|------------------------|
| URL | `https://example.com/page` |
| WiFi | `WIFI:T:WPA;S:NetworkName;P:password;;` |
| vCard (contact) | `BEGIN:VCARD...END:VCARD` |
| Email | `mailto:user@example.com?subject=Hello` |
| SMS | `SMSTO:+15551234567:Message text` |
| Phone | `tel:+15551234567` |
| Calendar event | `BEGIN:VEVENT...END:VEVENT` |
| Geo location | `geo:37.7749,-122.4194` |
| Bitcoin / crypto | `bitcoin:1A1zP1eP5QGefi2DMPTfTL5SLmv7Divf` |

---

## Use Cases and Best Practices

### Restaurant Menus

QR codes replaced paper menus at scale during 2020-2021. Place the code prominently on each table; link to a mobile-optimized menu page rather than a PDF. Use a dynamic code so the menu can be updated without reprinting. Include a brief label ("Scan for menu") -- QR codes have no inherent information scent and users are more likely to scan when told what to expect.

### Product Packaging

Encode a URL to product details, usage instructions, or a registration page. Use level H error correction to account for surface wear. Test on a curved or textured surface before mass production. Minimum recommended size for packaging is 1 cm x 1 cm at close range, though larger is always safer.

### Business Cards

A vCard QR code lets recipients save contact information directly to their phone. Keep the encoded data minimal (name, phone, email, website) to reduce module density. Size at no smaller than 1.5 cm x 1.5 cm. Use error correction level M or Q to handle card wear.

### Event Management

Dynamic QR codes on tickets can be invalidated after a single scan, making them suitable for access control. For large venues, print codes at a minimum of 3 cm x 3 cm to ensure reliable scanning at speed.

### Print Marketing

Place the QR code where it will be noticed and where scanning is physically convenient -- a flyer held at arm's length, for example. Always test the printed output; screen renders and print output can differ in resolution and contrast. Include a brief call to action near the code.

### Real Estate

Link to a property listing, virtual tour, or contact form. Since signs are scanned from distances of 1-3 m, codes should be printed at 10-25 cm. Use a dynamic code so the listing URL can be updated as properties change.

---

## Statistics and Market Data

- [Mordor Intelligence -- QR Codes Market](https://www.mordorintelligence.com/industry-reports/qr-codes-market) - Industry report on global QR code market size, segmentation, and growth forecasts through 2031.
- [Scanova -- QR Code Statistics](https://scanova.io/blog/qr-code-statistics/) - Regularly updated compilation of global usage, scan volumes, and demographic data, with source citations.
- [Barkoder -- QR Code Statistics 2025](https://barkoder.com/blog/30-shocking-qr-code-statistics-you-need-to-know-in-2025) - Aggregated statistics on adoption, scan behavior, and industry verticals.

---

## Articles and Guides

- [Nielsen Norman Group -- 13 QR-Code Usability Guidelines](https://www.nngroup.com/articles/qr-code-guidelines/) - Evidence-based UX research on labeling, destination relevance, and mobile optimization requirements.
- [Cloud Security Alliance -- The Rise of QR Code Phishing Attacks](https://cloudsecurityalliance.org/blog/2024/07/01/the-rise-of-qr-code-phishing-attacks-exploring-quishing-threats) - Technical overview of quishing attack vectors and organizational defenses.
- [Palo Alto Networks Unit 42 -- Evolution of QR Codes in Phishing](https://unit42.paloaltonetworks.com/qr-code-phishing/) - Threat research with attack taxonomy and detection techniques.
- [Real Python -- Generate Beautiful QR Codes With Python](https://realpython.com/python-generate-qr-code/) - Practical tutorial covering the `segno` library with worked examples for vCard, WiFi, and URL codes.
- [TechCrunch -- Beaconstac lands $25M for its QR code management platform](https://techcrunch.com/2023/01/17/beaconstac-lands-25m-investment-for-its-qr-code-management-platform/) - Industry context on the commercial QR code management landscape.
- [TechCrunch -- Bitly makes first acquisition with QR code leader Egoditor](https://techcrunch.com/2021/12/01/bitly-makes-first-acquisition-with-qr-code-leader-egoditor/) - Background on consolidation in the QR SaaS space.
- [Wikipedia -- QR code](https://en.wikipedia.org/wiki/QR_code) - Comprehensive reference covering history (Denso Wave, 1994), technical structure, and global adoption.

---

## Security

### Quishing (QR Code Phishing)

Quishing is a phishing technique that uses a malicious QR code in place of a traditional link. Because the encoded URL is not visible to the recipient before scanning, and because most enterprise email security tools analyze text and hyperlinks rather than images, quishing emails frequently bypass conventional filters.

Common attack patterns include:
- Fake multi-factor authentication prompts delivered by email or physical mail.
- Malicious QR stickers placed over legitimate codes on point-of-sale terminals, parking meters, and restaurant tables.
- QR codes in PDF attachments that route to credential harvesting pages.

### How to Verify a QR Code Before Scanning

1. **Use a scanner that previews the URL.** Modern iOS (via the Camera app) and Android (via Google Lens) display the destination URL before opening it. Third-party apps vary; prefer those that show the decoded URL prominently.
2. **Inspect physical codes for tampering.** A sticker placed over a printed code is a common attack vector. Look for misaligned or raised edges around the code.
3. **Check the domain carefully.** After the URL is displayed, verify the domain matches the expected organization before proceeding.
4. **Do not scan unsolicited codes.** An unexpected email or package containing only a QR code and urgency language is a reliable indicator of a phishing attempt.

### For Organizations

- Include QR code awareness in security training programs alongside standard phishing simulation exercises.
- Configure email security tools to decode and inspect URLs embedded in QR codes within images.
- Where possible, use dynamic QR codes from a managed platform so that malicious redirects can be identified and disabled quickly.

### Further Reading

- [Hoxhunt -- QR Code Phishing (Quishing) Explained](https://hoxhunt.com/blog/quishing) - Employee-facing explainer suitable for security awareness programs.
- [Keepnet -- QR Phishing Statistics and Trends](https://keepnetlabs.com/blog/qr-code-phishing-trends-in-depth-analysis-of-rising-quishing-statistics) - Data on quishing volume and attack patterns through 2026.
- [TechTarget -- Quishing Prevention Tips](https://www.techtarget.com/searchsecurity/feature/Quishing-on-the-rise-How-to-prevent-QR-code-phishing) - Fourteen concrete prevention measures for individuals and IT teams.

---

## Contributing

Contributions are welcome. Please read the [contribution guidelines](CONTRIBUTING.md) first.

To add an entry:
- The project or resource must be actively maintained or remain the canonical reference in its category.
- Descriptions should be one sentence, factual, and free of marketing language.
- Open a pull request with your addition in the appropriate section, following the existing format.

To report a broken link or outdated entry, open an issue.

---

## License

[![CC0](https://mirrors.creativecommons.org/presskit/buttons/88x31/svg/cc-zero.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

To the extent possible under law, the contributors have waived all copyright and related rights to this work.

---

Maintained by [QR Nova](https://qrcodenova.com)
