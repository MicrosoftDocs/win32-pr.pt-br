---
title: Tipagem forte
description: C é uma linguagem fracamente tipada, ou seja, o compilador permite operações como atribuição e comparação entre variáveis de tipos diferentes.
ms.assetid: 5f52adcc-22b9-4b4f-b921-5996d278b10e
keywords:
- RPC de chamada de procedimento remoto, descrito, digitação de dados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae47746119f4c1b22bc066075ed484ef836fa6a68ee103e06975018a6ae49012
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924842"
---
# <a name="strong-typing"></a>Tipagem forte

C é uma linguagem fracamente tipada, ou seja, o compilador permite operações como atribuição e comparação entre variáveis de tipos diferentes. Por exemplo, C permite que o valor de uma variável seja convertido em outro tipo. A capacidade de usar variáveis de diferentes tipos na mesma expressão promove a flexibilidade, bem como a eficiência.

Uma linguagem fortemente tipada impõe restrições em operações entre variáveis de tipos diferentes. Nesses casos, o compilador emite um erro que proíbe a operação. Essas diretrizes estritas sobre os tipos de dados são projetadas para evitar possíveis erros.

A dificuldade de usar uma linguagem de tipo fraco, como C para chamadas de procedimento remoto, é que os aplicativos distribuídos podem ser executados em vários computadores diferentes com compiladores de C diferentes e diferentes arquiteturas. Quando um aplicativo é executado em apenas um computador, você não precisa se preocupar com o formato de dados interno porque os dados são manipulados de maneira consistente. No entanto, em um ambiente de computação distribuído, computadores diferentes podem usar definições diferentes para seus tipos de dados base. Por exemplo, alguns computadores definem o tipo **int** , portanto, sua representação interna é de 16 bits, enquanto outros computadores usam 32 bits. Uma arquitetura de computador, conhecida como "little endian", atribui o byte menos significativo de dados para o endereço de memória mais baixo e o byte mais significativo para o endereço mais alto. Outra arquitetura, conhecida como "big endian", atribui o byte menos significativo ao endereço de memória mais alto associado a esses dados.

As chamadas de procedimento remoto exigem um controle estrito sobre os tipos de parâmetro. Para lidar com a transmissão de dados e a conversão pela rede, o MIDL impõe estritamente as restrições de tipo para os dados transferidos pela rede. Por esse motivo, MIDL inclui um conjunto de [tipos base](base-types.md)bem definidos. O MIDL impõe rigidez de tipos, obrigando o uso de palavras-chave que definem de forma não ambígua o tamanho e o tipo de dados. O efeito mais visível de tipagem forte é que MIDL não permite variáveis do tipo **void \***.

Nos tópicos a seguir, esta seção aborda os recursos de linguagem MIDL que impõem a digitação de dados forte:

-   [Tipos base](base-types.md)
-   [Tipos assinados e sem sinal](signed-and-unsigned-types.md)
-   [Tipos de caractere largo](wide-character-types.md)
-   [Estruturas](structures.md)
-   [Uniões](unions.md)
-   [Tipos enumerados](enumerated-types.md)
-   [matrizes](arrays.md)
-   [Atributos de função](function-attributes.md)
-   [Atributos de campo](field-attributes.md)
-   [Três tipos de ponteiro](three-pointer-types.md)
-   [Atributos de tipo](type-attributes.md)

 

 




