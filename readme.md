---
Este documento contém as respostas para o teste de Analista de Suporte, que simula o dia a dia dessa função na Dadosfera.
---

# Desafio Dadosfera - Analista de Suporte

## links:

    - Apresentação PDF: https://drive.google.com/file/d/1hpmyBzVFP6fyZt1hPjSeujn1a66H99MM/view?usp=sharing
    - Apresentação Notion: https://www.notion.so/Desafio-Dadosfera-Analista-de-Suporte-9f3960d1893149cab6774658da89e0f5?pvs=4
    - Vídeo de apresentação do case: https://youtu.be/e9fuzJpYans

## Item Troubleshooting

**Contexto:**

Um cliente interno, o time de Liderança, está enfrentando dificuldades ao tentar importar dados de uma planilha do Google Sheets para a Dadosfera. O erro ocorreu durante a pipeline de coleta.

**Resposta ao Cliente:**

Olá [Nome do Cliente],

Obrigado por entrar em contato. Entendo que você está enfrentando dificuldades ao importar os dados do Google Sheets para a Dadosfera. Vamos trabalhar juntos para resolver esse problema.

**Passos para Resolução:**

1. **Verificar o Formato dos Dados:**
   - Certifique-se de que a planilha esteja formatada de acordo com as especificações da Dadosfera. Todos os campos obrigatórios devem estar preenchidos e as colunas devem seguir o mesmo padrão da base de dados da plataforma
2. Identificaçao do problema:
   - Após uma breve análise nos logs de importação dos dados, foi identificado o seguinte problema: Encontra-se possíveis problemas com o tipo de dados em algumas células da planilha (PerformanceRating e EmployeeNumber), indicando que esses campos podem ter valores inesperados ou formatados de maneira incorreta. Após uma breve busca foram identificados valores nulos e em formatos errados nas céluls 202 e 205 da aba de PerformanceRating.
3. **Alteração no Dataset:**
   - Recomendo revisar os tipos de dados em cada coluna da planilha. Por exemplo, certifique-se de que as colunas de PerformanceRating e EmployeeNumber estejam preenchidas com o formato e valor correto nas células 202 e 205.

**Outros Cuidados ao Importar Dados:**

1. **Limpar Dados Inconsistentes:**
   - Remova quaisquer linhas duplicadas ou células com valores inválidos. O uso de funções do Google Sheets como `UNIQUE()` e `CLEAN()` pode ajudar a identificar e resolver esses problemas.
2. **Limitar o Tamanho do Dataset:**
   - Se a planilha for muito grande, considere dividir os dados em conjuntos menores para facilitar a importação e evitar sobrecarga na pipeline de coleta.
3. **Utilizar a Documentação para Baixar Logs:**
   - Por favor, baixe os logs de importação para identificar quaisquer mensagens de erro específicas. Isso pode ser feito através da documentação da Dadosfera, na seção Pipelines/pipelines-status, link: https://docs.dadosfera.ai/docs/status-da-pipeline-copy.

- **Validação Prévia dos Dados:**
  - Antes de importar, use ferramentas de validação de dados para garantir que não haja erros de digitação ou inconsistências.
- **Configurações de Compartilhamento:**
  - Verifique se a planilha do Google Sheets está corretamente compartilhada com as permissões necessárias para que a Dadosfera possa acessá-la.
- **Atualização da Documentação:**
  - Mantenha a documentação de integração atualizada com quaisquer novos requisitos ou mudanças na plataforma Dadosfera.

Espero que essas orientações sejam úteis. Se continuar a enfrentar problemas, por favor, envie-me os logs de erro e estarei pronto para ajudar a resolver.

Atenciosamente,

Willian Souza

---

## Item Processos Internos

**Contexto:**

A Dadosfera está passando por um upgrade para uma nova plataforma de gerenciamento de diretório em nuvem, com SSO e recursos de ciclo de vida do usuário. Isso impacta o caso anterior?

**Organização e Implementação da Transição:**

1. **Avaliação Inicial:**
   - **Mapeamento de Processos:** Identificar todos os processos que serão afetados pela mudança, incluindo o fluxo de importação de dados e acessos dos clientes.
2. **Planejamento da Transição:**
   - **Comunicação com Stakeholders:** Manter todas as partes interessadas informadas sobre o cronograma e o impacto das mudanças.
   - **Definição de Prazos:** Estabelecer datas para cada etapa do processo de migração, desde a preparação até a finalização.
3. **Implementação Técnica:**
   - **Configuração do SSO:** Integrar o novo SSO com a plataforma Dadosfera para garantir uma experiência de login segura e simplificada para os usuários.
   - **Gerenciamento do Ciclo de Vida do Usuário:** Configurar as políticas de criação, atualização e exclusão de usuários para que reflitam as novas práticas de segurança e eficiência.
4. **Testes e Validações:**
   - **Teste de Compatibilidade:** Verificar se a nova plataforma é compatível com os processos atuais e fazer ajustes conforme necessário.
   - **Feedback dos Usuários:** Recolher feedback dos usuários após a implementação para identificar possíveis melhorias.

**Impacto no Caso de Importação de Dados:**

- A transição para a nova plataforma de gerenciamento de diretório pode afetar o fluxo de importação de dados, especialmente se houver mudanças nas permissões de acesso. É crucial que os usuários sejam informados sobre as novas configurações e que recebam treinamento, se necessário, para garantir uma transição suave.

**Interação com a Base de Clientes:**

1. **Pré-Lançamento:**
   - **Sessões de Treinamento:** Oferecer sessões de treinamento para os usuários chave, demonstrando as novas funcionalidades e como elas afetarão suas operações diárias.
2. **Lançamento:**
   - **Comunicação Efetiva:** Enviar comunicações detalhadas para todos os usuários, explicando as mudanças e como elas devem se preparar para a transição.
3. **Pós-Lançamento:**
   - **Suporte Contínuo:** Disponibilizar canais de suporte dedicados para resolver quaisquer problemas ou dúvidas que surjam após a implementação.

Espero que esta estrutura ajude a Dadosfera a realizar uma transição suave e a melhorar a experiência do usuário com a plataforma.

Atenciosamente,

Willian Souza

## **_Boas-Práticas de Suporte_**

### Fluxo do Processo de Atendimento

1. **Início do Atendimento**
   - **Usuário:** O cliente inicia o atendimento via chat no portal da Dadosfera.
   - **IA (Chatbot):** Recebe a mensagem inicial e saúda o cliente. Coleta informações básicas para identificar a natureza do atendimento.
2. **Classificação e Coleta de Informações**
   - **IA (Chatbot):** Pergunta ao cliente sobre o problema ou a questão que ele está enfrentando.
   - **Usuário:** Fornece detalhes sobre o problema ou solicitação.
   - **IA (Chatbot):** Analisa a mensagem e determina se pode resolver a questão ou se deve encaminhar para um humano. Utiliza documentação da Dadosfera ([docs.dadosfera.ai](http://docs.dadosfera.ai/)) para buscar informações relevantes.
3. **Resolução de Problemas e Suporte**
   - **Se o problema pode ser resolvido pela IA:**
     - **IA (Chatbot):** Fornece uma resposta baseada nas informações da documentação e no conhecimento da IA.
     - **Usuário:** Recebe a resposta e confirma se o problema foi resolvido.
   - **Se o problema não pode ser resolvido pela IA:**
     - **IA (Chatbot):** Encaminha o cliente para um humano no suporte da Dadosfera.
     - **Humano (Suporte Dadosfera):** Recebe o caso com todas as informações coletadas pela IA e continua o atendimento.
4. **Interação com Suporte Humano**
   - **Humano (Suporte Dadosfera):** Fornece suporte mais detalhado, realiza diagnóstico adicional e oferece uma solução personalizada.
   - **Usuário:** Recebe o atendimento e pode fazer mais perguntas ou confirmar a resolução do problema.
5. **Feedback e Encerramento**
   - **IA (Chatbot) ou Humano (Suporte Dadosfera):** Solicita feedback do cliente sobre o atendimento.
   - **Usuário:** Fornece feedback que ajuda a melhorar o serviço.
   - **IA (Chatbot):** Finaliza a conversa e oferece links para mais informações ou ajuda adicional se necessário.

### Exemplo de Interação com IA

**Prompt do Usuário:**
"Estou tendo problemas para integrar o nosso sistema com a API da Dadosfera. Não estou conseguindo autenticar corretamente."

**Resposta da IA (Chatbot):**

> "Olá! Entendo que você está enfrentando dificuldades com a autenticação da API da Dadosfera. Para ajudá-lo melhor, posso fornecer algumas orientações gerais ou consultar a documentação específica. Por favor, me informe qual tipo de autenticação você está usando (por exemplo, Token Bearer, OAuth) e compartilhe qualquer mensagem de erro que você esteja recebendo."

**Se o usuário fornecer mais detalhes:**

**Prompt do Usuário:**
"Estou usando o Token Bearer e estou recebendo um erro 401 Unauthorized."

**Resposta da IA (Chatbot):**

> "Parece que o erro 401 Unauthorized indica que há um problema com a autenticação do Token Bearer. Aqui estão algumas etapas que você pode seguir para resolver isso:
>
> 1. Verifique se o Token Bearer está correto e não expirou.
> 2. Certifique-se de que o token está sendo enviado no cabeçalho da requisição com a chave 'Authorization'.
> 3. Confira a documentação da API [docs.dadosfera.ai](https://docs.dadosfera.ai/) para garantir que a requisição esteja configurada corretamente.
>
> Se você já verificou todos esses itens e o problema persiste, eu posso encaminhar seu caso para um especialista de suporte humano. Deseja seguir por esse caminho?"

**Prompt do Usuário:**
"Já verifiquei tudo isso. Preciso de ajuda de um especialista."

**Resposta da IA (Chatbot):**

> "Entendido. Vou encaminhar seu caso para um membro da equipe de suporte técnico que poderá oferecer uma assistência mais detalhada. Você será contatado em breve. Obrigado por sua paciência!"

Este fluxo permite que a IA ofereça uma ajuda imediata e direcionada, enquanto garante que os casos mais complexos sejam encaminhados para suporte humano, promovendo um atendimento mais eficiente e satisfatório.

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/54b57154-f3fa-40ba-a507-9568263fcfb2/7a17eeed-ff1d-4e99-af57-f536c94a7dbb/image.png)

## **_Item Consultas SQL_**

---

## Relatórios de Funcionários

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/54b57154-f3fa-40ba-a507-9568263fcfb2/dec6a4ed-e9a6-4f2b-9af5-fc684d450225/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/54b57154-f3fa-40ba-a507-9568263fcfb2/34c07266-1c90-4176-8b29-34082e10a188/image.png)

![image.png](https://prod-files-secure.s3.us-west-2.amazonaws.com/54b57154-f3fa-40ba-a507-9568263fcfb2/d392cbd2-41f1-4f19-a34c-0f83a98d3165/image.png)

### 1. Distribuição de Idade dos Funcionários

```sql
SELECT
    Age,
    COUNT(*) AS EmployeeCount
FROM
    TB__TAEZZB__EMPLOYEE
GROUP BY
    Age
ORDER BY
    Age;

```

### 2. Distribuição por Nível de Trabalho (Job Level)

```sql
SELECT
    Joblevel,
    COUNT(*) AS EmployeeCount
FROM
    TB__TAEZZB__EMPLOYEE
GROUP BY
    Joblevel;

```

### 3. Número de Funcionários por Gênero

```sql
SELECT
    Gender,
    COUNT(*) AS EmployeeCount
FROM
    TB__TAEZZB__EMPLOYEE
GROUP BY
    Gender;

```

### 4. Porcentagem de Colaboradores por Departamento

```sql
WITH total_employees AS (
    SELECT COUNT(*) AS total_count
    FROM TB__TAEZZB__EMPLOYEE
)

SELECT
    DEPARTMENT,
    COUNT(*) AS employee_count,
    ROUND(COUNT(*) * 100.0 / te.total_count, 2) AS percentage
FROM
    TB__TAEZZB__EMPLOYEE e
JOIN
    total_employees te
GROUP BY
    DEPARTMENT, te.total_count;

```

### 5. Quantidade de Colaboradores por Cargo

```sql
WITH total_employees AS (
    SELECT COUNT(*) AS total_count
    FROM TB__TAEZZB__EMPLOYEE
)

SELECT
    JOBROLE,
    COUNT(*) AS employee_count,
    ROUND(COUNT(*) * 100.0 / te.total_count, 2) AS percentage
FROM
    TB__TAEZZB__EMPLOYEE e
JOIN
    total_employees te
GROUP BY
    JOBROLE, te.total_count;

```

### 6. Análise de Over Time (Horas Extras)

```sql
SELECT
    Overtime,
    COUNT(*) AS EmployeeCount
FROM
    TB__TAEZZB__EMPLOYEE
GROUP BY
    Overtime;

```

### 7. Média de Tempo para Promoção

```sql
SELECT
    AVG(Yearssincelastpromotion) AS AvgYearsSinceLastPromotion
FROM
    TB__TAEZZB__EMPLOYEE;

```

### 8. Média de Anos na Empresa

```sql
SELECT
    AVG(Yearsatcompany) AS AvgYearsAtCompany
FROM
    TB__TAEZZB__EMPLOYEE;

```

### 9. Distribuição de Funcionários por Status Marital e Gênero

```sql
SELECT
    Maritalstatus,
    Gender,
    COUNT(*) AS EmployeeCount
FROM
    TB__TAEZZB__EMPLOYEE
GROUP BY
    Maritalstatus, Gender
ORDER BY
    Maritalstatus, Gender;

```

### 10. Número de Funcionários por Número de Empresas Trabalhadas

```sql
SELECT
    Numcompaniesworked,
    COUNT(*) AS EmployeeCount
FROM
    TB__TAEZZB__EMPLOYEE
GROUP BY
    Numcompaniesworked
ORDER BY
    Numcompaniesworked;

```

### 11. Média de Distância de casa para o trabalho

```sql
SELECT
    CASE
        WHEN Distancefromhome >= 20 THEN 'Far Work'
        ELSE 'Near Work'
    END AS WorkDistanceCategory,
    AVG(Distancefromhome) AS AverageDistanceFromHome,
    COUNT(*) AS TotalEmployees
FROM
    TB__TAEZZB__EMPLOYEE
GROUP BY
    CASE
        WHEN Distancefromhome >= 20 THEN 'Far Work'
        ELSE 'Near Work'
    END;

```

### 11. Distribuição de Educação

```sql
SELECT
    Educationfield,
    COUNT(*) AS EmployeeCount
FROM
    TB__TAEZZB__EMPLOYEE
GROUP BY
    Educationfield;

```
