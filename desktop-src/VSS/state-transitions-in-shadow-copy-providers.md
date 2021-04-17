---
description: 'O modelo de transição de estado em um provedor de cópia de sombra é simplificado pela serialização da criação da cópia de sombra a partir da hora em que IVssBackupComponents:: StartSnapshotSet é chamado até a chamada para IVssBackupComponents::D oSnapshotSet retorna.'
ms.assetid: 5dbf0fb3-53cb-4532-9a8f-bd955afe16c4
title: Transições de estado em provedores de cópia de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d628d11419158f947225b2e4cabd7f93975f421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784944"
---
# <a name="state-transitions-in-shadow-copy-providers"></a>Transições de estado em provedores de cópia de sombra

O modelo de transição de estado em um provedor de cópia de sombra é simplificado pela serialização da criação da cópia de sombra a partir da hora em que [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) é chamado até a chamada para [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) retorna. Se outro solicitante tentar criar uma cópia de sombra durante esse tempo, a chamada para **StartSnapshotSet** falhará com o erro **VSS \_ e o \_ \_ conjunto de instantâneos \_ em \_ andamento**, indicando que o segundo solicitante deve aguardar e tentar novamente.

O VSS só chamará [**IVssProviderCreateSnapshotSet:: AbortSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-abortsnapshots) depois que o solicitante tiver chamado [**DoSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset), mesmo se a cópia de sombra falhar ou for anulada antes desse ponto. Isso significa que um provedor não receberá uma chamada para **AbortSnapshots** até que [**IVssProviderCreateSnapshotSet:: EndPrepareSnapshots**](/windows/desktop/api/VsProv/nf-vsprov-ivssprovidercreatesnapshotset-endpreparesnapshots) tenha sido chamado. Se uma cópia de sombra for anulada ou falhar antes desse ponto, o provedor não receberá nenhuma indicação até que uma nova cópia de sombra seja iniciada. Por esse motivo, o provedor deve estar preparado para lidar com uma chamada fora de sequência para [**IVssHardwareSnapshotProvider:: BeginPrepareSnapshot**](/windows/desktop/api/VsProv/nf-vsprov-ivsshardwaresnapshotprovider-beginpreparesnapshot) em qualquer ponto. Essa chamada fora de sequência representa o início de uma nova sequência de cópia de sombra e terá uma nova ID de conjunto de cópias de sombra.

 

 



