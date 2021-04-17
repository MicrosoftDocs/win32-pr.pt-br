---
description: 'A versão 2003 do VSS do Windows Server não dá mais suporte ao seguinte:'
ms.assetid: 01993cae-433e-4d01-b805-f97592369575
title: Funcionalidade removida do Windows Server 2003
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181d053420f0fc947ebad024c0eaf2bbaf32f3e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763416"
---
# <a name="functionality-removed-from-windows-server-2003"></a><span data-ttu-id="38085-103">Funcionalidade removida do Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38085-103">Functionality Removed From Windows Server 2003</span></span>

<span data-ttu-id="38085-104">A versão 2003 do VSS do Windows Server não dá mais suporte ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="38085-104">The Windows Server 2003 release of VSS no longer supports the following:</span></span>

-   <span data-ttu-id="38085-105">Os gravadores não podem especificar novos destinos de restauração de arquivo ([*novos locais de destino*](vssgloss-n.md)) em operações de restauração.</span><span class="sxs-lookup"><span data-stu-id="38085-105">Writers cannot specify new file restore destinations ([*new target locations*](vssgloss-n.md)) at restore operations.</span></span>
-   <span data-ttu-id="38085-106">Não há mais suporte para a remontagem de uma cópia de sombra exposta como um volume gravável.</span><span class="sxs-lookup"><span data-stu-id="38085-106">Remounting an exposed shadow copy as a writable volume is no longer supported.</span></span> <span data-ttu-id="38085-107">O método **IVssBackupComponents:: RemountReadWrite** não está mais disponível.</span><span class="sxs-lookup"><span data-stu-id="38085-107">The **IVssBackupComponents::RemountReadWrite** method is no longer available.</span></span>
-   <span data-ttu-id="38085-108">Os gravadores não podem especificar arquivos explicitamente incluídos (usando [**IVssCreateWriterMetadata:: AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)).</span><span class="sxs-lookup"><span data-stu-id="38085-108">Writers cannot specify explicitly included files (using [**IVssCreateWriterMetadata::AddIncludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addincludefiles)).</span></span> <span data-ttu-id="38085-109">Os arquivos podem ser adicionados a um componente somente como parte de um conjunto de arquivos usando [**IVssCreateWriterMetadata:: AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata:: AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)ou [**IVssCreateWriterMetadata:: AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).</span><span class="sxs-lookup"><span data-stu-id="38085-109">Files can be added to a component only as part of a file set by using [**IVssCreateWriterMetadata::AddFilesToFileGroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles), or [**IVssCreateWriterMetadata::AddDatabaseLogFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles).</span></span>

    <span data-ttu-id="38085-110">Os arquivos ainda podem ser explicitamente excluídos de um componente usando [**IVssCreateWriterMetadata:: AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).</span><span class="sxs-lookup"><span data-stu-id="38085-110">Files can still be explicitly excluded from a component by using [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles).</span></span>

 

 



