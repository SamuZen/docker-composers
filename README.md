# Docker Compose para Teste do Hostinger Manager

Este projeto contém uma configuração simples de Docker Compose para testar o gerenciador do Hostinger.

## 🚀 Configuração

### Estrutura do Projeto
```
docker-composers/
├── docker-compose.yaml    # Configuração principal
├── html/
│   └── index.html        # Página estática de teste
└── README.md             # Este arquivo
```

### Serviços Incluídos
- **nginx:alpine** - Servidor web na porta 80
- **Volume** - Monta pasta `html/` para conteúdo estático
- **Restart Policy** - `unless-stopped`

## 📋 Como Usar

### 1. Teste Local
```bash
# Iniciar os serviços
docker-compose up -d

# Verificar status
docker-compose ps

# Acessar no navegador
http://localhost
```

### 2. Parar os Serviços
```bash
docker-compose down
```

### 3. Usar no Hostinger Manager

1. Faça upload deste projeto para um repositório Git (GitHub, GitLab, etc.)
2. No Hostinger Manager, forneça a URL do arquivo `docker-compose.yaml`
3. Exemplo de URL: `https://raw.githubusercontent.com/seu-usuario/docker-composers/main/docker-compose.yaml`

## 🌐 Acesso

Após configurar no Hostinger Manager, você poderá acessar a página de teste através do domínio fornecido pelo Hostinger.

## 📝 Personalização

Para personalizar a página:
1. Edite o arquivo `html/index.html`
2. Faça commit das alterações
3. O Hostinger Manager irá detectar as mudanças automaticamente

## 🔧 Troubleshooting

- **Erro de porta**: Verifique se a porta 80 está disponível
- **Volume não encontrado**: Certifique-se de que a pasta `html/` existe
- **Container não inicia**: Verifique os logs com `docker-compose logs`
