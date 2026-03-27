# ServiceNow Editors Suite - IBM

Uma suíte completa de editores HTML para ServiceNow Knowledge Base, com design profissional IBM Carbon Dark e funcionalidades avançadas.

## 🎯 O Problema que Resolve

Quando você cola HTML personalizado no editor de código-fonte do ServiceNow e salva:
- O ServiceNow envolve texto em `<span>` tags excessivas com estilos inline
- Remove blocos `<style>`
- Quebra a estrutura HTML original
- Torna praticamente impossível editar conteúdo como texto plano depois

## ✨ A Solução

Esta ferramenta fornece **dois editores especializados** em uma interface unificada:

### 🏠 Home Screen
- Tela inicial elegante com seleção de editor
- Design IBM Carbon Dark consistente
- Navegação simples entre ferramentas

### 📝 General Editor
Editor universal para qualquer KB article do ServiceNow:
1. **IMPORT** → Cole HTML "sujo" do ServiceNow
2. **EDIT** → Edite visualmente como um documento normal
3. **EXPORT** → Obtenha HTML limpo pronto para colar de volta

### 🖥️ 1756 Procedures Editor
Editor especializado para procedimentos operacionais IBM Mainframe (1756):
- Gerenciamento completo de procedures
- Upload de imagens (paste/drag/select)
- Compressão automática de imagens
- Import/Export com estrutura HTML completa
- Categorização automática por message code

## 🚀 Quick Start

### Option 1: Use Online (Recomendado)
Acesse a ferramenta online: **[Sua URL do GitHub Pages]**

### Option 2: Use Localmente
1. Baixe `editors_carbon.html`
2. Abra em qualquer navegador moderno
3. Comece a editar!

**Sem instalação, sem dependências, funciona offline!**

## 📖 Como Usar

### General Editor

#### Passo 1: Import HTML do ServiceNow
1. Abra seu KB article no ServiceNow
2. Clique no botão **Source Code** (`<>`)
3. Selecione todo HTML (Ctrl+A / Cmd+A)
4. Copie (Ctrl+C / Cmd+C)
5. Na ferramenta, clique **"Paste from Clipboard"** ou cole no textarea
6. Clique **"Clean & Import"**

#### Passo 2: Edite Visualmente
- Clique em qualquer lugar no documento para editar texto
- Selecione texto para ver a floating toolbar
- Use a toolbar para:
  - **Negrito**, *Itálico*, <u>Sublinhado</u>, ~~Tachado~~
  - Mudar para Heading 1, 2, 3, ou Parágrafo
  - Criar listas ordenadas ou não ordenadas
  - Inserir links
  - Limpar formatação

#### Passo 3: Export de Volta ao ServiceNow
1. Clique **"Export HTML"**
2. Clique **"Copy to Clipboard"**
3. Retorne ao ServiceNow
4. Clique **Source Code** (`<>`)
5. Selecione tudo (Ctrl+A / Cmd+A)
6. Cole (Ctrl+V / Cmd+V)
7. Salve seu article

### 1756 Procedures Editor

#### Passo 1: Import Procedures Existentes (Opcional)
1. Clique **"Import HTML"**
2. Cole o HTML completo do arquivo 1756
3. Procedures aparecerão na sidebar

#### Passo 2: Adicionar Nova Procedure
1. Clique **"Add Procedure"**
2. Preencha os campos obrigatórios:
   - **Message Code** (ex: DFHAP0001I)
   - **Description**
3. Preencha campos opcionais:
   - System, Priority, Support Group
   - Notes
   - Operations Action
4. **Adicione imagens** (3 métodos):
   - **Método 1**: Cole (Ctrl+V) no campo Operations Action
   - **Método 2**: Arraste imagens para a área de upload
   - **Método 3**: Clique na área de upload e selecione arquivo
5. Use a toolbar de formatação:
   - **B** (Bold)
   - **Exception Box** (caixa amarela de exceção)
   - **Note Box** (caixa azul de nota)
   - **Code** (código inline)
   - **Link** (inserir link)
6. Clique **"Create Procedure"**

#### Passo 3: Editar/Deletar Procedures
- Clique em qualquer procedure na sidebar para editar
- Use a barra de busca para filtrar procedures
- Clique **"Delete"** para remover procedure

#### Passo 4: Export para ServiceNow
1. Clique **"Export HTML"**
2. HTML completo copiado automaticamente para clipboard
3. Cole no ServiceNow Knowledge Base article

## 🖼️ Sistema de Imagens

### General Editor
**Importante:** Imagens do ServiceNow usam URLs internas como `/sys_attachment.do?sys_id=...`

- No editor, imagens aparecem como **placeholders** (padrão xadrez)
- Isso é normal! O HTML da imagem é preservado perfeitamente
- Quando colar de volta no ServiceNow, **imagens exibirão corretamente**
- A ferramenta preserva todos atributos, alt text e classes

### 1756 Procedures Editor
**Sistema Avançado de Upload com Compressão Automática:**

#### 3 Métodos de Upload:
1. **Paste (Ctrl+V)** - Cole imagens diretamente no textarea
2. **Drag & Drop** - Arraste imagens do computador
3. **File Select** - Clique na área de upload e selecione

#### Compressão Automática Inteligente:
- **Threshold**: Imagens > 200 KB são comprimidas automaticamente
- **Redimensionamento**: Mantém proporção, máximo 1200px
- **Qualidade**: 85% para JPEG, 100% para PNG
- **Resultado**: Redução de 80-90% no tamanho do arquivo
- **Notificações**: Mostra estatísticas de compressão
  - Exemplo: "Image compressed: 2.5 MB → 180 KB (93% smaller) ✓"

#### Formatos Suportados:
- PNG (com transparência)
- JPEG/JPG
- GIF
- WebP

#### Conversão Base64:
- Imagens são convertidas para base64
- Embutidas diretamente no HTML
- Não precisam de hosting externo
- Funcionam imediatamente no ServiceNow

## ✨ Funcionalidades Completas

### General Editor

#### Limpeza HTML
- ✅ Remove comentários XML namespace
- ✅ Remove classes Microsoft Office (`MsoNormal`, etc.)
- ✅ Remove atributos `data-*` desnecessários
- ✅ Remove estilos inline `mso-*`
- ✅ Colapsa spans vazios aninhados
- ✅ Decodifica entidades HTML
- ✅ **Preserva** toda estrutura HTML significativa
- ✅ **Preserva** imagens, tabelas, listas, links
- ✅ **Preserva** estilos inline necessários para ServiceNow

#### Edição Visual
- 📝 Interface ContentEditable (edite como documento)
- 🎨 Floating toolbar ao selecionar texto
- ⌨️ Atalhos de teclado (Ctrl+B, Ctrl+I, Ctrl+U)
- 🎯 Formate como headings, parágrafos, listas
- 🔗 Insira e edite links
- 🧹 Opção de limpar formatação

#### Experiência do Usuário
- 📋 Paste/copy de clipboard com um clique
- 📊 Contagem de caracteres e tags
- 📈 Estatísticas antes/depois
- 👁️ Modo preview no export
- 🔔 Notificações de sucesso/erro
- ⚠️ Avisos de mudanças não salvas

### 1756 Procedures Editor

#### Gerenciamento de Procedures
- 📋 Sidebar com lista completa
- 🔍 Busca/filtro em tempo real
- ✏️ Click para editar
- 🗑️ Delete com confirmação
- 📊 Contador de procedures
- 🏷️ Categorização automática por message code

#### Formulário de Edição
- ✅ Campos obrigatórios: Message Code, Description
- 📝 Campos opcionais: System, Priority, Support Group, Notes
- 📄 Operations Action (textarea com formatação)
- 🎨 Toolbar de formatação especializada
- ✅ Validação de campos

#### Upload e Compressão de Imagens
- 📎 3 métodos: Paste, Drag & Drop, File Select
- 🗜️ Compressão automática (> 200 KB)
- 📏 Redimensionamento inteligente (max 1200px)
- 📊 Estatísticas de compressão em tempo real
- 🎯 Qualidade otimizada (85% JPEG, 100% PNG)
- ⚡ Processamento rápido (100-300ms)

#### Formatação Especializada
- **Bold**: `<strong></strong>`
- **Exception Box**: Caixa amarela para exceções
- **Note Box**: Caixa azul para notas
- **Code**: `<code></code>`
- **Link**: `<a href=""></a>`

#### Import/Export
- 📥 Import de HTML existente (arquivo V6)
- 📤 Export completo com CSS embutido
- 🎯 Inclui header, instruções, workflow steps
- 📁 Todas procedures organizadas por categoria
- 📋 Cópia automática para clipboard

#### Auto-conversão
- Line breaks (`\n`) → `<br/>` automaticamente
- Apenas se não houver HTML já formatado
- Preserva formatação manual

### Seções "How to Use"
- 📖 Expandíveis/colapsáveis
- 📝 Passo a passo numerado
- 💡 Tips & best practices
- 🎨 Integradas ao design Carbon Dark
- 🔍 Sempre disponíveis, nunca intrusivas

## 🎨 IBM Carbon Design System

### Tema Dark Aplicado
```
Background principal:  #161616 (Gray 100)
Superfícies:          #262626, #393939, #525252 (Gray scale)
Texto primário:       #f4f4f4
Texto secundário:     #c6c6c6
Links:                #78a9ff (Blue 40)
Botões primários:     #4589ff (Blue 60)
Success:              #42be65 (Green 60)
Error:                #fa4d56 (Red 50)
Warning:              #f1c21b (Yellow)
```

### Tipografia
- **Fonte primária**: IBM Plex Sans
- **Fonte monospace**: IBM Plex Mono
- Carregadas via Google Fonts CDN
- Renderização otimizada para legibilidade

### Espaçamentos
- Baseado no sistema de spacing do Carbon
- Transições: 110ms (padrão Carbon)
- Bordas sem border-radius (estilo Carbon)
- Grid system responsivo

## 🛠️ Detalhes Técnicos

### Construído Com
- **React 18** - Framework UI com hooks
- **Tailwind CSS** - Estilização (configurado com tokens Carbon)
- **Lucide Icons** - Biblioteca de ícones
- **IBM Plex Fonts** - Tipografia oficial IBM
- **Canvas API** - Compressão de imagens client-side
- **Vanilla JavaScript** - Sem processo de build necessário

### Requisitos do Navegador
- Navegador moderno (Chrome, Firefox, Edge, Safari)
- JavaScript habilitado
- Clipboard API support (para recursos paste/copy)
- Canvas API support (para compressão de imagens)

### Privacidade & Segurança
- ✅ Roda inteiramente no navegador
- ✅ Nenhum dado enviado para servidor
- ✅ Sem tracking ou analytics
- ✅ Funciona completamente offline
- ✅ Seguro para conteúdo sensível
- ✅ Processamento de imagens 100% client-side

### Arquitetura
- **Arquivo único**: `editors_carbon.html` (72 KB)
- **CDNs utilizados**:
  - React 18 (unpkg.com)
  - Babel Standalone (unpkg.com)
  - Tailwind CSS (cdn.tailwindcss.com)
  - Lucide Icons (unpkg.com)
  - IBM Plex Fonts (Google Fonts)
- **Componentes React**:
  - App (navegação principal)
  - HomeScreen
  - GeneralEditor
  - Editor1756
  - ProcedureForm
  - Notification

## 📁 Arquivos no Repositório

- **editors_carbon.html** - Ferramenta completa integrada (PRINCIPAL)
- **README.md** - Esta documentação
- **EDITORS_CARBON_README.md** - Documentação técnica detalhada
- **CHANGELOG_v1.1.md** - Histórico de versões
- **index.html** - General Editor original (backup)
- **1756_FINAL_OPTIMIZED_V6_FINAL.html** - Arquivo de procedures otimizado

## 📊 Comparação de Versões

| Arquivo | Tamanho | Editores | Tema | Imagens | Compressão |
|---------|---------|----------|------|---------|------------|
| `index.html` | 25 KB | General | Light | ❌ | ❌ |
| `1756_editor_v2.html` | 15 KB | 1756 | Misto | ✅ | ❌ |
| `editors_integrated.html` | 40 KB | Home + Ambos | Misto | ✅ | ❌ |
| **`editors_carbon.html`** | **72 KB** | **Home + Ambos** | **IBM Carbon Dark** | **✅** | **✅** |

## 💡 Tips & Tricks

### Atalhos de Teclado no General Editor
- `Ctrl+B` / `Cmd+B` - Negrito
- `Ctrl+I` / `Cmd+I` - Itálico
- `Ctrl+U` / `Cmd+U` - Sublinhado
- `Ctrl+Z` / `Cmd+Z` - Desfazer
- `Ctrl+Y` / `Cmd+Y` - Refazer

### Atalhos no 1756 Editor
- `Ctrl+V` - Colar imagem no Operations Action
- `Ctrl+S` - Salvar procedure (quando implementado)

### Melhores Práticas

#### General Editor
1. Sempre use "Clean & Import" antes de editar
2. Faça todas edições em uma sessão
3. Use o preview antes de exportar
4. Mantenha backup do HTML original (por precaução)
5. Teste no ServiceNow após colar

#### 1756 Editor
1. Comece importando HTML existente (se houver)
2. Use busca para encontrar procedures rapidamente
3. Cole imagens grandes - deixe a compressão automática trabalhar
4. Revise estatísticas de compressão para otimizar
5. Use exception/note boxes para destacar informações importantes
6. Teste line breaks antes de adicionar `<br/>` manualmente

### Otimização de Imagens
- **Imagens > 200 KB**: Comprimidas automaticamente
- **Imagens < 200 KB**: Mantidas sem alteração
- **Dica**: Para screenshots, PNG é melhor para textos nítidos
- **Dica**: Para fotos, JPEG comprime mais eficientemente
- **Resultado esperado**:
  - Foto de celular (2-3 MB) → ~150-200 KB (90% menor)
  - Screenshot grande (800 KB) → ~80-100 KB (87% menor)
  - Ícone pequeno (50 KB) → Sem compressão (mantido original)

### Troubleshooting

**Q: Imagens não aparecem no General Editor**
A: Normal! Imagens do ServiceNow só funcionam dentro do ServiceNow. Funcionarão quando colar de volta.

**Q: Formatação parece diferente do ServiceNow**
A: O editor usa fontes web padrão. A estrutura HTML é preservada e renderizará corretamente no ServiceNow.

**Q: Posso editar tabelas?**
A: Sim! Tabelas são totalmente preservadas. Você pode editar texto dentro das células.

**Q: E quanto a CSS customizado?**
A: Estilos inline são preservados. Stylesheets externos não aplicam no editor mas funcionarão no ServiceNow.

**Q: A compressão de imagem degrada qualidade?**
A: Muito pouco. Com 85% de qualidade JPEG, a diferença visual é imperceptível mas o tamanho reduz drasticamente.

**Q: Posso desabilitar a compressão?**
A: Atualmente não há toggle. Imagens < 200 KB não são comprimidas. Para manter original, use imagens menores.

**Q: Quantas procedures posso adicionar?**
A: Teoricamente ilimitado. O arquivo V6 original tem 1,637 procedures (1.35 MB) e funciona perfeitamente.

## 🎓 Workflows de Exemplo

### General Editor Workflow
```
ServiceNow Article (HTML bagunçado)
         ↓
    [IMPORT & CLEAN]
         ↓
   Visual Editor (edite como documento)
         ↓
    [EXPORT CLEAN HTML]
         ↓
ServiceNow Article (HTML limpo)
```

### 1756 Editor Workflow
```
Arquivo HTML existente (opcional)
         ↓
    [IMPORT HTML]
         ↓
  Lista de Procedures na Sidebar
         ↓
  [EDIT] ou [ADD NEW] ou [DELETE]
         ↓
  Upload de Imagens (paste/drag/select)
         ↓
  Compressão Automática
         ↓
    [EXPORT HTML COMPLETO]
         ↓
ServiceNow KB Article (HTML + CSS + Imagens)
```

## 🌟 Por que Usar Esta Ferramenta?

### Benefícios Gerais
- **Economize Tempo** - Edite visualmente ao invés de lutar com tags HTML
- **Código Mais Limpo** - Remove markup lixo auto-gerado do ServiceNow
- **Melhor Workflow** - Edit → Export → Paste → Concluído
- **Sem Instalação** - Apenas abra e use
- **Offline Capable** - Funciona sem internet
- **Grátis & Open** - Sem custo, sem registro

### Específico para 1756 Procedures
- **Gerenciamento Centralizado** - Todas procedures em um lugar
- **Compressão Automática** - Imagens otimizadas sem esforço
- **Categorização Automática** - Organiza procedures por message code
- **Formatação Especializada** - Exception/Note boxes prontas
- **Import/Export Completo** - Migre procedures facilmente

### Design Profissional
- **IBM Carbon Dark Theme** - Visual consistente e profissional
- **Experiência Polida** - Notificações, animações, transições suaves
- **Responsivo** - Funciona em desktop, tablet, mobile
- **Acessível** - Seções "How to Use" sempre disponíveis

## 🚀 Deploy no GitHub Pages

### Passo a Passo
1. Crie repositório no GitHub
2. Faça upload de `editors_carbon.html`
3. Vá em Settings → Pages
4. Source: Deploy from a branch
5. Branch: `main` / Folder: `/ (root)`
6. Save
7. Acesse: `https://[username].github.io/[repo-name]/editors_carbon.html`

### Configuração Opcional
- Renomeie `editors_carbon.html` para `index.html` para URL mais limpa
- Adicione `CNAME` para custom domain
- Configure `README.md` na raiz para documentação

## 📞 Suporte

Se encontrar problemas ou tiver questões:
1. Verifique seção de troubleshooting acima
2. Revise `EDITORS_CARBON_README.md` para detalhes técnicos
3. Revise `CHANGELOG_v1.1.md` para mudanças recentes
4. Abra uma issue neste repositório

## 🤝 Contribuindo

Encontrou um bug ou tem uma sugestão? Por favor abra uma issue!

Ideias para contribuições:
- Toggle Dark/Light theme
- Atalhos de teclado customizáveis
- Drag & drop para reordenar procedures
- Templates de procedures
- Export para JSON/CSV
- Undo/Redo no 1756 Editor
- Suporte a mais formatos de imagem

## 📄 Licença

Esta ferramenta é fornecida como está para uso com ServiceNow Knowledge Base articles.

## 📋 Changelog

### v1.1 (2026-03-27)
- ✅ Botão "Back to Home" no General Editor
- ✅ Texto de boas-vindas corrigido no 1756 Editor
- ✅ Seções "How to Use" expandíveis em ambos editores
- ✅ Compressão automática de imagens (> 200 KB)
- ✅ Estatísticas de compressão em tempo real
- ✅ Correções de sintaxe e melhorias de performance

### v1.0 (2026-03-27)
- ✅ Integração de Home + General Editor + 1756 Editor
- ✅ IBM Carbon Dark Theme completo
- ✅ Upload de imagens (paste/drag/select)
- ✅ Import/Export completo
- ✅ Arquivo único (72 KB)

---

**Feito para editores de KB articles ServiceNow que merecem ferramentas melhores** 🚀

**Especialmente otimizado para IBM Mainframe 1756 Operational Procedures** 💻
