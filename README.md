# ServiceNow Editors - IBM

## 📦 Arquivo Integrado

**Nome:** `index.html`
**Tamanho:** 62 KB
**Linhas:** 1,172

## ✨ Funcionalidades

### 🏠 Home Screen
- Tela inicial elegante com IBM Carbon Dark theme
- Dois cards de seleção:
  - **General Editor** - Editor geral para qualquer KB article
  - **1756 Procedures Editor** - Editor especializado para procedimentos 1756

### 📝 General Editor (Completo)

1. **Import HTML**
   - Cole HTML bruto do ServiceNow
   - Botão "Paste from Clipboard"
   - Estatísticas em tempo real (caracteres, tags)

2. **Limpeza Automática**
   - Remove formatação Microsoft Office (classes MSO)
   - Remove atributos data-*
   - Remove tags span vazias
   - Remove estilos mso-*
   - Decodifica entidades HTML
   - Colapsa spans aninhados

3. **Editor Visual**
   - ContentEditable com preview em tempo real
   - Floating toolbar ao selecionar texto:
     - Bold, Italic, Underline, Strikethrough
     - H1, H2, H3, Paragraph
     - Ordered List, Unordered List
     - Link, Remove Format
   - Indicador de mudanças não salvas

4. **Export HTML**
   - Copia HTML editado para clipboard
   - Estatísticas comparativas (antes/depois)
   - Preview do resultado
   - Botão "Show/Hide Preview"

### 🖥️ 1756 Procedures Editor (Completo)
Editor especializado com:

1. **Gerenciamento de Procedures**
   - Sidebar com lista de procedures
   - Search/filter em tempo real
   - Click para editar
   - Contador de procedures

2. **Formulário de Edição**
   - Message Code *
   - Description *
   - System, Priority, Support Group
   - Notes
   - Operations Action (textarea)

3. **Upload de Imagens** 🖼️
   - **Paste (Ctrl+V)**: Cole imagens diretamente no textarea
   - **Drag & Drop**: Arraste imagens do computador
   - **File Select**: Clique na área de upload e selecione
   - Conversão automática para base64
   - Suporte para múltiplas imagens

4. **Toolbar de Formatação**
   - **Bold**: `<strong></strong>`
   - **Exception Box**: Caixa amarela de exceção
   - **Note Box**: Caixa azul de nota
   - **Code**: `<code></code>`
   - **Link**: `<a href=""></a>`

5. **Import/Export**
   - **Import HTML**: Importa procedures existentes do arquivo V6
   - **Export HTML**: Copia HTML completo com CSS para clipboard
   - Inclui:
     - Todo o CSS embutido
     - Header e instruções
     - Workflow steps
     - Todas as procedures organizadas por categoria

6. **Auto-conversão**
   - Line breaks (`\n`) → `<br/>` automaticamente
   - Apenas se não houver HTML já formatado

## 🎨 IBM Carbon Design System

### Tema Dark Aplicado
- **Background principal**: #161616 (Gray 100)
- **Superfícies**: #262626, #393939, #525252 (Gray scale)
- **Texto primário**: #f4f4f4
- **Texto secundário**: #c6c6c6
- **Links**: #78a9ff (Blue 40)
- **Botões primários**: #4589ff (Blue 60)
- **Success**: #42be65 (Green 60)
- **Error**: #fa4d56 (Red 50)
- **Warning**: #f1c21b (Yellow)

### Tipografia
- **Fonte primária**: IBM Plex Sans
- **Fonte monospace**: IBM Plex Mono
- Carregadas via Google Fonts CDN

### Espaçamentos
- Baseado no sistema de spacing do Carbon
- Transições: 110ms (padrão Carbon)
- Bordas sem border-radius (estilo Carbon)

## 📋 Como Usar

### 1. Abrir o Editor
```
Abra (https://cauedutramonteiro.github.io/snow-kb-editor/) no navegador
```

### 2. General Editor
1. Clique em "General Editor"
2. Cole HTML do ServiceNow
3. Clique "Clean & Import"
4. Edite visualmente (use floating toolbar ao selecionar texto)
5. Clique "Export HTML"
6. Copie para clipboard
7. Cole de volta no ServiceNow

### 3. 1756 Editor
1. Clique em "1756 Procedures Editor"
2. **Para importar existentes**:
   - Clique "Import HTML"
   - Cole o HTML do arquivo V6
   - Procedures aparecem na sidebar
3. **Para adicionar nova**:
   - Clique "Add Procedure"
   - Preencha o formulário
   - Use toolbar para formatar
   - **Para adicionar imagem**:
     - Opção 1: Cole imagem (Ctrl+V) no textarea
     - Opção 2: Arraste imagem para área de upload
     - Opção 3: Clique na área e selecione arquivo
   - Clique "Create Procedure"
4. **Para exportar**:
   - Clique "Export HTML"
   - HTML completo copiado para clipboard
   - Cole no ServiceNow

## 🚀 Compatibilidade GitHub Pages

### Arquivo Único
✅ Tudo em um único arquivo HTML
✅ Sem dependências locais
✅ Sem build/compilação necessária

### CDNs Utilizados
- React 18 (unpkg.com)
- Babel Standalone (unpkg.com)
- Tailwind CSS (cdn.tailwindcss.com)
- Lucide Icons (unpkg.com)
- IBM Plex Fonts (Google Fonts)

## ✅ Checklist de Funcionalidades

### General Editor
- [x] Import HTML com paste from clipboard
- [x] Limpeza automática (MS Office, etc)
- [x] Editor visual (contentEditable)
- [x] Floating toolbar
- [x] Export com estatísticas
- [x] Preview
- [x] Tema Carbon Dark

### 1756 Editor
- [x] List/search procedures
- [x] Add/Edit/Delete procedures
- [x] Form validation
- [x] Import from HTML
- [x] Export complete HTML with CSS
- [x] **Image upload (paste/drag/select)**
- [x] Formatting toolbar
- [x] Auto line break conversion
- [x] Category auto-assignment
- [x] Tema Carbon Dark

### Geral
- [x] Home screen com seleção
- [x] Navegação entre editores
- [x] Tema Carbon Dark consistente
- [x] Arquivo único (GitHub Pages ready)
- [x] Notificações
- [x] Responsivo

## 📝 Notas Importantes

### ServiceNow Images
Imagens do ServiceNow (`sys_attachment.do`) aparecem quebradas no editor mas funcionam corretamente quando coladas de volta no ServiceNow.

### Base64 Images
Imagens inseridas via upload são convertidas para base64 e ficam embutidas no HTML. Isso:
- ✅ **Vantagem**: Não precisa de hosting externo
- ⚠️ **Desvantagem**: Aumenta tamanho do HTML (para imagens grandes)

### Auto Line Breaks
O editor 1756 converte `\n` para `<br/>` automaticamente, EXCETO se o texto já contiver tags HTML (`<p>`, `<div>`, `<br>`).

---

**Data de Criação:** 2026-03-27
**Versão:** 1.0
**Status:** ✅ Pronto para produção
