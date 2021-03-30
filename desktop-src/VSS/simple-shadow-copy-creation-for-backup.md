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
# <a name="simple-shadow-copy-creation-for-backup"></a><span data-ttu-id="c6852-103">Criação de cópia de sombra simples para backup</span><span class="sxs-lookup"><span data-stu-id="c6852-103">Simple Shadow Copy Creation for Backup</span></span>

<span data-ttu-id="c6852-104">Há vários tipos diferentes de cópia de sombra que um solicitante pode criar.</span><span class="sxs-lookup"><span data-stu-id="c6852-104">There are a number of different types of shadow copy a requester can create.</span></span> <span data-ttu-id="c6852-105">No entanto, para a maioria dos aplicativos de backup, você deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c6852-105">However, for most backup applications, you would do the following:</span></span>

1.  <span data-ttu-id="c6852-106">Chame [**IVssBackupComponents:: SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) com um contexto de backup do VSS \_ CTX \_ .</span><span class="sxs-lookup"><span data-stu-id="c6852-106">Call [**IVssBackupComponents::SetContext**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setcontext) with a context of VSS\_CTX\_BACKUP.</span></span>
2.  <span data-ttu-id="c6852-107">Chame [**IVssBackupComponents:: GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) para inicializar a comunicação com gravadores.</span><span class="sxs-lookup"><span data-stu-id="c6852-107">Call [**IVssBackupComponents::GatherWriterMetadata**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-gatherwritermetadata) to initialize communication with writers.</span></span>
3.  <span data-ttu-id="c6852-108">Chame [**IVssBackupComponents:: addComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) para adicionar componentes de arquivo e de banco de dados ao backup.</span><span class="sxs-lookup"><span data-stu-id="c6852-108">Call [**IVssBackupComponents::AddComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addcomponent) to add file and database components to the backup.</span></span>
4.  <span data-ttu-id="c6852-109">Chame [**IVssBackupComponents:: StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) para inicializar o mecanismo de cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="c6852-109">Call [**IVssBackupComponents::StartSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-startsnapshotset) to initialize the shadow copy mechanism.</span></span>
5.  <span data-ttu-id="c6852-110">Chame [**IVssBackupComponents:: AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) para incluir volumes na cópia de sombra.</span><span class="sxs-lookup"><span data-stu-id="c6852-110">Call [**IVssBackupComponents::AddToSnapshotSet**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addtosnapshotset) to include volumes in the shadow copy.</span></span>
6.  <span data-ttu-id="c6852-111">Chame [**IVssBackupComponents::P repareforbackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) para notificar gravadores de operações de backup.</span><span class="sxs-lookup"><span data-stu-id="c6852-111">Call [**IVssBackupComponents::PrepareForBackup**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-prepareforbackup) to notify writers of backup operations.</span></span>

 

 



