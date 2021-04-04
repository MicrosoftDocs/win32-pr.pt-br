---
title: O stub do servidor
description: O stub de servidor fornece pontos de entrada substitutos no servidor para cada uma das operações definidas no arquivo IDL de entrada.
ms.assetid: e3263543-e78b-40a8-aafa-4315850112a8
keywords:
- MIDL do compilador MIDL, MIDL e prc RPC, interfaces, stub de servidor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b351c53fa9e1d1716e1240ddf4febdccdadda46
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005952"
---
# <a name="the-server-stub"></a>O stub do servidor

O stub de servidor fornece pontos de entrada substitutos no servidor para cada uma das operações definidas no arquivo IDL de entrada.

Quando uma rotina de stub de servidor é invocada pela biblioteca de tempo de execução RPC, ela executa as seguintes funções:

-   Desempacota os argumentos de entrada (descompacta os argumentos de seus formatos transmitidos).
-   Chama a implementação real do procedimento no servidor.
-   Realiza marshaling de argumentos de saída (empacota os argumentos nos formulários transmitidos).

O compilador MIDL alterna a opção [**/Server**](-server.md), [**/sstub**](-sstub.md)e [**/out**](-out.md) afeta o arquivo stub do servidor.

 

 




