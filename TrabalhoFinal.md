TODO:

- [ ] Criar um arquivo de configuração `roteadores.txt` para IPs iniciais
- [ ] Criar tabela de roteamento (Lógica)
  - [ ] Deve ter campos de origem, destino e métrica
  - [ ] Deve ter um método "comparar" ou "atualizar", que recebe uma nova entrada
    - [ ] Se a rota não exisir
      - [ ] deve ser adicionada
      - [ ] a métrica incrementada em 1
      - [ ] o endereço de origem deve ser o endereço do roteador que enviou a linha
    - [ ] Se existir e a métrica for menor
      - [ ] a métrica deve ser atualizada
      - [ ] o endereço de origem deve ser o endereço do roteador que enviou a linha
    - [ ] Se uma rota deixar de existir
      - [ ] deve ser removida
  - [ ] Deve ter um método "print" que imprime a tabela para o usuário
- [ ] Criar classe para tratamento de mensagens
  - [ ] Deve possuir tres subclasses, uma para mensagens de roteamento, outra para mensagens de anuncio e outra para mensagens de texto
  - [ ] Deve ter um método "parse" que recebe uma mensagem e a transforma em um objeto
  - [ ] Deve ter um método "serialize" que transforma um objeto em uma mensagem
  - [ ] Mensagens de roteamento devem estar no formato "@[destino]-[metrica]"
  - [ ] Mensagens de anúncio devem estar no formato "*[origem]"
  - [ ] Mensagens de texto devem estar no formato "![origem];[destino];[texto]"
- [ ] Utilizar socket UDP na porta 9000