---
description: Os solicitantes controlam os recursos de uma cópia de sombra definindo seu contexto. Esse contexto indica se a cópia de sombra sobreviverá à operação atual e o grau de coordenação de gravador/provedor.
ms.assetid: adf79bc8-e893-444a-b750-d7ffd09de7c9
title: Configurações de contexto de cópia de sombra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdb41d0e2604dcf92d27f490175cdcbafd49822c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505742"
---
# <a name="shadow-copy-context-configurations"></a>Configurações de contexto de cópia de sombra

Os solicitantes controlam os recursos de uma cópia de sombra definindo seu contexto. Esse contexto indica se a cópia de sombra sobreviverá à operação atual e o grau de coordenação de gravador/provedor.

## <a name="persistence-and-shadow-copy-context"></a>Contexto de persistência e cópia de sombra

Uma cópia de sombra pode ser [*persistente*](vssgloss-p.md), ou seja, a cópia de sombra não é excluída após o término de uma operação de backup ou o lançamento de um objeto [**IVssBackupComponents**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssbackupcomponents) .

As cópias de sombra persistentes exigem contextos de [**\_ \_ \_ contexto de instantâneo**](/windows/desktop/api/Vss/ne-vss-vss_snapshot_context) do VSS do **VSS \_ CTX \_ cliente \_ acessível**, **\_ \_ \_ reversão de aplicativo VSS CTX** ou **\_ \_ \_ reversão de nas CTX do VSS**. Cópias de sombra persistentes só podem ser feitas para volumes NTFS.

Cópias de sombra não persistentes são criadas com contextos de backup do **VSS \_ CTX \_** ou backup de compartilhamento de **arquivos do VSS \_ CTX \_ \_ \_**. Cópias de sombra não persistentes podem ser feitas para volumes NTFS e não NTFS.

## <a name="writer-participation-and-shadow-copies"></a>Participação no gravador e cópias de sombra

Um contexto de cópia de sombra pode ser classificado como envolvendo gravadores ou não envolvendo gravadores.

Os contextos de cópia de sombra que envolvem gravadores em sua criação incluem:

-   **reversão do \_ aplicativo VSS CTX \_ \_**
-   **BACKUP do VSS \_ CTX \_**
-   **\_ \_ gravadores acessíveis ao cliente VSS CTX \_ \_**

Aqueles que não envolvem gravadores em sua criação incluem:

-   **VSS \_ CTX \_ cliente \_ acessível**
-   **\_backup de \_ compartilhamento de arquivos CTX \_ VSS \_**
-   **reversão de nas do VSS \_ CTX \_ \_**

Um contexto pode ser usado com ambos os tipos de cópias de sombra, mas não pode ser usado na criação de uma cópia de sombra:

-   **\_CTX VSS \_ All**

Não há suporte para a criação de uma cópia de sombra com um contexto de **\_ CTX VSS \_ All** (usando [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) e [**IVssBackupComponents::D osnapshotset**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-dosnapshotset)).

As operações que dão suporte a um contexto de **CTX do VSS são \_ \_ todas** as operações administrativas [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query), [**IVssBackupComponents::D Eletesnapshots**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-deletesnapshots), [**IVssBackupComponents:: BreakSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-breaksnapshotset)e [**IVssBackupComponents:: ExposeSnapshot**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-exposesnapshot).

## <a name="obtaining-shadow-copy-information"></a>Obtendo informações de cópia de sombra

Se um solicitante souber o GUID de identificação de uma cópia de sombra (sua **\_ ID VSS**), ele poderá obter informações sobre o contexto de uma cópia de sombra específica (identificada por sua **\_ ID do VSS**) ao desempacotar a estrutura de [**\_ \_ prop snapshot do VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) retornada por uma chamada para [**IVssBackupComponents:: getinstantâneoproperties**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-getsnapshotproperties).

Para obter informações de contexto sobre todas as cópias de sombra em um sistema, um solicitante examina o membro **m \_ lSnapshotAttributes** do membro **obj. snap** do [**\_ objeto VSS \_ prop**](/windows/desktop/api/Vss/ns-vss-vss_object_prop) (que é uma estrutura de [**\_ \_ prop instantâneo de VSS**](/windows/desktop/api/Vss/ns-vss-vss_snapshot_prop) ) obtida usando [**IVssEnumObject**](/windows/desktop/api/Vss/nn-vss-ivssenumobject) para iterar sobre a lista de objetos retornados por uma chamada para [**IVssBackupComponents:: Query**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-query).

 

 



