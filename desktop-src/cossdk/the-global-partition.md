---
description: A partição global
ms.assetid: db11e6f5-0a3d-44ce-9a51-90d7e2b80981
title: A partição global
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc218067bbf7170a1c2df6f306b6dfe5787ac2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457160"
---
# <a name="the-global-partition"></a><span data-ttu-id="2f6c8-103">A partição global</span><span class="sxs-lookup"><span data-stu-id="2f6c8-103">The Global Partition</span></span>

<span data-ttu-id="2f6c8-104">Além de partições definidas pelo administrador e conjuntos de partição, há uma partição especial em cada computador chamada de *partição global*.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-104">In addition to administrator-defined partitions and partition sets, there is a special partition on each computer called a *global partition*.</span></span> <span data-ttu-id="2f6c8-105">Uma partição global é criada automaticamente quando o COM+ é instalado.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-105">A global partition is automatically created when COM+ is installed.</span></span> <span data-ttu-id="2f6c8-106">A partição global foi projetada para conter aplicativos de todo o sistema que precisam ser acessíveis a todos os usuários em um servidor ou no domínio.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-106">The global partition is designed to contain system-wide applications that need to be accessible to all users on a server or in the domain.</span></span> <span data-ttu-id="2f6c8-107">A instalação de um aplicativo na partição global elimina a necessidade de instalar uma cópia do aplicativo em cada conjunto de partições do usuário individual.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-107">Installing an application into the global partition removes the need to install a copy of the application into each individual user's partition set.</span></span>

<span data-ttu-id="2f6c8-108">Se o conjunto de partições de um usuário não incluir um aplicativo específico que o usuário está tentando acessar, mas esse aplicativo estiver instalado na partição global, o aplicativo será ativado da partição global.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-108">If a user's partition set does not include a specific application that the user is attempting to access, but that application is installed in the global partition, the application is activated from the global partition.</span></span> <span data-ttu-id="2f6c8-109">Nesse caso, no entanto, todos os componentes do aplicativo instalados na partição global devem ser marcados como componentes públicos, não privados.</span><span class="sxs-lookup"><span data-stu-id="2f6c8-109">In this case, however, all components of the application installed in the global partition must be marked as public, not private, components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f6c8-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2f6c8-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f6c8-111">Partições padrão</span><span class="sxs-lookup"><span data-stu-id="2f6c8-111">Default Partitions</span></span>](default-partitions.md)
</dt> <dt>

[<span data-ttu-id="2f6c8-112">Partições locais</span><span class="sxs-lookup"><span data-stu-id="2f6c8-112">Local Partitions</span></span>](local-partitions.md)
</dt> <dt>

[<span data-ttu-id="2f6c8-113">Propriedades da partição</span><span class="sxs-lookup"><span data-stu-id="2f6c8-113">Partition Properties</span></span>](partition-properties.md)
</dt> <dt>

[<span data-ttu-id="2f6c8-114">Partições e Active Directory</span><span class="sxs-lookup"><span data-stu-id="2f6c8-114">Partitions and Active Directory</span></span>](partitions-and-active-directory.md)
</dt> </dl>

 

 



