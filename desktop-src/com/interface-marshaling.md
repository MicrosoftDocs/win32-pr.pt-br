---
title: Interface Marshaling
description: Interface Marshaling
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cdee8762fb9ef69507fb5b2c4295531dd87a98d5174ab4e10f05a66cab718d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029866"
---
# <a name="interface-marshaling"></a>Interface Marshaling

A menos que você saiba sem dúvida que sua interface nunca será usada entre limites de apartment, thread ou processo, você precisa decidir como fornecer suporte de marshaling para suas interfaces. Há três maneiras de fornecer suporte a marshaling:

-   Escreva seu próprio código proxy/stub que chama o canal COM, que, por sua vez, chama as bibliotecas de tempo de run-time RPC. Teoricamente, é possível fazer isso, mas, na prática, é quase impossível fazer sem uma quantidade significativa de esforço.
-   Descreva suas interfaces em um arquivo IDL (linguagem de definição de interface) e use o compilador MIDL para gerar uma DLL de proxy/stub. Esse método fornece o melhor desempenho e a maior flexibilidade em termos de tipos de dados aceitáveis. Usando stubs de proxy gerados por MIDL, você pode controlar não apenas o gerenciamento de memória, mas até mesmo o marshaling e o desmarque de tipos de dados complexos em diferentes plataformas.
-   Use MIDL para gerar uma biblioteca de tipos que o sistema usa para fornecer suporte de marshaling em tempo de operação. Essa é a maneira mais fácil de implementar o suporte a marshaling. Tudo o que você precisa fazer é gerar uma biblioteca de tipos e registrá-la. Suas interfaces devem ser compatíveis com Automação [**(oleautomation**](/windows/desktop/Midl/oleautomation) ou [**dual),**](/windows/desktop/Midl/dual)o que coloca algumas restrições nos tipos de dados que você pode usar como parâmetros de método. No entanto, na maioria dos casos, a vantagem de ter suas interfaces acessíveis para programas escritos em outras linguagens, como Microsoft Visual Basic e Java, supera as limitações dos tipos de dados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comunicação entre objetos](inter-object-communication.md)
</dt> </dl>

 

 