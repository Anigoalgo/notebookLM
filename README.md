# notebookLM
Para fazer um teste automatizado corretamente, você deve seguir princípios de estruturação de código, estratégias de organização de suítes de testes e boas práticas de design. Com base nos documentos fornecidos, aqui está um resumo estruturado:
### 1. Estrutura Básica de um Teste (Padrão Triple A)
Todo teste automatizado eficaz deve ser organizado em três etapas claras para garantir legibilidade e manutenção:
 * **Montar o cenário (Arrange):** Definir os dados de entrada e o estado inicial (ex: criar usuários ou configurar banco de dados).
 * **Executar a ação (Act):** Invocar a funcionalidade ou o método específico que será validado.
 * **Validar a saída (Assert):** Comparar o resultado obtido com o esperado através de asserções (ex: assertEquals).
### 2. Estratégia de Organização: A Pirâmide de Testes
Para uma automação eficiente, utilize o modelo da pirâmide, que define a distribuição ideal de esforço:
 * **Base (Testes de Unidade):** Devem ser a grande maioria. São rápidos, testam métodos isolados e dão feedback imediato ao desenvolvedor.
 * **Meio (Testes de Integração):** Validam a comunicação entre diferentes componentes ou sistemas externos (ex: banco de dados).
 * **Topo (Testes de Sistema/E2E):** Garantem que o sistema funciona como um todo ("tudo ligado"), simulando a experiência do usuário.
### 3. Boas Práticas e Design
 * **Page Objects:** Em testes de sistema (como Selenium), crie classes que representam as páginas da aplicação. Isso evita que mudanças na interface quebrem múltiplos testes, concentrando a lógica de manipulação em um só lugar.
 * **Abordagem Shift-Left:** Inicie os testes o mais cedo possível no ciclo de desenvolvimento (SDLC), como revisando requisitos antes mesmo da implementação, para encontrar defeitos precocemente.
 * **Independência:** Use anotações como @Before para preparar o ambiente antes de cada teste, garantindo que o resultado de um teste não dependa de outro.
 * **Cuidado com Casos de Borda:** Não teste apenas o "caminho feliz". É essencial validar listas vazias, valores nulos e exceções.
### 4. O que evitar
 * **Teste Exaustivo:** Testar todas as combinações é inviável. Use técnicas como o **Particionamento de Equivalência** para selecionar casos representativos.
 * **Ignorar a Cobertura:** Embora 100% de cobertura nem sempre seja viável ou necessário, monitore-a para identificar áreas críticas não testadas.
 * **Acoplamento Excessivo:** Evite que o teste dependa de detalhes internos de implementação que mudam frequentemente.
### 5. Ferramentas Comuns
 * **JUnit:** Muito utilizado para testes de unidade e integração em Java.
 * **Selenium:** Framework para automatizar interações no navegador em testes de sistema.
