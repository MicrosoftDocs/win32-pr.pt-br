---
description: As cópias de sombra transportáveis podem ser usadas para facilitar uma recuperação rápida.
ms.assetid: 2eaffcf7-01b2-44ce-8bc4-fd9fa42c8a8c
title: Recuperação rápida usando volumes copiados de sombra transportável
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb5ddd7604b1463def4ceaa6cd474487255682cf4489b13c5da520128c06811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006396"
---
# <a name="fast-recovery-using-transportable-shadow-copied-volumes"></a>Recuperação rápida usando volumes copiados de sombra transportável

As [*cópias de sombra transportáveis*](vssgloss-t.md) podem ser usadas para facilitar uma *recuperação rápida*.

A recuperação rápida pode ser usada para reverter rapidamente para uma cópia de sombra anterior. As etapas envolvidas são:

1.  Crie a cópia de sombra transportável dos LUNs apropriados. A cópia de sombra pode ser [*persistente*](vssgloss-p.md) ou não persistente.
2.  Remover os LUNs originais
    1.  Se o computador estiver dentro de um cluster, marque os recursos de disco afetados como offline ou habilite o [modo de manutenção](/previous-versions/windows/desktop/mscs/maintaining-physical-disk-resources) para esses recursos de disco.
    2.  Mascarar os LUNs afetados deste computador (e todos os outros nós se o computador estiver em um cluster).
3.  Importe a cópia de sombra usando o método [**IVssBackupComponents:: ImportSnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-importsnapshots) .
4.  Quebre a cópia de sombra usando o método [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset) .
5.  Marque os novos volumes de cópia de sombra como leitura/gravação.
6.  Se o computador estiver em um cluster, expor os novos LUNs de cópia de sombra como os LUNs originais.
    1.  Desmascarar os LUNs de cópia de sombra para os outros nós no cluster.
    2.  Marque os recursos que foram marcados anteriormente como offline ou desabilite o modo de manutenção para esses recursos de disco.

> [!Note]  
> as cópias de sombra transportáveis em um cluster não têm suporte antes do Windows Server 2003 com Service Pack 1 (SP1). Isso só é suportado com LUNs compatíveis, que têm pelo menos uma página VPD (dados vitais do produto) SCSI 0x83 \_ identificador de armazenamento do tipo 1, 2 ou 8 e Associação 0, e os LUNs devem manter um disco básico com particionamento MBR.

 

 

 
