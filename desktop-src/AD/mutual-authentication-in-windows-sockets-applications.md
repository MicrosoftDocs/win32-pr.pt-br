---
title: Autenticação mútua em aplicativos do Windows Sockets
description: O Microsoft Windows Sockets Services pode usar as APIs de RnR (registro e resolução) para publicar serviços ou podem usar pontos de conexão de serviço.
ms.assetid: 2b73a754-4f16-41a2-8441-a4ee5f80035c
ms.tgt_platform: multiple
keywords:
- Autenticação mútua em aplicativos do Windows Sockets
- Active Directory, usando a autenticação mútua, em aplicativos do Windows Sockets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29062fa5c9fa7b9b003f1c3aa6f8bc384a785f83
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159311"
---
# <a name="mutual-authentication-in-windows-sockets-applications"></a>Autenticação mútua em aplicativos do Windows Sockets

O Microsoft Windows Sockets Services pode usar as APIs de RnR (registro e resolução) para publicar serviços ou podem usar pontos de conexão de serviço.

Para obter mais informações e um exemplo de código que mostra como executar a autenticação mútua para um serviço do Windows Sockets que publica usando um ponto de conexão de serviço, consulte [autenticação mútua em um serviço de soquetes do Windows com um SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md). Este exemplo de código usa um pacote de segurança SSPI para gerenciar as negociações de autenticação entre um cliente e o serviço WinSock.

Um serviço WinSock RnR pode usar um código semelhante para executar a autenticação mútua usando um pacote SSPI. Nesse caso, o serviço comporia seus SPNs usando o nome distinto da entrada do serviço no contêiner Winsockservices no diretório.

Por exemplo, se o serviço se registrar com o nome "WinSockRnRSampleService", você comporia o SPN do serviço a partir do seguinte nome distinto:


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




