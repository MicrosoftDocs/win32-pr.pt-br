---
description: Um solicitante pode quebrar um conjunto de cópias de sombra usando o método IVssBackupComponents::BreakSnapshotSet ou IVssBackupComponentsEx2::BreakSnapshotSetEx.
ms.assetid: fb796b2f-b6fb-48ee-8d42-36f88cb165aa
title: Cópias de sombra da quebra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fee7a17a77bb806bc6e3713c00c9a01b9bc583f56822b9940b0fe2afebb4e7f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032896"
---
# <a name="breaking-shadow-copies"></a>Cópias de sombra da quebra

Um solicitante pode quebrar um conjunto de cópias de sombra usando o método [**IVssBackupComponents::BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) ou [**IVssBackupComponentsEx2::BreakSnapshotSetEx.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex)

Uma cópia de sombra quebrada é um volume que contém uma cópia de sombra que não é mais gerenciada pelo VSS. A quebra de uma cópia de sombra terá significado apenas se o provedor da cópia [*de*](vssgloss-p.md) sombra for um provedor [*de hardware*](vssgloss-h.md). Isso porque somente provedores de hardware podem implementar uma cópia de sombra como um volume real com um ciclo de vida independente do VSS. Se o VSS não gerenciar esse volume, ele ainda estará disponível.

Os provedores de software mantêm cópias de sombra somente enquanto estão envolvidos em operações do VSS. Por esse motivo, a quebra de uma cópia de sombra não tem nenhum significado para provedores de software.

Se a cópia de sombra tiver sido gerenciada por um provedor de hardware, o solicitante deverá importar a cópia de sombra antes de chamar [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) ou [**BreakSnapshotSetEx.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex) No caso de cópias de sombra não transportáveis (criadas por um provedor de hardware), elas são importadas implicitamente como parte da chamada [**IVssBackupComponents::D oSnapshotSet.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)

Depois que o solicitante tiver chamado [**BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) ou [**BreakSnapshotSetEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-breaksnapshotsetex), o conjunto de cópias de sombra ainda será acessível por meio de seus objetos de dispositivo ou outros caminhos de acesso, mas não será mais um conjunto de cópias de sombra. Ele pode ser gerenciado como um ou mais LUNs usando as interfaces COM do VDS (Serviço de Disco Virtual). Usando o VDS, um solicitante pode converter os LUNs para leitura/gravação, montá-los com letras de unidade ou mascarar/desem máscara para outros computadores. Confira a [documentação da API do VDS](../vds/virtual-disk-service-portal.md) para obter mais informações.

 

 
