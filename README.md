# 💰 ERP Financeiro JW v3.0

Sistema completo de gestão financeira pessoal com **controle de dívidas**, navegação entre meses e interface profissional.

## 🆕 NOVIDADES DA VERSÃO 3.0

### ⚠️ **KPI DE DÍVIDAS** (PRINCIPAL NOVIDADE)
- **Dívida como tipo separado de lançamento**
- KPI destacado em vermelho com alerta visual
- Ícone pulsante para chamar atenção
- Mensagem motivacional: "⚠️ Priorize quitação"
- Toast especial ao registrar dívida

### 📊 **6 KPIs Financeiros**
1. 💵 Renda Total
2. 🏦 Poupança Total
3. 🔴 Despesas Essenciais
4. 🟢 Despesas Livres
5. 💳 **DÍVIDAS TOTAIS** ← NOVO!
6. 💎 Saldo a Distribuir

### 🏗️ **4 Colunas de Lançamentos**
- Receita
- Poupança
- Despesas (Essenciais/Livres)
- **Dívidas** ← NOVO!

---

## 📋 Características Principais

- ✅ **100% Offline** - Funciona sem internet
- ✅ **Controle de Dívidas** - KPI separado e destacado
- ✅ **Controle Mensal** - Organize suas finanças mês a mês
- ✅ **CRUD Completo** - Criar, Ler, Editar e Deletar
- ✅ **Navegação entre Meses** - Veja histórico completo
- ✅ **Toast Notifications** - Feedback visual elegante
- ✅ **Modal de Edição** - Interface moderna
- ✅ **Perfil Financeiro** - Configure seus percentuais
- ✅ **Gráficos Interativos** - Chart.js 4.4
- ✅ **Exportação PDF** - Imprima relatórios
- ✅ **Responsivo** - Funciona em qualquer dispositivo

---

## 🗂️ Estrutura de Arquivos

```
ERP-JW-version-3.0-main/
├── 📄 index.html              # Login/Cadastro
├── 📄 dashboard.html          # Dashboard principal (4 colunas)
├── 📄 perfil.html             # Perfil financeiro
├── 📄 historico.html          # Histórico de meses
├── 📄 charts.html             # Gráficos
├── 📄 style.css               # Estilos (com KPI de dívidas)
├── 📁 js/
│   └── 📄 dashboard.js        # Lógica completa
├── 📄 README.md               # Este arquivo
├── 📄 CHANGELOG.md            # Histórico de versões
├── 📄 .gitignore              # Config Git
└── 📄 LICENSE                 # MIT License
```

---

## 🚀 Como Usar

### 1. **Primeiro Acesso**
1. Abra `index.html` no navegador
2. Crie sua conta (senha com hash SHA-256)
3. Faça login

### 2. **Registrar Lançamentos**

#### 💵 Receitas
- Salário, rendas extras, reembolsos
- **Bancos**: Cartão, Itaú, Mercado Pago, Nubank, Clear

#### 🏦 Poupança
- Reservas, investimentos, aplicações
- **Bancos**: Itaú, Mercado Pago, Nubank, Clear

#### 💳 Despesas
- **Essenciais**: Alimentação, moradia, saúde, transporte...
- **Livres**: Lazer, viagens, vestuário, extras...
- **Bancos**: Cartão, Itaú, Mercado Pago, Nubank, Clear

#### ⚠️ **DÍVIDAS** (NOVO)
- Cartão de crédito, empréstimos, financiamentos
- **Categorias especializadas**:
  - Cartão de Crédito
  - Empréstimo Pessoal
  - Empréstimo Consignado
  - Financiamento de Veículo
  - Financiamento Imobiliário
  - Cheque Especial
  - Crédito Rotativo
  - Parcelamento de Compra
  - Empréstimo Familiar
  - Outros
- **Bancos**: Todos + BB, Caixa, Santander, Bradesco

---

## 📊 Como o KPI de Dívidas Funciona

### **Cálculo do Saldo**
```javascript
Saldo a Distribuir = Renda - Poupança - Despesas Essenciais - Despesas Livres - DÍVIDAS
```

### **Exemplo Prático**
```
💵 Renda Total:           R$ 5.000,00
🏦 Poupança:              R$   500,00
🔴 Despesas Essenciais:   R$ 2.000,00
🟢 Despesas Livres:       R$ 1.000,00
💳 DÍVIDAS:               R$   800,00 ← DESTAQUE VERMELHO
─────────────────────────────────────
💎 Saldo a Distribuir:    R$   700,00
```

### **Destaque Visual**
- ⚠️ Ícone pulsante no KPI
- Fundo vermelho degradê
- Borda vermelha destacada
- Mensagem: "⚠️ Priorize quitação"
- Toast especial ao registrar dívida

---

## 💾 Armazenamento de Dados

### LocalStorage Keys
```javascript
gf_erp_user          // Dados do usuário
gf_erp_logged        // Status de login
gf_erp_perfil        // Perfil financeiro
gf_erp_tx_2025-02    // Transações de fev/2025
```

### Estrutura de Lançamento com Dívida
```javascript
{
  id: "uuid",
  tipo: "divida",        // ← NOVO TIPO
  data: "2025-02-10",
  valor: "800.00",
  categoria: "Cartão de Crédito",
  banco: "Nubank",
  descricao: "Fatura parcelada 12x"
}
```

---

## 🎨 Categorias Disponíveis

### Dívidas (NOVO)
- Cartão de Crédito
- Empréstimo Pessoal
- Empréstimo Consignado
- Financiamento de Veículo
- Financiamento Imobiliário
- Cheque Especial
- Crédito Rotativo
- Parcelamento de Compra
- Empréstimo Familiar
- Outros

### Receitas
- Salário
- Renda Extra
- Reembolso
- Rendimentos
- Serviços

### Poupança
- Reserva
- Investimento
- Aplicação

### Despesas Essenciais
- ALIMENTAÇÃO ESSENCIAL
- ASSINATURAS ESSENCIAIS
- BEM-ESTAR ESSENCIAL
- COMUNICAÇÃO
- CUIDADO PESSOAL
- EDUCAÇÃO
- IMPOSTOS E TRIBUTOS
- SAÚDE
- TRANSPORTE
- MORADIA E SERVIÇOS ESSENCIAIS

### Despesas Livres
- LAZER E ENTRETENIMENTO
- ALIMENTAÇÃO FORA
- VESTUÁRIO
- VIAGENS E PASSEIOS
- MIMOS E EXTRAS

---

## 🔒 Segurança

- ✅ Senhas com hash SHA-256
- ✅ Validação de formulários
- ✅ Proteção contra XSS
- ✅ Dados privados (localStorage)

---

## 📱 Responsividade

- 🖥️ Desktop (1920px+)
- 💻 Laptop (1366px+)
- 📱 Tablet (768px+)
- 📱 Mobile (320px+)

---

## 🎯 Recursos Especiais

### 1. **Toast Notifications**
- Sucesso (verde)
- Erro (vermelho)
- Info (azul)
- Especial para dívidas (vermelho com ⚠️)

### 2. **Modal de Edição**
- Interface moderna
- Categorias dinâmicas
- Validações em tempo real

### 3. **Navegação de Meses**
- Botão "← Anterior"
- Botão "Mês Atual"
- Botão "Próximo →"
- Label do mês ativo

### 4. **Gráficos**
- Distribuição do orçamento (pizza)
- Receitas vs Despesas (barras)
- **Evolução de dívidas** (linha temporal)
- Top categorias de gastos

---

## 🛠️ Tecnologias

- HTML5
- CSS3 (Grid, Flexbox, Animações)
- JavaScript Vanilla (ES6+)
- Chart.js 4.4
- LocalStorage API
- Web Crypto API (SHA-256)

---

## 📄 Licença

MIT License - Código aberto e gratuito

---

## 🆚 Diferenças das Versões

| Feature | v2.0 | v3.0 |
|---------|------|------|
| KPI de Dívidas | ❌ | ✅ |
| 4 Colunas | ❌ | ✅ |
| Categorias de Dívida | ❌ | ✅ (10 tipos) |
| Toast Especial Dívida | ❌ | ✅ |
| Dívida no Cálculo | ❌ | ✅ |
| Design Responsivo | ✅ | ✅ Melhorado |
| CRUD Completo | ✅ | ✅ |
| Navegação de Meses | ✅ | ✅ |
| Gráficos | ✅ | ✅ |

---

## 👨‍💻 Desenvolvedor

**JW** - ERP Financeiro Pessoal v3.0

---

**Versão**: 3.0.0  
**Última atualização**: Fevereiro 2025  
**Status**: ✅ Produção
