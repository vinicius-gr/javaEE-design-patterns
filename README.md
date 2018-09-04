# About

This Readme file intends to be an abstract of the *Modern Java EE Design Patterns* by *Markus Eisele* published by *O'Rilley*. The purpose of making an abstract of this book is to not only solidify my knowlegde of the read but to also be a source of consultation for future questions and challanges. I don't learn by just reading something so writing along helps a lot. 

# Chapter 1 - Enterprise Development Today

Este capítulo começa discutindo brevemente as razões pelas quais sistemas tão complexos surgem nas grandes organizações, apontando a necessidade de padronização e incapacidade de mover-se rapidamente como as principais causas. Além disso é também explicado como a tecnologia Java EE se tornou tão importante no contexto corporativo e quais foram seus propósitos. O Java EE não foi criado para inovação. O paradoxo surge justamente da necessidade de inovação que o mercado exige. Tipicamente 5 a 10 anos é o tempo necessário para a indústria produzir uma nova tecnologia disruptiva.

## Enterprise Goals and Objectives

Operações e decisões de compra focam em gerar resultados a curto prazo e redução de custos.

## Resistant to Change and Economically Efficient

Operações geralmente vencem a batalha contra os negócios o que resulta nas tecnologias de ponta cada vez mais distante do que as empresas permitem que os desenvolvedores usem para trabalhar.

## Developers Left Alone

## Technology-Centric Versus Business-Centric

A maioria das empresas são business-centric e tratam TI e operações como centros de custos. Isto vem mudando.

## Aims and Scope

O foco principal é entender os padrões de projeto Java EE, e trabalhar com os novos paradigmas de desenvolvimento, como micro-serviços, DevOps e operações baseadas em nuvem.

# Chapter 2 - History of Java EE

O surgimento da Internet e dos browsers levou a implementação do primeiro servidor Java bem como as especificações  Servlets e JSPs. Essas duas se tornaram a fundação do J2EE. Foi renomeada em 2006 para Java EE. Todas as vantagens do Java EE vieram com uma desvantagem. Ainda é possível ver muitas aplicações baseadas em Java EE 5, 2006.

## Mistakes We Made

A aplicações seguiam o padrão do livro Core J2EE Patterns e foram separadas em três camadas principais: Presentation, Business e Integration. A camada Presentation era empacotada em Web Application Archives (WARs) enquanto as camadas Business e Integration iam para Java Archives (JARs). Juntas formavam um Enterprise Archive (EAR). 
Essas especificações foram suficientes para desenvolver aplicações monolíticas. Essas aplicações podiam ser escaladas com ajuda de mais instâncias e um load balancer.
Tudo era muito acoplado, as aplicações exigiam testes criteriosos. Uma nova versão era lançada uma ou duas vezes no ano. A aplicações eram muito mais do que os artefatos escritos: também consistia de incontáveis deployment descriptors e server configuration files, além de propriedades para ambientes de terceiros.
Com o tempo, os monolitos foram mantidos sobre controle.

## Evolution Continues with ESBs

Surgiu então o enterprise service vus (ESB) prometendo entregar reusabilidade, ainda sendo centralizado. Todas as aplicações precisavam ser fatiadas e reconstruídas para suportar exchangeable services. Service-oriented architectures (SOA) foram o novo paradigma. Só que a interface escolhida geralmente era web services (WS). WSs trasportam dados entre sistemas transformando-os em XML e fazem o transporte utilizando o Simple Object Access Protocol (SOAP). Isso trouxe muito mais código e descritores para os projetos.
Os desenvolvedores passaram a ter muito trabalho conectando as diferentes partes da aplicação.
O que era monolítico e difícil de testar se tornou distribuído e mais difícil ainda de testar.

## Challanges and Lessons Learned

A indústria aprendeu a gerir os projetos de maneira diferente. Abordagens iterativas e ágeis se tornaram populares.

## DevOps: Highly Effective Teams

Outra parte importante do sucesso na entrega foi a aproximação entre operações e desenvolvimento. DevOps é sobre cultura de time. Procura aumentar comunicação e colaboração entre desenvolvedores, operações e outros profissionais de TI. Software de alta qualidade mais rapidamente em Produção.

## Microservices: Lightweight and Fast

Componentes centralizados nao cabem mais no paradigma. Ao invés de roteamento inteligente e transformações, micro-serviços usam rotas simples e encapsulam lógica no endpoint. Não há um tamanho definido para eles. Tratam-se de haver um único propósito para cada um. Ainda sim não são completamente perfeitos para as operações. 

## Containers: Fully Contained Applications
