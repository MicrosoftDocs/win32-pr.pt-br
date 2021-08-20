---
description: O modelo de transição de estado em um provedor de cópia de sombra é simplificado pela serialização da criação de cópia de sombra a partir do momento em que IVssBackupComponents::StartSnapshotSet é chamado até que a chamada para IVssBackupComponents::D oSnapshotSet seja retornada.
ms.assetid: 5dbf0fb3-53cb-4532-9a8f-bd955afe16c4
title: Transições de estado em provedores de cópia de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad6141b9b8f221a1e67e95fde1e6b33ad819c0cbdead57eeb676164e89acc392
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118121596"
---
# <a name="state-transitions-in-shadow-copy-providers"></a>Transições de estado em provedores de cópia de sombra

O modelo de transição de estado em um provedor de cópia de sombra é simplificado pela serialização da criação de cópia de sombra a partir do momento em que [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) é chamado até que a chamada para [**IVssBackupComponents::D oSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) seja retornada. Se outro solicitante tentar criar uma cópia de sombra durante esse tempo, a chamada para **StartSnapshotSet** falhará com o erro **VSS \_ E SNAPSHOT SET \_ IN \_ \_ \_ PROGRESS**, indicando que o segundo solicitante deve aguardar e tentar novamente.

O VSS chamará [**somente IVssProviderCreateSnapshotSet::AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) depois que o solicitante tiver chamado [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), mesmo que a cópia de sombra falhe ou seja anulada antes desse ponto. Isso significa que um provedor não receberá uma chamada para **AbortSnapshots** até que [**IVssProviderCreateSnapshotSet::EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) tenha sido chamado. Se uma cópia de sombra for anulada ou falhar antes desse ponto, o provedor não recebe nenhuma indicação até que uma nova cópia de sombra seja iniciada. Por esse motivo, o provedor deve estar preparado para lidar com uma chamada fora de sequência para [**IVssHardwareSnapshotProvider::BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) a qualquer momento. Essa chamada fora de sequência representa o início de uma nova sequência de cópia de sombra e terá uma nova ID do conjunto de cópias de sombra.

 

 



