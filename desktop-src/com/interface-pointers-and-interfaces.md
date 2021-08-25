---
title: Ponteiros de interface e interfaces
description: Ponteiros de interface e interfaces
ms.assetid: 8a8671fe-f0b2-4698-8c98-89753fffce0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abeb6040c2e55168fee1aa2c73db0056de557d0ddafaed6499e7da048dfc56de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854366"
---
# <a name="interface-pointers-and-interfaces"></a>Ponteiros de interface e interfaces

Uma instância de uma implementação de interface é, na verdade, um ponteiro para uma matriz de ponteiros para métodos , ou seja, uma tabela de funções que se refere a uma implementação de todos os métodos especificados na interface. Objetos com várias interfaces podem fornecer ponteiros para mais de uma tabela de funções. Qualquer código que tenha um ponteiro por meio do qual possa acessar a matriz pode chamar os métodos nessa interface.

Falar precisamente sobre essa indionação múltipla é inconveniente, portanto, em vez disso, o ponteiro para a tabela de funções de interface que outro objeto deve ter para chamar seus métodos é chamado simplesmente de um *ponteiro de interface*. Você pode criar manualmente tabelas de funções em um aplicativo C ou quase automaticamente usando Visual C++ (ou outras linguagens orientadas a objeto que suportam COM).

Com o suporte apropriado ao compilador (que é inerente em C e C++), um cliente pode chamar um método de interface por meio de seu nome, não sua posição na matriz. Como uma interface é um tipo, o compilador, considerando os nomes dos métodos, pode verificar os tipos de parâmetros e retornar valores de cada chamada de método de interface. Por outro lado, se um cliente usar um esquema de chamada baseado em posição, essa verificação de tipo não estará disponível, mesmo em C ou C++.

Cada interface é um contrato imutável de um grupo funcional de métodos. Você faz referência a uma interface em tempo de executar com um IID (identificador de interface globalmente exclusivo). Essa IID, que é uma instância específica de um GUID (identificador global exclusivo) compatível com o COM, permite que um cliente pergunte a um objeto precisamente se ele dá suporte à semântica da interface, sem sobrecarga desnecessária e sem a confusão que pode surgir em um sistema de ter várias versões da mesma interface com o mesmo nome.

Para resumir, é importante entender o que é uma interface COM e não é:

-   Uma interface COM não é igual a uma classe C++. A definição virtual pura não carrega nenhuma implementação. Se você for um programador do C++, poderá definir sua implementação de uma interface como uma classe, mas isso se enquadra no título de detalhes de implementação, que o COM não especifica. Uma instância de um objeto que implementa uma interface deve ser criada para que a interface realmente exista. Além disso, classes de objeto diferentes podem implementar uma interface de forma diferente, mas ser usada de forma intercambiável em formato binário, desde que o comportamento esteja em conformidade com a definição da interface.
-   Uma interface COM não é um objeto . Ele é simplesmente um grupo relacionado de funções e é o padrão binário por meio do qual os clientes e objetos se comunicam. Desde que ele possa fornecer ponteiros para métodos de interface, o objeto pode ser implementado em qualquer linguagem com qualquer representação de estado interno.
-   As interfaces COM são fortemente digitados. Cada interface tem seu próprio identificador de interface (um GUID), o que elimina a possibilidade de duplicação que pode ocorrer com qualquer outro esquema de nomenização.
-   As interfaces COM são imutáveis. Não é possível definir uma nova versão de uma interface antiga e dar a ela o mesmo identificador. Adicionar ou remover métodos de uma interface ou alterar a semântica cria uma nova interface, não uma nova versão de uma interface antiga. Portanto, uma nova interface não pode conflitar com uma interface antiga. No entanto, os objetos podem dar suporte a várias interfaces simultaneamente e podem expor interfaces que são revisões sucessivas de uma interface, com identificadores diferentes. Portanto, cada interface é um contrato separado e os objetos em todo o sistema não precisam se preocupar se a versão da interface que estão chamando é aquela esperada. A ID da interface (IID) define o contrato de interface de forma explícita e exclusiva.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos e interfaces COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 




