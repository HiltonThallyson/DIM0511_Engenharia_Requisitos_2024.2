## [Código do requisito] - Nome do requisito

**COMO** [quem vai realizar, persona]  
**QUERO** [a inteção da pessoa, o que deseja alcançar] 
**PARA** [objetivo geral, o que vou conseguir ao realizar esse requisito] 

---

**Prioridade** [informa qual a prioridade do requisito]
[prioridade selecionada]
**Requisitos relacionados** [Quais outros requisitos dependem deste requisito]
[requisitos relacionaos aqui]

## **Dados e Validações**
1. **Dados Necessários**
   //exemplo
   - **Identificador do Leito**  
     - Tipo: String  
     - Validação: Deve ser único e não vazio.  
   - **Nome ou Código da Ala**  
     - Tipo: String  
     - Validação: Deve corresponder a uma ala previamente cadastrada no sistema.  
   - **Status do Leito**  
     - Tipo: Enum (Disponível, Ocupado, Manutenção)  
     - Validação: Deve ser selecionado um status válido.  
   - **Capacidade do Leito**  
     - Tipo: Inteiro  
     - Validação: Deve ser um número positivo.  

2. **Validações Adicionais**
     //exemplo
   - Os campos obrigatórios devem ser preenchidos antes de salvar.  
   - Não é permitido associar mais de um leito ao mesmo identificador.  
   - O sistema deve verificar se a ala associada está ativa.  

---

## **Critérios de Aceitação** //Exemplos
1. **Cadastro bem-sucedido:**  
   - Quando todos os campos obrigatórios são preenchidos corretamente, o leito deve ser cadastrado e associado à ala escolhida.  

2. **Validação de identificador único:**  
   - Caso o identificador do leito já esteja em uso, o sistema deve exibir uma mensagem de erro:  
     `"O identificador do leito já está em uso. Por favor, utilize um identificador único."`  

3. **Verificação da ala:**  
   - Se a ala informada não estiver cadastrada ou ativa, o sistema deve exibir uma mensagem de erro:  
     `"A ala selecionada não é válida ou está inativa."`  

4. **Confirmação de cadastro:**  
   - Após o cadastro, o sistema deve exibir uma mensagem de confirmação:  
     `"Leito cadastrado com sucesso e associado à ala <Nome da Ala>."`  

5. **Listagem de leitos:**  
   - O leito recém-cadastrado deve aparecer na listagem de leitos disponíveis para aquela ala.  
