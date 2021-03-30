---
description: Há vários tipos diferentes de cópia de sombra que um solicitante pode criar.
ms.assetid: a20570ea-e3eb-4d65-b8fa-9a27ce1a3e74
title: Criação de cópia de sombra simples para backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c11e030c0531c96eee40e9cd5bb7cc9366284985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647032"
---
# <a name="simple-shadow-copy-creation-for-backup"></a>Criação de cópia de sombra simples para backup

Há vários tipos diferentes de cópia de sombra que um solicitante pode criar. No entanto, para a maioria dos aplicativos de backup, você deve fazer o seguinte:

1.  Chame [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) com um contexto de backup do VSS \_ CTX \_ .
2.  Chame [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) para inicializar a comunicação com gravadores.
3.  Chame [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para adicionar componentes de arquivo e de banco de dados ao backup.
4.  Chame [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) para inicializar o mecanismo de cópia de sombra.
5.  Chame [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) para incluir volumes na cópia de sombra.
6.  Chame [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) para notificar gravadores de operações de backup.

 

 



