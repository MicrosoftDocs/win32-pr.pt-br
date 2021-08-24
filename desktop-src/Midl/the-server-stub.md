---
title: O stub do servidor
description: O stub de servidor fornece pontos de entrada substitutos no servidor para cada uma das operações definidas no arquivo IDL de entrada.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL do compilador MIDL, MIDL e prc RPC, interfaces, stub de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddfc940ebbd90e4e028ce96dc3b5c47eb15179d41cfbd064cd235e87192822f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119559896"
---
# <a name="the-server-stub"></a>O stub do servidor

O stub de servidor fornece pontos de entrada substitutos no servidor para cada uma das operações definidas no arquivo IDL de entrada.

Quando uma rotina de stub de servidor é invocada pela biblioteca de tempo de execução RPC, ela executa as seguintes funções:

-   Desempacota os argumentos de entrada (descompacta os argumentos de seus formatos transmitidos).
-   Chama a implementação real do procedimento no servidor.
-   Realiza marshaling de argumentos de saída (empacota os argumentos nos formulários transmitidos).

O compilador MIDL alterna a opção [**/Server**](-server.md), [**/sstub**](-sstub.md)e [**/out**](-out.md) afeta o arquivo stub do servidor.

 

 




