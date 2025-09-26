# 📧 Configuração do Template EmailJS - InnoHub

## 🎯 Template Personalizado Criado

Criei um template de email personalizado que combina perfeitamente com o design dos cards do seu site InnoHub.

## 🔧 Como Configurar no EmailJS:

### Passo 1: Acessar o EmailJS
1. Vá para [https://www.emailjs.com/](https://www.emailjs.com/)
2. Faça login na sua conta
3. Acesse o dashboard

### Passo 2: Criar/Editar o Template
1. No menu lateral, clique em **"Email Templates"**
2. Clique em **"Create New Template"** ou edite o existente
3. Use o ID: `template_b089ucx`

### Passo 3: Configurar o Template

**Subject (Assunto):**
```
🚀 Nova mensagem de contato - InnoHub: {{subject}}
```

**Content (Conteúdo HTML):**
Cole todo o conteúdo do arquivo `template-emailjs.html` que foi criado.

### Passo 4: Variáveis do Template
Certifique-se de que estas variáveis estão configuradas:
- `{{user_name}}` - Nome do cliente
- `{{user_email}}` - Email do cliente  
- `{{phone}}` - Telefone do cliente
- `{{subject}}` - Assunto da mensagem
- `{{message}}` - Mensagem do cliente
- `{{current_date}}` - Data atual (opcional)
- `{{current_time}}` - Horário atual (opcional)

## 🎨 Características do Template:

### ✨ **Design Moderno:**
- **Gradientes** que combinam com o site
- **Cards elegantes** similares aos do site
- **Ícones** para cada seção
- **Sombras e bordas** arredondadas
- **Animações** sutis no hover

### 📱 **Responsivo:**
- **Mobile-first** design
- **Adaptação automática** para todas as telas
- **Botões** que se ajustam ao tamanho da tela

### 🎯 **Funcionalidades:**
- **Botão de resposta** direto para o cliente
- **Botão de ligação** com o telefone
- **Informações organizadas** em cards
- **Footer** com dados da empresa
- **Timestamp** da mensagem

### 🎨 **Cores e Estilo:**
- **Header:** Gradiente azul/roxo (#667eea → #764ba2)
- **Cards:** Fundo cinza claro (#f8f9fa)
- **Bordas:** Azul principal (#667eea)
- **Botões:** Gradientes verdes e azuis
- **Texto:** Cinza escuro (#333)

## 📋 Estrutura do Template:

```
┌─────────────────────────────────────┐
│           🚀 InnoHub               │
│    Nova mensagem de contato        │
├─────────────────────────────────────┤
│  👤 Informações do Cliente         │
│     • Nome: {{user_name}}          │
│     • Email: {{user_email}}        │
│     • Telefone: {{phone}}          │
│     • Assunto: {{subject}}         │
├─────────────────────────────────────┤
│  💬 Mensagem                       │
│     {{message}}                    │
├─────────────────────────────────────┤
│  [📧 Responder] [📞 Ligar]         │
├─────────────────────────────────────┤
│  📅 Data e Horário                 │
├─────────────────────────────────────┤
│        Footer da Empresa           │
└─────────────────────────────────────┘
```

## 🚀 Como Testar:

1. **Configure o template** no EmailJS com o HTML fornecido
2. **Execute o projeto:** `npm run dev`
3. **Acesse a seção Contato** no site
4. **Preencha o formulário** com dados de teste
5. **Envie a mensagem** e verifique o email recebido

## 📧 Resultado Final:

O email recebido terá:
- ✅ **Visual profissional** combinando com o site
- ✅ **Informações organizadas** em cards elegantes
- ✅ **Botões de ação** para responder e ligar
- ✅ **Design responsivo** para todos os dispositivos
- ✅ **Identidade visual** da InnoHub

## 🔧 Configurações Adicionais:

### Para adicionar data/hora automática:
No JavaScript, você pode adicionar:
```javascript
const formData = {
  user_name: document.getElementById('user_name').value,
  user_email: document.getElementById('user_email').value,
  subject: document.getElementById('subject').value,
  phone: document.getElementById('phone').value,
  message: document.getElementById('message').value,
  current_date: new Date().toLocaleDateString('pt-BR'),
  current_time: new Date().toLocaleTimeString('pt-BR')
};
```

O template está pronto e funcionará perfeitamente com o seu formulário! 🎉
