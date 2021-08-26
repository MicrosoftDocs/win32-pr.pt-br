---
title: Interfaces e implementações de interface
description: COM faz uma distinção fundamental entre as definições de interface e suas implementações.
ms.assetid: f50b3e8f-bf87-4525-b47b-96e75b3a05b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bee00521b847acbd063f1cd7ad84a0eb231f78d7bd274b7a4658996dbdd61150
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992696"
---
# <a name="interfaces-and-interface-implementations"></a>Interfaces e implementações de interface

COM faz uma distinção fundamental entre as definições de interface e suas implementações.

Uma *interface* é, na verdade, um contrato que consiste em um grupo de protótipos de função relacionados cujo uso é definido, mas cuja implementação não é. Esses protótipos de função são equivalentes a classes de base virtual puras na programação C++. Uma definição de interface especifica as funções de membro da interface, chamadas *métodos*, seus tipos de retorno, o número e os tipos de seus parâmetros e o que eles devem fazer. Não há nenhuma implementação associada a uma interface.

Uma *implementação de interface* é o código que um programador fornece para realizar as ações especificadas em uma definição de interface. Implementações de muitas das interfaces que um programador pode usar em um aplicativo baseado em objeto são incluídas nas bibliotecas COM. No entanto, os programadores estão livres para ignorar essas implementações e escrever suas próprias. Uma implementação de interface deve ser associada a um objeto quando uma instância desse objeto é criada e a implementação fornece os serviços que o objeto oferece.

Por exemplo, uma interface hipotética chamada istachar pode definir dois métodos, chamados push e pop, especificando que as chamadas sucessivas para o método pop retornam, na ordem inversa, os valores passados anteriormente para o método Push. Essa definição de interface não especificaria como as funções devem ser implementadas no código. Na implementação da interface, um programador pode implementar a pilha como uma matriz e implementar os métodos push e pop de forma a acessar essa matriz, enquanto outro programador pode usar uma lista vinculada e implementar os métodos adequadamente. Independentemente de uma implementação específica dos métodos push e pop, a representação na memória de um ponteiro para uma interface istachar e, portanto, seu uso por um cliente, é completamente determinada pela definição da interface.

Os objetos simples dão suporte apenas a uma única interface. Objetos mais complicados, como objetos incorporáveis, normalmente dão suporte a várias interfaces. Os clientes têm acesso a um objeto COM somente por meio de um ponteiro para uma de suas interfaces, o que, por sua vez, permite que o cliente chame qualquer um dos métodos que compõem essa interface. Esses métodos determinam como um cliente pode usar os dados do objeto.

As interfaces definem um contrato entre um objeto e seus clientes. O contrato especifica os métodos que devem ser associados a cada interface e qual o comportamento de cada um dos métodos deve estar em termos de entrada e saída. O contrato geralmente não define como implementar os métodos em uma interface. Outro aspecto importante do contrato é que, se um objeto oferecer suporte a uma interface, ele deverá dar suporte a todos os métodos dessa interface de alguma maneira. Nem todos os métodos em uma implementação precisam fazer algo. Se um objeto não oferecer suporte à função implícita por um método, sua implementação poderá ser um retorno simples ou talvez o retorno de uma mensagem de erro significativa — mas os métodos devem existir.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Objetos e interfaces COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 




