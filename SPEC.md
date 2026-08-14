# SPEC.md - Website Quảng Bá Thủ Công Mỹ Nghệ - Văn Hoá Việt Nam
## Vietnamese Metro UI + Windows Phone 8 Style

---

## 1. Concept & Vision

**Định hướng:** Kết hợp giữa màu sắc đặc trưng Việt Nam (đỏ son, vàng kim, đen Metro) với giao diện Windows Phone 8 Metro UI. Website mang phong cách hiện đại nhưng vẫn giữ được bản sắc văn hóa Việt Nam qua màu sắc và hình ảnh.

**Cảm hứng:** Windows Phone 8 Metro UI, Windows Store, đồng thời mang đậm dấu ấn Việt Nam qua bảng màu đỏ son và vàng kim truyền thống.

---

## 2. Color Palette - Vietnamese Signature

### Primary Colors
```
Đỏ Son (Vietnam Red):    #B8383B - Màu chủ đạo như sơn mài truyền thống
Đỏ Son Đậm:             #9A2F32 - Biến thể đậm
Đỏ Son Nhạt:             #D45658 - Biến thể nhạt

Vàng Kim (Gold):          #C9A962 - Hoa văn cao cấp
Vàng Kim Nhạt:            #E5D4A1 - Biến thể nhạt
Vàng Kim Đậm:             #A68B4B - Biến thể đậm
```

### Metro Dark (Background)
```
Metro Dark:               #1A1A1A - Nền tảng hiện đại
Metro Surface:            #252525 - Surface dark
Metro Surface Light:      #2F2F2F
Metro Border:             #3A3A3A
```

### Text Colors
```
Primary:                  #FFFFFF
Secondary:               #B0B0B0
Muted:                   #707070
```

---

## 3. Typography

```
Font Family:             'Segoe UI', 'Noto Sans', system-ui, sans-serif

Weights:
- Light:                 200
- Semi-light:            300
- Regular:               400
- Semi-bold:             600
- Bold:                  700

Type Scale:
- Hero:                  72px / Light / tracking: -2px
- H1:                    42px / Light / tracking: -1px
- H2:                    32px / Light
- H3:                    28px / Semi-light
- Body Large:            20px / Regular
- Body:                  17px / Regular
- Caption:               14px / Regular
- Small:                 13px / Semi-light
```

---

## 4. Layout Structure

### 4.1 Navigation Flow
```
┌─────────────────────────────────────────────────────────────┐
│  HEADER - Fixed, gradient border bottom (đỏ son)           │
├─────────────────────────────────────────────────────────────┤
│  HERO - Full viewport, parallax background                  │
│  - Badge với viền vàng kim                                  │
│  - Gradient title (đỏ son → vàng kim)                      │
├─────────────────────────────────────────────────────────────┤
│  PIVOT NAVIGATION - Sticky, gradient underline             │
├─────────────────────────────────────────────────────────────┤
│  SECTIONS:                                                 │
│  - Products (4-column grid)                                │
│  - Custom Order (Windows Store style)                       │
│  - Artisans (People Hub style)                             │
│  - CTA                                                     │
├─────────────────────────────────────────────────────────────┤
│  BOTTOM APP BAR - Fixed, đỏ son border top                 │
└─────────────────────────────────────────────────────────────┘
```

### 4.2 Responsive Breakpoints
```
Desktop:     > 1024px  - Full layout
Tablet:      768-1024px - 2-column grids
Mobile:      < 768px   - Single column, mobile menu
```

---

## 5. Components

### 5.1 Products Grid (4 columns)
- Card với hover scale + shadow
- Image với zoom effect
- Badge overlay (Best seller, New, Limited)
- Price display
- Artisan name
- Buy button

### 5.2 Custom Order Section (Windows Store Style)
```
┌─────────────────────────────────────────────────────────────┐
│  APP HERO                                                  │
│  ┌──────────┐  Category: Design Service                     │
│  │  Image   │  Title: Đặt Tranh Theo Yêu Cầu              │
│  │          │  Rating: ★★★★☆ (4.8/5)                        │
│  │          │  Price Badge: Từ 1.500.000 VNĐ              │
│  └──────────┘  [Install Button]                             │
├─────────────────────────────────────────────────────────────┤
│  SCREENSHOTS (4-column grid)                               │
├─────────────────────────────────────────────────────────────┤
│  DESCRIPTION                                               │
│  - Service description text                                 │
│  - Features (2x2 grid):                                   │
│    • Custom Design                                         │
│    • Professional Artisans                                 │
│    • Flexible Timeline                                     │
│    • Quality Warranty                                      │
├─────────────────────────────────────────────────────────────┤
│  OPTIONS (3-column grid)                                   │
│  - Oil Painting: Từ 2.5M                                   │
│  - Lacquer Painting: Từ 4.0M                              │
│  - Ceramic: Từ 1.5M                                       │
├─────────────────────────────────────────────────────────────┤
│  ORDER FORM                                                │
│  - Name, Phone, Email (2-column row)                       │
│  - Product Type, Size (2-column row)                       │
│  - Description textarea                                    │
│  - [Submit Button]                                         │
└─────────────────────────────────────────────────────────────┘
```

### 5.3 Artisans (People Hub Style)
```
┌─────────────────────────────────────────────────────────────┐
│  HUB HEADER                                                │
│  [Icon] Nghệ Nhân (8 người đang hoạt động)   [+][Filter]  │
├─────────────────────────────────────────────────────────────┤
│  SEARCH BAR                                                │
├─────────────────────────────────────────────────────────────┤
│  FEATURED ARTISAN CARD                                     │
│  ┌─────┐  Nguyễn Văn Minh                                  │
│  │     │  🎨 Tranh Đông Hồ                                 │
│  │Avatar│  Nghệ nhân ưu tú...                              │
│  └─────┘  156 tác phẩm | 30+ năm                          │
│           [Liên hệ] [Hồ sơ]                               │
├─────────────────────────────────────────────────────────────┤
│  Nghệ nhân nổi bật                                        │
│  ┌─────┐ Trần Thị Lan  🎨 Nghệ nhân Lụa...   [💬][ℹ️]  │
│  │     │ 📍 Vạn Phúc, Hà Nội                             │
│  └─────┘                                                   │
│  ┌─────┐ Lê Hồng Sơn  ☕ Nghệ nhân Gốm...   [💬][ℹ️]    │
│  └─────┘                                                   │
│  ┌─────┐ Phạm Thị Hương  👑 Nghệ nhân...   [💬][ℹ️]     │
│  └─────┘                                                   │
└─────────────────────────────────────────────────────────────┘
```

### 5.4 App Bar (Bottom Navigation)
- 4 items với icon + label
- Active indicator (đỏ son dot)
- Fixed position

---

## 6. Animations

### 6.1 Bouncy Tile Effect
```css
@keyframes tile-bounce {
    0% { transform: scale(1); }
    20% { transform: scale(0.92); }
    50% { transform: scale(1.06); }
    75% { transform: scale(0.98); }
    100% { transform: scale(1); }
}
```

### 6.2 Live Pulse
```css
@keyframes live-pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.7; }
}
```

### 6.3 Red Glow (Featured)
```css
@keyframes red-glow {
    0%, 100% { box-shadow: 0 0 20px rgba(184, 56, 59, 0.3); }
    50% { box-shadow: 0 0 40px rgba(184, 56, 59, 0.5); }
}
```

### 6.4 Fade Slide Up (Scroll reveal)
```css
@keyframes fade-slide-up {
    from { opacity: 0; transform: translateY(40px); }
    to { opacity: 1; transform: translateY(0); }
}
```

---

## 7. Features

### 7.1 Language Toggle (VI/EN)
- Dual language support
- All text content duplicated with `data-lang-vi` and `data-lang-en`
- Placeholder text also translated

### 7.2 Product Cards
- Hover: scale(1.02) + shadow
- Click: bouncy animation
- Image zoom on hover
- Price badge overlay
- Artisan attribution

### 7.3 Windows Store Style Order Form
- Hero image với red glow animation
- Rating display
- Screenshot gallery
- Feature highlights
- Option selection (radio-style)
- Form validation
- Submit feedback

### 7.4 People Hub Search
- Live filter by name and craft
- Group header visibility toggle

### 7.5 Pivot Navigation
- Scroll spy active state
- Gradient underline animation

---

## 8. Accessibility

- Semantic HTML structure
- ARIA labels for interactive elements
- Focus states
- Reduced motion support
- Color contrast compliance

---

## 9. Technical Notes

### Icons
- Phosphor Icons (CDN)
- Consistent icon weight (regular)

### Fonts
- Google Fonts: Noto Sans (weights: 200, 300, 400, 500, 600, 700)

### Images
- Unsplash for demo images
- Lazy loading for performance
- Object-fit cover for consistency

---

*Document Version: 3.0 - Vietnamese Metro UI*
*Last Updated: August 2026*
