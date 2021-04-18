---
description: 'Um solicitante pode interromper um conjunto de cópias de sombra usando o método IVssBackupComponents:: BreakSnapshotSet ou IVssBackupComponentsEx2:: BreakSnapshotSetEx.'
ms.assetid: fb796b2f-b6fb-48ee-8d42-36f88cb165aa
title: Quebrando cópias de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dac84c9f45d16d8a88f9d61ad6e4c277dfad3ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770578"
---
# <a name="breaking-shadow-copies"></a>Quebrando cópias de sombra

Um solicitante pode interromper um conjunto de cópias de sombra usando o método [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) ou [**IVssBackupComponentsEx2:: BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) .

Uma cópia de sombra quebrada é um volume que contém uma cópia de sombra que não é mais gerenciada pelo VSS. Interromper uma cópia de sombra tem significado apenas se o [*provedor*](vssgloss-p.md) da cópia de sombra for um [*provedor de hardware*](vssgloss-h.md). Isso ocorre porque somente os provedores de hardware podem implementar uma cópia de sombra como um volume real com um ciclo de vida independente do VSS. Se o VSS não gerenciar esse volume, ele ainda estará disponível.

Os provedores de software mantêm cópias de sombra somente quando envolvidas em operações VSS. Por esse motivo, a interrupção de uma cópia de sombra não tem significado para os provedores de software.

Se a cópia de sombra foi gerenciada por um provedor de hardware, o solicitante deve importar a cópia de sombra antes de chamar [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) ou [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex). No caso de cópias de sombra não transportáveis (criadas por um provedor de hardware), elas são importadas implicitamente como parte da chamada [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset) .

Depois que o solicitante tiver chamado [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) ou [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex), o conjunto de cópias de sombra ainda será acessível por meio de seus objetos de dispositivo ou de outros caminhos de acesso, mas não é mais um conjunto de cópias de sombra. Ele pode ser gerenciado como um ou mais LUNs usando as interfaces COM do VDS (serviço de disco virtual). Usando o VDS, um solicitante pode converter os LUNs para leitura/gravação, montá-los com letras de unidade ou mascarar/remover a máscara para outros computadores. Consulte a [documentação da API do VDS](../vds/virtual-disk-service-portal.md) para obter mais informações.

 

 
