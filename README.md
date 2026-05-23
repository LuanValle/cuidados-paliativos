# App Cuidados Paliativos

## Estrutura do Projeto

```
prototipo fabiane/
├── index-novo.html          # Arquivo HTML principal (organizado)
├── index.html               # Arquivo HTML original (backup)
├── css/
│   └── style.css           # Estilos separados
├── js/
│   └── navigation.js       # Navegação e funções JavaScript
├── imagens/                # CRIE ESTA PASTA e mova todas as imagens aqui
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
└── README.md
```

## Instruções de Organização

### Passo 1: Criar a pasta de imagens
1. Crie uma pasta chamada `imagens` na raiz do projeto

### Passo 2: Mover as imagens
Mova todos os arquivos de imagem para a pasta `imagens/`:
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

### Passo 3: Usar o novo arquivo
Renomeie ou delete o `index.html` antigo e renomeie `index-novo.html` para `index.html`

## Melhorias Implementadas

### Organização de Código
- ✅ CSS separado em arquivo próprio (`css/style.css`)
- ✅ JavaScript separado em arquivo próprio (`js/navigation.js`)
- ✅ Todas as referências de imagens atualizadas para `imagens/`
- ✅ Código HTML mais limpo e organizado

### Estrutura Modular
- Separação clara entre conteúdo (HTML), apresentação (CSS) e comportamento (JS)
- Facilita manutenção e atualizações futuras
- Melhora a performance de carregamento (cache de arquivos CSS/JS)

### Navegação
- Sistema de navegação por histórico mantido
- Funções `goTo()` e `goBack()` centralizadas em `navigation.js`

## Como Executar

1. Certifique-se de que todas as imagens estão na pasta `imagens/`
2. Abra o arquivo `index.html` (renomeado de `index-novo.html`) em um navegador
3. Navegue pelas diferentes seções do aplicativo

## Seções do Aplicativo

1. **Tela Principal**: Acesso a Pacientes/Família, Profissionais, Gestores
2. **Profissionais de Saúde**:
   - Especialidades (6 áreas com vídeos)
   - Conforto & Clínica
   - Humanização & Finitude (Empatia, Religioso, SPIKES)
   - Individualização do Cuidado
   - Ferramentas e Avaliação

## Tecnologias Utilizadas

- HTML5
- CSS3
- JavaScript (Vanilla)
- YouTube Embed API

## Observações

- O arquivo original `index.html` foi mantido como backup
- Todos os caminhos de imagem foram atualizados para usar o prefixo `imagens/`
- O CSS usa caminho relativo `../imagens/` para a imagem de fundo da tela 1
