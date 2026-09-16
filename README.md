# Deploy static (chi file build, khong co ma nguon)

1. Repo nay chi chua HTML/JS/CSS da build san.
2. **Vercel**: Framework = Other, khong can build/install (xem `vercel.json`).
3. **Netlify**: publish = `.`, khong build; dung `_redirects` + `netlify.toml`.
4. Test: `/contact/` (tu gen so) va `/vps-health`
5. Link goc `/` se redirect ve TikTok

## Netlify — tai sao /contact bi ve TikTok?

Flow: `/contact/` -> JS redirect `/contact/{token}/` -> can rewrite slug -> `/contact/0/`.
Neu thieu `_redirects`, Netlify tra 404; `404.html` redirect ve TikTok (tu `not-found.tsx`).
