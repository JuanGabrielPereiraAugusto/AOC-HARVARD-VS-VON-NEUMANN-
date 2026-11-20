# 🏛️ Arquitetura de Harvard × Arquitetura de von Neumann

Trabalho da disciplina de **Arquitetura e Organização de Computadores** na **Fatec Taquaritinga** comparando as duas arquiteturas clássicas de computadores e mostrando como elas aparecem nos processadores atuais.

📄 **Trabalho completo:** [`Harvard_vs_Von_Neumann.pdf`](Harvard_vs_Von_Neumann.pdf)

---

## 🧱 As duas arquiteturas

**Von Neumann (1945, EDVAC):** instruções e dados ficam na **mesma memória** e passam pelo **mesmo barramento**. É o conceito de **programa armazenado**.

**Harvard (1944, Harvard Mark I):** instruções e dados ficam em **memórias separadas**, cada uma com **seu próprio barramento**.

```
      VON NEUMANN                         HARVARD

   ┌─────────────┐              ┌───────────┐   ┌───────────┐
   │   Memória   │              │ Memória de│   │ Memória de│
   │ instruções  │              │ instruções│   │   dados   │
   │   + dados   │              └─────┬─────┘   └─────┬─────┘
   └──────┬──────┘                    │               │
          │ 1 barramento              │  2 barramentos│
   ┌──────┴──────┐              ┌─────┴───────────────┴─────┐
   │     CPU     │              │            CPU            │
   └─────────────┘              └───────────────────────────┘
```

---

## ⚖️ Comparação

| Critério | Von Neumann | Harvard |
|---|---|---|
| **Memória** | Única, para instruções e dados | Separada: instruções e dados |
| **Barramentos** | Um só | Independentes |
| **Acesso simultâneo** | ❌ Busca de instrução e de dado se alternam | ✅ Instrução e dado ao mesmo tempo |
| **Desempenho** | Limitado pelo **gargalo de von Neumann** | Maior vazão, favorece o pipeline |
| **Custo** | Hardware mais simples e barato | Hardware mais complexo e caro |
| **Flexibilidade** | Memória usada livremente | Divisão fixa entre programa e dados |
| **Uso típico** | Computadores de uso geral | Microcontroladores e DSPs |

---

## 🔀 Harvard modificada: o que se usa hoje

Os processadores de computadores e celulares **combinam as duas ideias**:
- **Para o programador**, a memória principal é **única**, como no modelo de von Neumann.
- **Dentro do processador**, o cache de primeiro nível (L1) é **dividido em cache de instruções e cache de dados**, como em Harvard.

Assim, juntam a **flexibilidade** de von Neumann com o **desempenho** de Harvard.

---

## 📚 Referências

- PATTERSON, D. A.; HENNESSY, J. L. **Organização e projeto de computadores**. 5. ed. Elsevier, 2017.
- STALLINGS, W. **Arquitetura e organização de computadores**. 10. ed. Pearson, 2017.
- TANENBAUM, A. S.; AUSTIN, T. **Organização estruturada de computadores**. 6. ed. Pearson, 2013.

---

## 🎓 Informações acadêmicas

| | |
|---|---|
| **Instituição** | Fatec Taquaritinga |
| **Curso** | Análise e Desenvolvimento de Sistemas — 1º semestre |
| **Disciplina** | Arquitetura e Organização de Computadores |
| **Ano** | 2025 |

## 👤 Autor

**Juan Gabriel Pereira Augusto**
GitHub: [@JuanGabrielPereiraAugusto](https://github.com/JuanGabrielPereiraAugusto)
