export default function FrutCavLanding() {
  return (
    <div className="min-h-screen bg-white text-slate-900">
      {/* Header */}
      <header className="sticky top-0 z-50 bg-white/80 backdrop-blur border-b">
        <div className="mx-auto max-w-6xl px-4 py-3 flex items-center justify-between">
          <a href="#top" className="flex items-center gap-2 group">
            <div className="h-9 w-9 rounded-full bg-red-600 grid place-items-center text-white font-black">FC</div>
            <div className="leading-tight">
              <p className="font-bold tracking-tight">FrutCav</p>
              <p className="text-xs text-slate-500 -mt-0.5">Packing House • SC</p>
            </div>
          </a>
          <nav className="hidden md:flex gap-6 text-sm">
            <a href="#servicos" className="hover:text-red-600">Serviços</a>
            <a href="#produtos" className="hover:text-red-600">Produtos</a>
            <a href="#sobre" className="hover:text-red-600">Sobre</a>
            <a href="#contato" className="hover:text-red-600">Contato</a>
          </nav>
          <a
            href="https://wa.me/5500000000000?text=Olá%20FrutCav!%20Quero%20falar%20sobre%20maçãs."
            className="inline-flex items-center rounded-2xl border border-red-600 px-4 py-2 text-sm font-medium text-red-700 hover:bg-red-50"
          >WhatsApp</a>
        </div>
      </header>

      {/* Hero */}
      <section id="top" className="relative overflow-hidden">
        <div className="absolute inset-0 -z-10 bg-gradient-to-b from-red-50 via-white to-white" />
        <div className="mx-auto max-w-6xl px-4 py-16 md:py-24 grid md:grid-cols-2 gap-10 items-center">
          <div>
            <h1 className="text-4xl md:text-6xl font-extrabold tracking-tight leading-tight">
              Maçãs selecionadas, <span className="text-red-600">padrão FrutCav</span>
            </h1>
            <p className="mt-4 text-slate-600 md:text-lg">
              Operamos em Santa Catarina com classificação Sienz, processos de qualidade e logística ágil para atender varejo, atacado e exportadores.
            </p>
            <div className="mt-6 flex gap-3">
              <a
                href="#contato"
                className="rounded-2xl bg-red-600 px-5 py-3 text-white font-semibold shadow hover:shadow-md"
              >Solicitar cotação</a>
              <a
                href="#servicos"
                className="rounded-2xl px-5 py-3 border font-semibold hover:bg-slate-50"
              >Ver serviços</a>
            </div>
            <div className="mt-8 grid grid-cols-3 gap-4 text-center">
              {[
                {k: "+10 mil", v: "bins/ano"},
                {k: "18 kg", v: "padrão caixa"},
                {k: "SC", v: "São Joaquim • Fraiburgo"},
              ].map((item, i) => (
                <div key={i} className="rounded-2xl border p-4">
                  <p className="text-xl font-extrabold">{item.k}</p>
                  <p className="text-xs text-slate-500">{item.v}</p>
                </div>
              ))}
            </div>
          </div>
          <div className="relative">
            <div className="aspect-square rounded-3xl border shadow-sm bg-white p-6">
              <div className="h-full w-full rounded-2xl bg-gradient-to-br from-red-500/10 to-emerald-500/10 grid place-items-center">
                <div className="text-center">
                  <div className="mx-auto h-28 w-28 rounded-full bg-red-600/90 grid place-items-center text-white text-3xl font-black">🍎</div>
                  <p className="mt-4 text-sm text-slate-500">Espaço para sua foto/logo</p>
                </div>
              </div>
            </div>
            <div className="absolute -bottom-4 -left-4 bg-white rounded-2xl border shadow p-3">
              <p className="text-xs text-slate-500">Certificação e rastreabilidade</p>
            </div>
          </div>
        </div>
      </section>

      {/* Serviços */}
      <section id="servicos" className="mx-auto max-w-6xl px-4 py-16">
        <h2 className="text-2xl md:text-3xl font-bold tracking-tight">Serviços</h2>
        <p className="mt-2 text-slate-600">Do campo ao cliente com eficiência e padronização.</p>
        <div className="mt-8 grid md:grid-cols-3 gap-6">
          {[
            {
              title: "Classificação & Embalagem",
              desc: "Linha Sienz, calibres consistentes, montagem de caixa 18 kg e private label.",
            },
            {
              title: "Armazenagem & Tratamentos",
              desc: "Câmara fria, MCP e Atmosfera Controlada (parceiros) para maior vida de prateleira.",
            },
            {
              title: "Logística & Expedição",
              desc: "Paletização, romaneio, carregamento rápido e documentação para CEASAs e clientes.",
            },
          ].map((c, i) => (
            <div key={i} className="rounded-2xl border p-6 hover:shadow-sm transition">
              <h3 className="font-semibold text-lg">{c.title}</h3>
              <p className="mt-2 text-sm text-slate-600">{c.desc}</p>
            </div>
          ))}
        </div>
      </section>

      {/* Produtos */}
      <section id="produtos" className="mx-auto max-w-6xl px-4 py-16">
        <h2 className="text-2xl md:text-3xl font-bold tracking-tight">Produtos</h2>
        <p className="mt-2 text-slate-600">Maçãs, pêssegos e ameixas selecionados.</p>
        <div className="mt-8 grid md:grid-cols-3 gap-6">
          {[
            {nome: "Maçã Gala/Fuji", nota: "Cat. 1 • calibres 100–140"},
            {nome: "Pêssego", nota: "Safra verão • seleção premium"},
            {nome: "Ameixa", nota: "Padronização e aparência"},
          ].map((p, i) => (
            <div key={i} className="rounded-2xl border p-6">
              <div className="aspect-video rounded-xl bg-slate-100 grid place-items-center text-3xl">📦</div>
              <h3 className="mt-4 font-semibold">{p.nome}</h3>
              <p className="text-sm text-slate-600">{p.nota}</p>
            </div>
          ))}
        </div>
      </section>

      {/* Sobre */}
      <section id="sobre" className="mx-auto max-w-6xl px-4 py-16">
        <div className="grid md:grid-cols-2 gap-10 items-center">
          <div>
            <h2 className="text-2xl md:text-3xl font-bold tracking-tight">Sobre a FrutCav</h2>
            <p className="mt-3 text-slate-600">
              Marca catarinense com foco em qualidade, padronização e relacionamento de confiança
              com produtores e compradores. Operamos com indicadores de custo por caixa, metas de margem e
              transparência nas negociações.
            </p>
            <ul className="mt-4 text-slate-700 text-sm space-y-2 list-disc list-inside">
              <li>Processos auditáveis e rastreáveis</li>
              <li>Parcerias com produtores de São Joaquim e Fraiburgo</li>
              <li>Atendimento a CEASAs e redes regionais</li>
            </ul>
          </div>
          <div className="rounded-3xl border p-6">
            <div className="grid grid-cols-2 gap-4 text-sm">
              {[
                {k: "Classificadora", v: "Sienz"},
                {k: "Caixa padrão", v: "18 kg"},
                {k: "Volume atual", v: "+10.000 bins/ano"},
                {k: "Indústria", v: "6–15% (média)"},
              ].map((i, idx) => (
                <div key={idx} className="rounded-xl border p-4">
                  <p className="text-xs text-slate-500">{i.k}</p>
                  <p className="font-semibold">{i.v}</p>
                </div>
              ))}
            </div>
          </div>
        </div>
      </section>

      {/* CTA */}
      <section className="mx-auto max-w-6xl px-4 py-16">
        <div className="rounded-3xl border p-8 md:p-12 bg-gradient-to-br from-red-600 to-red-500 text-white">
          <h3 className="text-2xl md:text-3xl font-extrabold tracking-tight">Vamos fazer negócio?</h3>
          <p className="mt-2 text-white/90 max-w-2xl">
            Envie uma mensagem agora e receba lista de calibres, disponibilidade e valores atualizados.
          </p>
          <div className="mt-6 flex flex-wrap gap-3">
            <a
              href="https://wa.me/5500000000000?text=Olá%20FrutCav!%20Quero%20cotação%20de%20maçãs."
              className="rounded-2xl bg-white text-red-600 px-5 py-3 font-semibold hover:bg-white/90"
            >Falar no WhatsApp</a>
            <a href="#contato" className="rounded-2xl border border-white/30 px-5 py-3 font-semibold hover:bg-white/10">Formulário</a>
          </div>
        </div>
      </section>

      {/* Contato */}
      <section id="contato" className="mx-auto max-w-6xl px-4 py-16">
        <h2 className="text-2xl md:text-3xl font-bold tracking-tight">Contato</h2>
        <p className="mt-2 text-slate-600">Preencha e retornamos rapidamente.</p>
        <form className="mt-8 grid md:grid-cols-2 gap-4">
          <input className="rounded-xl border p-3" placeholder="Nome" />
          <input className="rounded-xl border p-3" placeholder="Telefone/WhatsApp" />
          <input className="rounded-xl border p-3 md:col-span-2" placeholder="E-mail (opcional)" />
          <textarea className="rounded-xl border p-3 md:col-span-2" placeholder="Mensagem"></textarea>
          <button type="button" className="rounded-2xl bg-red-600 text-white px-5 py-3 font-semibold w-fit">Enviar</button>
        </form>
      </section>

      {/* Footer */}
      <footer className="border-t">
        <div className="mx-auto max-w-6xl px-4 py-8 text-sm text-slate-600 flex flex-col md:flex-row items-center justify-between gap-4">
          <p>© {new Date().getFullYear()} FrutCav • Santa Catarina, Brasil</p>
          <div className="flex gap-4">
            <a href="#top" className="hover:text-red-600">Voltar ao topo</a>
            <a href="#" className="hover:text-red-600">Política de Privacidade</a>
          </div>
        </div>
      </footer>
    </div>
  );
}
