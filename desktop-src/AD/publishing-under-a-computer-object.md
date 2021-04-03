---
title: Publicação em um objeto de computador
description: Normalmente, os serviços baseados em host criam SCPs sob o objeto de computador para o computador host. Os serviços baseados em host são serviços fortemente vinculados a um único computador host.
ms.assetid: ecd7d8bc-4714-408a-856c-7cab8360bf81
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77fe382001910f3b78b4461c622e94b14c54fb59
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/17/2020
ms.locfileid: "103823637"
---
# <a name="publishing-under-a-computer-object"></a><span data-ttu-id="9c4e7-104">Publicação em um objeto de computador</span><span class="sxs-lookup"><span data-stu-id="9c4e7-104">Publishing Under a Computer Object</span></span>

<span data-ttu-id="9c4e7-105">Normalmente, os serviços baseados em host criam SCPs sob o objeto de computador para o computador host.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-105">Typically, host-based services create SCPs under the computer object for the host computer.</span></span> <span data-ttu-id="9c4e7-106">Os serviços baseados em host são serviços fortemente vinculados a um único computador host.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-106">Host-based services are services closely tied to a single host computer.</span></span>

<span data-ttu-id="9c4e7-107">**Para criar SCPs em um objeto de computador**</span><span class="sxs-lookup"><span data-stu-id="9c4e7-107">**To create SCPs under a computer object**</span></span>

1.  <span data-ttu-id="9c4e7-108">Chame a função [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) para obter o DN (nome distinto) no diretório do objeto de computador do computador local.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-108">Call the [**GetComputerObjectName**](/windows/desktop/api/secext/nf-secext-getcomputerobjectnamea) function to get the distinguished name (DN) in the directory of the computer object for the local computer.</span></span>
2.  <span data-ttu-id="9c4e7-109">Use esse DN para associar ao objeto de computador e criar o SCP.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-109">Use that DN to bind to the computer object and create the SCP.</span></span>

<span data-ttu-id="9c4e7-110">Para obter mais informações e um exemplo de código, consulte [como os clientes encontram e usam um ponto de conexão de serviço](how-clients-find-and-use-a-service-connection-point.md).</span><span class="sxs-lookup"><span data-stu-id="9c4e7-110">For more information and a code example, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).</span></span>

<span data-ttu-id="9c4e7-111">Lembre-se de que somente computadores membros do domínio têm objetos de computador válidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="9c4e7-111">Be aware that only domain-member computers have valid computer objects in the directory.</span></span>

<span data-ttu-id="9c4e7-112">Para obter o nome DNS ou NetBIOS do computador local, chame a função [**GetComputerNameEx devia**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) .</span><span class="sxs-lookup"><span data-stu-id="9c4e7-112">To get the DNS or NetBIOS name of the local computer, call the [**GetComputerNameEx**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa) function.</span></span>

 

 