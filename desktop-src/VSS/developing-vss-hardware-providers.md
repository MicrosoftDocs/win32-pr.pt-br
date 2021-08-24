---
description: Os provedores de hardware implementam as interfaces IVssProviderCreateSnapshotSet e IVssHardwareSnapshotProvider.
ms.assetid: 9f40f1d1-a63a-4edc-aa8d-b3998ecb2716
title: Desenvolvendo provedores de hardware VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29533838b814a07f3da5310302a283f6cd60dc75779b4eb29dcdbf6b10816aa3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032706"
---
# <a name="developing-vss-hardware-providers"></a>Desenvolvendo provedores de hardware VSS

Os provedores de hardware implementam as interfaces [**IVssProviderCreateSnapshotSet**](/windows/desktop/api/VsProv/nn-vsprov-ivssprovidercreatesnapshotset) e [**IVssHardwareSnapshotProvider.**](/windows/desktop/api/VsProv/nn-vsprov-ivsshardwaresnapshotprovider) **IVssProviderCreateSnapshotSet** implementa o sequenciamento de estado de cópia de sombra. **IVssHardwareSnapshotProvider** opera em uma abstração de LUN. Os provedores devem ser implementados como um servidor COM fora do processo. Os provedores usam mecanismos específicos do provedor (geralmente IOCTLs privados) para se comunicar com o subsistema de armazenamento que instanam os LUNs de cópia de sombra.

-   [Registro e carregamento do provedor de cópia de sombra](shadow-copy-provider-registration-and-loading.md)
-   [Criação de cópia de sombra para provedores](shadow-copy-creation-for-providers.md)
-   [Comportamentos e interações do provedor de hardware](hardware-provider-interactions-and-behaviors.md)

 

 



