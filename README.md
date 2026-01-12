# 🌊 Pureza - Site Turístico com Banco de Dados

Um site informativo sobre o município fictício de Pureza com **histórias, lendas, turismo e cultura**, desenvolvido com **Flask** e **MySQL**.

## ✨ Características

- **Frontend Moderno**: Bootstrap 5.3 com CSS customizado
- **Design Responsivo**: Otimizado para todos os dispositivos
- **Banco de Dados MySQL**: Estrutura relacional completa
- **Sem Dashboard Admin**: Interface pública apenas
- **Animações Suave**: CSS3 e JavaScript
- **Tema de Cores**: Azul (#0a7ea4), Branco e Verde (#2e7d32)

## 📋 Requisitos

- Python 3.8+
- MySQL 8.0+
- pip (gerenciador de pacotes Python)

## 🚀 Instalação Rápida

### 1️⃣ Clonar/Preparar Projeto
```bash
cd BLOG-4BM
```

### 2️⃣ Instalar Dependências
```bash
pip install -r requirements.txt
```

### 3️⃣ Criar Banco de Dados
```bash
mysql -u root -p < sistemablog.sql
```

*Nota: Se sua senha MySQL for diferente, edite `app.py` na configuração `db_config`*

### 4️⃣ Executar Aplicação
```bash
python app.py
```

Acesse: **http://localhost:5000**

## 📁 Estrutura

```
BLOG-4BM/
├── app.py                    # Flask app + funções de banco
├── requirements.txt          # Dependências Python
├── sistemablog.sql          # Script SQL do banco
├── README.md                
├── static/
│   ├── css/style.css        # Estilos (747 linhas)
│   └── js/script.js         # JavaScript interativo
└── templates/               # Templates HTML
    ├── base.html            # Template base
    ├── index.html           # Início
    ├── historia.html        # Histórias
    ├── lendas.html          # Lendas
    ├── turismo.html         # Turismo
    ├── pau-brasil.html      # Pau Brasil
    ├── cultura.html         # Cultura
    ├── detalhe.html         # Detalhe genérico
    ├── sobre.html           # Sobre
    └── 404.html             # Erro
```

## 🌍 Páginas Disponíveis

| Rota | Descrição |
|------|-----------|
| `/` | Página inicial |
| `/historia` | Lista histórias |
| `/historia/{slug}` | Detalhe história |
| `/lendas` | Lista lendas |
| `/lenda/{slug}` | Detalhe lenda |
| `/turismo` | Pontos turísticos |
| `/turismo/{slug}` | Detalhe turismo |
| `/pau-brasil` | Página Pau Brasil |
| `/cultura` | Aspectos culturais |
| `/cultura/{slug}` | Detalhe cultura |
| `/sobre` | Sobre projeto |

## 📊 Banco de Dados

### Tabelas
- **categorias**: História, Lendas, Turismo, Cultura, Pau-Brasil
- **posts**: Conteúdo do site com relacionamentos
- **autores**: Autores dos posts

### Dados Pré-carregados
✅ 3 histórias  
✅ 3 lendas  
✅ 3 pontos turísticos  
✅ 3 aspectos culturais  

### Adicionar Novo Post
```sql
INSERT INTO posts (titulo, slug, descricao, conteudo, imagem, categoria_id, autor_id, ativo) 
VALUES ('Título', 'slug', 'Desc', 'Conteúdo', 'URL', 1, 1, TRUE);
```

## 🎨 Tecnologias

| Tecnologia | Versão |
|-----------|--------|
| Flask | 2.3.2 |
| MySQL Connector | 8.0.33 |
| Bootstrap | 5.3.0 |
| Font Awesome | 6.4.0 |
| Python | 3.8+ |

## 🎯 Funcionalidades JavaScript

- ✅ Animações ao scroll
- ✅ Card hover effects
- ✅ Smooth scroll
- ✅ Compartilhamento social
- ✅ Lightbox para imagens
- ✅ Lazy loading
- ✅ Botão "voltar ao topo"

## 📱 Responsivo

- **Mobile**: até 576px
- **Tablet**: 576px - 768px  
- **Desktop**: 768px+

## 🔒 Segurança

- Sem painel de administração público
- Prepared statements para queries SQL
- Validação de slugs
- Posts com flag de ativo/inativo

## 📝 Customização

### Mudar Conexão MySQL
Edite em `app.py`:
```python
db_config = {
    'host': 'localhost',
    'user': 'seu_usuario',
    'password': 'sua_senha',
    'database': 'sistemablog'
}
```

### Alterar Cores
Edite `static/css/style.css`:
```css
:root {
    --primary-blue: #0a7ea4;
    --primary-green: #2e7d32;
    /* ... mais cores */
}
```

## 🐛 Troubleshooting

**"Erro ao conectar ao banco"**
- Verifique se MySQL está rodando
- Confirme credenciais em `db_config`
- Execute `sistemablog.sql`

**"Template não encontrado"**
- Certifique-se que está na pasta raiz do projeto
- Verifique se `templates/` existe

**Imagens não carregam**
- Use URLs absolutas (https://...)
- Ou coloque imagens em `static/images/`

## 📄 Licença

Projeto educacional

---

**Desenvolvido com ❤️ para Pureza - Um Tesouro de Águas Cristalinas** 🌊

## 🎯 Objetivo

Criar uma plataforma atrativa para:
- 📍 Divulgar locais turísticos de Pureza
- 📖 Compartilhar lendas e histórias locais
- 🏞️ Explorar as belezas das águas cristalinas
- 🔐 Manter controle editorial dos desenvolvedores

## ✨ Destaques

| Recurso | Descrição |
|---------|-----------|
| 🎨 **Design Moderno** | Tema aquático com cores azuis e turquesas |
| 📱 **Responsivo** | Funciona perfeitamente em móvel, tablet e desktop |
| 🔐 **Seguro** | Apenas desenvolvedores podem publicar conteúdo |
| 📂 **Categorizado** | 4 categorias para organizar posts |
| 👤 **Admin Dashboard** | Painel completo para gerenciar artigos |
| 🔄 **Social Sharing** | Compartilhe nos redes sociais (Facebook, Twitter, WhatsApp) |

## 🚀 Quick Start

### 1. Instalação do Banco de Dados
```sql
-- No MySQL, execute:
source sistemablog_novo.sql;
```

### 2. Instalar Dependências
```bash
pip install -r requirements.txt
```

### 3. Rodar a Aplicação
```bash
python app.py
```

### 4. Acessar
- **Home**: http://localhost:5000/
- **Admin**: http://localhost:5000/admin/login

## 🔐 Credenciais Padrão (Desenvolvedores)

```
Email:    mariaeloisaaxr@gmail.com
Senha:    1406
```

⚠️ **Segurança**: Altere essas credenciais em produção!

## 📊 Estrutura de Pastas

```
BLOG-4BM/
│
├── 📄 app.py                      # Aplicação Flask
├── 🗄️ sistemablog_novo.sql        # Schema do banco
├── 📋 requirements.txt            # Dependências Python
├── 📖 README.md                   # Este arquivo
│
├── 📁 static/
│   └── 📁 css/
│       └── 🎨 style.css           # Tema águas cristalinas
│
└── 📁 templates/
    ├── 🏠 index.html              # Página inicial
    ├── 📄 ver_post.html           # Artigo completo
    ├── 🏷️ categoria.html          # Posts por categoria
    ├── ✏️ novo_post.html          # Criar novo artigo
    ├── 📝 editar_post.html        # Editar artigo
    ├── ⚙️ admin_dashboard.html    # Painel admin
    ├── 🔑 login.html              # Login desenvolvedores
    ├── ℹ️ sobre.html              # Sobre o projeto
    └── ⚠️ 404.html                # Página de erro
```

## 🎨 Paleta de Cores

Inspirada em **águas cristalinas e céu limpo**:

```
🟦 Azul Primário      #0a7ea4
🟦 Azul Claro        #1fa3c5
🟦 Azul do Céu       #4fc3f7
🟦 Ciano             #80deea
🟦 Teal/Verde Água   #00897b
```

## 📚 Banco de Dados

### Tabela: **autores**
```
ID_Autor          | int (PK)
Nome              | varchar(255)
Email             | varchar(255) UNIQUE
Bio               | text
Eh_Desenvolvedor  | boolean
```

### Tabela: **categorias**
```
ID_Categoria  | int (PK)
Nome          | varchar(100)
Descricao     | text
Icone         | varchar(50) [Font Awesome]
```

### Tabela: **posts**
```
ID_Post           | int (PK)
Titulo            | varchar(255)
Slug              | varchar(255) UNIQUE
Conteudo          | longtext
Resumo            | text
ID_Categoria      | int (FK)
ID_Autor          | int (FK)
Data_Publicacao   | datetime
Data_Atualizacao  | datetime
Visualizacoes     | int
Status            | enum('Publicado', 'Rascunho')
Imagem_URL        | varchar(255)
```

## 🗂️ Categorias Disponíveis

1. **🏞️ Locais Turísticos** - Pontos de interesse e belezas naturais
2. **📖 Lendas e Histórias** - Mitos e narrativas culturais
3. **🎒 Aventuras** - Experiências e trilhas
4. **💡 Curiosidades** - Fatos interessantes

## 🔧 Configuração

### Alterar Credenciais de Acesso

Em `app.py`, localize a função `login()` e modifique:

```python
if email == 'seu-email@exemplo.com' and senha == 'sua-senha':
    # ...
```

### Conectar a um MySQL Remoto

Em `app.py`, função `conectar_bd()`:

```python
cnx = connect(
    user='seu_usuario',
    password='sua_senha',
    host='seu_host.com',  # ex: db.example.com
    database='sistemablog'
)
```

## 💻 Tecnologias Utilizadas

| Tecnologia | Versão | Propósito |
|------------|--------|----------|
| **Flask** | 2.x+ | Framework web Python |
| **MySQL/MariaDB** | 5.7+ | Banco de dados relacional |
| **Bootstrap** | 5.3 | Framework CSS responsivo |
| **Font Awesome** | 6.4 | Ícones |
| **Python** | 3.7+ | Linguagem backend |

## 📖 Como Usar

### Para Visitantes
1. ✅ Acesse a página inicial
2. ✅ Navegue pelos posts recentes
3. ✅ Clique em um post para ler na íntegra
4. ✅ Use as categorias para filtrar
5. ✅ Compartilhe nos redes sociais

### Para Desenvolvedores

#### Login
```
1. Acesse: http://localhost:5000/admin/login
2. Digite seu email e senha
3. Você será redirecionado ao dashboard
```

#### Criar Post
```
1. Clique em "Novo Post"
2. Preencha os campos:
   • Título
   • Categoria
   • Resumo (breve descrição)
   • Conteúdo (HTML permitido)
   • URL da Imagem (opcional)
3. Clique em "Publicar"
```

#### Editar Post
```
1. No dashboard, clique em "Editar"
2. Modifique os campos desejados
3. Clique em "Atualizar"
```

#### Deletar Post
```
1. No dashboard, clique em "Deletar"
2. Confirme a ação
```

## 🔍 Endpoints Principais

| Rota | Método | Descrição |
|------|--------|-----------|
| `/` | GET | Página inicial |
| `/sobre` | GET | Sobre o projeto |
| `/post/<slug>` | GET | Visualizar artigo |
| `/categoria/<id>` | GET | Posts por categoria |
| `/admin/login` | GET/POST | Login |
| `/admin/dashboard` | GET | Painel admin |
| `/admin/novo-post` | GET/POST | Criar post |
| `/admin/editar-post/<id>` | GET/POST | Editar post |
| `/admin/deletar-post/<id>` | POST | Deletar post |

## 🐛 Troubleshooting

### ❌ Erro: "Can't connect to MySQL server"
**Solução**: 
- Verifique se MySQL está rodando
- Confirme credenciais em `app.py`
- Teste: `mysql -u root -p`

### ❌ Posts não aparecem
**Solução**:
- Verifique o status do post (deve estar "Publicado")
- Execute novamente `sistemablog_novo.sql`

### ❌ Estilos não carregam
**Solução**:
- Limpe cache: Ctrl+Shift+Delete
- Verifique se `style.css` existe em `static/css/`

## 🔒 Considerações de Segurança

- ✅ Apenas desenvolvedores podem publicar
- ✅ Senhas armazenadas em session
- ✅ Proteção contra acesso direto ao admin
- ⚠️ Em produção: use variáveis de ambiente para credenciais
- ⚠️ Implemente HTTPS para dados sensíveis

## 📈 Próximas Melhorias

- [ ] Upload de imagens (em vez de URLs externas)
- [ ] Sistema de comentários
- [ ] Busca por texto completo
- [ ] Agendamento de posts
- [ ] Múltiplos usuários/autores
- [ ] Sistema de tags
- [ ] Analytics e estatísticas

## 📞 Suporte

Para dúvidas ou problemas:
1. Consulte a documentação em `DOCUMENTACAO.md`
2. Verifique o console do navegador (F12)
3. Revise os logs do Flask no terminal

## 📄 Licença

Projeto desenvolvido para fins educacionais e turísticos.

---

### 💡 Dica Importante

**Antes de colocar em produção**:
- [ ] Altere o secret key do Flask
- [ ] Mude as credenciais de admin
- [ ] Configure HTTPS
- [ ] Atualize credenciais do MySQL
- [ ] Teste em todos os navegadores
- [ ] Configure backups regulares do banco

---

**Desenvolvido com ❤️ para Pureza** 🌊

*"Um Tesouro de Águas Cristalinas"*
