# Protótipo de Cuidados Paliativos - Arquitetura Multi-Página

Este é um projeto web de informações sobre Cuidados Paliativos, organizado com arquitetura multi-página para facilitar navegação e manutenção.

## 📁 Estrutura do Projeto

```
prototipo fabiane/
│
├── index-multipage.html          # Página inicial (substitua index.html por este)
├── index.html                     # Versão original (backup)
├── index-novo.html                # Versão SPA (backup)
│
├── css/
│   ├── style-multipage.css        # Estilos para arquitetura multi-página
│   └── style.css                  # Estilos originais SPA
│
├── js/
│   └── navigation.js              # (Não usado na versão multi-página)
│
├── imagens/                       # Pasta de imagens (MOVER ARQUIVOS AQUI)
│   ├── capa.jpeg
│   ├── pacientes_familiares.png
│   ├── profissionais da saude.png
│   ├── gestores.png
│   ├── equipe_multiprofissional_saude.png
│   ├── medidas_conforto.png
│   ├── humanizacao_finitude.png
│   ├── individualizacao.png
│   ├── icone_pulmao.png
│   ├── icone_nutricao.png
│   ├── icone_psicologia.png
│   ├── icone_medicina.png
│   ├── icone_enfermagem.png
│   ├── icone_espiritualidade.png
│   ├── empatia.jpeg
│   ├── religioso.jpeg
│   └── spike.jpeg
│
└── pages/
    │
    ├── profissionais/
    │   ├── profissionais.html         # Página Profissionais da Saúde
    │   ├── pacientes_familiares.html  # Página Pacientes e Familiares
    │   ├── gestores.html              # Página Gestores em Saúde
    │   ├── medidas_conforto.html      # Página Medidas de Conforto
    │   └── individualizacao.html      # Página Individualização do Cuidado
    │
    ├── humanizacao/
    │   ├── humanizacao.html           # Hub de Humanização
    │   ├── empatia.html               # Guia de Empatia
    │   ├── religioso.html             # Guia Inter-Religioso
    │   └── spikes.html                # Protocolo SPIKES
    │
    └── especialidades/
        ├── pneumologia.html           # Vídeos Pneumologia
        ├── nutricao.html              # Vídeos Nutrição
        ├── psicologia.html            # Vídeos Psicologia
        ├── medicina.html              # Vídeos Medicina
        ├── enfermagem.html            # Vídeos Enfermagem
        └── espiritualidade.html       # Vídeos Espiritualidade
```

## 🚀 Como Usar

### Passo 1: Mover as Imagens
Você precisa mover manualmente os arquivos de imagem para a pasta `imagens/`:

1. Localize os arquivos na raiz do projeto
2. Mova todos para `imagens/`

Lista de arquivos para mover:
- capa.jpeg
- pacientes_familiares.png
- profissionais da saude.png
- gestores.png
- equipe_multiprofissional_saude.png
- medidas_conforto.png
- humanizacao_finitude.png
- individualizacao.png
- icone_pulmao.png
- icone_nutricao.png
- icone_psicologia.png
- icone_medicina.png
- icone_enfermagem.png
- icone_espiritualidade.png
- empatia.jpeg
- religioso.jpeg
- spike.jpeg

### Passo 2: Ativar a Versão Multi-Página
Você tem duas opções:

**Opção A (Recomendada):**
```powershell
# Renomear arquivo original como backup
Rename-Item index.html index-spa-backup.html

# Renomear nova versão para index.html
Rename-Item index-multipage.html index.html
```

**Opção B (Manual):**
1. Renomeie `index.html` para `index-spa-backup.html`
2. Renomeie `index-multipage.html` para `index.html`

### Passo 3: Atualizar referência CSS no index.html
Após renomear, edite o novo `index.html` e certifique-se de que a linha do CSS está:
```html
<link rel="stylesheet" href="css/style-multipage.css">
```

### Passo 4: Testar
Abra `index.html` no navegador e navegue pelas páginas.

## ✨ Características da Arquitetura Multi-Página

### Vantagens:
- ✅ **URLs Individuais**: Cada página tem seu próprio endereço
- ✅ **Melhor SEO**: Motores de busca indexam cada página separadamente
- ✅ **Carregamento Mais Rápido**: Apenas a página necessária é carregada
- ✅ **Histórico do Navegador**: Botão "Voltar" funciona nativamente
- ✅ **Compartilhamento**: URLs diretas para conteúdo específico
- ✅ **Manutenção Facilitada**: Cada seção em arquivo separado

### Estrutura de Navegação:
```
Página Inicial (index.html)
│
├── Profissionais da Saúde → pages/profissionais/profissionais.html
│   ├── Equipe Multiprofissional → pages/humanizacao/humanizacao.html
│   ├── Medidas de Conforto → pages/profissionais/medidas_conforto.html
│   ├── Humanização da Finitude → pages/humanizacao/humanizacao.html
│   └── Individualização → pages/profissionais/individualizacao.html
│
├── Pacientes e Familiares → pages/profissionais/pacientes_familiares.html
│   ├── Medidas de Conforto → pages/profissionais/medidas_conforto.html
│   └── Humanização da Finitude → pages/humanizacao/humanizacao.html
│
└── Gestores em Saúde → pages/profissionais/gestores.html
    ├── Equipe Multiprofissional → pages/humanizacao/humanizacao.html
    └── Individualização → pages/profissionais/individualizacao.html

Humanização (pages/humanizacao/humanizacao.html)
│
├── Especialidades:
│   ├── Pneumologia → pages/especialidades/pneumologia.html
│   ├── Nutrição → pages/especialidades/nutricao.html
│   ├── Psicologia → pages/especialidades/psicologia.html
│   ├── Medicina → pages/especialidades/medicina.html
│   ├── Enfermagem → pages/especialidades/enfermagem.html
│   └── Espiritualidade → pages/especialidades/espiritualidade.html
│
└── Recursos Adicionais:
    ├── Empatia → pages/humanizacao/empatia.html
    ├── Inter-Religioso → pages/humanizacao/religioso.html
    └── Protocolo SPIKES → pages/humanizacao/spikes.html
```

## 📄 Conteúdo das Páginas

### Página Inicial
- Apresentação do projeto
- Links para 3 públicos-alvo: Profissionais, Pacientes/Familiares, Gestores

### Páginas de Profissionais
- **profissionais.html**: 4 cards de navegação
- **pacientes_familiares.html**: 2 cards de navegação
- **gestores.html**: 2 cards de navegação
- **medidas_conforto.html**: Conteúdo sobre medidas de conforto
- **individualizacao.html**: Conteúdo sobre individualização

### Páginas de Humanização
- **humanizacao.html**: Hub com 6 ícones de especialidades + 3 botões quadrados
- **empatia.html**: 5 princípios de empatia profissional
- **religioso.html**: Guia inter-religioso com 11 seções
- **spikes.html**: Protocolo SPIKES completo (6 etapas)

### Páginas de Especialidades
Cada página contém vídeos do YouTube sobre o tema:
- **pneumologia.html**: 3 vídeos
- **nutricao.html**: 2 vídeos
- **psicologia.html**: 3 vídeos
- **medicina.html**: 4 vídeos
- **enfermagem.html**: 3 vídeos
- **espiritualidade.html**: 2 vídeos

**Total: 17 vídeos educacionais**

## 🎨 Estilos CSS

O arquivo `css/style-multipage.css` contém:
- Estilos globais e tipografia
- Layout responsivo
- Botão de voltar fixo
- Cards com hover effects
- Grade de ícones para especialidades
- Layout split-screen para homepage
- Containers de vídeo responsivos
- Media queries para mobile

## 🔧 Tecnologias Utilizadas

- **HTML5**: Estrutura semântica
- **CSS3**: Estilos modernos com flexbox
- **JavaScript**: Apenas `window.history.back()` no botão voltar
- **YouTube Embed API**: Para vídeos educacionais

## 📱 Responsividade

O projeto é totalmente responsivo:
- Desktop: Layout split-screen na homepage, 2 colunas
- Tablet: Layout adaptado
- Mobile: Layout em coluna única, vídeos redimensionados

## 🆚 Comparação: Multi-Página vs SPA

### Arquitetura Multi-Página (Ativa):
- Arquivos separados por funcionalidade
- Navegação via links `<a href="...">`
- Histórico nativo do navegador
- Melhor para SEO e compartilhamento

### SPA - Single Page Application (Backup):
- Um único arquivo HTML (`index-novo.html`)
- Navegação via JavaScript
- Transições mais suaves
- Menor consumo de dados

## 📝 Notas Importantes

1. **Imagens**: Certifique-se de mover TODAS as imagens para a pasta `imagens/`
2. **Paths Relativos**: Todos os caminhos usam navegação relativa (`../../`)
3. **Botão Voltar**: Usa `window.history.back()` para voltar na navegação
4. **CSS Centralizado**: Um único arquivo CSS para toda a aplicação
5. **Sem JavaScript**: Exceto para o botão voltar, toda navegação é HTML puro

## 🔄 Versões Disponíveis

- **index.html** → Versão original monolítica (backup)
- **index-novo.html** → Versão SPA organizada (backup)
- **index-multipage.html** → Versão multi-página (ATUAL - renomeie para index.html)

## 📞 Manutenção

Para adicionar novo conteúdo:
1. Crie novo arquivo HTML na pasta apropriada
2. Use o template de uma página existente
3. Atualize os links nas páginas relacionadas
4. Mantenha o padrão de paths relativos

---

**Desenvolvido para facilitar o acesso a informações sobre Cuidados Paliativos**
