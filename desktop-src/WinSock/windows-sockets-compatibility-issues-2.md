---
description: Windows Os soquetes 2 continuam a dar suporte a todas as chamadas de função e semântica do Windows Sockets 1.1, exceto aquelas que lidam com pseudo-bloqueio.
ms.assetid: e4dc4019-d421-49b8-825a-faa6d5f5fcae
title: Windows Problemas de compatibilidade de soquetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d3fa7aba32ed74f04b04d717e0b2897dc92e0c78079d2a8c20e2c3bcdd85191
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051464"
---
# <a name="windows-sockets-compatibility-issues"></a>Windows Problemas de compatibilidade de soquetes

Windows Os soquetes 2 continuam a dar suporte a todas as chamadas de função e semântica do Windows Sockets 1.1, exceto aquelas que lidam com pseudo-bloqueio. Como Windows Sockets 2 é executado somente em ambientes agendados preventivamente de 32 bits, não é necessário implementar o pseudo-bloqueio encontrado no Windows Sockets 1.1. Isso significa que o código de erro WSAEINPROGRESS nunca será indicado e que as seguintes funções do Windows Sockets 1.1 não estão disponíveis para aplicativos Windows Sockets 2:

-   WSACancelBlockingCall
-   WSAIsBlocking
-   WSASetBlockingHook
-   WSAUnhookBlockingHook

Windows Os programas sockets 1.1 gravados para utilizar pseudo-bloqueio continuarão funcionando corretamente, pois eles se vinculam a Winsock.dll ou Wsock32.dll. Ambos continuam a dar suporte ao conjunto completo de funções Windows Sockets 1.1. Para que os programas se tornem aplicativos Windows Sockets 2, algumas modificações de código devem ocorrer. Na maioria dos casos, o uso criterioso de threads pode ser substituído para acomodar o processamento que estava sendo realizado com uma função de gancho de bloqueio.

 

 



