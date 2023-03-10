## ...em andamento
# Mentoria Typescript da plataforma DIO - Digital Innovation One

## Do que você vai precisar
Ferramentas necessárias:  
* Do Node instalado na sua máquina  
* Instalar o typescript usando o npm (npm install -g typescript)
    * É interessante que ele seja instalado de forma global, para que o usuário possa usar a biblioteca a qualquer momento e em qualquer projeto para fazer testes rápidos com o TS.
* De uma IDE como o visual studio code  

## (Grande parte do texto é do especialista da mentoria)

Requisitos técnicos:  
* Lógica de programação
* Mas é melhor ainda se tiver um conhecimento básico de javascript  

## Sobre o tsconfig.json  
* Algumas configurações e funcionalidades legais são:
    1. Opções básicas:
        * target
            * Define para qual versão do ECMAScript o typescript vai ser convertido
        * lib
            * Define quais bibliotecas vão vir por default com o TS. Isso é bacana caso o TS esteja sendo usado no backend e a iteração com o DOM não é necessária. Como teste, tentem remover as bibliotecas do DOM e olhem seu código enchendo de erros porque não sabe o que é um document
        * sourceMap
            * Cria arquivos .map.js que geram uma cópia do seu arquivo TS no source do browser (aquele do inspect). Podem ser debugados via breakpoint direto no browser e são uma excelente ajuda, já que o código compilado de JS é menos legível que o TS.
        * outDir
            * Pasta para onde seus arquivos JS serão enviados
        * rootDir
            * Pasta de onde seus arquivos TS serão coletados. Pode ser necessário inserir a opção include fora do *compilerOptions* com a pasta *src* inclusa
    2. Opções de checagem de tipo:
        * strict
            * Marca todas opções de checagem de tipo como verdadeiras. Ideal caso seja a intenção do usuário ter o código mais consistente possível
        * noImplicitAny
            * Levanta erro caso variáveis não estejam tipadas. Caso essa seja a intenção, um "any" tem que ser explicitamente tipado
        * strictNullChecks
            * Pode levantar erro caso uma variável em uso seja potencialmente nula. 
                * Ex: um botão que foi buscado usando um getElementById que não necessariamente vai encontrar um elemento é usado para escutar um evento.
    3. Outras opções
        * noUnusedLocals
            * Levanta erro sempre que uma variável local não está sendo utilizada, como um let dentro de uma função
        * nuUnusedParameters
            * Mesmo caso de noUnusedLocals, mas para parâmetros de função
        * noImplicitReturns
            * Levanta um erro caso uma função tenha caminhos que retornam valor e outros que não retornam
    4. Existem outras regras e explicações mais elaboradas na documentação oficial (https://www.typescriptlang.org/tsconfig)
   

