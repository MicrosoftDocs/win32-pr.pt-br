---
description: 'Durante uma operação de restauração, o solicitante pode usar o método IVssBackupComponents:: setrestore para definir o tipo de operação de restauração em andamento.'
ms.assetid: f6bf1979-7604-450f-8988-2a17da6b82d7
title: Estado de restauração do VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97581d33f5695890ba83e87c6f6155a9e7f92f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763958"
---
# <a name="vss-restore-state"></a><span data-ttu-id="b2c1d-103">Estado de restauração do VSS</span><span class="sxs-lookup"><span data-stu-id="b2c1d-103">VSS Restore State</span></span>

<span data-ttu-id="b2c1d-104">Durante uma operação de restauração, o solicitante pode usar o método [**IVssBackupComponents:: setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) para definir o tipo de operação de restauração em andamento.</span><span class="sxs-lookup"><span data-stu-id="b2c1d-104">During a restore operation, the requester can use the [**IVssBackupComponents::SetRestoreState**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) method to define the type of restore operation in progress.</span></span> <span data-ttu-id="b2c1d-105">No entanto, a maioria das operações de restauração não precisará substituir o tipo de restauração padrão (VSS \_ RTYPE \_ indefinido).</span><span class="sxs-lookup"><span data-stu-id="b2c1d-105">However, most restore operations will not need to override the default restore type (VSS\_RTYPE\_UNDEFINED).</span></span> <span data-ttu-id="b2c1d-106">Os gravadores devem tratar esse tipo de restauração como se fosse o VSS \_ RTYPE \_ por \_ cópia.</span><span class="sxs-lookup"><span data-stu-id="b2c1d-106">Writers should treat this restore type as if it were VSS\_RTYPE\_BY\_COPY.</span></span> <span data-ttu-id="b2c1d-107">Para obter mais informações sobre valores de tipo de restauração, consulte a enumeração de [**\_ \_ tipo de restauração do VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) .</span><span class="sxs-lookup"><span data-stu-id="b2c1d-107">For more information about restore type values, see the [**VSS\_RESTORE\_TYPE**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) enumeration.</span></span>

 

 



