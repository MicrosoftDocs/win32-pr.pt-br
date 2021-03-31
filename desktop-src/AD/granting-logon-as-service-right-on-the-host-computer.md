---
title: Concedendo logon como serviço diretamente no computador host
description: Ao instalar um serviço para ser executado em uma conta de usuário de domínio, a conta deve ter o direito de fazer logon como um serviço no computador local.
ms.assetid: 1b217650-4397-4e28-b53e-8b03f3caf903
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95ef2bb87c3cf461e67cb7da20f36d9ac07fb362
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103634939"
---
# <a name="granting-logon-as-service-right-on-the-host-computer"></a><span data-ttu-id="633ae-103">Concedendo logon como serviço diretamente no computador host</span><span class="sxs-lookup"><span data-stu-id="633ae-103">Granting Logon as Service Right on the Host Computer</span></span>

<span data-ttu-id="633ae-104">Ao instalar um serviço para ser executado em uma conta de usuário de domínio, a conta deve ter o direito de fazer logon como um serviço no computador local.</span><span class="sxs-lookup"><span data-stu-id="633ae-104">When installing a service to run under a domain user account, the account must have the right to logon as a service on the local computer.</span></span> <span data-ttu-id="633ae-105">Lembre-se de que esse direito de logon se aplica somente ao computador local e deve ser concedido na política LSA local de cada computador host.</span><span class="sxs-lookup"><span data-stu-id="633ae-105">Be aware that this logon right applies only to the local computer and must be granted in the local LSA policy of each host computer.</span></span> <span data-ttu-id="633ae-106">Essa etapa não será necessária se o serviço for executado como LocalSystem, que, por padrão, terá esse direito.</span><span class="sxs-lookup"><span data-stu-id="633ae-106">This step is not required if your service runs as LocalSystem, which, by default, is granted this right.</span></span>

<span data-ttu-id="633ae-107">Para obter mais informações sobre como conceder programaticamente o direito de logon como um serviço, consulte o [código de exemplo LSAPrivs](https://www.google.com/#q=LSAPrivs).</span><span class="sxs-lookup"><span data-stu-id="633ae-107">For more information on how to programmatically grant logon as a service right, see the [LSAPrivs sample code](https://www.google.com/#q=LSAPrivs).</span></span>

 

 




