<div align="center">
  <img src="https://media.giphy.com/media/sIIhZliB2McAo/giphy.gif" width="400" alt="cat" />
</div>

---

```tsx
import type { Metadata } from "next";

export const metadata: Metadata = {
  title:       "Augusto Santos",
  description: "solo dev · brasil",
};

const projetos = [
  { nome: "Fragbase",   sobre: "plataforma de torneios de cs2",               href: "github.com/SkzeR666/fragbase"   },
  { nome: "Fraguard",   sobre: "anticheat em go e rust",                      href: "github.com/SkzeR666/fraguard"   },
  { nome: "OrçaZap",    sobre: "orçamento direto no pix",                     href: "github.com/SkzeR666/orcazap"    },
  { nome: "Zer0 Autos", sobre: "curadoria de veículos selecionados à venda", href: "github.com/SkzeR666/Zer0-Autos" },
] as const;

const stack = {
  linguagens: ["TypeScript", "Go", "Rust"],
  frontend:   ["React", "Next.js", "Tailwind"],
  backend:    ["Node.js", "Go"],
  dados:      ["PostgreSQL", "Redis"],
  infra:      ["Docker", "Linux", "Git"],
} as const;

const contato = {
  github:    "github.com/SkzeR666",
  email:     "augustowebdev0@gmail.com",
  instagram: "instagram.com/augusto.santos696",
} as const;

export default function Augusto() {
  return (
    <main>
      <h1>Augusto Santos</h1>
      <p>solo dev · brasil · ADS (UNITAU)</p>

      <section id="foco">
        Fragbase — plataforma de torneios de CS2
      </section>

      <section id="projetos">
        {projetos.map(({ nome, sobre, href }) => (
          <a key={nome} href={`https://${href}`}>
            <strong>{nome}</strong> — {sobre}
          </a>
        ))}
      </section>

      <section id="stack">
        {Object.entries(stack).map(([area, techs]) => (
          <p key={area}>{area}: {techs.join(", ")}</p>
        ))}
      </section>

      <footer>
        {Object.entries(contato).map(([rede, url]) => (
          <a key={rede} href={`https://${url}`}>{rede}</a>
        ))}
      </footer>
    </main>
  );
}
```
