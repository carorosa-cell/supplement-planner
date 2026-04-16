import { useState, useEffect, useRef } from "react";

// ─── SUPPLEMENT DATABASE ───
const SUPPLEMENTS = [
  { id: "vitD", name: "Vitamin D3", category: "Vitamine", icon: "☀️", desc: "Knochengesundheit, Immunsystem, Stimmung", defaultDose: 2000, unit: "IE", doseRange: [400, 10000], step: 200, timing: "morgens", withFood: true, fatSoluble: true, refRanges: { blood: "25-OH-Vitamin D", optimal: [40, 80], unit: "ng/ml", deficitNote: "Mangel sehr häufig, besonders im Winter. Bei Werten unter 30 supplementieren.", genderNotes: null, veganNote: "D3 aus Flechten wählen (vegane Quelle)" } },
  { id: "vitK2", name: "Vitamin K2 (MK-7)", category: "Vitamine", icon: "🦴", desc: "Knochen & Gefäßgesundheit, leitet Calcium", defaultDose: 200, unit: "µg", doseRange: [50, 400], step: 25, timing: "morgens", withFood: true, fatSoluble: true, refRanges: null },
  { id: "vitC", name: "Vitamin C", category: "Vitamine", icon: "🍊", desc: "Immunsystem, Antioxidans, Kollagenbildung", defaultDose: 500, unit: "mg", doseRange: [100, 2000], step: 100, timing: "morgens", withFood: false, fatSoluble: false, refRanges: null },
  { id: "vitB", name: "B-Komplex", category: "Vitamine", icon: "⚡", desc: "Energiestoffwechsel, Nervensystem", defaultDose: 1, unit: "Kaps.", doseRange: [1, 2], step: 1, timing: "morgens", withFood: true, fatSoluble: false, refRanges: { blood: "Vitamin B12", optimal: [400, 900], unit: "pg/ml", deficitNote: "B12-Mangel bei Veganern fast garantiert ohne Supplementierung.", genderNotes: null, veganNote: "PFLICHT-Supplement bei veganer Ernährung!" } },
  { id: "vitE", name: "Vitamin E", category: "Vitamine", icon: "🛡️", desc: "Antioxidans, Zellschutz, Hautgesundheit", defaultDose: 200, unit: "IE", doseRange: [100, 400], step: 50, timing: "morgens", withFood: true, fatSoluble: true, refRanges: null },
  { id: "vitA", name: "Vitamin A", category: "Vitamine", icon: "👁️", desc: "Sehkraft, Haut, Immunsystem", defaultDose: 800, unit: "µg", doseRange: [400, 1500], step: 100, timing: "morgens", withFood: true, fatSoluble: true, refRanges: null },
  { id: "folate", name: "Folsäure (B9)", category: "Vitamine", icon: "🧬", desc: "Zellteilung, DNA-Synthese", defaultDose: 400, unit: "µg", doseRange: [200, 800], step: 100, timing: "morgens", withFood: false, fatSoluble: false, refRanges: { blood: "Folsäure", optimal: [5, 20], unit: "ng/ml", deficitNote: "Besonders wichtig bei Kinderwunsch und Schwangerschaft.", genderNotes: { f: "Frauen im gebärfähigen Alter: 400-800 µg empfohlen" }, veganNote: null } },
  { id: "magnesium", name: "Magnesium", category: "Mineralstoffe", icon: "💤", desc: "Muskelentspannung, Schlaf, Nervensystem", defaultDose: 400, unit: "mg", doseRange: [100, 600], step: 50, timing: "abends", withFood: true, fatSoluble: false, refRanges: { blood: "Magnesium", optimal: [0.85, 1.1], unit: "mmol/l", deficitNote: "Serumspiegel zeigt nur 1% des Gesamtmagnesiums. Oft subklinischer Mangel.", genderNotes: null, veganNote: null } },
  { id: "zinc", name: "Zink", category: "Mineralstoffe", icon: "🔬", desc: "Immunsystem, Haut, Wundheilung", defaultDose: 15, unit: "mg", doseRange: [5, 50], step: 5, timing: "morgens", withFood: true, fatSoluble: false, refRanges: { blood: "Zink", optimal: [80, 120], unit: "µg/dl", deficitNote: "Phytatreiche Ernährung hemmt Zinkaufnahme.", genderNotes: { m: "Männer: höherer Bedarf durch Verlust über Schweiß" }, veganNote: "Veganer brauchen ca. 50% mehr Zink wegen Phytaten" } },
  { id: "iron", name: "Eisen", category: "Mineralstoffe", icon: "🩸", desc: "Blutbildung, Sauerstofftransport, Energie", defaultDose: 14, unit: "mg", doseRange: [5, 30], step: 1, timing: "morgens", withFood: false, fatSoluble: false, refRanges: { blood: "Ferritin", optimal: [50, 150], unit: "ng/ml", deficitNote: "Ferritin unter 30 = Eisenmangel. Unter 15 = schwerer Mangel.", genderNotes: { f: "Frauen vor Menopause: deutlich höherer Bedarf (15-20 mg)", m: "Männer: Vorsicht vor Überladung, nur bei Mangel supplementieren!" }, veganNote: "Pflanzliches Eisen schlechter bioverfügbar – mit Vitamin C kombinieren" } },
  { id: "calcium", name: "Calcium", category: "Mineralstoffe", icon: "🦷", desc: "Knochen, Zähne, Muskelfunktion", defaultDose: 500, unit: "mg", doseRange: [200, 1200], step: 100, timing: "abends", withFood: true, fatSoluble: false, refRanges: null },
  { id: "selenium", name: "Selen", category: "Mineralstoffe", icon: "🧪", desc: "Schilddrüse, Antioxidans, Immunsystem", defaultDose: 100, unit: "µg", doseRange: [50, 200], step: 25, timing: "morgens", withFood: true, fatSoluble: false, refRanges: { blood: "Selen", optimal: [100, 140], unit: "µg/l", deficitNote: "In Europa häufig suboptimal wegen selenarmer Böden.", genderNotes: null, veganNote: "1-2 Paranüsse/Tag decken den Bedarf oft ab" } },
  { id: "copper", name: "Kupfer", category: "Mineralstoffe", icon: "🔶", desc: "Eisenstoffwechsel, Bindegewebe", defaultDose: 2, unit: "mg", doseRange: [0.5, 3], step: 0.5, timing: "morgens", withFood: true, fatSoluble: false, refRanges: null },
  { id: "omega3", name: "Omega-3 (EPA/DHA)", category: "Fettsäuren", icon: "🐟", desc: "Herz, Gehirn, Entzündungshemmung", defaultDose: 2000, unit: "mg", doseRange: [500, 5000], step: 250, timing: "morgens", withFood: true, fatSoluble: true, refRanges: { blood: "Omega-3-Index", optimal: [8, 11], unit: "%", deficitNote: "Omega-3-Index unter 4% = hohes kardiovaskuläres Risiko.", genderNotes: null, veganNote: "Algenöl statt Fischöl verwenden!" } },
  { id: "probiotics", name: "Probiotika", category: "Darmgesundheit", icon: "🦠", desc: "Darmflora, Verdauung, Immunsystem", defaultDose: 20, unit: "Mrd. KBE", doseRange: [5, 100], step: 5, timing: "morgens", withFood: false, fatSoluble: false, refRanges: null },
  { id: "collagen", name: "Kollagen", category: "Sonstiges", icon: "✨", desc: "Haut, Haare, Gelenke, Bindegewebe", defaultDose: 10, unit: "g", doseRange: [2.5, 20], step: 2.5, timing: "morgens", withFood: false, fatSoluble: false, refRanges: null, veganNote: "Nicht vegan – Alternative: Vitamin C + Silizium" },
  { id: "ashwagandha", name: "Ashwagandha", category: "Adaptogene", icon: "🌿", desc: "Stressreduktion, Schlaf, Regeneration", defaultDose: 600, unit: "mg", doseRange: [150, 1200], step: 150, timing: "abends", withFood: true, fatSoluble: false, refRanges: null },
  { id: "creatine", name: "Kreatin", category: "Sport", icon: "💪", desc: "Kraft, Muskelaufbau, kognitive Leistung", defaultDose: 5, unit: "g", doseRange: [2, 10], step: 1, timing: "egal", withFood: true, fatSoluble: false, refRanges: null },
  { id: "curcumin", name: "Curcumin", category: "Sonstiges", icon: "🟡", desc: "Entzündungshemmung, Antioxidans", defaultDose: 500, unit: "mg", doseRange: [250, 1500], step: 250, timing: "morgens", withFood: true, fatSoluble: true, refRanges: null },
];

const SYNERGIES = [
  { a: "vitD", b: "vitK2", reason: "K2 leitet das durch D3 aufgenommene Calcium in die Knochen statt in die Gefäße" },
  { a: "vitD", b: "magnesium", reason: "Magnesium wird für die Aktivierung von Vitamin D benötigt" },
  { a: "vitD", b: "omega3", reason: "Fett verbessert die Aufnahme von fettlöslichem Vitamin D" },
  { a: "vitD", b: "calcium", reason: "Vitamin D fördert die Calcium-Aufnahme im Darm" },
  { a: "vitC", b: "iron", reason: "Vitamin C steigert die Eisenaufnahme drastisch (bis zu 6-fach)" },
  { a: "vitC", b: "vitE", reason: "Vitamin C regeneriert verbrauchtes Vitamin E" },
  { a: "vitC", b: "collagen", reason: "Vitamin C ist essentiell für die Kollagensynthese" },
  { a: "zinc", b: "vitB", reason: "Zink unterstützt den B-Vitamin-Stoffwechsel" },
  { a: "curcumin", b: "omega3", reason: "Beide wirken entzündungshemmend – synergistischer Effekt" },
  { a: "probiotics", b: "magnesium", reason: "Gesunde Darmflora verbessert die Mineralstoffaufnahme" },
  { a: "selenium", b: "vitE", reason: "Beide arbeiten als Antioxidantien synergistisch zusammen" },
  { a: "vitK2", b: "calcium", reason: "K2 sorgt dafür, dass Calcium in Knochen eingelagert wird" },
];

const CONFLICTS = [
  { a: "iron", b: "calcium", reason: "Calcium blockiert die Eisenaufnahme – mindestens 2h Abstand!", severity: "high" },
  { a: "iron", b: "zinc", reason: "Eisen und Zink konkurrieren um den gleichen Transporter", severity: "medium" },
  { a: "zinc", b: "copper", reason: "Zink hemmt die Kupferaufnahme bei Langzeiteinnahme", severity: "medium" },
  { a: "calcium", b: "magnesium", reason: "In hohen Dosen konkurrieren sie um die Aufnahme – getrennt einnehmen", severity: "medium" },
  { a: "calcium", b: "zinc", reason: "Calcium kann die Zinkaufnahme reduzieren", severity: "low" },
  { a: "vitE", b: "vitK2", reason: "Hohe Dosen Vitamin E können die Vitamin-K-Wirkung hemmen", severity: "low" },
  { a: "iron", b: "vitE", reason: "Vitamin E kann die Eisenaufnahme beeinträchtigen", severity: "low" },
];

function analyzeBloodWork(values, profile) {
  const results = [];
  SUPPLEMENTS.forEach(sup => {
    if (!sup.refRanges) return;
    const key = sup.refRanges.blood;
    const val = values[key];
    if (val === undefined || val === null || val === "") return;
    const numVal = parseFloat(val);
    if (isNaN(numVal)) return;
    const [lo, hi] = sup.refRanges.optimal;
    let status, recommendation, duration;
    if (numVal < lo) {
      const deficit = ((lo - numVal) / lo) * 100;
      if (deficit > 50) {
        status = "critical"; recommendation = "Schwerer Mangel. Sofort supplementieren."; duration = "3–6 Monate, dann Blutwerte kontrollieren";
      } else {
        status = "low"; recommendation = "Unter Optimalbereich. Supplementierung empfohlen."; duration = "2–3 Monate, dann nachkontrollieren";
      }
    } else if (numVal > hi) {
      status = "high"; recommendation = "Über Optimalbereich. Supplementierung pausieren."; duration = "Nicht nötig";
    } else {
      status = "optimal"; recommendation = "Im Optimalbereich. Supplementierung optional."; duration = "Erhaltungsdosis möglich";
    }
    let extra = sup.refRanges.deficitNote || "";
    if (profile.gender && sup.refRanges.genderNotes?.[profile.gender]) extra += " " + sup.refRanges.genderNotes[profile.gender];
    if ((profile.diet === "vegan" || profile.diet === "vegetarisch") && sup.refRanges.veganNote) extra += " " + sup.refRanges.veganNote;
    results.push({ sup, value: numVal, unit: sup.refRanges.unit, optRange: sup.refRanges.optimal, status, recommendation, duration, extra, bloodParam: key });
  });
  return results;
}

const P = {
  bg: "#0B0F1A", card: "#141929", accent: "#6EE7B7", accentDim: "rgba(110,231,183,0.13)", accentGlow: "rgba(110,231,183,0.25)",
  warn: "#FBBF24", warnDim: "rgba(251,191,36,0.13)", danger: "#F87171", dangerDim: "rgba(248,113,113,0.13)",
  synergy: "#34D399", conflict: "#FB923C", text: "#E2E8F0", textDim: "#64748B", border: "rgba(255,255,255,0.06)",
  blue: "#60A5FA", blueDim: "rgba(96,165,250,0.13)",
};

function Pill({ children, color = P.textDim, bg = "rgba(255,255,255,0.06)", style = {} }) {
  return <span style={{ fontSize: 10, padding: "3px 10px", borderRadius: 99, background: bg, color, fontFamily: "'DM Sans',sans-serif", fontWeight: 600, whiteSpace: "nowrap", ...style }}>{children}</span>;
}

export default function App() {
  const [selected, setSelected] = useState([]);
  const [doses, setDoses] = useState({});
  const [view, setView] = useState("stack");
  const [search, setSearch] = useState("");
  const [catFilter, setCatFilter] = useState("Alle");
  const [profile, setProfile] = useState({ gender: "", age: "", diet: "" });
  const [showProfile, setShowProfile] = useState(false);
  const [reminders, setReminders] = useState({});
  const [bloodValues, setBloodValues] = useState({});
  const [bloodResults, setBloodResults] = useState(null);
  const [showBloodEntry, setShowBloodEntry] = useState(false);
  const [reminderToast, setReminderToast] = useState(null);

  const categories = ["Alle", ...new Set(SUPPLEMENTS.map(s => s.category))];
  const toggle = id => setSelected(p => p.includes(id) ? p.filter(x => x !== id) : [...p, id]);
  const getDose = id => doses[id] ?? SUPPLEMENTS.find(s => s.id === id)?.defaultDose;
  const setDoseVal = (id, v) => setDoses(p => ({ ...p, [id]: v }));

  const getInter = id => ({
    synergies: SYNERGIES.filter(s => (s.a === id || s.b === id) && selected.includes(s.a) && selected.includes(s.b)),
    conflicts: CONFLICTS.filter(c => (c.a === id || c.b === id) && selected.includes(c.a) && selected.includes(c.b)),
  });

  const allSyn = SYNERGIES.filter(s => selected.includes(s.a) && selected.includes(s.b));
  const allCon = CONFLICTS.filter(c => selected.includes(c.a) && selected.includes(c.b));

  const genSchedule = () => {
    const slots = {
      morgens_nüchtern: { label: "Morgens nüchtern", emoji: "🌅", time: "07:00", items: [], note: "30 Min vor dem Frühstück, mit Wasser" },
      morgens_essen: { label: "Zum Frühstück", emoji: "🍳", time: "08:00", items: [], note: "Mit einer fetthaltigen Mahlzeit" },
      mittags: { label: "Mittags", emoji: "🌤️", time: "13:00", items: [], note: "Zum Mittagessen" },
      abends_essen: { label: "Zum Abendessen", emoji: "🌙", time: "19:00", items: [], note: "Mit dem Abendessen" },
      abends_spät: { label: "Vor dem Schlaf", emoji: "😴", time: "21:30", items: [], note: "30 Min vor dem Schlafen" },
    };
    selected.map(id => SUPPLEMENTS.find(s => s.id === id)).filter(Boolean).forEach(s => {
      const entry = { ...s, customDose: getDose(s.id) };
      if (s.timing === "morgens" && !s.withFood && !s.fatSoluble) slots.morgens_nüchtern.items.push(entry);
      else if (s.timing === "morgens") slots.morgens_essen.items.push(entry);
      else if (s.timing === "abends" && (s.id === "ashwagandha" || s.id === "magnesium")) slots.abends_spät.items.push(entry);
      else if (s.timing === "abends") slots.abends_essen.items.push(entry);
      else slots.mittags.items.push(entry);
    });
    const ironIn = slots.morgens_nüchtern.items.find(i => i.id === "iron");
    const calcIn = slots.morgens_essen.items.find(i => i.id === "calcium");
    if (ironIn && calcIn) {
      slots.morgens_essen.items = slots.morgens_essen.items.filter(i => i.id !== "calcium");
      const c = SUPPLEMENTS.find(s => s.id === "calcium");
      slots.abends_essen.items.push({ ...c, customDose: getDose("calcium") });
    }
    return Object.entries(slots).filter(([, sl]) => sl.items.length > 0).map(([key, sl]) => ({ ...sl, key }));
  };

  const schedule = genSchedule();

  const toggleReminder = (slotKey, time, label) => {
    setReminders(p => {
      const next = { ...p };
      if (next[slotKey]) { delete next[slotKey]; setReminderToast({ text: `Erinnerung für "${label}" deaktiviert`, type: "off" }); }
      else { next[slotKey] = time; setReminderToast({ text: `🔔 Erinnerung um ${time} für "${label}" aktiviert`, type: "on" }); }
      return next;
    });
    setTimeout(() => setReminderToast(null), 3000);
  };

  const filtered = SUPPLEMENTS.filter(s => {
    const ms = s.name.toLowerCase().includes(search.toLowerCase()) || s.desc.toLowerCase().includes(search.toLowerCase());
    return ms && (catFilter === "Alle" || s.category === catFilter);
  });

  const tabs = [
    { key: "stack", label: "Stack", icon: "📦" },
    { key: "schedule", label: "Plan", icon: "📋" },
    { key: "interactions", label: "Check", icon: "🔗" },
    { key: "blood", label: "Blutbild", icon: "🩸" },
    { key: "library", label: "Wiki", icon: "📚" },
  ];

  return (
    <div style={{ background: P.bg, minHeight: "100vh", color: P.text, fontFamily: "'DM Sans',sans-serif" }}>
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=DM+Sans:wght@300;400;500;600;700;800&family=Fraunces:wght@700;800;900&display=swap');
        @keyframes slideUp { from { opacity:0; transform:translateY(16px); } to { opacity:1; transform:translateY(0); } }
        @keyframes fadeIn { from { opacity:0; } to { opacity:1; } }
        @keyframes toastIn { from { opacity:0; transform:translateY(30px); } to { opacity:1; transform:translateY(0); } }
        @keyframes toastOut { from { opacity:1; } to { opacity:0; transform:translateY(10px); } }
        * { box-sizing: border-box; margin: 0; padding: 0; }
        input:focus, select:focus { outline: none; }
        ::-webkit-scrollbar { width: 3px; height: 3px; }
        ::-webkit-scrollbar-thumb { background: rgba(255,255,255,0.08); border-radius: 4px; }
        input[type=range] { -webkit-appearance: none; width: 100%; height: 4px; border-radius: 4px; background: rgba(255,255,255,0.1); }
        input[type=range]::-webkit-slider-thumb { -webkit-appearance: none; width: 18px; height: 18px; border-radius: 50%; background: #6EE7B7; cursor: pointer; border: 2px solid #0B0F1A; }
      `}</style>

      {/* TOAST */}
      {reminderToast && (
        <div style={{
          position: "fixed", bottom: 80, left: "50%", transform: "translateX(-50%)", zIndex: 200,
          background: reminderToast.type === "on" ? P.accent : "rgba(255,255,255,0.1)",
          color: reminderToast.type === "on" ? P.bg : P.text,
          padding: "10px 20px", borderRadius: 12, fontWeight: 700, fontSize: 13,
          animation: "toastIn 0.3s ease", boxShadow: "0 4px 20px rgba(0,0,0,0.4)",
          whiteSpace: "nowrap",
        }}>{reminderToast.text}</div>
      )}

      {/* HEADER */}
      <div style={{ background: "linear-gradient(180deg, rgba(110,231,183,0.06) 0%, transparent 100%)", padding: "30px 18px 16px", borderBottom: `1px solid ${P.border}` }}>
        <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start" }}>
          <div>
            <h1 style={{ fontFamily: "'Fraunces',serif", fontWeight: 900, fontSize: 22, background: `linear-gradient(135deg, ${P.accent}, #A7F3D0)`, WebkitBackgroundClip: "text", WebkitTextFillColor: "transparent" }}>💊 Supplement Planner</h1>
            <p style={{ color: P.textDim, fontSize: 11, marginTop: 3 }}>Dein intelligenter Einnahmeplan</p>
          </div>
          <button onClick={() => setShowProfile(!showProfile)} style={{
            background: profile.gender ? P.accentDim : "rgba(255,255,255,0.06)",
            border: `1px solid ${profile.gender ? "rgba(110,231,183,0.3)" : P.border}`,
            borderRadius: 10, padding: "7px 12px", cursor: "pointer",
            color: profile.gender ? P.accent : P.textDim, fontSize: 11, fontFamily: "'DM Sans',sans-serif", fontWeight: 700,
          }}>👤 {profile.gender ? (profile.gender === "m" ? "♂" : "♀") + (profile.diet === "vegan" ? " 🌱" : profile.diet === "vegetarisch" ? " 🥗" : "") : "Profil"}</button>
        </div>
        {selected.length > 0 && (
          <div style={{ display: "flex", gap: 8, marginTop: 12, flexWrap: "wrap" }}>
            <Pill color={P.accent} bg={P.accentDim}>{selected.length} Supplements</Pill>
            {allSyn.length > 0 && <Pill color={P.synergy} bg="rgba(52,211,153,0.1)">✦ {allSyn.length}</Pill>}
            {allCon.length > 0 && <Pill color={P.conflict} bg="rgba(251,146,60,0.1)">⚠ {allCon.length}</Pill>}
            {Object.keys(reminders).length > 0 && <Pill color={P.blue} bg={P.blueDim}>🔔 {Object.keys(reminders).length}</Pill>}
          </div>
        )}
      </div>

      {/* PROFILE MODAL */}
      {showProfile && (
        <div style={{ position: "fixed", inset: 0, background: "rgba(0,0,0,0.75)", zIndex: 100, display: "flex", alignItems: "center", justifyContent: "center", padding: 20, animation: "fadeIn 0.2s" }}>
          <div style={{ background: P.card, borderRadius: 20, padding: 24, width: "100%", maxWidth: 360, border: `1px solid ${P.border}` }}>
            <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 20 }}>
              <span style={{ fontWeight: 800, fontSize: 17 }}>👤 Mein Profil</span>
              <button onClick={() => setShowProfile(false)} style={{ background: "none", border: "none", color: P.textDim, fontSize: 20, cursor: "pointer" }}>✕</button>
            </div>
            <div style={{ marginBottom: 16 }}>
              <label style={{ fontSize: 11, color: P.textDim, display: "block", marginBottom: 6, fontWeight: 700 }}>Geschlecht</label>
              <div style={{ display: "flex", gap: 6 }}>
                {[["m", "♂ Mann"], ["f", "♀ Frau"]].map(([v, l]) => (
                  <button key={v} onClick={() => setProfile(p => ({ ...p, gender: v }))} style={{
                    flex: 1, padding: "10px", borderRadius: 10, border: `1px solid ${profile.gender === v ? P.accent : P.border}`,
                    background: profile.gender === v ? P.accentDim : "rgba(255,255,255,0.03)",
                    color: profile.gender === v ? P.accent : P.textDim, fontFamily: "'DM Sans',sans-serif", fontWeight: 700, fontSize: 13, cursor: "pointer",
                  }}>{l}</button>
                ))}
              </div>
            </div>
            <div style={{ marginBottom: 16 }}>
              <label style={{ fontSize: 11, color: P.textDim, display: "block", marginBottom: 6, fontWeight: 700 }}>Alter</label>
              <input type="number" value={profile.age} onChange={e => setProfile(p => ({ ...p, age: e.target.value }))} placeholder="z.B. 32" style={{
                width: "100%", padding: "10px 14px", borderRadius: 10, border: `1px solid ${P.border}`,
                background: "rgba(255,255,255,0.03)", color: P.text, fontFamily: "'DM Sans',sans-serif", fontSize: 14,
              }} />
            </div>
            <div style={{ marginBottom: 16 }}>
              <label style={{ fontSize: 11, color: P.textDim, display: "block", marginBottom: 6, fontWeight: 700 }}>Ernährung</label>
              <div style={{ display: "flex", gap: 6 }}>
                {[["misch", "🥩 Misch"], ["vegetarisch", "🥗 Veg."], ["vegan", "🌱 Vegan"]].map(([v, l]) => (
                  <button key={v} onClick={() => setProfile(p => ({ ...p, diet: v }))} style={{
                    flex: 1, padding: "10px", borderRadius: 10, border: `1px solid ${profile.diet === v ? P.accent : P.border}`,
                    background: profile.diet === v ? P.accentDim : "rgba(255,255,255,0.03)",
                    color: profile.diet === v ? P.accent : P.textDim, fontFamily: "'DM Sans',sans-serif", fontWeight: 700, fontSize: 12, cursor: "pointer",
                  }}>{l}</button>
                ))}
              </div>
            </div>
            <div style={{ background: P.accentDim, borderRadius: 12, padding: "12px 14px", border: "1px solid rgba(110,231,183,0.15)", fontSize: 11, color: P.textDim, lineHeight: 1.6 }}>
              {profile.gender === "f" && "♀ Angepasste Empfehlungen für Frauen (Eisen, Folsäure)"}
              {profile.gender === "m" && "♂ Angepasste Empfehlungen für Männer (Zink, Eisen-Vorsicht)"}
              {!profile.gender && "Profil personalisiert Dosierung & Blutbild-Analyse"}
              {(profile.diet === "vegan" || profile.diet === "vegetarisch") && <><br />🌱 B12, Omega-3, Eisen, Zink besonders beachten</>}
              {profile.age && parseInt(profile.age) > 50 && <><br />👴 Ab 50: Vitamin D, B12, Calcium besonders wichtig</>}
            </div>
          </div>
        </div>
      )}

      {/* NAV */}
      <div style={{ display: "flex", gap: 2, padding: "8px 10px", overflowX: "auto", borderBottom: `1px solid ${P.border}`, position: "sticky", top: 0, zIndex: 10, background: P.bg }}>
        {tabs.map(t => (
          <button key={t.key} onClick={() => setView(t.key)} style={{
            flex: "none", padding: "7px 12px", borderRadius: 99, border: "none",
            background: view === t.key ? P.accentDim : "transparent",
            color: view === t.key ? P.accent : P.textDim,
            fontFamily: "'DM Sans',sans-serif", fontWeight: 700, fontSize: 12, cursor: "pointer", whiteSpace: "nowrap",
          }}>{t.icon} {t.label}</button>
        ))}
      </div>

      {/* CONTENT */}
      <div style={{ padding: "16px 14px", maxWidth: 540, margin: "0 auto", animation: "fadeIn 0.2s" }}>

        {/* STACK */}
        {view === "stack" && (<>
          <input value={search} onChange={e => setSearch(e.target.value)} placeholder="🔍 Supplement suchen..." style={{ width: "100%", padding: "10px 14px", borderRadius: 12, border: `1px solid ${P.border}`, background: P.card, color: P.text, fontFamily: "'DM Sans',sans-serif", fontSize: 13, marginBottom: 10 }} />
          <div style={{ display: "flex", gap: 4, flexWrap: "wrap", marginBottom: 12 }}>
            {categories.map(c => (
              <button key={c} onClick={() => setCatFilter(c)} style={{ padding: "4px 11px", borderRadius: 99, border: "none", background: catFilter === c ? P.accent : "rgba(255,255,255,0.05)", color: catFilter === c ? P.bg : P.textDim, fontFamily: "'DM Sans',sans-serif", fontWeight: 700, fontSize: 10.5, cursor: "pointer" }}>{c}</button>
            ))}
          </div>
          <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 8 }}>
            {filtered.map(sup => {
              const isSel = selected.includes(sup.id);
              const inter = getInter(sup.id);
              return (
                <div key={sup.id} style={{
                  background: isSel ? `linear-gradient(145deg, ${P.card}, ${P.accentDim})` : P.card,
                  border: `1px solid ${isSel ? P.accent : P.border}`, borderRadius: 14, padding: 12, cursor: "pointer",
                  boxShadow: isSel ? `0 0 18px ${P.accentGlow}` : "none", position: "relative",
                }} onClick={() => toggle(sup.id)}>
                  {isSel && <div style={{ position: "absolute", top: 6, right: 6, width: 18, height: 18, borderRadius: "50%", background: P.accent, display: "flex", alignItems: "center", justifyContent: "center", fontSize: 10, color: P.bg, fontWeight: 800 }}>✓</div>}
                  <div style={{ fontSize: 22, marginBottom: 3 }}>{sup.icon}</div>
                  <div style={{ fontWeight: 700, fontSize: 13, color: P.text, marginBottom: 2 }}>{sup.name}</div>
                  <div style={{ fontSize: 10, color: P.textDim, lineHeight: 1.4, marginBottom: 6 }}>{sup.desc}</div>
                  {isSel ? (
                    <div onClick={e => e.stopPropagation()} style={{ marginBottom: 4 }}>
                      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 3 }}>
                        <span style={{ fontSize: 9, color: P.accent, fontWeight: 700 }}>Dosis:</span>
                        <span style={{ fontSize: 12, color: P.accent, fontWeight: 800 }}>{getDose(sup.id)} {sup.unit}</span>
                      </div>
                      <input type="range" min={sup.doseRange[0]} max={sup.doseRange[1]} step={sup.step} value={getDose(sup.id)} onChange={e => setDoseVal(sup.id, parseFloat(e.target.value))} />
                      <div style={{ display: "flex", justifyContent: "space-between" }}>
                        <span style={{ fontSize: 8, color: P.textDim }}>{sup.doseRange[0]}</span>
                        <span style={{ fontSize: 8, color: P.textDim }}>{sup.doseRange[1]} {sup.unit}</span>
                      </div>
                    </div>
                  ) : (
                    <div style={{ display: "flex", gap: 4, flexWrap: "wrap" }}>
                      <Pill>{sup.defaultDose} {sup.unit}</Pill>
                      {sup.fatSoluble && <Pill color={P.warn} bg={P.warnDim}>fettlösl.</Pill>}
                    </div>
                  )}
                  {isSel && (inter.synergies.length > 0 || inter.conflicts.length > 0) && (
                    <div style={{ display: "flex", gap: 6, marginTop: 4 }}>
                      {inter.synergies.length > 0 && <span style={{ fontSize: 9, color: P.synergy }}>✦ {inter.synergies.length}</span>}
                      {inter.conflicts.length > 0 && <span style={{ fontSize: 9, color: P.conflict }}>⚠ {inter.conflicts.length}</span>}
                    </div>
                  )}
                  {(profile.diet === "vegan" || profile.diet === "vegetarisch") && (sup.refRanges?.veganNote || sup.veganNote) && (
                    <div style={{ marginTop: 4, fontSize: 9, color: "#86EFAC", background: "rgba(134,239,172,0.08)", padding: "3px 6px", borderRadius: 5, lineHeight: 1.3 }}>🌱 {sup.refRanges?.veganNote || sup.veganNote}</div>
                  )}
                </div>
              );
            })}
          </div>
          {filtered.length === 0 && <div style={{ textAlign: "center", padding: 40, color: P.textDim }}>Kein Supplement gefunden</div>}
        </>)}

        {/* SCHEDULE */}
        {view === "schedule" && (
          selected.length === 0 ?
            <div style={{ textAlign: "center", padding: "50px 20px" }}><div style={{ fontSize: 40, marginBottom: 12 }}>📋</div><div style={{ color: P.textDim, fontSize: 14, lineHeight: 1.7 }}>Wähle zuerst Supplements in "Stack" aus</div></div>
          : (
            <div style={{ display: "flex", flexDirection: "column", gap: 10 }}>
              <div style={{ background: P.accentDim, borderRadius: 12, padding: "12px 14px", border: "1px solid rgba(110,231,183,0.15)" }}>
                <div style={{ fontSize: 11, fontWeight: 700, color: P.accent, marginBottom: 3 }}>💡 Optimierter Tagesplan</div>
                <div style={{ fontSize: 10.5, color: P.textDim, lineHeight: 1.5 }}>{selected.length} Supplements optimal verteilt. Tippe 🔔 für Erinnerungen.</div>
              </div>
              {schedule.map((slot, i) => (
                <div key={slot.key} style={{ background: P.card, borderRadius: 14, padding: 16, border: `1px solid ${P.border}`, animation: `slideUp 0.4s ease ${i * 0.07}s both` }}>
                  <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 8 }}>
                    <div style={{ display: "flex", alignItems: "center", gap: 6 }}>
                      <span style={{ fontSize: 18 }}>{slot.emoji}</span>
                      <span style={{ fontWeight: 700, fontSize: 14 }}>{slot.label}</span>
                    </div>
                    <div style={{ display: "flex", alignItems: "center", gap: 5 }}>
                      <span style={{ fontSize: 11, color: P.accent, background: P.accentDim, padding: "2px 8px", borderRadius: 99 }}>{slot.time}</span>
                      <button onClick={() => toggleReminder(slot.key, slot.time, slot.label)} style={{
                        width: 30, height: 30, borderRadius: 8, border: `1px solid ${reminders[slot.key] ? P.blue : P.border}`,
                        background: reminders[slot.key] ? P.blueDim : "rgba(255,255,255,0.03)",
                        color: reminders[slot.key] ? P.blue : P.textDim, cursor: "pointer", fontSize: 13,
                        display: "flex", alignItems: "center", justifyContent: "center",
                      }}>🔔</button>
                    </div>
                  </div>
                  <div style={{ fontSize: 10, color: P.textDim, marginBottom: 10, fontStyle: "italic" }}>{slot.note}</div>
                  {reminders[slot.key] && (
                    <div style={{ background: P.blueDim, borderRadius: 7, padding: "5px 10px", marginBottom: 8, display: "flex", alignItems: "center", gap: 5, border: "1px solid rgba(96,165,250,0.2)" }}>
                      <span style={{ fontSize: 11 }}>🔔</span><span style={{ fontSize: 10, color: P.blue, fontWeight: 700 }}>Erinnerung um {slot.time} aktiv</span>
                    </div>
                  )}
                  {slot.items.map(s => (
                    <div key={s.id} style={{ display: "flex", alignItems: "center", gap: 8, background: "rgba(255,255,255,0.02)", borderRadius: 8, padding: "8px 10px", marginBottom: 4 }}>
                      <span style={{ fontSize: 18 }}>{s.icon}</span>
                      <div style={{ flex: 1 }}>
                        <div style={{ fontWeight: 700, fontSize: 12.5 }}>{s.name}</div>
                        <div style={{ fontSize: 11, color: P.accent, fontWeight: 700 }}>{s.customDose} {s.unit}</div>
                      </div>
                      {s.fatSoluble && <Pill color={P.warn} bg={P.warnDim} style={{ fontSize: 8 }}>🧈+Fett</Pill>}
                    </div>
                  ))}
                </div>
              ))}
              {/* Set all reminders button */}
              <button onClick={() => {
                const newR = {};
                schedule.forEach(s => { newR[s.key] = s.time; });
                setReminders(newR);
                setReminderToast({ text: `🔔 ${schedule.length} Erinnerungen aktiviert`, type: "on" });
                setTimeout(() => setReminderToast(null), 3000);
              }} style={{
                width: "100%", padding: "12px", borderRadius: 12, border: `1px solid ${P.blue}`,
                background: P.blueDim, color: P.blue, fontWeight: 700, fontSize: 13,
                cursor: "pointer", fontFamily: "'DM Sans',sans-serif", marginTop: 4,
              }}>🔔 Alle Erinnerungen aktivieren</button>
            </div>
          )
        )}

        {/* INTERACTIONS */}
        {view === "interactions" && (
          selected.length < 2 ?
            <div style={{ textAlign: "center", padding: "50px 20px" }}><div style={{ fontSize: 40, marginBottom: 12 }}>🔗</div><div style={{ color: P.textDim, fontSize: 14, lineHeight: 1.7 }}>Mindestens 2 Supplements wählen</div></div>
          : (
            <div style={{ display: "flex", flexDirection: "column", gap: 16 }}>
              {allCon.length > 0 && (<div>
                <div style={{ display: "flex", alignItems: "center", gap: 6, marginBottom: 10 }}>
                  <span style={{ fontSize: 16 }}>⚠️</span><span style={{ fontWeight: 700, fontSize: 15, color: P.conflict }}>Konflikte ({allCon.length})</span>
                </div>
                <div style={{ display: "flex", flexDirection: "column", gap: 8 }}>
                  {allCon.map((c, i) => {
                    const a = SUPPLEMENTS.find(s => s.id === c.a), b = SUPPLEMENTS.find(s => s.id === c.b);
                    return (
                      <div key={i} style={{ background: "rgba(251,146,60,0.06)", borderRadius: 12, padding: "12px 14px", border: "1px solid rgba(251,146,60,0.15)" }}>
                        <div style={{ display: "flex", alignItems: "center", gap: 5, marginBottom: 5 }}>
                          <span style={{ fontSize: 14 }}>{a?.icon}</span><span style={{ color: P.conflict, fontWeight: 800, fontSize: 12 }}>⚡</span><span style={{ fontSize: 14 }}>{b?.icon}</span>
                          <span style={{ fontWeight: 700, fontSize: 12, color: P.conflict }}>{a?.name} & {b?.name}</span>
                        </div>
                        <div style={{ fontSize: 11, color: P.textDim, lineHeight: 1.5 }}>{c.reason}</div>
                        <Pill style={{ marginTop: 6 }} color={c.severity === "high" ? P.danger : c.severity === "medium" ? P.warn : P.textDim} bg={c.severity === "high" ? P.dangerDim : c.severity === "medium" ? P.warnDim : "rgba(255,255,255,0.05)"}>
                          {c.severity === "high" ? "⛔ Kritisch" : c.severity === "medium" ? "⚠ Beachten" : "ℹ Gering"}
                        </Pill>
                      </div>
                    );
                  })}
                </div>
              </div>)}
              {allSyn.length > 0 && (<div>
                <div style={{ display: "flex", alignItems: "center", gap: 6, marginBottom: 10 }}>
                  <span style={{ fontSize: 16 }}>✦</span><span style={{ fontWeight: 700, fontSize: 15, color: P.synergy }}>Synergien ({allSyn.length})</span>
                </div>
                <div style={{ display: "flex", flexDirection: "column", gap: 8 }}>
                  {allSyn.map((s, i) => {
                    const a = SUPPLEMENTS.find(x => x.id === s.a), b = SUPPLEMENTS.find(x => x.id === s.b);
                    return (
                      <div key={i} style={{ background: "rgba(52,211,153,0.06)", borderRadius: 12, padding: "12px 14px", border: "1px solid rgba(52,211,153,0.15)" }}>
                        <div style={{ display: "flex", alignItems: "center", gap: 5, marginBottom: 5 }}>
                          <span style={{ fontSize: 14 }}>{a?.icon}</span><span style={{ color: P.synergy, fontWeight: 800 }}>+</span><span style={{ fontSize: 14 }}>{b?.icon}</span>
                          <span style={{ fontWeight: 700, fontSize: 12, color: P.synergy }}>{a?.name} & {b?.name}</span>
                        </div>
                        <div style={{ fontSize: 11, color: P.textDim, lineHeight: 1.5 }}>{s.reason}</div>
                      </div>
                    );
                  })}
                </div>
              </div>)}
              {allSyn.length === 0 && allCon.length === 0 && <div style={{ textAlign: "center", padding: 30, color: P.textDim }}>Keine bekannten Interaktionen</div>}
            </div>
          )
        )}

        {/* BLOOD WORK */}
        {view === "blood" && (
          <div style={{ display: "flex", flexDirection: "column", gap: 12 }}>
            {!profile.gender && (
              <div style={{ background: P.warnDim, borderRadius: 12, padding: "12px 14px", border: "1px solid rgba(251,191,36,0.2)" }}>
                <div style={{ fontSize: 11, color: P.warn, fontWeight: 700 }}>⚠ Profil unvollständig</div>
                <div style={{ fontSize: 10.5, color: P.textDim, marginTop: 3 }}>Lege zuerst Geschlecht, Alter & Ernährung fest.</div>
                <button onClick={() => setShowProfile(true)} style={{ marginTop: 6, padding: "5px 12px", borderRadius: 7, border: "none", background: P.warn, color: P.bg, fontWeight: 700, fontSize: 11, cursor: "pointer", fontFamily: "'DM Sans',sans-serif" }}>Profil anlegen →</button>
              </div>
            )}
            <div style={{ background: P.card, borderRadius: 14, padding: 18, border: `1px solid ${P.border}` }}>
              <div style={{ fontWeight: 800, fontSize: 15, marginBottom: 3 }}>🔬 Blutbild-Analyse</div>
              <div style={{ fontSize: 11, color: P.textDim, lineHeight: 1.6, marginBottom: 14 }}>Trage deine Blutwerte ein und erhalte personalisierte Empfehlungen mit Dauer-Angabe.</div>
              <button onClick={() => setShowBloodEntry(!showBloodEntry)} style={{
                width: "100%", padding: "11px", borderRadius: 10, border: `1px solid ${P.accent}`,
                background: P.accentDim, color: P.accent, fontWeight: 700, fontSize: 13, cursor: "pointer", fontFamily: "'DM Sans',sans-serif",
              }}>{showBloodEntry ? "Eingabe schließen" : "📋 Blutwerte eingeben"}</button>
            </div>
            {showBloodEntry && (
              <div style={{ background: P.card, borderRadius: 14, padding: 16, border: `1px solid ${P.border}`, animation: "slideUp 0.3s" }}>
                <div style={{ fontWeight: 700, fontSize: 13, marginBottom: 12 }}>Werte eintragen</div>
                {SUPPLEMENTS.filter(s => s.refRanges).map(sup => (
                  <div key={sup.id} style={{ display: "flex", alignItems: "center", gap: 8, marginBottom: 8 }}>
                    <span style={{ fontSize: 16, width: 24 }}>{sup.icon}</span>
                    <div style={{ flex: 1 }}>
                      <div style={{ fontSize: 10, color: P.textDim, marginBottom: 1 }}>{sup.refRanges.blood}</div>
                      <div style={{ display: "flex", alignItems: "center", gap: 4 }}>
                        <input type="number" step="0.1" placeholder="—" value={bloodValues[sup.refRanges.blood] || ""}
                          onChange={e => setBloodValues(p => ({ ...p, [sup.refRanges.blood]: e.target.value }))}
                          style={{ width: 70, padding: "6px 8px", borderRadius: 7, border: `1px solid ${P.border}`, background: "rgba(255,255,255,0.03)", color: P.text, fontSize: 12, fontFamily: "'DM Sans',sans-serif" }} />
                        <span style={{ fontSize: 10, color: P.textDim }}>{sup.refRanges.unit}</span>
                        <span style={{ fontSize: 8, color: P.textDim, marginLeft: "auto" }}>opt: {sup.refRanges.optimal[0]}–{sup.refRanges.optimal[1]}</span>
                      </div>
                    </div>
                  </div>
                ))}
                <button onClick={() => { setBloodResults(analyzeBloodWork(bloodValues, profile)); setShowBloodEntry(false); }} style={{
                  width: "100%", marginTop: 10, padding: "11px", borderRadius: 10, border: "none",
                  background: `linear-gradient(135deg, ${P.accent}, #34D399)`, color: P.bg,
                  fontWeight: 800, fontSize: 13, cursor: "pointer", fontFamily: "'DM Sans',sans-serif",
                }}>🔬 Analyse starten</button>
              </div>
            )}
            {bloodResults && bloodResults.length > 0 && (
              <div style={{ display: "flex", flexDirection: "column", gap: 8 }}>
                <div style={{ display: "flex", alignItems: "center", gap: 6, marginBottom: 4 }}>
                  <span style={{ fontSize: 16 }}>📊</span><span style={{ fontWeight: 700, fontSize: 15, color: P.accent }}>Ergebnisse ({bloodResults.length})</span>
                </div>
                {bloodResults.sort((a, b) => {
                  const o = { critical: 0, low: 1, high: 2, optimal: 3 };
                  return o[a.status] - o[b.status];
                }).map((r, i) => {
                  const st = {
                    critical: { bg: P.dangerDim, border: "rgba(248,113,113,0.25)", color: P.danger, label: "⛔ Schwerer Mangel", bar: P.danger },
                    low: { bg: P.warnDim, border: "rgba(251,191,36,0.25)", color: P.warn, label: "⚠ Unter Optimal", bar: P.warn },
                    high: { bg: P.blueDim, border: "rgba(96,165,250,0.25)", color: P.blue, label: "↑ Über Optimal", bar: P.blue },
                    optimal: { bg: "rgba(52,211,153,0.06)", border: "rgba(52,211,153,0.2)", color: P.synergy, label: "✅ Optimal", bar: P.synergy },
                  }[r.status];
                  const maxBar = r.optRange[1] * 1.5;
                  const valPct = Math.min((r.value / maxBar) * 100, 100);
                  const loPct = (r.optRange[0] / maxBar) * 100;
                  const hiPct = (r.optRange[1] / maxBar) * 100;
                  return (
                    <div key={i} style={{ background: st.bg, borderRadius: 12, padding: "14px 16px", border: `1px solid ${st.border}`, animation: `slideUp 0.4s ease ${i * 0.05}s both` }}>
                      <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 6 }}>
                        <div style={{ display: "flex", alignItems: "center", gap: 6 }}>
                          <span style={{ fontSize: 18 }}>{r.sup.icon}</span>
                          <div>
                            <div style={{ fontWeight: 700, fontSize: 13 }}>{r.sup.name}</div>
                            <div style={{ fontSize: 10, color: P.textDim }}>{r.bloodParam}</div>
                          </div>
                        </div>
                        <Pill color={st.color} bg="rgba(0,0,0,0.2)">{st.label}</Pill>
                      </div>
                      <div style={{ position: "relative", height: 14, background: "rgba(255,255,255,0.04)", borderRadius: 99, marginBottom: 6, overflow: "hidden" }}>
                        <div style={{ position: "absolute", left: `${loPct}%`, width: `${hiPct - loPct}%`, height: "100%", background: "rgba(52,211,153,0.1)", borderRadius: 99 }} />
                        <div style={{ position: "absolute", left: `${Math.max(valPct - 0.5, 0)}%`, width: 3, height: "100%", background: st.bar, borderRadius: 99, boxShadow: `0 0 6px ${st.bar}` }} />
                      </div>
                      <div style={{ display: "flex", justifyContent: "space-between", fontSize: 9.5, color: P.textDim, marginBottom: 8 }}>
                        <span>Dein Wert: <b style={{ color: st.color }}>{r.value} {r.unit}</b></span>
                        <span>Optimal: {r.optRange[0]}–{r.optRange[1]}</span>
                      </div>
                      <div style={{ fontSize: 11.5, color: P.text, fontWeight: 600, marginBottom: 3 }}>{r.recommendation}</div>
                      <div style={{ fontSize: 10.5, color: P.textDim, marginBottom: 4 }}>⏱️ Empfohlene Dauer: {r.duration}</div>
                      {r.extra && <div style={{ fontSize: 10, color: P.textDim, lineHeight: 1.5, borderTop: "1px solid rgba(255,255,255,0.05)", paddingTop: 6, marginTop: 4 }}>{r.extra}</div>}
                    </div>
                  );
                })}
              </div>
            )}
            {bloodResults && bloodResults.length === 0 && <div style={{ textAlign: "center", padding: 30, color: P.textDim, fontSize: 13 }}>Keine Werte eingegeben</div>}
          </div>
        )}

        {/* LIBRARY */}
        {view === "library" && (
          <div style={{ display: "flex", flexDirection: "column", gap: 8 }}>
            <div style={{ background: P.card, borderRadius: 12, padding: "14px 16px", border: `1px solid ${P.border}`, marginBottom: 4 }}>
              <div style={{ fontSize: 13, fontWeight: 800, color: P.accent, marginBottom: 8 }}>📖 Grundregeln</div>
              {[
                ["🧈", "Fettlöslich", "A, D, E, K immer mit Fett einnehmen"],
                ["🩸", "Eisen", "Nüchtern + Vit. C. Nie mit Calcium/Kaffee/Tee"],
                ["💤", "Magnesium", "Abends – fördert Entspannung und Schlaf"],
                ["🦠", "Probiotika", "30 Min vor dem Frühstück, leerer Magen"],
                ["🔬", "Zink+Kupfer", "Nicht langfristig Zink ohne Kupfer (15:1)"],
                ["☀️", "D3+K2", "Pflicht-Duo – nie D3 ohne K2"],
              ].map(([ic, title, text], i) => (
                <div key={i} style={{ display: "flex", gap: 8, marginBottom: 7, alignItems: "flex-start" }}>
                  <span style={{ fontSize: 14, flexShrink: 0 }}>{ic}</span>
                  <div style={{ fontSize: 11 }}><b style={{ color: P.text }}>{title}:</b> <span style={{ color: P.textDim }}>{text}</span></div>
                </div>
              ))}
            </div>
            {SUPPLEMENTS.map(sup => {
              const syn = SYNERGIES.filter(s => s.a === sup.id || s.b === sup.id);
              const con = CONFLICTS.filter(c => c.a === sup.id || c.b === sup.id);
              return (
                <div key={sup.id} style={{ background: P.card, borderRadius: 12, padding: 14, border: `1px solid ${P.border}` }}>
                  <div style={{ display: "flex", alignItems: "center", gap: 6, marginBottom: 6 }}>
                    <span style={{ fontSize: 20 }}>{sup.icon}</span>
                    <div><div style={{ fontWeight: 800, fontSize: 13 }}>{sup.name}</div><div style={{ fontSize: 9.5, color: P.accent }}>{sup.category}</div></div>
                  </div>
                  <div style={{ fontSize: 11, color: P.textDim, lineHeight: 1.5, marginBottom: 6 }}>{sup.desc}</div>
                  <div style={{ display: "flex", gap: 4, flexWrap: "wrap" }}>
                    <Pill>📏 {sup.defaultDose} {sup.unit}</Pill>
                    <Pill>⏰ {sup.timing}</Pill>
                    <Pill>{sup.withFood ? "🍽️ mit Essen" : "💧 nüchtern"}</Pill>
                    {sup.fatSoluble && <Pill color={P.warn} bg={P.warnDim}>🧈 fettlösl.</Pill>}
                  </div>
                  {(syn.length > 0 || con.length > 0) && (
                    <div style={{ marginTop: 6, paddingTop: 6, borderTop: `1px solid ${P.border}` }}>
                      {syn.length > 0 && <div style={{ fontSize: 10 }}><span style={{ color: P.synergy, fontWeight: 700 }}>✦ </span><span style={{ color: P.textDim }}>{syn.map(s => SUPPLEMENTS.find(x => x.id === (s.a === sup.id ? s.b : s.a))?.name).join(", ")}</span></div>}
                      {con.length > 0 && <div style={{ fontSize: 10, marginTop: 2 }}><span style={{ color: P.conflict, fontWeight: 700 }}>⚠ </span><span style={{ color: P.textDim }}>{con.map(c => SUPPLEMENTS.find(x => x.id === (c.a === sup.id ? c.b : c.a))?.name).join(", ")}</span></div>}
                    </div>
                  )}
                </div>
              );
            })}
          </div>
        )}
      </div>

      <div style={{ textAlign: "center", padding: "24px 20px", color: P.textDim, fontSize: 9, borderTop: `1px solid ${P.border}`, marginTop: 24 }}>
        Supplement Planner · Quellen: Examine.com, NIH ODS, PubMed<br />Keine medizinische Beratung – konsultiere deinen Arzt
      </div>
    </div>
  );
}
