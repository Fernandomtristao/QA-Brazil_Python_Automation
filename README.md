# Projeto 8: Teste com Selenium - Bootcamp TripleTen

Este projeto faz parte do Bootcamp de QA da TripleTen e tem como objetivo desenvolver testes automatizados com Selenium para simular todo o processo de solicitação de um táxi no aplicativo Urban Routes.

---

## Descrição

Os testes devem cobrir todas as etapas necessárias para realizar uma corrida, incluindo seleção de endereço, escolha de plano, preenchimento de informações e envio do pedido.

---

## Objetivos dos Testes

1. Definir o endereço  
   - Inserir os campos "De" e "Para".

2. Selecionar o plano Comfort  
   - Utilizar uma condição if para verificar se a tarifa Comfort está disponível antes de selecionar.  
   - Evitar cliques desnecessários que podem causar falhas.

3. Preencher o número de telefone  
   - Utilizar o método retrieve_phone_code() do arquivo helpers.py para recuperar o código SMS.

4. Adicionar um cartão de crédito  
   - Preencher os campos do cartão corretamente.  
   - O botão "Adicionar" só fica habilitado após o campo CVV perder o foco.  
   - Simular a interação do usuário pressionando Tab ou clicando em outro local.

5. Escrever um comentário para o motorista  
   - Inserir um comentário no campo específico.

6. Pedir um cobertor e lenços  
   - Utilizar o seletor correto para clicar na opção.  
   - Executar um assert para verificar se o estado foi alterado.

7. Pedir 2 sorvetes  
   - Simular a seleção de múltiplos itens.

8. Pedir um táxi com a tarifa Comfort  
   - Adicionar uma mensagem para o motorista.  
   - Verificar se a janela modal de busca de carros aparece corretamente.

---

## Ferramentas Utilizadas

- Python 3.x
- Selenium WebDriver
- Pytest para execução dos testes
- helpers.py para funções auxiliares (ex.: recuperar código SMS)

---

## Estrutura Sugerida do Projeto

urban_routes_project/
  tests/
    test_urban_routes.py      # Arquivo principal com os testes
  pages/
    urban_routes_page.py       # Page Object Model (POM) para mapeamento de elementos
  helpers/
    helpers.py                 # Funções auxiliares (ex.: retrieve_phone_code)
  requirements.txt             # Dependências do projeto
  README.md                    # Documentação do projeto

---

## Como Executar os Testes

1. Clonar o repositório  
2. Instalar as dependências com pip install -r requirements.txt  
3. Executar os testes com pytest -v --headed  

O parâmetro --headed garante que o navegador seja aberto durante os testes.

---

## Critérios de Sucesso

- Todos os elementos do processo de pedido devem ser localizados corretamente.  
- O teste deve validar as condições esperadas (ex.: mudança de estado, modal exibido).  
- O fluxo completo da corrida deve ser concluído sem falhas.

---

## Autor

Projeto desenvolvido no Bootcamp de QA da TripleTen.

