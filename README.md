```tsx
import type { Metadata } from "next";

export const metadata: Metadata = {
  title:       "Augusto Santos",
  description: "solo dev · brasil · do bug ao deploy",
};

type Projeto = { nome: string; sobre: string };

const projetos: readonly Projeto[] = [
  { nome: "Fragbase",   sobre: "saas de torneios de cs2 — o hub competitivo" },
  { nome: "Fraguard",   sobre: "anticheat em go + rust que não tira folga"   },
  { nome: "OrçaZap",    sobre: "do orçamento ao pix sem sair do zap"         },
  { nome: "Zer0 Autos", sobre: "curadoria de veículos selecionados à venda"  },
] as const;

const stack = {
  linguagens: ["TypeScript", "Go", "Rust"],
  frontend:   ["React", "Next.js", "Tailwind"],
  backend:    ["Node.js", "Go"],
  dados:      ["PostgreSQL", "Redis"],
  infra:      ["Docker", "Linux", "Git"],
} as const;

const contato = {
  github:    "https://github.com/SkzeR666",
  instagram: "https://instagram.com/augusto.santos696",
  email:     "mailto:augustowebdev0@gmail.com",
} as const;

export default function Augusto() {
  return (
    <main className="grind">
      <h1>Augusto Santos</h1>
      <p>solo dev · brasil · commita e reza</p>

      <section id="foco">
        {"// no momento: subindo a Fragbase, plataforma de torneios de CS2"}
      </section>

      <section id="projetos">
        {projetos.map(({ nome, sobre }) => (
          <article key={nome}>
            <strong>{nome}</strong> — {sobre}
          </article>
        ))}
      </section>

      <section id="stack">
        {Object.entries(stack).map(([area, techs]) => (
          <p key={area}>{area}: {techs.join(" · ")}</p>
        ))}
      </section>

      <footer>
        {Object.entries(contato).map(([rede, href]) => (
          <a key={rede} href={href}>{rede}</a>
        ))}
      </footer>
    </main>
  );
}
```

```ini
# .env
LOCATION=Brasil
ROLE=solo_dev
STATUS=shipping
TZ=America/Sao_Paulo
DEPLOY_TARGET=vercel
COFFEE_LEVEL=over9000
SLEEP=optional
CATS=true
CURRENT_BOSS=prazo
UPTIME=99.9%
DEBUG=false         
FAVORITE_BUG=works_on_my_machine
NEXT_PUBLIC_VIBE=cinematic
```
