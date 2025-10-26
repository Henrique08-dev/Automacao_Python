## 🎯 Visão Geral

Este projeto foi desenvolvido para automatizar a busca por oportunidades de emprego no LinkedIn, filtrando vagas relevantes publicadas nas últimas 24 horas e enviando-as diretamente para o e-mail do usuário. A solução resolve problemas comuns de busca geográfica através da implementação de um sistema de geoIDs personalizado.

## ✨ Funcionalidades

- **🔍 Busca Inteligente**: Filtragem por múltiplos critérios (país, estado, cidade, categoria, nível de experiência)
- **⏰ Filtro Temporal**: Captura apenas vagas publicadas nas últimas 24 horas
- **🌎 Suporte Geográfico**: Sistema de geoIDs para buscas precisas por localização
- **📧 Notificação Automática**: Envio de e-mails com vagas formatadas em HTML
- **⚙️ Interface Interativa**: Menu interativo para configuração dos filtros
- **📊 Ordenação Inteligente**: Vagas ordenadas das mais recentes para as mais antigas

## 🛠 Tecnologias Utilizadas

- **Python 3.7+**
- **BeautifulSoup4** - Web scraping e parsing HTML
- **Requests** - Requisições HTTP
- **Pandas** - Manipulação de dados (para futuras expansões)
- **smtplib** - Envio de e-mails
- **email.mime** - Formatação de e-mails HTML

## 📥 Instalação

### Pré-requisitos
- Python 3.7 ou superior
- Conta Gmail para envio de e-mails

### Clone o repositório
```bash
git clone https://github.com/seu-usuario/linkedin-job-scraper.git
cd linkedin-job-scraper
```

### Instale as dependências
```bash
pip install -r requirements.txt
```

## ⚙️ Configuração

### Configuração do E-mail
Para usar o sistema de envio de e-mails, você precisa:

1. Ativar a verificação em 2 etapas no Gmail
2. Gerar uma senha de aplicativo:
   - Acesse: Google Account → Security → 2-Step Verification → App passwords
   - Gere uma senha para "Mail"
   - Use essa senha no campo `senha` do código

### GeoIDs Suportados
O sistema inclui suporte pré-configurado para:
- 🇧🇷 Brasil: `106057199`
- 🇺🇸 Estados Unidos: `103644278`

Para adicionar novos países, inclua seus geoIDs no dicionário `geoIds`.

## 🚀 Uso

Execute o script principal:
```bash
python projeto_vagas_linkedin.py
```

### Fluxo de Interação:

1. **Seleção de Filtros**: Escolha entre três opções de filtragem
2. **Configuração de Parâmetros**: Defina critérios específicos de busca
3. **Processamento Automático**: O sistema busca, filtra e ordena as vagas
4. **Envio por E-mail**: Insira os e-mails destinatários

### Opções de Filtro:

1. **Todos os Filtros**: País, Estado, Cidade, Categoria, Experiência
2. **Filtro Básico**: Apenas País, Categoria e Experiência  
3. **Filtro Geográfico**: País, Estado e Cidade

## 💡 Exemplos de Uso

### Exemplo 1: Busca Completa
```
Filtro escolhido: 1 (Todos)
Vaga: "Analista de Dados"
País: "Brasil"
Estado: "São Paulo"
Cidade: "São Paulo"
Categoria: 2 (Remoto)
Experiência: 3 (Júnior)
Páginas: 3
```

### Exemplo 2: Busca Simplificada
```
Filtro escolhido: 2 (Básico)
Vaga: "Desenvolvedor Python"
País: "Estados Unidos"
Categoria: 2 (Remoto)
Experiência: 4 (Pleno-Sênior)
Páginas: 2
```

## 🤝 Contribuição

Contribuições são bem-vindas! Siga estos passos:

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

### Melhorias Futuras
- [ ] Implementação de database para histórico de vagas
- [ ] Agendamento de buscas automáticas
- [ ] Análise de tendências de mercado

## ⚠️ Aviso Legal

Este projeto é para fins educacionais e de portfólio. O uso deve respeitar os Termos de Serviço do LinkedIn. Recomendamos:
- Usar moderadamente para não sobrecarregar os servidores
- Respeitar os rate limits
- Não usar para spam ou atividades maliciosas

---

**Desenvolvido como parte do programa "Profissionais do Futuro" da Xperiun**
