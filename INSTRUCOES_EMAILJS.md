# 📧 Configuração do EmailJS - InnoHub

## ✅ O que já foi configurado:

1. **EmailJS adicionado ao projeto** ✅
2. **Formulário de contato configurado** ✅
3. **JavaScript funcional implementado** ✅
4. **Template de email criado** ✅

## 🔧 Como configurar o template no EmailJS:

### Passo 1: Acessar o EmailJS
1. Vá para [https://www.emailjs.com/](https://www.emailjs.com/)
2. Faça login na sua conta
3. Acesse o dashboard

### Passo 2: Configurar o Template
1. No menu lateral, clique em **"Email Templates"**
2. Clique em **"Create New Template"**
3. Use o ID: `template_b089ucx` (já configurado no código)

### Passo 3: Configurar o Conteúdo do Template

**Subject (Assunto):**
```
Nova mensagem de contato - InnoHub: {{subject}}
```

**Content (Conteúdo HTML):**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Novo Contato - InnoHub</title>
    <style>
        body {
            font-family: 'Roboto', Arial, sans-serif;
            line-height: 1.6;
            color: #333;
            background-color: #f8f9fa;
            margin: 0;
            padding: 20px;
        }
        
        .email-container {
            max-width: 600px;
            margin: 0 auto;
            background: white;
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }
        
        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 30px;
            text-align: center;
        }
        
        .header h1 {
            margin: 0;
            font-size: 28px;
            font-weight: 700;
        }
        
        .header p {
            margin: 10px 0 0 0;
            opacity: 0.9;
        }
        
        .content {
            padding: 30px;
        }
        
        .contact-card {
            background: #f8f9fa;
            border-radius: 8px;
            padding: 20px;
            margin: 20px 0;
            border-left: 4px solid #667eea;
        }
        
        .contact-card h3 {
            color: #667eea;
            margin: 0 0 15px 0;
            font-size: 18px;
            font-weight: 600;
        }
        
        .field {
            margin: 15px 0;
            padding: 10px;
            background: white;
            border-radius: 5px;
            border: 1px solid #e9ecef;
        }
        
        .field-label {
            font-weight: 600;
            color: #495057;
            margin-bottom: 5px;
            display: block;
        }
        
        .field-value {
            color: #333;
            word-wrap: break-word;
        }
        
        .message-field {
            background: #f8f9fa;
            border: 1px solid #e9ecef;
            border-radius: 5px;
            padding: 15px;
            margin: 15px 0;
        }
        
        .message-field .field-label {
            color: #667eea;
            font-weight: 600;
            margin-bottom: 10px;
        }
        
        .message-content {
            background: white;
            padding: 15px;
            border-radius: 5px;
            border: 1px solid #e9ecef;
            white-space: pre-wrap;
        }
        
        .footer {
            background: #343a40;
            color: white;
            padding: 20px;
            text-align: center;
        }
        
        .footer p {
            margin: 0;
            opacity: 0.8;
        }
        
        .cta-button {
            display: inline-block;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 12px 30px;
            text-decoration: none;
            border-radius: 25px;
            font-weight: 600;
            margin: 20px 0;
            transition: transform 0.2s;
        }
        
        .timestamp {
            color: #6c757d;
            font-size: 14px;
            text-align: center;
            margin-top: 20px;
            padding-top: 20px;
            border-top: 1px solid #e9ecef;
        }
    </style>
</head>
<body>
    <div class="email-container">
        <div class="header">
            <h1>🚀 InnoHub</h1>
            <p>Nova mensagem de contato recebida</p>
        </div>
        
        <div class="content">
            <div class="contact-card">
                <h3>📋 Informações do Cliente</h3>
                
                <div class="field">
                    <span class="field-label">👤 Nome:</span>
                    <span class="field-value">{{user_name}}</span>
                </div>
                
                <div class="field">
                    <span class="field-label">📧 Email:</span>
                    <span class="field-value">{{user_email}}</span>
                </div>
                
                <div class="field">
                    <span class="field-label">📱 Telefone:</span>
                    <span class="field-value">{{phone}}</span>
                </div>
                
                <div class="field">
                    <span class="field-label">📝 Assunto:</span>
                    <span class="field-value">{{subject}}</span>
                </div>
            </div>
            
            <div class="message-field">
                <span class="field-label">💬 Mensagem:</span>
                <div class="message-content">{{message}}</div>
            </div>
            
            <div style="text-align: center;">
                <a href="mailto:{{user_email}}" class="cta-button">📧 Responder Cliente</a>
            </div>
            
            <div class="timestamp">
                📅 Recebido em: {{current_date}}
            </div>
        </div>
        
        <div class="footer">
            <p>© 2024 InnoHub - Agência de Marketing Digital</p>
            <p>Este email foi enviado automaticamente através do formulário de contato do site.</p>
        </div>
    </div>
</body>
</html>
```

### Passo 4: Configurar as Variáveis
No EmailJS, certifique-se de que as seguintes variáveis estão configuradas:
- `{{user_name}}` - Nome do cliente
- `{{user_email}}` - Email do cliente  
- `{{phone}}` - Telefone do cliente
- `{{subject}}` - Assunto da mensagem
- `{{message}}` - Mensagem do cliente
- `{{current_date}}` - Data atual (opcional)

### Passo 5: Salvar e Testar
1. Clique em **"Save"** para salvar o template
2. Teste o formulário no seu site
3. Verifique se o email está sendo recebido corretamente

## 🎯 Funcionalidades Implementadas:

✅ **Formulário funcional** com validação
✅ **Feedback visual** (loading, sucesso, erro)
✅ **Notificações** elegantes
✅ **Template responsivo** baseado no design do site
✅ **Integração completa** com EmailJS

## 🚀 Como testar:

1. Execute `npm run dev` no terminal
2. Acesse o site no navegador
3. Vá para a seção "Contato"
4. Preencha o formulário
5. Clique em "Enviar Mensagem"
6. Verifique se recebeu o email

## 📱 Recursos do Template:

- **Design responsivo** que funciona em todos os dispositivos
- **Cores e estilo** consistentes com o site InnoHub
- **Informações organizadas** em cards elegantes
- **Botão de resposta** direto para o cliente
- **Timestamp** da mensagem
- **Footer** com informações da empresa

O formulário está 100% funcional e pronto para uso! 🎉
