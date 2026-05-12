# iPhone 3D Model

## Setup

1. Tempat file model `.obj` di folder ini: `model.obj`
2. Pastikan nama file tepat: **`model.obj`** (case-sensitive)
3. Jangan gunakan `.mtl` (material file) - OBJ akan dimuat tanpa materials

## Konfigurasi Positioning & Scaling

Edit file `src/content/products/appleIphone.ts` untuk mengubah:

```typescript
arModel: {
  url: '/assets/models/apple-iphone/model.obj',
  scale: [1, 1, 1],           // Ubah untuk resize: [0.5, 0.5, 0.5] = 50% lebih kecil
  position: [0, 0, 0],        // [x, y, z] untuk geser posisi
  rotation: [0, 0, 0],        // [x, y, z] untuk rotate (dalam radians)
},
```

### Contoh pengubahan:

```typescript
// Resize model 50% lebih kecil:
scale: [0.5, 0.5, 0.5],

// Geser ke atas:
position: [0, 0.5, 0],

// Rotate 90 derajat ke Y axis (dalam radians, π/2 ≈ 1.57):
rotation: [0, 1.57, 0],
```

## Notes

- Format: **.obj** (tanpa .mtl)
- Ukuran file: Sebaiknya < 5MB
- Koordinat sistem: Three.js standard (Y-up)
- Skala: Eksperimental, mulai dari `[1, 1, 1]` dan sesuaikan
