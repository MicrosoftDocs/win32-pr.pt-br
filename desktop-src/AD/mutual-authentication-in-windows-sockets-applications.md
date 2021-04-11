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
# <a name="mutual-authentication-in-windows-sockets-applications"></a><span data-ttu-id="ead0f-105">Autenticação mútua em aplicativos do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="ead0f-105">Mutual Authentication in Windows Sockets Applications</span></span>

<span data-ttu-id="ead0f-106">O Microsoft Windows Sockets Services pode usar as APIs de RnR (registro e resolução) para publicar serviços ou podem usar pontos de conexão de serviço.</span><span class="sxs-lookup"><span data-stu-id="ead0f-106">Microsoft Windows Sockets services can use the Registration and Resolution (RnR) APIs to publish services, or they can use service connection points.</span></span>

<span data-ttu-id="ead0f-107">Para obter mais informações e um exemplo de código que mostra como executar a autenticação mútua para um serviço do Windows Sockets que publica usando um ponto de conexão de serviço, consulte [autenticação mútua em um serviço de soquetes do Windows com um SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md).</span><span class="sxs-lookup"><span data-stu-id="ead0f-107">For more information and a code example that shows how to perform mutual authentication for a Windows Sockets service that publishes using a service connection point, see [Mutual Authentication in a Windows Sockets Service with an SCP](mutual-authentication-in-a-windows-sockets-service-with-an-scp.md).</span></span> <span data-ttu-id="ead0f-108">Este exemplo de código usa um pacote de segurança SSPI para gerenciar as negociações de autenticação entre um cliente e o serviço WinSock.</span><span class="sxs-lookup"><span data-stu-id="ead0f-108">This code example uses an SSPI security package to manage the authentication negotiations between a client and the WinSock service.</span></span>

<span data-ttu-id="ead0f-109">Um serviço WinSock RnR pode usar um código semelhante para executar a autenticação mútua usando um pacote SSPI.</span><span class="sxs-lookup"><span data-stu-id="ead0f-109">A WinSock RnR service can use similar code to perform mutual authentication using an SSPI package.</span></span> <span data-ttu-id="ead0f-110">Nesse caso, o serviço comporia seus SPNs usando o nome distinto da entrada do serviço no contêiner Winsockservices no diretório.</span><span class="sxs-lookup"><span data-stu-id="ead0f-110">In this case, the service would compose its SPNs using the distinguished name of the service's entry in the WinsockServices container in the directory.</span></span>

<span data-ttu-id="ead0f-111">Por exemplo, se o serviço se registrar com o nome "WinSockRnRSampleService", você comporia o SPN do serviço a partir do seguinte nome distinto:</span><span class="sxs-lookup"><span data-stu-id="ead0f-111">For example, if the service registers itself with the name "WinSockRnRSampleService", you would compose the service's SPN from the following distinguished name:</span></span>


```C++
cn=WinSockRnRSampleService,cn=WinsockServices,cn=System,<domain DN>
```



 

 




