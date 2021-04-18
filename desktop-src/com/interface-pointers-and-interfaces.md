---
title: Ponteiros de interface e interfaces
description: Ponteiros de interface e interfaces
ms.assetid: 8a8671fe-f0b2-4698-8c98-89753fffce0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa23d53f529c43fa7529d657108cc75cb6a23b15
ms.sourcegitcommit: d482e4276cc06515e9fade2f253a257ffc418ce5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/24/2019
ms.locfileid: "105807905"
---
# <a name="interface-pointers-and-interfaces"></a>Ponteiros de interface e interfaces

Uma instância de uma implementação de interface é, na verdade, um ponteiro para uma matriz de ponteiros para métodos, ou seja, uma tabela de funções que se refere a uma implementação de todos os métodos especificados na interface. Objetos com várias interfaces podem fornecer ponteiros para mais de uma tabela de funções. Qualquer código que tenha um ponteiro pelo qual ele possa acessar a matriz pode chamar os métodos nessa interface.

Falar precisamente sobre esse indireção não é conveniente, então, em vez disso, o ponteiro para a tabela de funções de interface que outro objeto deve ter para chamar seus métodos é chamado simplesmente de um *ponteiro de interface*. Você pode criar manualmente tabelas de funções em um aplicativo C ou quase automaticamente usando Visual C++ (ou outras linguagens orientadas a objeto que dão suporte a COM).

Com o suporte de compilador apropriado (que é inerente em C e C++), um cliente pode chamar um método de interface por meio de seu nome, não sua posição na matriz. Como uma interface é um tipo, o compilador, dado os nomes dos métodos, pode verificar os tipos de parâmetros e retornar valores de cada chamada de método de interface. Por outro lado, se um cliente usar um esquema de chamada baseado em posição, tal verificação de tipo não estará disponível, mesmo em C ou C++.

Cada interface é um contrato imutável de um grupo funcional de métodos. Você faz referência a uma interface em tempo de execução com um IID (identificador de interface globalmente exclusivo). Essa IID, que é uma instância específica de um GUID (identificador global exclusivo) com suporte do COM, permite que um cliente pergunte a um objeto precisamente se ele dá suporte à semântica da interface, sem sobrecarga desnecessária e sem a confusão que pode surgir em um sistema de ter várias versões da mesma interface com o mesmo nome.

Para resumir, é importante entender o que é uma interface COM e não é:

-   Uma interface COM não é a mesma que uma classe C++. A definição virtual pura não transporta nenhuma implementação. Se você for um programador de C++, poderá definir a implementação de uma interface como uma classe, mas isso se enquadrará no cabeçalho dos detalhes da implementação, que COM não especifica. Uma instância de um objeto que implementa uma interface deve ser criada para que a interface realmente exista. Além disso, classes de objeto diferentes podem implementar uma interface de forma diferente, ainda que seja usada de maneira intercambiável em formato binário, desde que o comportamento esteja de acordo com a definição da interface.
-   Uma interface COM não é um objeto. Ele é simplesmente um grupo de funções relacionado e é o padrão binário por meio do qual os clientes e objetos se comunicam. Desde que ele possa fornecer ponteiros para métodos de interface, o objeto pode ser implementado em qualquer linguagem com qualquer representação de estado interno.
-   Interfaces COM são fortemente tipadas. Cada interface tem seu próprio identificador de interface (um GUID), o que elimina a possibilidade de duplicação que pode ocorrer com qualquer outro esquema de nomenclatura.
-   Interfaces COM são imutáveis. Você não pode definir uma nova versão de uma interface antiga e dar a ela o mesmo identificador. Adicionar ou remover métodos de uma interface ou alterar a semântica cria uma nova interface, não uma nova versão de uma interface antiga. Portanto, uma nova interface não pode entrar em conflito com uma interface antiga. No entanto, os objetos podem dar suporte a várias interfaces simultaneamente e podem expor interfaces que são revisões sucessivas de uma interface, com identificadores diferentes. Portanto, cada interface é um contrato separado, e os objetos de todo o âmbito não precisam se preocupar se a versão da interface que eles estão chamando é a esperada. A ID de interface (IID) define o contrato de interface de forma explícita e exclusiva.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos e interfaces COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 




