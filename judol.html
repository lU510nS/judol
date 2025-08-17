import React, { useMemo, useState, useEffect } from "react";
import { motion } from "framer-motion";
import { Coins, Gamepad2, Trophy, Shield, Info, Star, LogIn, Gift, Menu, Crown } from "lucide-react";
import { Button } from "@/components/ui/button";
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";
import { Input } from "@/components/ui/input";
import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs";
import { Progress } from "@/components/ui/progress";

// NOTE: Arcade-style demo with fictional credits only. No real money, no gambling.

const mockGames = [
  { id: "astro", title: "Astro Spin Demo", rtp: 98, volatility: "Low", rating: 4.7, tag: "New" },
  { id: "pirate", title: "Pirate Treasure Demo", rtp: 96, volatility: "Medium", rating: 4.5, tag: "Hot" },
  { id: "neon", title: "Neon Fruits Demo", rtp: 97, volatility: "Low", rating: 4.6, tag: "Featured" },
  { id: "myth", title: "Mythic Realms Demo", rtp: 95, volatility: "High", rating: 4.2, tag: "Classic" },
  { id: "speed", title: "Speed Wheels Demo", rtp: 96, volatility: "Medium", rating: 4.3, tag: "Racing" },
  { id: "blocks", title: "Block Cascade Demo", rtp: 99, volatility: "Low", rating: 4.9, tag: "Chill" },
];

function formatCredits(x) {
  return new Intl.NumberFormat(undefined, { maximumFractionDigits: 0 }).format(x);
}

function Sparkle() {
  return (
    <motion.span
      initial={{ opacity: 0, scale: 0.6 }}
      animate={{ opacity: 1, scale: 1 }}
      transition={{ duration: 0.6, repeat: Infinity, repeatType: "reverse" }}
      className="inline-block"
    >
      ✨
    </motion.span>
  );
}

function GameCard({ game, onPlay }) {
  return (
    <Card className="hover:shadow-xl transition-shadow duration-300 rounded-2xl">
      <CardHeader className="pb-2">
        <div className="flex items-center justify-between">
          <CardTitle className="text-lg flex items-center gap-2">
            <Gamepad2 className="w-5 h-5" /> {game.title}
          </CardTitle>
          <span className="text-xs px-2 py-1 rounded-full bg-primary/10 text-primary font-medium">{game.tag}</span>
        </div>
      </CardHeader>
      <CardContent className="space-y-3">
        <div className="h-28 w-full rounded-xl bg-gradient-to-br from-zinc-200 to-zinc-300 dark:from-zinc-800 dark:to-zinc-700 flex items-center justify-center">
          <motion.div
            initial={{ rotate: -8 }}
            animate={{ rotate: [ -8, 8, -8 ] }}
            transition={{ duration: 4, repeat: Infinity }}
            className="text-5xl"
          >
            🎮
          </motion.div>
        </div>
        <div className="grid grid-cols-3 gap-2 text-xs">
          <div className="p-2 rounded-lg bg-muted">RTP <b>{game.rtp}%</b></div>
          <div className="p-2 rounded-lg bg-muted">Vol: <b>{game.volatility}</b></div>
          <div className="p-2 rounded-lg bg-muted flex items-center gap-1"><Star className="w-3 h-3"/> {game.rating}</div>
        </div>
        <Button className="w-full" onClick={() => onPlay(game)}>
          Play Demo
        </Button>
      </CardContent>
    </Card>
  );
}

function DemoPlay({ game, onBack, onAddCredits }) {
  const [credits, setCredits] = useState(1000);
  const [bet, setBet] = useState(50);
  const [message, setMessage] = useState("Welcome! Press Spin to play.");
  const [spinning, setSpinning] = useState(false);
  const [progress, setProgress] = useState(0);

  function spin() {
    if (spinning) return;
    if (bet <= 0) return setMessage("Bet must be > 0");
    if (credits < bet) return setMessage("Not enough demo credits – claim bonus!");

    setSpinning(true);
    setCredits((c) => c - bet);
    setMessage("Spinning… Good luck!");

    const duration = 1200;
    const start = performance.now();
    function tick(now) {
      const pct = Math.min(100, ((now - start) / duration) * 100);
      setProgress(pct);
      if (pct < 100) requestAnimationFrame(tick);
    }
    requestAnimationFrame(tick);

    setTimeout(() => {
      const winChance = game.rtp / 100; // purely illustrative for demo
      const isWin = Math.random() < winChance * 0.4; // scaled down to feel natural
      const multiplier = isWin ? (1 + Math.round(Math.random() * 8)) : 0;
      const win = bet * multiplier;
      setCredits((c) => c + win);
      setSpinning(false);
      setProgress(0);
      setMessage(isWin ? `Nice! You won ${formatCredits(win)} demo credits` : "No luck this time – try again!");
    }, duration + 50);
  }

  return (
    <div className="space-y-4">
      <div className="flex items-center justify-between">
        <Button variant="ghost" onClick={onBack} className="flex items-center gap-2"><Menu className="w-4 h-4"/> Games</Button>
        <div className="flex items-center gap-3 text-sm">
          <div className="px-3 py-1 rounded-full bg-muted flex items-center gap-2"><Coins className="w-4 h-4"/> {formatCredits(credits)} credits</div>
          <Button size="sm" onClick={() => { setCredits((c) => c + 1000); onAddCredits?.(1000); }} className="flex items-center gap-2"><Gift className="w-4 h-4"/> Claim 1,000</Button>
        </div>
      </div>

      <Card className="rounded-2xl">
        <CardHeader>
          <CardTitle className="flex items-center gap-2"><Crown className="w-5 h-5"/> {game.title}</CardTitle>
        </CardHeader>
        <CardContent className="space-y-4">
          <div className="h-56 w-full rounded-2xl bg-gradient-to-br from-purple-200 to-indigo-200 dark:from-purple-900/40 dark:to-indigo-900/40 flex items-center justify-center">
            <motion.div
              initial={{ scale: 0.95 }}
              animate={{ scale: [0.95, 1.05, 0.95] }}
              transition={{ duration: 2.2, repeat: Infinity }}
              className="text-6xl"
            >
              🎰
            </motion.div>
          </div>

          <div className="grid grid-cols-1 sm:grid-cols-3 gap-3 items-end">
            <div className="space-y-2">
              <label className="text-sm">Demo Bet</label>
              <div className="flex gap-2">
                <Input type="number" value={bet} min={1} onChange={(e) => setBet(Math.max(1, Number(e.target.value)))} />
                <Button variant="secondary" onClick={() => setBet((b) => Math.max(1, Math.floor(b/2)))}>½</Button>
                <Button variant="secondary" onClick={() => setBet((b) => b * 2)}>2×</Button>
              </div>
            </div>
            <div className="space-y-2">
              <label className="text-sm">Volatility</label>
              <div className="text-xs p-2 rounded-lg bg-muted">{game.volatility}</div>
            </div>
            <div className="flex gap-3">
              <Button className="flex-1" onClick={spin} disabled={spinning}>Spin</Button>
              <Button className="flex-1" variant="outline" onClick={() => setMessage("Auto-Play is disabled in demo (responsible gaming)")}>Auto</Button>
            </div>
          </div>

          <div className="space-y-2">
            <label className="text-sm">Spin Progress</label>
            <Progress value={progress} />
          </div>

          <div className="text-sm p-3 rounded-xl bg-muted/60 flex items-center gap-2">
            <Info className="w-4 h-4"/> {message}
          </div>
        </CardContent>
      </Card>
    </div>
  );
}

export default function ArcadeNoGambling() {
  const [query, setQuery] = useState("");
  const [selectedGame, setSelectedGame] = useState(null);
  const [bonusBank, setBonusBank] = useState(0);

  const filtered = useMemo(() => {
    const q = query.toLowerCase();
    return mockGames.filter(g => g.title.toLowerCase().includes(q));
  }, [query]);

  useEffect(() => {
    // Dark mode hint for nicer neon feel (optional)
    document.documentElement.classList.add("dark");
  }, []);

  return (
    <div className="min-h-screen bg-gradient-to-b from-zinc-50 to-zinc-100 dark:from-zinc-900 dark:to-black text-zinc-900 dark:text-zinc-100">
      {/* Header */}
      <header className="sticky top-0 z-40 backdrop-blur supports-[backdrop-filter]:bg-white/50 dark:supports-[backdrop-filter]:bg-zinc-900/40 border-b">
        <div className="max-w-6xl mx-auto px-4 py-3 flex items-center justify-between">
          <div className="flex items-center gap-2 text-xl font-bold">
            <span className="rounded-xl px-2 py-1 bg-primary/10 text-primary">ARCADE</span>
            <span className="hidden sm:inline">Neo</span><Sparkle/>
          </div>
          <div className="flex items-center gap-2">
            <Input placeholder="Search games…" value={query} onChange={(e) => setQuery(e.target.value)} className="w-40 sm:w-64" />
            <Button variant="outline" className="flex items-center gap-2"><LogIn className="w-4 h-4"/> Sign In</Button>
          </div>
        </div>
      </header>

      {/* Hero */}
      <section className="max-w-6xl mx-auto px-4 py-10">
        <div className="grid md:grid-cols-2 gap-6 items-center">
          <div className="space-y-4">
            <h1 className="text-3xl sm:text-5xl font-extrabold leading-tight">
              Neon Arcade <span className="text-primary">Demo</span> —
              <br className="hidden sm:block"/> Play for Fun, No Real Money
            </h1>
            <p className="text-zinc-600 dark:text-zinc-300">
              Situs demo bertema kasino untuk portofolio & hiburan. Pakai <b>kredit fiktif</b>, tanpa deposit, tanpa cash‑out, dan dilengkapi <b>fitur gaming bertanggung jawab</b>.
            </p>
            <div className="flex flex-wrap gap-3">
              <Button className="flex items-center gap-2"><Gamepad2 className="w-4 h-4"/> Play Now</Button>
              <Button variant="secondary" className="flex items-center gap-2"><Trophy className="w-4 h-4"/> Leaderboard</Button>
            </div>
            <div className="text-xs text-zinc-500 flex items-center gap-2 pt-1">
              <Shield className="w-4 h-4"/> 18+, No real-money gambling. For demonstration only.
            </div>
          </div>
          <motion.div
            initial={{ opacity: 0, y: 10 }}
            animate={{ opacity: 1, y: 0 }}
            transition={{ duration: 0.6 }}
            className="rounded-3xl p-6 bg-gradient-to-br from-fuchsia-500/20 via-indigo-500/10 to-cyan-500/20 border"
          >
            <div className="grid grid-cols-3 gap-3">
              {mockGames.slice(0,6).map(g => (
                <div key={g.id} className="aspect-square rounded-2xl bg-zinc-200/60 dark:bg-zinc-800/60 flex items-center justify-center text-3xl">
                  🎲
                </div>
              ))}
            </div>
          </motion.div>
        </div>
      </section>

      {/* Main */}
      <main className="max-w-6xl mx-auto px-4 pb-16">
        <Tabs defaultValue="all" className="w-full">
          <TabsList className="grid grid-cols-3 sm:inline-flex">
            <TabsTrigger value="all">All Games</TabsTrigger>
            <TabsTrigger value="new">New</TabsTrigger>
            <TabsTrigger value="top">Top Rated</TabsTrigger>
          </TabsList>
          <TabsContent value="all" className="mt-6">
            {selectedGame ? (
              <DemoPlay game={selectedGame} onBack={() => setSelectedGame(null)} onAddCredits={(x) => setBonusBank(b => b + x)} />
            ) : (
              <div className="grid sm:grid-cols-2 lg:grid-cols-3 gap-4">
                {filtered.map(g => (
                  <GameCard key={g.id} game={g} onPlay={setSelectedGame} />
                ))}
              </div>
            )}
          </TabsContent>
          <TabsContent value="new" className="mt-6">
            <div className="grid sm:grid-cols-2 lg:grid-cols-3 gap-4">
              {mockGames.filter(g => g.tag === "New").map(g => (
                <GameCard key={g.id} game={g} onPlay={setSelectedGame} />
              ))}
            </div>
          </TabsContent>
          <TabsContent value="top" className="mt-6">
            <div className="grid sm:grid-cols-2 lg:grid-cols-3 gap-4">
              {mockGames.filter(g => g.rating >= 4.6).map(g => (
                <GameCard key={g.id} game={g} onPlay={setSelectedGame} />
              ))}
            </div>
          </TabsContent>
        </Tabs>
      </main>

      {/* Footer */}
      <footer className="border-t">
        <div className="max-w-6xl mx-auto px-4 py-10 grid md:grid-cols-4 gap-6 text-sm">
          <div className="space-y-2">
            <div className="font-semibold">Neo Arcade</div>
            <p className="text-zinc-500">Demo UI bertema kasino untuk hiburan & portofolio. Tidak mendukung perjudian uang asli.</p>
          </div>
          <div>
            <div className="font-semibold mb-2">Legal</div>
            <ul className="space-y-1 text-zinc-500">
              <li>Terms of Use (Demo)</li>
              <li>Privacy Policy</li>
              <li>Responsible Gaming</li>
            </ul>
          </div>
          <div>
            <div className="font-semibold mb-2">Community</div>
            <ul className="space-y-1 text-zinc-500">
              <li>Discord</li>
              <li>Twitter/X</li>
              <li>Reddit</li>
            </ul>
          </div>
          <div className="space-y-2">
            <div className="font-semibold">Demo Wallet</div>
            <div className="text-zinc-500">Bonus claimed: {formatCredits(bonusBank)} credits</div>
            <Button variant="outline" className="w-full">Download App</Button>
          </div>
        </div>
        <div className="text-center text-xs text-zinc-500 pb-8">© {new Date().getFullYear()} Neo Arcade — Demo Only</div>
      </footer>
    </div>
  );
}
