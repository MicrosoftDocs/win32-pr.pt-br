---
description: O Windows Sockets 2 continua a dar suporte a todas as semânticas e chamadas de função do Windows Sockets 1,1, exceto aquelas que lidam com o pseudo-bloqueio.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Problemas de compatibilidade do Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58495db7ff504b68d0db41104fe0fff79b93f985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164866"
---
# <a name="windows-sockets-compatibility-issues"></a>Problemas de compatibilidade do Windows Sockets

O Windows Sockets 2 continua a dar suporte a todas as semânticas e chamadas de função do Windows Sockets 1,1, exceto aquelas que lidam com o pseudo-bloqueio. Como o Windows Sockets 2 é executado somente em ambientes de 32 bits e programados de vez em diante, não é necessário implementar o pseudo-bloqueio encontrado no Windows Sockets 1,1. Isso significa que o código de erro WSAEINPROGRESS nunca será indicado e que as seguintes funções do Windows Sockets 1,1 não estão disponíveis para aplicativos do Windows Sockets 2:

-   WSACancelBlockingCall
-   WSAIsBlocking
-   WSASetBlockingHook
-   WSAUnhookBlockingHook

Os programas do Windows Sockets 1,1 que são gravados para utilizar o pseudo-bloqueio continuarão a operar corretamente, pois eles se vinculam a Winsock.dll ou Wsock32.dll. Ambos continuam a dar suporte ao conjunto completo de funções do Windows Sockets 1,1. Para que os programas se tornem aplicativos do Windows Sockets 2, deve ocorrer alguma modificação de código. Na maioria dos casos, o uso criterioso de threads pode ser substituído para acomodar o processamento que estava sendo realizado com uma função de gancho de bloqueio.

 

 



