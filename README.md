# EcoSphere— Circular Economy Marketplace

> **“Keep products in use. Keep resources in motion.”**
> AI Zero-Waste Infrastructure • Multimodal Vision Diagnostics • Right-to-Repair Network • Live Scrap Index

---

## 🌟 Overview & Problem Statement

Linear "take-make-waste" industrial systems generate over **54 million metric tonnes of discarded consumer goods and e-waste** each year. Millions of functional laptops, smartphones, furniture pieces, and industrial materials end up in municipal landfills simply because consumers and enterprises lack:
1. **Instant, transparent diagnostics** on item condition, repairability, and realistic resale value.
2. **Frictionless circular pathways** connecting items to certified local repairers, barter partners, and verified recyclers.
3. **Quantifiable environmental impact tracking** (CO₂ avoided, kilograms diverted, and materials recovered).

**CIRVANA** solves this by unifying **Multimodal Vision AI**, a **Verified Peer-to-Peer Marketplace**, a **Right-to-Repair Network**, and a **Live Commodity Scrap Index** (priced in ₹/kg) into a cohesive circular operating system.

---

## 🚀 Key User Flow

1. **Home Screen**:
   - Inspect the product lifecycle and live ecosystem metrics (Tons waste avoided, products reused, items repaired).
   - Click **"Explore Marketplace"** or **"Scan an Item"**.

2. **AI Multimodal Vision Evaluator**:
   - Upload any product photo or select quick sample presets (**Used Laptop, Refurbished Smartphone, Second-hand Office Chair, Used Engineering Books, E-Waste PCB, Recycled HDPE Plastic, Scrap Aluminium**).
   - Click **"Run AI Circular Analysis"**.
   - Vision AI analyzes the item's condition, calculates resale/repair estimates in ₹, determines recyclability %, computes a **0–100 Circularity Score**, and recommends a 5R pathway (**REUSE, REPAIR, RESELL, DONATE, or RECYCLE**).

3. **1-Click Circular Conversion**:
   - Click **"List Marketplace"** to instantly pre-fill and publish a verified listing.
   - Click **"Find Repair Hub"** to book diagnostics with certified local technicians.
   - Click **"Recycle Network"** to dispatch doorstep material collection at live market scrap rates.

4. **Marketplace & Detail View**:
   - Browse listings by category, condition, price range, and circularity score.
   - Inspect product details with embodied carbon savings, repair history, and escrow checkout.

5. **Impact Dashboard**:
   - Track metrics: **Landfill Waste Diverted (kg)**, **CO₂ Avoided (kg)**, **Listed Items**, **Purchased Items**, **Reused Items**, **Repaired Items**, **Donated Items**, **Recycled Material Batches**, and **Circular Impact Score (Pts)**.

---

## 🛠️ Tech Stack & Architecture

- **Frontend**: React 19, TypeScript, Tailwind CSS v4, Lucide Icons, Canvas Confetti
- **Backend API**: Express.js server running in Node.js (with TSX in development and bundled with esbuild for production)
- **AI Engine**: `@google/genai` (Gemini 2.5 Flash / Gemini 2.0 Flash) hosted strictly server-side via `/api/analyze-product` and `/api/classify-waste`
- **Security**: No API keys or secrets exposed to the browser client; server-side proxying with robust fallbacks
- **Deployment**: Production-ready container workflow on port `3000`

---

## 📦 Getting Started & Local Setup

### 1. Prerequisites
- Node.js (v18 or higher recommended)
- npm or bun

### 2. Installation
```bash
# Clone the repository
git clone https://github.com/your-username/cirvana-marketplace.git
cd cirvana-marketplace

# Install dependencies
npm install
```

### 3. Environment Variables
Create a `.env` file based on `.env.example`:
```bash
cp .env.example .env
```

Add your Gemini API Key (optional — includes realistic fallback diagnostics):
```env
GEMINI_API_KEY="your-gemini-api-key-here"
```

### 4. Run Development Server
```bash
npm run dev
```
Open your browser and navigate to `http://localhost:3000`.

### 5. Production Build & Start
```bash
# Compile client assets and bundle server
npm run build

# Launch production server
npm start
```

---

## 🔒 Security & Best Practices

- All AI requests are routed exclusively through backend endpoints in `server.ts`.
- `.env*` files are strictly excluded via `.gitignore`.
- Built-in type safety via TypeScript compilation (`tsc --noEmit`).

---

## 📄 License
MIT License.
