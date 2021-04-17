---
title: Limitações de autenticação mútua com Kerberos
description: A conta do cliente e a conta do serviço devem estar em domínios do Windows 2000 nativo ou de modo misto porque os serviços Kerberos não estão disponíveis em domínios de nível inferior.
ms.assetid: 54685e88-b289-4db9-b4cb-f5c22a216a0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290bd93050c9cb4c89052ce644b4c588f638f312
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104453500"
---
# <a name="limitations-of-mutual-authentication-with-kerberos"></a><span data-ttu-id="4abe0-103">Limitações de autenticação mútua com Kerberos</span><span class="sxs-lookup"><span data-stu-id="4abe0-103">Limitations of Mutual Authentication with Kerberos</span></span>

<span data-ttu-id="4abe0-104">A conta do cliente e a conta do serviço devem estar em domínios do Windows 2000 nativo ou de modo misto porque os serviços Kerberos não estão disponíveis em domínios de nível inferior.</span><span class="sxs-lookup"><span data-stu-id="4abe0-104">Both the client's account and the service's account must be in Windows 2000 native or mixed-mode domains because Kerberos services are not available in downlevel domains.</span></span> <span data-ttu-id="4abe0-105">Além disso, as contas de cliente e serviço devem estar na mesma floresta porque o KDC do cliente usa o catálogo global para pesquisar o nome da entidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="4abe0-105">In addition, both client and service accounts must be in the same forest because the client's KDC uses the global catalog to search for the service principal name.</span></span>

<span data-ttu-id="4abe0-106">Tanto o serviço quanto o cliente devem estar em execução no Windows 2000, caso contrário, a autenticação mútua com o Kerberos falhará porque as versões anteriores do Windows não dão suporte ao Kerberos.</span><span class="sxs-lookup"><span data-stu-id="4abe0-106">Both service and client must be running on Windows 2000, otherwise mutual authentication with Kerberos will fail because earlier versions of Windows do not support Kerberos.</span></span>

<span data-ttu-id="4abe0-107">Os nomes da entidade de serviço devem incluir o nome DNS do servidor host no qual o serviço está em execução.</span><span class="sxs-lookup"><span data-stu-id="4abe0-107">Service principal names must include the DNS name of the host server on which the service is running.</span></span> <span data-ttu-id="4abe0-108">Você deve usar o nome DNS.</span><span class="sxs-lookup"><span data-stu-id="4abe0-108">You must use the DNS name.</span></span>

 

 




