Gerenciador de Tarefas

Aplicação web full stack para organizar tarefas, com cadastro e login de usuários. Cada pessoa vê e gerencia apenas as próprias tarefas.

Status: em desenvolvimento 🚧 Demo: em breve <!-- TODO: colocar o link do deploy -->

<!-- TODO: adicionar um print ou GIF da aplicação funcionando -->
Sobre o projeto

Projeto de portfólio feito para praticar o ciclo completo de uma aplicação web: banco de dados relacional, API REST com autenticação, interface em React e deploy.

<!-- TODO: contar em 2 ou 3 linhas por que você criou este projeto e o tema escolhido (ex.: tarefas de estudo por disciplina) -->
Funcionalidades

Escopo mínimo (o que o projeto faz):

 Cadastro de usuários
 Login com autenticação via JWT (senha armazenada com hash)
 CRUD de tarefas (criar, listar, editar e excluir)
 Cada usuário acessa somente as próprias tarefas
 Marcar tarefa como concluída
 Filtrar por status e por categoria
 Deploy em produção

O que o projeto não faz (por enquanto):

Compartilhamento de tarefas entre usuários
Notificações
Aplicativo mobile
Login com contas externas (Google, GitHub)
Tecnologias
Camada	Tecnologia
Front-end	React (Vite)
Back-end	Node.js, Express
Banco de dados	PostgreSQL
Autenticação	JWT
<!-- TODO: atualizar esta tabela com o que for realmente usado (ex.: bibliotecas de teste, validação, ORM) -->
Modelo de dados

Dois relacionamentos principais: um usuário possui várias tarefas (1 para N).

usuarios (id, nome, email, senha_hash, criado_em)
tarefas  (id, usuario_id, titulo, descricao, categoria, concluida, criado_em)
<!-- TODO: ajustar para refletir as tabelas finais -->
Rotas da API (planejado)
Método	Rota	Descrição	Autenticação
POST	/auth/register	Cadastra um usuário	Não
POST	/auth/login	Faz login e retorna o token	Não
GET	/tasks	Lista as tarefas do usuário	Sim
POST	/tasks	Cria uma tarefa	Sim
PUT	/tasks/:id	Atualiza uma tarefa	Sim
DELETE	/tasks/:id	Exclui uma tarefa	Sim
<!-- TODO: atualizar conforme as rotas forem implementadas -->
Estrutura do repositório
gerenciador-tarefas/
├── backend/     # API em Node.js + Express
├── frontend/    # Interface em React
└── README.md
Como rodar localmente
Pré-requisitos
Node.js (versão LTS)
PostgreSQL
Git
Passo a passo
bash
# 1. Clonar o repositório
git clone https://github.com/amaraalmatheus/gerenciador-tarefas.git
cd gerenciador-tarefas

# 2. Back-end
cd backend
npm install
cp .env.example .env   # preencha as variáveis (veja abaixo)
npm run dev

# 3. Front-end (em outro terminal)
cd frontend
npm install
npm run dev
<!-- TODO: testar este passo a passo do zero e corrigir os comandos conforme o projeto real -->
Variáveis de ambiente (backend/.env)
PORT=3000
DATABASE_URL=postgresql://usuario:senha@localhost:5432/gerenciador_tarefas
JWT_SECRET=uma_chave_longa_e_aleatoria

Nunca suba o arquivo .env para o GitHub. Ele já está no .gitignore.

Decisões técnicas
<!-- TODO: preencher ao longo do desenvolvimento. Este é um dos trechos mais valiosos do README. Exemplos de perguntas: - Por que escolhi JWT para autenticação? Quais são as limitações? - Como organizei as pastas do back-end? - Como garanti que um usuário não acesse tarefas de outro? - Onde e como fiz o deploy? -->
O que aprendi
<!-- TODO: preencher ao final do projeto, com 3 a 5 pontos honestos (dificuldades e como resolveu) -->
Próximos passos
 Testes automatizados na API
 Paginação da lista de tarefas
 Melhorias de acessibilidade e responsividade
Referências
<!-- TODO: se usou cursos, documentações ou tutoriais como apoio (ex.: The Odin Project), cite aqui. Ser transparente é uma qualidade. -->
Licença

Distribuído sob a licença MIT. <!-- TODO: se não adicionou licença, remova esta seção -->

Autor

Matheus Amaral Alves Estudante de Sistemas de Informação na USP (São Carlos) GitHub: @amaraalmatheus