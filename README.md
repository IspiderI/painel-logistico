# 🚚 Painel Logístico - Gestão Inteligente de Cargas

> Sistema web moderno para gestão de cargas, controle financeiro e monitoramento de entregas logísticas.

## 🌐 Acesso Online

**Site publicado:** [https://ispideri.github.io/painel-logistico](https://ispideri.github.io/painel-logistico)

---

## ✨ Funcionalidades

### 📊 Dashboard Interativo
- **KPIs em Tempo Real**: Visualização de métricas principais
  - Total de cargas
  - Receita por tabela
  - Reduções aplicadas
  - Pagamentos a motoristas
  - Resultado operacional
  - Resultado geral

- **Gráficos Dinâmicos**: Evolução financeira com Chart.js
  - Análise temporal de receitas
  - Comparação de resultados
  - Visualização de tendências

### 📋 Planilha de Dados
- **Edição Inline**: Edite dados diretamente na tabela
- **Cálculos Automáticos**: 
  - Resultado Operacional = Tabela - Redução - Motorista
  - Resultado Geral = Tabela - Motorista
- **Gestão Completa**: Adicionar, editar e excluir registros

### 📥📤 Importação/Exportação
- **Importar CSV**: Suporta formato PT-BR e internacional
- **Exportar CSV**: Baixe seus dados com cálculos incluídos
- **Reconhecimento Automático**: Detecta colunas automaticamente

### 🔍 Filtros Avançados
- Filtrar por **Ano**
- Filtrar por **Mês**
- Filtrar por **Semana**
- Filtrar por **Data Específica**
- Combinação de múltiplos filtros

### 💾 Armazenamento Local
- **Auto-Save**: Salvamento automático ao editar
- **LocalStorage**: Dados salvos no navegador
- **Persistência**: Seus dados permanecem mesmo após fechar o navegador

---

## 🛠️ Tecnologias Utilizadas

- **HTML5**: Estrutura semântica moderna
- **CSS3**: Design responsivo com gradientes e animações
- **JavaScript (Vanilla)**: Lógica de negócio sem dependências
- **Chart.js**: Biblioteca para gráficos interativos
- **LocalStorage API**: Armazenamento de dados no navegador

---

## 🚀 Como Usar

### Opção 1: Usar Online (Recomendado)

Acesse diretamente: **[https://ispideri.github.io/painel-logistico](https://ispideri.github.io/painel-logistico)**

### Opção 2: Executar Localmente

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/IspiderI/painel-logistico.git
   cd painel-logistico
   ```

2. **Abra o arquivo:**
   - Basta abrir `index.html` no seu navegador
   - Ou use um servidor local:
     ```bash
     # Python 3
     python -m http.server 8000
     
     # Node.js
     npx serve
     ```

3. **Acesse:** `http://localhost:8000`

---

## 📚 Guia de Uso

### 1️⃣ Adicionar Dados

**Método 1 - Manualmente:**
1. Acesse a aba **"Planilha de Dados"**
2. Clique em **"➕ Adicionar Linha"**
3. Preencha os campos:
   - Data da entrega
   - Status (Pendente, Concluído, etc.)
   - Quantidade de itens
   - Rota (origem-destino)
   - Nome do motorista
   - Valor da tabela
   - Valor de redução/desconto
   - Valor pago ao motorista

**Método 2 - Importar CSV:**
1. Prepare um arquivo CSV com as colunas:
   ```
   Data,Status,Quantidade,Rota,Motorista,Vlr Tabela,Redução,Vlr Motorista
   ```
2. Clique em **"📤 Importar CSV"**
3. Selecione seu arquivo
4. Os dados serão importados automaticamente

### 2️⃣ Visualizar Dashboard

1. Acesse a aba **"📊 Dashboard"**
2. Visualize:
   - **Cards de KPI**: Métricas principais em destaque
   - **Gráfico de Linha**: Evolução financeira ao longo do tempo

### 3️⃣ Filtrar Dados

1. Use os filtros no topo da página:
   - Selecione **Ano**, **Mês** ou **Semana**
   - Ou escolha uma **Data Específica**
2. O dashboard e a tabela serão atualizados automaticamente
3. Clique em **"Limpar Filtros"** para resetar

### 4️⃣ Exportar Dados

1. Aplique os filtros desejados (opcional)
2. Clique em **"📥 Exportar"**
3. Um arquivo CSV será baixado com:
   - Todos os dados filtrados
   - Cálculos de resultado incluídos
   - Nome: `painel-logistico-AAAA-MM-DD.csv`

### 5️⃣ Gerenciar Dados

- **Editar**: Clique diretamente nos campos da tabela
- **Deletar**: Clique no ícone 🗑️ na linha desejada
- **Limpar Tudo**: Botão "🗑️ Limpar Tudo" (requer confirmação)
- **Recarregar**: Botão "🔄 Recarregar" atualiza a página

---

## 📊 Formato de Dados

### Estrutura do Registro

```javascript
{
  "id": 1234567890,           // ID único automático
  "data": "2026-03-04",       // Formato: AAAA-MM-DD
  "status": "Concluído",     // Texto livre
  "quantidade": 1,            // Número inteiro
  "rota": "São Paulo - Rio", // Texto livre
  "motorista": "João Silva", // Texto livre
  "valorTabela": 5000.00,     // Número decimal
  "reducao": 200.00,          // Número decimal
  "valorMotorista": 3500.00   // Número decimal
}
```

### Cálculos Automáticos

```javascript
// Resultado Operacional
resultadoOp = valorTabela - reducao - valorMotorista

// Resultado Geral  
resultadoGeral = valorTabela - valorMotorista
```

---

## 🎨 Design

### Características Visuais

- ✨ **Gradiente de fundo**: Roxo/Azul moderno
- 📱 **Responsivo**: Adapta-se a mobile, tablet e desktop
- 🎨 **Animações**: Transições suaves em hover
- 🌐 **Cards translucentes**: Efeito glassmorphism
- 📊 **Gráficos coloridos**: Paleta de cores harmoniosa

### Paleta de Cores

- **Primária**: `#3b82f6` (Azul)
- **Sucesso**: `#10b981` (Verde)
- **Perigo**: `#ef4444` (Vermelho)
- **Alerta**: `#f59e0b` (Âmbar)
- **Destaque**: `#6366f1` (Indigo)

---

## 🔒 Segurança e Privacidade

- ✅ **Armazenamento Local**: Dados salvos apenas no seu navegador
- ✅ **Sem Servidor**: Nenhum dado enviado para servidores externos
- ✅ **Offline-First**: Funciona sem internet após carregamento inicial
- ✅ **Sem Login**: Acesso direto sem cadastro

> **Nota**: Como os dados são salvos localmente, limpar cache/histórico do navegador apagará seus dados. Faça exportações regulares!

---

## ⚙️ Compatibilidade

### Navegadores Suportados

- ✅ Google Chrome (90+)
- ✅ Firefox (88+)
- ✅ Safari (14+)
- ✅ Edge (90+)
- ✅ Opera (76+)

### Dispositivos

- 💻 Desktop/Laptop
- 📱 Smartphones
- 📱 Tablets

---

## 📝 Changelog

### v1.0.0 - 04/03/2026

- ✨ Lançamento inicial
- 📊 Dashboard com KPIs e gráficos
- 📋 Planilha editável com cálculos automáticos
- 🔍 Sistema de filtros avançados
- 📥📤 Importação/Exportação CSV
- 💾 Armazenamento local automático
- 🔄 Botão de recarregar página
- 🎨 Design responsivo moderno

---

## 👤 Autor

**Idalecio Silva**  
📧 Email: [57044409+IspiderI@users.noreply.github.com](mailto:57044409+IspiderI@users.noreply.github.com)  
🐾 GitHub: [@IspiderI](https://github.com/IspiderI)  
🏭 Empresa: R&I Tech Store

---

## 📝 Licença

Este projeto está disponível publicamente. Sinta-se livre para usar, modificar e distribuir.

---

## 🤝 Contribuindo

Contribuições são bem-vindas! Para contribuir:

1. Faça um **Fork** do projeto
2. Crie uma **Branch** para sua feature (`git checkout -b feature/NovaFuncionalidade`)
3. **Commit** suas mudanças (`git commit -m 'Adiciona nova funcionalidade'`)
4. **Push** para a Branch (`git push origin feature/NovaFuncionalidade`)
5. Abra um **Pull Request**

---

## ❓ FAQ

### Como faço backup dos meus dados?
Clique em **"📥 Exportar"** para baixar um CSV com todos os seus dados.

### Posso usar em vários computadores?
Sim, mas os dados não sincronizam automaticamente. Use a função de exportar/importar para transferir dados.

### O site funciona offline?
Sim! Após o primeiro carregamento, funciona totalmente offline.

### Onde os dados são armazenados?
No LocalStorage do seu navegador, apenas no seu computador.

### Posso personalizar as colunas?
Atualmente não, mas esta funcionalidade pode ser adicionada em versões futuras.

---

## 🚀 Próximas Features (Roadmap)

- [ ] Modo escuro/claro
- [ ] Exportação em Excel
- [ ] Gráficos de pizza e barras
- [ ] Relatórios em PDF
- [ ] Integração com APIs externas
- [ ] Sistema de notificações
- [ ] Comparação de períodos
- [ ] Dashboard customizável

---

<div align="center">

**Desenvolvido com ❤️ por Idalecio Silva**

🌐 [Acesse o Site](https://ispideri.github.io/painel-logistico) | 🐛 [Reportar Bug](https://github.com/IspiderI/painel-logistico/issues) | ⭐ [Dar Estrela](https://github.com/IspiderI/painel-logistico)

</div>