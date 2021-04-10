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
# <a name="developing-vss-hardware-providers"></a>Desenvolvendo provedores de hardware VSS

Os provedores de hardware implementam as interfaces [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) e [**IVssHardwareSnapshotProvider**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) . **IVssProviderCreateSnapshotSet** implementa o sequenciamento de estado de cópia de sombra. O **IVssHardwareSnapshotProvider** opera em uma abstração de LUN. Os provedores devem ser implementados como um servidor COM fora do processo. Os provedores usam mecanismos específicos do provedor (geralmente IOCTLs privados) para se comunicar com o subsistema de armazenamento que instancia os LUNs de cópia de sombra.

-   [Registro e carregamento do provedor de cópia de sombra](shadow-copy-provider-registration-and-loading.md)
-   [Criação de cópia de sombra para provedores](shadow-copy-creation-for-providers.md)
-   [Interações e comportamentos do provedor de hardware](hardware-provider-interactions-and-behaviors.md)

 

 



