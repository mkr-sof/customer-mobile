## Project Structure
<pre style="white-space: pre-wrap;">
customer-mobile
app/
│
├── _layout.tsx
├── index.tsx
│
├── (auth)/
│   ├── login.tsx
│   └── register.tsx
│
├── (tabs)/
│   ├── _layout.tsx
│   ├── home.tsx
│   ├── orders.tsx
│   ├── favorites.tsx
│   └── profile.tsx
│
├── product/
│   └── [id].tsx
│
├── cart/
│   └── index.tsx
│
└── checkout/
    └── index.tsx

src/
│
├── components/
│   ├── ProductCard.tsx
│   ├── CategoryCard.tsx
│   └── Header.tsx
│
├── hooks/
│   ├── useDebounce.ts
│   └── useLocation.ts
│
├── providers/
│   └── AppProvider.tsx
│
├── store/
│   ├── mmkvStorage.ts        # single MMKV instance + Zustand persist adapter
│   ├── cart.ts
│   └── auth.ts
│
├── api/
│   ├── client.ts             # axios instance + QueryClient instance
│   ├── products.ts           # raw fetch functions
│   ├── orders.ts             # raw fetch functions
│   └── queries/
│       ├── useProducts.ts    # useQuery wrappers, query keys live here
│       └── useOrders.ts
│
├── types/
│   ├── product.ts
│   ├── order.ts
│   ├── user.ts
│   ├── cart.ts
│   └── address.ts            # leaf node, no deps on other type files
│
└── theme/
    └── colors.ts
 </pre>
