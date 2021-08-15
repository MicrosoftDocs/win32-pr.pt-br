---
description: Há vários tipos diferentes de cópia de sombra que um solicitante pode criar.
ms.assetid: a20570ea-e3eb-4d65-b8fa-9a27ce1a3e74
title: Criação de cópia de sombra simples para backup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f9cda7a2d2679979879a2333b30621fb7f73a449f4a15b55b42c603cd913713
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119394166"
---
# <a name="simple-shadow-copy-creation-for-backup"></a>Criação de cópia de sombra simples para backup

Há vários tipos diferentes de cópia de sombra que um solicitante pode criar. No entanto, para a maioria dos aplicativos de backup, você deve fazer o seguinte:

1.  Chame [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) com um contexto de backup do VSS \_ CTX \_ .
2.  Chame [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) para inicializar a comunicação com gravadores.
3.  Chame [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para adicionar componentes de arquivo e de banco de dados ao backup.
4.  Chame [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) para inicializar o mecanismo de cópia de sombra.
5.  Chame [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) para incluir volumes na cópia de sombra.
6.  Chame [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) para notificar gravadores de operações de backup.

 

 



