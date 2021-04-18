---
title: Empacotamento de interface
description: Empacotamento de interface
ms.assetid: 71069bd3-5f90-406a-be78-bb1af9b1c1c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5112b67e643fb95e1025fd4ed297043f81f576e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105789364"
---
# <a name="interface-marshaling"></a>Empacotamento de interface

A menos que você saiba além de todas as dúvidas de que sua interface nunca será usada em limites de apartamento, thread ou processo, você precisa decidir como fornecer suporte de marshaling para suas interfaces. Há três maneiras de fornecer suporte ao marshaling:

-   Escreva seu próprio código de proxy/stub que chama o canal COM que, por sua vez, chama as bibliotecas de tempo de execução RPC. Teoricamente, é possível fazer isso, mas na prática é quase impossível fazer isso sem uma quantidade significativa de esforço.
-   Descreva suas interfaces em um arquivo IDL (linguagem de definição de interface) e use o compilador MIDL para gerar uma DLL de proxy/stub. Esse método fornece o melhor desempenho e maior flexibilidade em termos de tipos de dados aceitáveis. Usando stubs de proxy gerados por MIDL, você pode controlar não apenas o gerenciamento de memória, mas até mesmo o marshaling e o desempacotamento de tipos de dados complexos em diferentes plataformas.
-   Use MIDL para gerar uma biblioteca de tipos que o sistema usa para fornecer suporte de marshaling em tempo de execução. Essa é a maneira mais fácil de implementar o suporte de marshaling. Tudo o que você precisa fazer é gerar uma biblioteca de tipos e registrá-la. Suas interfaces devem ser compatíveis com a automação ( [**oleautomation**](/windows/desktop/Midl/oleautomation) ou [**Dual**](/windows/desktop/Midl/dual)), que coloca algumas restrições nos tipos de tipos de dados que você pode usar como parâmetros de método. No entanto, na maioria dos casos, a vantagem de ter suas interfaces acessíveis a programas escritos em outras linguagens, como o Microsoft Visual Basic e o Java, supera as limitações dos tipos de dados.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Comunicação entre objetos](inter-object-communication.md)
</dt> </dl>

 

 