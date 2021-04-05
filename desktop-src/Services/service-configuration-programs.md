---
description: Os programadores e administradores do sistema usam programas de configuração de serviço para modificar ou consultar o banco de dados dos serviços instalados.
ms.assetid: 8ab97a4b-a4c2-4123-b5f5-27029bc3eb15
title: Programas de configuração de serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85a2bfc87b093988c1a12c70ce64a4881c79397
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090245"
---
# <a name="service-configuration-programs"></a><span data-ttu-id="8b67c-103">Programas de configuração de serviço</span><span class="sxs-lookup"><span data-stu-id="8b67c-103">Service Configuration Programs</span></span>

<span data-ttu-id="8b67c-104">Os programadores e administradores do sistema usam programas de configuração de serviço para modificar ou consultar o banco de dados dos serviços instalados.</span><span class="sxs-lookup"><span data-stu-id="8b67c-104">Programmers and system administrators use service configuration programs to modify or query the database of installed services.</span></span> <span data-ttu-id="8b67c-105">O banco de dados também pode ser acessado usando as funções de registro.</span><span class="sxs-lookup"><span data-stu-id="8b67c-105">The database can also be accessed by using the registry functions.</span></span> <span data-ttu-id="8b67c-106">No entanto, você deve usar apenas as funções de configuração do SCM, que garantem que o serviço esteja instalado e configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="8b67c-106">However, you should only use the SCM configuration functions, which ensure that the service is properly installed and configured.</span></span>

<span data-ttu-id="8b67c-107">As funções de configuração do SCM exigem um identificador para um objeto SCManager ou um identificador para um objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="8b67c-107">The SCM configuration functions require either a handle to an SCManager object or a handle to a service object.</span></span> <span data-ttu-id="8b67c-108">Para obter esses identificadores, o programa de configuração de serviço deve:</span><span class="sxs-lookup"><span data-stu-id="8b67c-108">To obtain these handles, the service configuration program must:</span></span>

1.  <span data-ttu-id="8b67c-109">Use a função [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) para obter um identificador para o banco de dados SCM em um computador especificado.</span><span class="sxs-lookup"><span data-stu-id="8b67c-109">Use the [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera) function to obtain a handle to the SCM database on a specified machine.</span></span>
2.  <span data-ttu-id="8b67c-110">Use a função [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) ou [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) para obter um identificador para o objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="8b67c-110">Use the [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea) or [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) function to obtain a handle to the service object.</span></span>

<span data-ttu-id="8b67c-111">Para mais informações, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="8b67c-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="8b67c-112">Instalação, remoção e enumeração de serviço</span><span class="sxs-lookup"><span data-stu-id="8b67c-112">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
-   [<span data-ttu-id="8b67c-113">Configuração do serviço</span><span class="sxs-lookup"><span data-stu-id="8b67c-113">Service Configuration</span></span>](service-configuration.md)
-   [<span data-ttu-id="8b67c-114">Configurando um serviço usando SC</span><span class="sxs-lookup"><span data-stu-id="8b67c-114">Configuring a Service Using SC</span></span>](configuring-a-service-using-sc.md)

 

 



