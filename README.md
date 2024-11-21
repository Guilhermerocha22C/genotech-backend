# GenoTech Backend

Este é o repositório do backend para o projeto GenoTech, uma plataforma educacional interativa focada em genética e biotecnologia.

## Tecnologias Utilizadas

- Node.js
- Express.js
- MySQL (via mysql2)
- Cors
- Multer (para upload de arquivos)
- SendGrid (para envio de e-mails)
- dotenv (para gerenciamento de variáveis de ambiente)
- Axios (para requisições HTTP)
- reCAPTCHA (para proteção contra bots)

## Funcionalidades Principais

1. **Autenticação de Usuários**
   - Login de usuário com verificação reCAPTCHA
   - Login de administrador
   - Registro de novos usuários

2. **Gerenciamento de Perfil**
   - Atualização de informações do usuário
   - Upload de imagem de perfil

3. **Sistema de Pontuação e Ranking**
   - Atualização de pontos e XP dos usuários
   - Exibição de ranking de usuários

4. **Recuperação de Senha**
   - Geração de token para recuperação de senha
   - Envio de e-mail com link para redefinição de senha

5. **Painel de Administração**
   - Visualização de todos os usuários
   - Edição e remoção de usuários

6. **Integração com Frontend**
   - Servindo arquivos estáticos do frontend
   - Rotas API para comunicação com o frontend

## Estrutura do Projeto

- `server.js`: Arquivo principal do servidor
- `/uploads`: Diretório para armazenamento de imagens de perfil
- Rotas principais:
  - `/api/login`: Login de usuário
  - `/api/admin/login`: Login de administrador
  - `/api/register`: Registro de novo usuário
  - `/api/user/:id`: Busca de dados do usuário
  - `/api/user/update/:id`: Atualização de perfil do usuário
  - `/api/ranking`: Obtenção do ranking de usuários
  - `/api/recuperar-senha`: Recuperação de senha
  - `/api/redefinir-senha`: Redefinição de senha

## Segurança

- Uso de reCAPTCHA para proteção contra bots no login
- Armazenamento seguro de senhas (considere implementar hashing)
- Tokens para recuperação de senha

## Deploy

- O backend está configurado para ser hospedado na Vercel
