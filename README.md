# atvsql

# Atividade_SQLAdelson

1. Selecione todos os dados dos países da tabela_paises;
 
select * from  tabela_paises;

## Resultado esperado

![image](https://github.com/Mylenacm/atvsql/assets/145984011/b9cebc48-084e-4b26-aa70-52f62a9a8193)

2. Selecione todas as cidades cujo país seja brazil;

select cidade 
from tabela_paises 
where pais = 'Brazil';

## Resultado esperado

![image](https://github.com/Mylenacm/atvsql/assets/145984011/a806d5ed-54fd-4afd-9e6d-a44b58ace719)

3. Selecione todas as cidades cuja região(estado) é ceará;

select cidade 
from tabela_paises 
where regiao = 'Ceará';

## Resultado esperado

![image](https://github.com/Mylenacm/atvsql/assets/145984011/85e4858c-8b24-4073-9005-ebd9d388c34e)

4. Utilize a função count para saber quantas regiões(estados) existem na China,
utilize também o group by;

select count(*) as quantidade_regioes 
from tabela_paises 
where pais = 'China' group by regiao;

## Resultado esperado

![image](https://github.com/Mylenacm/atvsql/assets/145984011/07d250ff-f7f1-4abb-a0f8-819f1d4fc239)

5. Quais regiões, diferentes, existem no Canadá?

select distinct regiao, count(*) as quantidade_regioes 
from tabela_paises 
where pais = 'Canada' group by regiao;

## Resultado esperado

![image](https://github.com/Mylenacm/atvsql/assets/145984011/78390056-7182-4e7e-bc59-78b7880f5f79)

6. Quantos países diferentes existem na tabela 'tabela_paises';

select count(distinct pais) as paises_distintos
from tabela_paises;

## Resultado esperado

![image](https://github.com/Mylenacm/atvsql/assets/145984011/1c3789b7-3b96-4f6b-9383-af0ac11ca2d6)

7. Quantas cidades diferentes existem no brazil;

select count(distinct cidade) as cidades_diferentes 
from tabela_paises 
where pais = 'Brazil';

## Resultado esperado

![image](https://github.com/Mylenacm/atvsql/assets/145984011/ff36b75a-8d3e-4601-bcb3-2ccdc66a770b)

8. Selecione os países e quantas regiões cada país possui;

select pais, count(distinct regiao) as quantidade_regioes 
from tabela_paises group by pais;

## Resultado esperado

![image](https://github.com/Mylenacm/atvsql/assets/145984011/8e80449f-c8e9-4c38-bddc-5200d257a605)

9. Quantas pessoas com nome começando em 'João' existem no banco?

select count(*) as quantidade_pessoas 
from tabela_paises 
where nome like 'João%';

## Resultado esperado

![image](https://github.com/Mylenacm/atvsql/assets/145984011/9b68f45e-81c6-47ef-98bd-1ccb936a2fb2)

10. Quantas pessoas têm o nome John?

select count(*) as quantidade_john
from tabela_paises
where nome like  'John%';

## Resultado esperado

![image](https://github.com/Mylenacm/atvsql/assets/145984011/1e9a0874-f651-4615-8445-14f94fb5d12c)

11. Ordene os nomes dos países sem repetição em ordem alfabética;

select distinct pais from tabela_paises 
order by pais;

## Resultado esperado

![image](https://github.com/Mylenacm/atvsql/assets/145984011/1fbacec5-4d99-489a-afbe-41c7da3dd632)

