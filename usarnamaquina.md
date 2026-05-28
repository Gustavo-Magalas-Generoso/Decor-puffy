# 🎉 Como Usar o Sistema Decor Puffy na sua Máquina

## 📋 Pré-requisitos

- **XAMPP** instalado ([Download aqui](https://www.apachefriends.org/))
- PHP 7.4 ou superior
- Navegador web (Chrome, Firefox, Edge, etc.)

---

## 🚀 Como Iniciar

### 1️⃣ **Inicie o XAMPP**
- Abra o **XAMPP Control Panel**
- Clique em **"Start"** ao lado de **"Apache"**
- Clique em **"Start"** ao lado de **"MySQL"**

Você verá algo assim:
```
Apache          [Start] ✓ Running
MySQL           [Start] ✓ Running
```

### 2️⃣ **Acesse a Aplicação**

No seu navegador, digite:
```
http://localhost/Decor__Puffy-main/public/login.php
```

---

## 🔓 Como Fazer Login como ADMIN

### Passo a Passo:

1. **Você verá uma tela de login** com 3 campos:
   - Usuário
   - Email
   - Senha

2. **Preencha assim:**
   - **Usuário**: `admin` (exatamente como está escrito)
   - **Email**: deixe **em branco** (não preencha nada)
   - **Senha**: `123` (números um, dois, três)

3. **Clique em "Entrar"**

4. **Pronto!** Você verá a tela com a tabela de "Decorações Cadastradas" ✅

### ⚠️ Atenção Importante:
- O campo **Email** precisa estar **VAZIO**
- Se preencher o email, o login não funciona!
- Digite `123` (a senha é literal, não é um código)

---

## 🔐 Credenciais de Login

### **Admin** (Gerenciador do sistema)
- **Usuário**: `admin`
- **Email**: (deixe em branco)
- **Senha**: `123`

### **Usuário Comum** (Apenas visualizar/alugar)
- **Usuário**: `usuario`
- **Email**: `teste@gmail.com`
- **Senha**: `123`

---

## 👨‍💼 O que cada Perfil Pode Fazer?

### 🔧 **ADMIN**
- ✅ Adicionar novas decorações
- ✅ Editar decorações existentes
- ✅ Deletar decorações
- ✅ Alugar decorações
- ✅ Devolver decorações
- ✅ Calcular previsão de aluguel
- ✅ Ver todas as decorações

### 👤 **USUÁRIO COMUM**
- ❌ Não pode adicionar/editar/deletar
- ✅ Pode visualizar decorações disponíveis
- ✅ Pode calcular previsão de aluguel
- ✅ Não pode fazer aluguel direto (tabela reduzida)

---

## 📖 Como Usar as Funcionalidades

### 1. **Adicionar uma Nova Decoração** (Apenas Admin)
1. Faça login como admin
2. Preencha o formulário "Adicionar Nova Decoração"
3. Digite o **tema** (ex: "Decoração Homem Aranha")
4. Escolha o **tamanho** (Pequeno, Médio ou Grande)
5. Escolha o **tipo** (Aniversário, Casamento, Formatura, Materiais)
6. Selecione uma **imagem** (a imagem fica em `uploads/` após envio)
7. Clique em **"Adicionar Decoração"**

### 2. **Editar uma Decoração** (Apenas Admin)
1. Na tabela "Decorações Cadastradas", clique no botão **"Editar"** (verde)
2. Modifique os dados na janela que aparecer
3. Clique em **"Atualizar"** para salvar

### 3. **Deletar uma Decoração** (Apenas Admin)
1. Na tabela, clique em **"Deletar"** (vermelho lixo)
2. A decoração será removida imediatamente

### 4. **Alugar uma Decoração**
1. Se admin: clique em **"Alugar"** na linha da decoração
2. Se usuário comum: clique em **"Calcular"** para ver o preço
3. Digite quantos **dias** deseja alugar
4. O sistema calcula o valor automaticamente

### 5. **Devolver uma Decoração** (Apenas Admin)
1. Na tabela, procure uma decoração com status **"Indisponível"**
2. Clique em **"Devolver"** (amarelo)
3. A decoração voltará para "Disponível"

### 6. **Calcular Previsão de Aluguel**
1. Escolha o **tamanho** da decoração
2. Escolha o **tipo**
3. Digite a **quantidade de dias**
4. Clique em **"Calcular Previsão"**
5. O sistema mostrará o valor total

---

## 📁 Estrutura de Pastas do Projeto

```
Decor__Puffy-main/
├── public/              # Arquivos públicos (login, index)
│   ├── login.php       # Página de login
│   └── index.php       # Página principal
├── views/              # Templates HTML
│   └── template.php    # Template principal
├── data/               # Arquivos de dados
│   ├── decoracoes.json # Lista de decorações
│   └── usuarios.json   # Lista de usuários
├── config/             # Configurações
│   └── config.php      # Variáveis globais
├── services/           # Lógica de negócio
│   ├── auth.php        # Autenticação
│   └── locadora.php    # Gerenciamento de decorações
├── models/             # Modelos de dados
│   ├── decoracao.php
│   ├── niver.php
│   ├── casamento.php
│   ├── forma.php
│   └── materiais.php
├── img/                # Imagens da decoração
├── uploads/            # Imagens enviadas (criada automaticamente)
├── css/                # Estilos CSS
├── script/             # Scripts JavaScript
└── README.md           # Documentação principal
```

---

## ⚠️ Problemas Comuns

### ❌ **"Página não encontrada" ou "localhost recusou a conexão"**
- Apache não está rodando
- Solução: Clique em **"Start"** no XAMPP Control Panel

### ❌ **As imagens não aparecem**
- Verificar se a pasta `uploads/` existe
- As imagens precisam estar na pasta `img/` ou `uploads/`

### ❌ **Login não funciona**
- Verifique se digitou corretamente o **usuário** e a **senha**
- O email para admin deve estar **vazio**
- MySQL precisa estar rodando

### ❌ **"500 Internal Server Error"**
- Verifique a pasta `data/` e se os arquivos `.json` existem
- Conferir permissões de escrita na pasta `data/`

---

## 🔄 Dados do Sistema

### Decorações Padrão
O sistema já vem com 7 decorações cadastradas:
- Decoração do Deadpool (Pequeno - Disponível)
- Decoração do Homem-Aranha (Pequeno - Indisponível)
- Decoração Safari (Grande - Indisponível)
- Decoração Noivado (Médio - Indisponível)
- Decoração Noivado Branco (Grande - Disponível)
- Lewis Hamilton (Pequeno e Médio)

### Usuários Padrão
O sistema já vem com 14 usuários cadastrados (veja `data/usuarios.json`).

---

## 💡 Dicas Importantes

1. **Logout**: Clique no botão **"Sair"** no canto superior direito
2. **Busca**: Existe um campo de busca no topo (em desenvolvimento)
3. **Responsivo**: O sistema funciona em desktop e mobile
4. **Dados Persistem**: Tudo é salvo em `data/decoracoes.json` e `data/usuarios.json`
5. **Imagens Novas**: Quando você adiciona uma decoração com imagem, ela fica em `uploads/`

---

## 🎯 Próximos Passos

Após deixar o sistema funcionando, você pode:
- ✏️ Adicionar mais decorações
- 👥 Registrar novos usuários
- 🎨 Customizar as cores e estilos (pasta `css/`)
- 📱 Testar em diferentes navegadores

---

**Pronto! Agora você já sabe como usar o sistema! 🎉**
