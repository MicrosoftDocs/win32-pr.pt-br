---
description: Os provedores de hardware implementam as interfaces IVssProviderCreateSnapshotSet e IVssHardwareSnapshotProvider.
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: Desenvolvendo provedores de hardware VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca6e9775eb6ee4ee5f16451f51f29cc1c87b300
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171811"
---
# <a name="developing-vss-hardware-providers"></a><span data-ttu-id="e4885-103">Desenvolvendo provedores de hardware VSS</span><span class="sxs-lookup"><span data-stu-id="e4885-103">Developing VSS Hardware Providers</span></span>

<span data-ttu-id="e4885-104">Os provedores de hardware implementam as interfaces [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) e [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) .</span><span class="sxs-lookup"><span data-stu-id="e4885-104">Hardware providers implement the [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) and [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) interfaces.</span></span> <span data-ttu-id="e4885-105">**IVssProviderCreateSnapshotSet** implementa o sequenciamento de estado de cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="e4885-105">**IVssProviderCreateSnapshotSet** implements the shadow copy state sequencing.</span></span> <span data-ttu-id="e4885-106">O **IVssHardwareSnapshotProvider** opera em uma abstração de LUN.</span><span class="sxs-lookup"><span data-stu-id="e4885-106">**IVssHardwareSnapshotProvider** operates on a LUN abstraction.</span></span> <span data-ttu-id="e4885-107">Os provedores devem ser implementados como um servidor COM fora do processo.</span><span class="sxs-lookup"><span data-stu-id="e4885-107">Providers must be implemented as an out-of-process COM server.</span></span> <span data-ttu-id="e4885-108">Os provedores usam mecanismos específicos do provedor (geralmente IOCTLs privados) para se comunicar com o subsistema de armazenamento que instancia os LUNs de cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="e4885-108">Providers use provider-specific mechanisms (often private IOCTLs) to communicate with the storage subsystem that instantiates the shadow copy LUNs.</span></span>

-   [<span data-ttu-id="e4885-109">Registro e carregamento do provedor de cópia de sombra</span><span class="sxs-lookup"><span data-stu-id="e4885-109">Shadow Copy Provider Registration and Loading</span></span>](shadow-copy-provider-registration-and-loading.md)
-   [<span data-ttu-id="e4885-110">Criação de cópia de sombra para provedores</span><span class="sxs-lookup"><span data-stu-id="e4885-110">Shadow Copy Creation for Providers</span></span>](shadow-copy-creation-for-providers.md)
-   [<span data-ttu-id="e4885-111">Interações e comportamentos do provedor de hardware</span><span class="sxs-lookup"><span data-stu-id="e4885-111">Hardware Provider Interactions and Behaviors</span></span>](hardware-provider-interactions-and-behaviors.md)

 

 



