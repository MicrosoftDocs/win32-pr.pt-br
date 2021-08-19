---
title: Autenticação mútua em aplicativos Windows Sockets
description: Os serviços Windows Sockets da Microsoft podem usar as APIs de Registro e Resolução (RnR) para publicar serviços ou podem usar pontos de conexão de serviço.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- Autenticação mútua em aplicativos Windows Sockets
- Active Directory, usando a autenticação mútua, em Windows soquetes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a7267159f826d572a8efd101ab86338f5a24c6966b8d2af3a260e1f4af6244
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025744"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a>Autenticação mútua em aplicativos Windows Sockets

Os serviços Windows Sockets da Microsoft podem usar as APIs de Registro e Resolução (RnR) para publicar serviços ou podem usar pontos de conexão de serviço.

Para obter mais informações e um exemplo de código que mostra como executar a autenticação mútua para um serviço soquetes do Windows que publica usando um ponto de conexão de serviço, consulte Autenticação mútua em um serviço de soquetes do Windows com [um SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md). Este exemplo de código usa um pacote de segurança SSPI para gerenciar as negociações de autenticação entre um cliente e o serviço WinSock.

Um serviço WinSock RnR pode usar um código semelhante para executar a autenticação mútua usando um pacote SSPI. Nesse caso, o serviço comporia seus SPNs usando o nome diferenciado da entrada do serviço no contêiner WinsockServices no diretório .

Por exemplo, se o serviço se registrar com o nome "WinSockRnRSampleService", você comporá o SPN do serviço com o seguinte nome diferenciado:


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




