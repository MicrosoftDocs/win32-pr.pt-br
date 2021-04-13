---
description: 'A combinação de caminho, especificação de arquivo e sinalizador de recursão (wszPath, wszFileSpec e bRecursive, respectivamente) deve corresponder à de um dos conjuntos de arquivos adicionados a um dos componentes do gravador usando IVssCreateWriterMetadata:: AddFilesToFileGroup, IVssCreateWriterMetadata:: AddDatabaseFiles ou IVssCreateWriterMetadata:: AddDatabaseLogFiles quando:'
ms.assetid: debf181a-1579-46f2-86ef-a1d2a850e99e
title: Alterações semânticas no Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b9d2edc56f215f554b497eebff9f76a1da53dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165419"
---
# <a name="semantic-changes-to-windows-server-2003"></a><span data-ttu-id="6ad4b-103">Alterações semânticas no Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="6ad4b-103">Semantic Changes to Windows Server 2003</span></span>

<span data-ttu-id="6ad4b-104">A combinação de caminho, especificação de arquivo e sinalizador de recursão (*wszPath*, *wszFileSpec* e *bRecursive*, respectivamente) deve corresponder à de um dos conjuntos de arquivos adicionados a um dos componentes do gravador usando [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) quando:</span><span class="sxs-lookup"><span data-stu-id="6ad4b-104">The combination of path, file specification, and recursion flag (*wszPath*, *wszFileSpec*, and *bRecursive*, respectively) must match that of one of the file sets added to one of the writer's components using [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), or [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) when:</span></span>

-   <span data-ttu-id="6ad4b-105">Um solicitante adiciona um novo destino usando [**IVssBackupComponents:: AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).</span><span class="sxs-lookup"><span data-stu-id="6ad4b-105">A requester adds a new target using [**IVssBackupComponents::AddNewTarget**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addnewtarget).</span></span>
-   <span data-ttu-id="6ad4b-106">Um gravador adiciona um mapeamento de local alternativo usando [**IVssCreateWriterMetadata:: AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping).</span><span class="sxs-lookup"><span data-stu-id="6ad4b-106">A writer adds an alternate location mapping using [**IVssCreateWriterMetadata::AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping).</span></span>
-   <span data-ttu-id="6ad4b-107">Os arquivos existentes são adicionados como arquivos diferenciados usando [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime).</span><span class="sxs-lookup"><span data-stu-id="6ad4b-107">Existing files are added as differenced files using [**IVssComponent::AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime).</span></span>
-   <span data-ttu-id="6ad4b-108">Um solicitante indica que um mapeamento de local alternativo foi usado para restaurar um conjunto de arquivos usando [**IVssBackupComponents:: AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping).</span><span class="sxs-lookup"><span data-stu-id="6ad4b-108">A requester indicates that an alternate location mapping was used to restore a file set using [**IVssBackupComponents::AddAlternativeLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponents-addalternativelocationmapping).</span></span>

 

 



