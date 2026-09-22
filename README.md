# 🏫 Sistema de Cantina Escolar 360

**🔗 [Acessar o Sistema Online](https://melryandhieksy.github.io/Cantina-Escolar/)** 
Um sistema web moderno e responsivo criado para a gestão inteligente de refeiçõeescolares (Lanche da Manhã, Almoço e Lanche da Tarde). Desenvolvido para eliminar o desperdício de comida e evitar a duplicação de refeições, o projeto utiliza a geração e leitura de **QR Codes** com armazenamento na nuvem em tempo real através do **Google Sheets (Serverless)**.

---

## 🚀 Funcionalidades Principais

* **Geração de Tickets (QR Code):** Alunos e professores geram um QR Code único para cada refeição do dia. O sistema bloqueia automaticamente tentativas de gerar bilhetes duplicados para o mesmo turno.
* **Leitura Ultrarrápida:** Validador de câmara otimizado (acesso à câmara traseira a 30fps) para leitura instantânea na fila da cantina.
* **Prevenção de Fraudes:** Validação estrita que rejeita QR Codes de dias anteriores ou tentativas de usar tickets da equipa na fila dos alunos (e vice-versa).
* **Aprovação de Cadastros:** Fluxo de segurança onde novos utilizadores ficam retidos com o status "Pendente" até aprovação da diretoria.
* **Cardápio Dinâmico:** Atualização da ementa semanal diretamente pela interface do sistema com sincronização imediata na nuvem.
* **Monitorização em Tempo Real:** Painel administrativo com estatísticas diárias e mapa visual de consumo (Não Gerou, Na Fila, Entregue) filtrável por turma.

---

## 👥 Perfis de Acesso

O sistema adapta a interface e as permissões conforme o tipo de utilizador autenticado:

1. **👨‍🎓 Aluno:** Visualiza o cardápio e gera os seus QR Codes para as refeições.
2. **👩‍🏫 Equipa Escolar:** Professores, coordenadores e secretaria. Possuem filas e estatísticas de consumo separadas dos alunos.
3. **👨‍🍳 Cantina:** Realiza a leitura dos QR Codes, acompanha as métricas da fila de espera e edita o cardápio.
4. **👩‍💼 Diretoria:** Aprova cadastros pendentes, edita o cardápio e possui acesso total ao painel de auditoria.

---

## 🛠️ Tecnologias Utilizadas

Este projeto adota uma arquitetura **Serverless** (sem servidor tradicional de backend), focada em performance, baixo custo e facilidade de manutenção:

* **Frontend:** HTML5, CSS3, JavaScript (Vanilla).
* **Estilização:** [Tailwind CSS](https://tailwindcss.com/) para uma interface fluida e responsiva (Mobile-First).
* **Leitura e Geração de QR:** `qrcode.js` e `html5-qrcode`.
* **Ícones:** [Lucide Icons](https://lucide.dev/).
* **Backend / Base de Dados:** Google Apps Script integrado ao Google Sheets, atuando como uma API REST personalizada.
* **Hospedagem:** GitHub Pages.
