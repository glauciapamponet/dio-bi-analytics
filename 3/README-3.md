# Desafio Modulo 3 - Processamento de Dados Simplificado com Power BI

### Simbologia:
- **<<:** junão externa à esquerda (left join)
- **>>:** junção externa à direita (right join)
- **><:** junção interna exclusiva (inner join)

## 1 - Mesclagens e junções

- Junção de tablea de projetos e empregados envolvidos (employee >< words_on >< project>): busca de visualização das horas gastas em cada projeto por cada empregado. A junção fortalece o trabalho de agregação para o relatório, que deve extraír as estatisticas das horas gastas para cada projeto e por cada funcionário.

- Junção solicitada no desafio -  tabelas de empregados e departamento a partir da tabela de empregados (employee >< departament): foi mantidas as informações base de cada tabela e excluidas as relaçõeos e as colunas repetidas.

- Junção solicitada no desafio -  tabela de colaboradores e seus respectivos superiores (employee << superior): a junção a esquerda foi justificada pela existencia do gerente superior que não possui superiores. Sendo assim seu dado original era null, porem ele ainda faz parte da lista de colaboradores.

- Junção solitidada no desafio - tabela de departamentos e localização (dept >< locations): realizada com a mesclagem em nova tabela, mas sem identificador proprio pois, os departamentos se repetem em numero. A identificação teria que ser feita pela união dos nomes de localização e departamento. Tanto esse quanto os outros casos de junção realizados não podem ser efetuados usando Acrescentar Consultas, pois trata-se de relação de chave estrangeira entre as tabelas. Acrescentar colunas, nesse caso, não traria resultados coerentes nem por causa da relação de tabelas, mas também porque não possuem colunas compatíveis.

## 2 - Tratamento de dados

- Junção de nomes dos empregados
- Separação do endereço dos empregados
- Tipos de formato de numeros (decimal)
- Tratamento de null para o gerente superior (null = 0)
- Nomeação de colunas em formato intuitivo
<img src=".\trat-employee.png">

<br>

- União dos nomes de departamento e localização
<img src=".\dept-locations.png" >

<br>

## 3 - Agregação e qualidade das colunas
- Agregação da quantidade de funcionarios para cada superior, usando a função "Agregar Por"
<img src=".\agreg-employee-sup.png">

- Estatisticas de coluna e qualidade das amostras
<img src=".\employee-workson-project.png">

