# Passo 1: Configuração do Ambiente de Desenvolvimento

# 1. Instalar Node.js e npm (Se já estiverem instalados, verifique as versões)
node -v
npm -v

# 2. Criar um novo diretório para o projeto
mkdir academia-stackx
cd academia-stackx

# 3. Inicializar um novo projeto npm
npm init -y

# Passo 2: Instalação de Dependências do React

# 1. Instalar React e ReactDOM
npm install react react-dom

# 2. Instalar Create React App globalmente
npm install -g create-react-app

# 3. Criar um novo projeto React
npx create-react-app academia-stackx

# Passo 3: Estrutura de Arquivos e Componentes

# 1. Navegar até o diretório do projeto e abrir no editor de código
cd academia-stackx
code .

# 2. Modificar ou excluir arquivos conforme necessário
# Dentro do diretório 'src', criar novos componentes (exemplo com Bash)

# Criar diretório de componentes
mkdir src/components

# Criar arquivos de componentes
touch src/components/Header.js src/components/Footer.js src/components/Dashboard.js

# Exemplo de conteúdo para os componentes
echo "import React from 'react';

function Header() {
  return (
    <header>
      <h1>Academia StackX</h1>
    </header>
  );
}

export default Header;" > src/components/Header.js

echo "import React from 'react';

function Footer() {
  return (
    <footer>
      <p>© 2024 Academia StackX</p>
    </footer>
  );
}

export default Footer;" > src/components/Footer.js

echo "import React from 'react';

function Dashboard() {
  return (
    <main>
      <h2>Bem-vindo ao Painel da Academia StackX</h2>
      <p>Conteúdo do painel aqui...</p>
    </main>
  );
}

export default Dashboard;" > src/components/Dashboard.js

# Modificar App.js para usar os novos componentes
echo "import React from 'react';
import Header from './components/Header';
import Footer from './components/Footer';
import Dashboard from './components/Dashboard';
import './App.css';

function App() {
  return (
    <div className='App'>
      <Header />
      <Dashboard />
      <Footer />
    </div>
  );
}

export default App;" > src/App.js

# Passo 4: Estilização

# Usar CSS (ou Sass) para estilizar os componentes
# Exemplo de arquivo CSS para App.css
echo ".App {
  text-align: center;
}

header {
  background-color: #282c34;
  padding: 20px;
  color: white;
}

footer {
  background-color: #282c34;
  padding: 10px;
  color: white;
  position: fixed;
  bottom: 0;
  width: 100%;
}

main {
  padding: 20px;
}" > src/App.css

# Passo 5: Testando

# Executar a aplicação
npm start

# Passo 6: Implantação

# Construir a aplicação para produção
npm run build

# Fazer o deploy usando Vercel
# Instalar Vercel CLI globalmente
npm install -g vercel

# Fazer login no Vercel
vercel login

# Executar o comando para fazer o deploy
vercel
