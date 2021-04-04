---
description: Os diagramas de fluxo nas seções a seguir ilustram as regras de controle de versão de arquivo padrão usadas quando o arquivo de chave de um componente que está sendo instalado tem o mesmo nome que um arquivo já instalado no local de destino.
ms.assetid: a09e091c-ee82-4951-b129-d1d4c8948883
title: Controle de versão de arquivo padrão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fad33a7af49c28b560d9d558abbc86b220c4cb42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829010"
---
# <a name="default-file-versioning"></a><span data-ttu-id="58e1c-103">Controle de versão de arquivo padrão</span><span class="sxs-lookup"><span data-stu-id="58e1c-103">Default File Versioning</span></span>

<span data-ttu-id="58e1c-104">Os diagramas de fluxo nas seções a seguir ilustram as regras de controle de versão de arquivo padrão usadas quando o arquivo de chave de um componente que está sendo instalado tem o mesmo nome que um arquivo já instalado no local de destino.</span><span class="sxs-lookup"><span data-stu-id="58e1c-104">The flow diagrams in the following sections illustrate the default file versioning rules used when the key file of a component being installed has the same name as a file already installed in the target location.</span></span> <span data-ttu-id="58e1c-105">O controle de versão de arquivo padrão também é ilustrado na [substituição de arquivos existentes](replacing-existing-files.md).</span><span class="sxs-lookup"><span data-stu-id="58e1c-105">Default file versioning is also illustrated in [Replacing Existing Files](replacing-existing-files.md).</span></span>

<span data-ttu-id="58e1c-106">Observe que, com Windows Installer, o hash de arquivo está disponível para otimizar a cópia dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="58e1c-106">Note that with Windows Installer, file hashing is available to optimize the copying of files.</span></span> <span data-ttu-id="58e1c-107">Para obter detalhes, consulte [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) e a [tabela MsiFileHash](msifilehash-table.md).</span><span class="sxs-lookup"><span data-stu-id="58e1c-107">For details, see [**MsiGetFileHash**](/windows/desktop/api/Msi/nf-msi-msigetfilehasha) and the [MsiFileHash table](msifilehash-table.md).</span></span> <span data-ttu-id="58e1c-108">A tabela MsiFileHash só pode ser usada com arquivos sem versão.</span><span class="sxs-lookup"><span data-stu-id="58e1c-108">The MsiFileHash table can only be used with unversioned files.</span></span>

-   [<span data-ttu-id="58e1c-109">Ambos os arquivos têm uma versão</span><span class="sxs-lookup"><span data-stu-id="58e1c-109">Both Files Have a Version</span></span>](both-files-have-a-version.md)
-   [<span data-ttu-id="58e1c-110">Nenhum arquivo tem uma versão</span><span class="sxs-lookup"><span data-stu-id="58e1c-110">Neither File Has a Version</span></span>](neither-file-has-a-version.md)
-   [<span data-ttu-id="58e1c-111">Nenhum arquivo tem uma versão com verificação de hash de arquivo</span><span class="sxs-lookup"><span data-stu-id="58e1c-111">Neither File Has a Version with File Hash Check</span></span>](neither-file-has-a-version-with-file-hash-check.md)
-   [<span data-ttu-id="58e1c-112">Um arquivo tem uma versão</span><span class="sxs-lookup"><span data-stu-id="58e1c-112">One File Has a Version</span></span>](one-file-has-a-version.md)

 

 



