# Ham Radio Exam - Εξετάσεις Ραδιοερασιτεχνών 📻

Σύγχρονη desktop εφαρμογή για προετοιμασία στις εξετάσεις ραδιοερασιτεχνών.

## Χαρακτηριστικά

### 🎯 Κατηγορίες Εξετάσεων
- **Εισαγωγικό Επίπεδο (Entry Level)** - 344 ερωτήσεις, 100 στο τεστ
- **Κατηγορία 1 (CEPT / HAREC)** - 726 ερωτήσεις, 100 στο τεστ
- **Εισαγωγικό με Απαλλαγή Κεφ. Α'** - 230 ερωτήσεις, 80 στο τεστ
- **Κατηγορία 1 με Απαλλαγή Κεφ. Α'** - 181 ερωτήσεις, 50 στο τεστ

### 📝 Λειτουργίες
- **Πλήρες Τεστ**: Προσομοίωση πραγματικής εξέτασης
- **Προσαρμοσμένο Τεστ**: Επιλογή συγκεκριμένων ενοτήτων και πλήθους ερωτήσεων
- **Προσωποποιημένο Τεστ**: Εξάσκηση με βάση λάθη, δύσκολες ερωτήσεις ή επανεξέταση
- **Χρονόμετρο**: Αντίστροφη μέτρηση με προειδοποιήσεις
- **Αναλυτικά αποτελέσματα & στατιστικά**: Δείτε λάθη, πρόοδο και επιδόσεις ανά ενότητα

### ⌨️ Συντομεύσεις Πληκτρολογίου
- `←` / `→` ή `P` / `N`: Προηγούμενη / Επόμενη ερώτηση
- `1-4` ή `A-D`: Επιλογή υπαρκτής απάντησης στην τρέχουσα ερώτηση

## Εγκατάσταση

### Προαπαιτούμενα
- [Node.js](https://nodejs.org/) (v18+)
- [Rust](https://rustup.rs/)
- [Tauri CLI](https://tauri.app/start/prerequisites/)

### Βήματα

```bash
# 1. Clone ή extract το project
cd ham-radio-exam-app

# 2. Εγκατάσταση dependencies
npm install

# 3. Development mode
npm run tauri dev

# 4. Build για production
npm run tauri build
```

## Δεδομένα ερωτήσεων

Τα JSON αρχεία στο `src/data/` γίνονται encrypted Rust bundle στο `src-tauri/src/data_blob.rs`.
Το Tauri `dev` και `build` τρέχουν αυτόματα `npm run bundle-data` πριν από το frontend command, ώστε το desktop app να μη χτίζεται με παλιό bundle.

Για χειροκίνητη αναγέννηση μετά από αλλαγές στα JSON δεδομένα:

```bash
npm run bundle-data
```

## Δομή Project

```
ham-radio-exam-app/
├── src/
│   ├── components/       # React components
│   │   ├── Header.tsx
│   │   ├── CategorySelect.tsx
│   │   ├── ExamModeSelect.tsx
│   │   ├── Quiz.tsx
│   │   ├── Results.tsx
│   │   └── Statistics.tsx
│   ├── data/            # JSON δεδομένα ερωτήσεων
│   │   ├── Entry_Level/
│   │   ├── CEPT/
│   │   ├── Entry_Apallages/
│   │   └── CEPT_Apallages/
│   ├── hooks/           # React hooks
│   ├── utils/           # Utilities και Tauri data bridge
│   ├── types/           # TypeScript types
│   └── styles/          # CSS
├── public/
│   └── images/          # Εικόνες ερωτήσεων (RADIO*.jpg)
├── scripts/             # Data bundle scripts
├── src-tauri/           # Tauri/Rust backend
└── package.json
```

## Τεχνολογίες

- **Frontend**: React 19 + TypeScript + Tailwind CSS
- **Desktop**: Tauri 2 (Rust)
- **Icons**: Lucide React

## Άδεια

MIT License

## Συγγραφέας

Heraklis - Evohia Event Catering & Private Chef Services
