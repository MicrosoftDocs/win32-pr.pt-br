---
description: O estado de instalação de um arquivo complementar não depende de suas próprias informações de controle de versão de arquivo, mas no controle de versão de seu pai complementar.
ms.assetid: 3c1e3507-8ed9-4ce8-8d38-6c8248a9e883
title: Arquivos complementares
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c927c377c7111e89c6f97b385610da9e09f8bdd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922250"
---
# <a name="companion-files"></a><span data-ttu-id="5d112-103">Arquivos complementares</span><span class="sxs-lookup"><span data-stu-id="5d112-103">Companion Files</span></span>

<span data-ttu-id="5d112-104">O estado de instalação de um arquivo complementar não depende de suas próprias informações de controle de versão de arquivo, mas no controle de versão de seu pai complementar.</span><span class="sxs-lookup"><span data-stu-id="5d112-104">The installation state of a companion file depends not on its own file versioning information, but on the versioning of its companion parent.</span></span> <span data-ttu-id="5d112-105">Consulte as [regras de controle de versão de arquivo](file-versioning-rules.md).</span><span class="sxs-lookup"><span data-stu-id="5d112-105">See the [File Versioning Rules](file-versioning-rules.md).</span></span> <span data-ttu-id="5d112-106">Para especificar um arquivo complementar, a chave primária do pai complementar na tabela de [arquivos](file-table.md) deve ser criada na coluna versão do registro para o complemento.</span><span class="sxs-lookup"><span data-stu-id="5d112-106">To specify a companion file, the primary key of the companion parent in the [File table](file-table.md) must be authored into the Version column of the record for the companion.</span></span>

<span data-ttu-id="5d112-107">No exemplo a seguir, fileA é o pai complementar e FileB é o arquivo complementar.</span><span class="sxs-lookup"><span data-stu-id="5d112-107">In the following example, FileA is the companion parent and FileB is the companion file.</span></span>

<span data-ttu-id="5d112-108">[Tabela de arquivos](file-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="5d112-108">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="5d112-109">Arquivo</span><span class="sxs-lookup"><span data-stu-id="5d112-109">File</span></span>  | <span data-ttu-id="5d112-110">Versão</span><span class="sxs-lookup"><span data-stu-id="5d112-110">Version</span></span> |
|-------|---------|
| <span data-ttu-id="5d112-111">FileA</span><span class="sxs-lookup"><span data-stu-id="5d112-111">FileA</span></span> | <span data-ttu-id="5d112-112">1.0.0.0</span><span class="sxs-lookup"><span data-stu-id="5d112-112">1.0.0.0</span></span> |
| <span data-ttu-id="5d112-113">FileB</span><span class="sxs-lookup"><span data-stu-id="5d112-113">FileB</span></span> | <span data-ttu-id="5d112-114">FileA</span><span class="sxs-lookup"><span data-stu-id="5d112-114">FileA</span></span>   |



 

<span data-ttu-id="5d112-115">Neste exemplo, o estado de instalação de FileB depende das [regras de controle de versão de arquivo](file-versioning-rules.md) e das informações de controle de versão do fileA.</span><span class="sxs-lookup"><span data-stu-id="5d112-115">In this example, the installation state of FileB depends on the [File Versioning Rules](file-versioning-rules.md) and the versioning information for FileA.</span></span> <span data-ttu-id="5d112-116">Se o instalador determinar que a versão do ArquivoA no pacote deve ser instalada em uma versão mais antiga do fileA que já existe no computador do usuário, ele também instalará o FileB do pacote, independentemente da versão de qualquer FileB instalado.</span><span class="sxs-lookup"><span data-stu-id="5d112-116">If the installer determines that the version of FileA in the package should be installed over an older version of FileA that already exists on the user's computer, it will also install FileB from the package regardless of the version of any installed FileB.</span></span>

<span data-ttu-id="5d112-117">Observe que um arquivo que é o caminho de chave para seu componente não deve ser um arquivo complementar.</span><span class="sxs-lookup"><span data-stu-id="5d112-117">Note that a file that is the key path for its component must not be a companion file.</span></span> <span data-ttu-id="5d112-118">Isso resultaria na lógica de controle de versão do arquivo de caminho de chave sendo determinado pelo arquivo pai complementar.</span><span class="sxs-lookup"><span data-stu-id="5d112-118">This would result in the versioning logic of the key path file being determined by the companion parent file.</span></span>

 

 



