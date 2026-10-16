## Laboratório 01: Endereçamento IP e sub-redes

**Equipamento:** Roteador Huawei WiFi AX3S

### Objetivo
Alterar o endereço IP e a faixa da rede local do roteador para evitar
conflito com a rede do modem, e configurar servidores DNS públicos.

### O que foi feito
1. **Alteração do IP e da rede local (LAN):** o IP do roteador foi
   alterado de IP dinâmico para IP estático(para teste), com máscara `255.255.255.0`.
   Assim, o roteador e o modem ficam em redes diferentes, e é possível
   acessar a página de configuração dos dois equipamentos. Se houver
   problema no roteador, ainda consigo acessar o modem diretamente.
2. **Configuração de DNS:** foram definidos os DNS do Google
   (8.8.8.8) e da Cloudflare (1.1.1.1), buscando
   maior velocidade e estabilidade na resolução de nomes.

### Testes realizados
- `ipconfig` para confirmar IP, gateway e DNS recebidos
- `ping` para o gateway e para 8.8.8.8
- `nslookup google.com` para validar o DNS
- Acesso às páginas de administração do modem e do roteador

### Aprendizados
- Dois equipamentos na mesma faixa de IP geram conflito.
- O DNS traduz nomes em IPs e pode ser trocado na rede toda pelo roteador.
