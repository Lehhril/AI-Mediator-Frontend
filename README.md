Folder Structure

/ai-mediation-frontend
├── public/                         # Static files (images, favicon, robots.txt, etc.)
├── src/
│   ├── app/                        # Next.js app router (routes + layouts)
│   │   ├── layout.tsx              # Root layout (applies globally)
│   │   ├── page.tsx                # Root landing page ("/")
│   │   ├── loading.tsx             # Global loading UI
│   │   ├── error.tsx               # Global error UI
│   │
│   │   ├── auth/                   # Auth feature routes
│   │   │   ├── layout.tsx          # Optional auth layout (e.g. centered form)
│   │   │   ├── login/
│   │   │   │   └── page.tsx        # /auth/login
│   │   │   ├── signup/
│   │   │   │   └── page.tsx        # /auth/signup
│   │   │   └── forgot-password/
│   │   │       └── page.tsx        # /auth/forgot-password
│   │
│   │   ├── mediation/              # Mediation feature routes
│   │   │   ├── layout.tsx          # Mediation-specific layout (sidebar, etc.)
│   │   │   ├── page.tsx            # /mediation (list disputes)
│   │   │   ├── create/
│   │   │   │   └── page.tsx        # /mediation/create (create new dispute)
│   │   │   ├── [disputeId]/        # Dynamic dispute details
│   │   │   │   ├── layout.tsx      # Optional layout for dispute details
│   │   │   │   └── page.tsx        # /mediation/:disputeId
│   │   │   └── history/
│   │   │       └── page.tsx        # /mediation/history
│   │
│   │   ├── dashboard/              # User dashboard routes
│   │   │   ├── layout.tsx          # Dashboard layout (e.g. nav, sidebar)
│   │   │   ├── page.tsx            # /dashboard
│   │   │   ├── settings/
│   │   │   │   └── page.tsx        # /dashboard/settings
│   │   │   └── notifications/
│   │   │       └── page.tsx        # /dashboard/notifications
│   │
│   │   └── (common)/               # Group route for shared UI (modals, toasts)
│   │       ├── modal.tsx
│   │       ├── toast.tsx
│   │       └── loading.tsx
│   │
│   ├── components/                 # Shared UI components across features
│   │   ├── Button.tsx
│   │   ├── Input.tsx
│   │   ├── Modal.tsx
│   │   └── ...
│   │
│   ├── features/                   # Feature-specific logic, UI, hooks, API calls
│   │   ├── auth/
│   │   │   ├── components/         # LoginForm, SignupForm, etc.
│   │   │   ├── hooks/              # useAuth, useLogin, etc.
│   │   │   ├── api.ts              # API calls related to auth
│   │   │   └── authLogic.ts        # Business logic, validation, helpers
│   │   │
│   │   ├── mediation/
│   │   │   ├── components/         # DisputeList, DisputeForm, MediationDetails
│   │   │   ├── hooks/              # useDisputes, useCreateDispute, etc.
│   │   │   ├── api.ts
│   │   │   └── mediationLogic.ts
│   │   │
│   │   └── dashboard/
│   │       ├── components/         # Dashboard widgets, notifications list
│   │       ├── hooks/              # useDashboardData, etc.
│   │       ├── api.ts
│   │       └── dashboardLogic.ts
│   │
│   ├── hooks/                      # Global reusable hooks (useFetch, useDebounce)
│   ├── lib/                        # Utils, API clients, 3rd party integrations
│   ├── styles/                     # Global CSS, Tailwind config, etc.
│   └── types/                      # TypeScript types/interfaces
│
├── .env.local                     # Environment variables
├── next.config.js
├── package.json
├── tsconfig.json
└── README.md
