# Aurora Plena: site de uma clínica de saúde integral

Site de apresentação (*landing page*) da clínica **Aurora Plena**, com foco em cuidado integral, humanizado e acolhedor para a saúde física e mental. Feito com **HTML, CSS e JavaScript puros**.

## Para que serve

Apresentar a clínica, suas especialidades e profissionais, e levar o visitante ao agendamento: os botões **Agendar Consulta** abrem o WhatsApp da clínica com uma mensagem pronta.

## Seções da página

| Seção | Conteúdo |
|---|---|
| **Início** | Título, mensagem de acolhimento e chamada para conhecer a clínica. |
| **Especialidades / Nossos Serviços** | Cartões: Consulta Psicológica, Avaliação Médica, Nutrição Personalizada e Bem-estar Corporal. |
| **Nossa Abordagem** | Acolhimento humanizado, diagnóstico personalizado e saúde contínua. |
| **Quem somos** | Profissionais e depoimentos. |
| **Agendamento** | Chamada final para marcar consulta. |

O cabeçalho fica fixo no topo e a rolagem entre as seções é suave.

## Como o texto é carregado

Os textos principais não ficam escritos direto no HTML: elementos marcados com `data-i18n="N"` recebem seu conteúdo do arquivo **`pt.json`** quando a página abre (via `fetch`). Isso deixa o site preparado para ter outros idiomas: basta criar um novo arquivo de textos, como `en.json`.

## Estrutura

```
├── index.html     # estrutura da página e script que carrega os textos
├── styles.css     # estilos (fontes do Google Fonts e ícones Bootstrap Icons)
├── pt.json        # textos em português
└── imagens/       # logo, ícone e fotos
```

## Como visualizar

Como a página usa `fetch` para ler o `pt.json` e caminhos que começam em `/`, é preciso abri-la por um **servidor local** (abrir o arquivo direto no navegador não carrega os textos):

```bash
git clone https://github.com/guilherf/AuroraSite.git
cd AuroraSite
python3 -m http.server 8000
# acesse http://localhost:8000
```

## Autor

Desenvolvido por Guilherme Ferreira — [@guilherf](https://github.com/guilherf)
