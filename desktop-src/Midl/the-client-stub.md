---
title: O stub do cliente
description: O módulo stub de cliente fornece pontos de entrada substitutos no cliente para cada uma das operações definidas no arquivo IDL de entrada.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL de MIDL e RPC, interfaces, stub de cliente
- MIDL de interfaces
- interfaces MIDL, MIDL e RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c718f0910c2e6834c93409b6d8cd4969e3d2bbe9c53c65821dc0fe0eb19ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146219"
---
# <a name="the-client-stub"></a>O stub do cliente

O módulo stub de cliente fornece pontos de entrada substitutos no cliente para cada uma das operações definidas no arquivo IDL de entrada.

Quando o aplicativo cliente faz uma chamada para o procedimento remoto, sua chamada primeiro vai para a rotina substituta no arquivo stub do cliente. A rotina de stub do cliente executa as seguintes funções:

-   Realiza marshaling de argumentos. O stub de cliente empacota os argumentos de entrada em um formulário que pode ser transmitido para o servidor.
-   Chama a biblioteca de tempo de execução do cliente para transmitir argumentos para o espaço de endereço remoto e invoca o procedimento remoto no espaço de endereço do servidor.
-   Desempacota os argumentos de saída. O stub de cliente desempacota os argumentos de saída e retorna ao chamador.

O compilador MIDL alterna [**/Client**](-client.md), [**/cstub**](-cstub.md)e [**/out**](-out.md) afeta o arquivo stub do cliente.

 

 




