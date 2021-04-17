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
# <a name="vss-restore-state"></a>Estado de restauração do VSS

Durante uma operação de restauração, o solicitante pode usar o método [**IVssBackupComponents:: setrestore**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-setrestorestate) para definir o tipo de operação de restauração em andamento. No entanto, a maioria das operações de restauração não precisará substituir o tipo de restauração padrão (VSS \_ RTYPE \_ indefinido). Os gravadores devem tratar esse tipo de restauração como se fosse o VSS \_ RTYPE \_ por \_ cópia. Para obter mais informações sobre valores de tipo de restauração, consulte a enumeração de [**\_ \_ tipo de restauração do VSS**](/windows/desktop/api/Vss/ne-vss-vss_restore_type) .

 

 



