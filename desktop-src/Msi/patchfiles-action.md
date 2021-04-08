---
description: A ação PatchFiles consulta a tabela de patch para determinar quais patches devem ser aplicados. A ação PatchFiles também executa a aplicação de patches em byte dos arquivos.
ms.assetid: 4026755e-a006-40c0-8816-de5358f4582e
title: Ação PatchFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53583a93089444f014d9cc837fb18acf21cec82d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828436"
---
# <a name="patchfiles-action"></a><span data-ttu-id="74db3-104">Ação PatchFiles</span><span class="sxs-lookup"><span data-stu-id="74db3-104">PatchFiles Action</span></span>

<span data-ttu-id="74db3-105">A ação PatchFiles consulta a [tabela de patch](patch-table.md) para determinar quais patches devem ser aplicados.</span><span class="sxs-lookup"><span data-stu-id="74db3-105">The PatchFiles action queries the [Patch table](patch-table.md) to determine which patches are to be applied.</span></span> <span data-ttu-id="74db3-106">A ação PatchFiles também executa a aplicação de patches em byte dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="74db3-106">The PatchFiles action also performs the byte-wise patching of the files.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="74db3-107">Restrições de sequência</span><span class="sxs-lookup"><span data-stu-id="74db3-107">Sequence Restrictions</span></span>

<span data-ttu-id="74db3-108">Se o arquivo a ser corrigido não estiver instalado, a ação PatchFiles deverá vir após a [ação InstallFiles](installfiles-action.md) que instala o arquivo.</span><span class="sxs-lookup"><span data-stu-id="74db3-108">If the file that is to be patched is not installed, the PatchFiles action must come after the [InstallFiles action](installfiles-action.md) that installs the file.</span></span> <span data-ttu-id="74db3-109">Os arquivos instalados anteriormente podem ser corrigidos em qualquer ponto na sequência de ação.</span><span class="sxs-lookup"><span data-stu-id="74db3-109">Previously installed files may be patched at any point in the action sequence.</span></span> <span data-ttu-id="74db3-110">A [ação DuplicateFiles](duplicatefiles-action.md) deve vir após a ação PatchFiles para impedir a duplicação da versão sem patch do arquivo.</span><span class="sxs-lookup"><span data-stu-id="74db3-110">The [DuplicateFiles Action](duplicatefiles-action.md) must come after the PatchFiles action to prevent duplicating the unpatched version of the file.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="74db3-111">Mensagens ActionData</span><span class="sxs-lookup"><span data-stu-id="74db3-111">ActionData Messages</span></span>



| <span data-ttu-id="74db3-112">Campo</span><span class="sxs-lookup"><span data-stu-id="74db3-112">Field</span></span> | <span data-ttu-id="74db3-113">Descrição dos dados da ação</span><span class="sxs-lookup"><span data-stu-id="74db3-113">Description of action data</span></span>                    |
|-------|-----------------------------------------------|
| <span data-ttu-id="74db3-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="74db3-114">\[1\]</span></span> | <span data-ttu-id="74db3-115">Identificador do arquivo com patch.</span><span class="sxs-lookup"><span data-stu-id="74db3-115">Identifier of patched file.</span></span>                   |
| <span data-ttu-id="74db3-116">\[2\]</span><span class="sxs-lookup"><span data-stu-id="74db3-116">\[2\]</span></span> | <span data-ttu-id="74db3-117">Identificador do diretório que contém o arquivo com patch.</span><span class="sxs-lookup"><span data-stu-id="74db3-117">Identifier of directory holding patched file.</span></span> |
| <span data-ttu-id="74db3-118">\[3\]</span><span class="sxs-lookup"><span data-stu-id="74db3-118">\[3\]</span></span> | <span data-ttu-id="74db3-119">Tamanho do patch em bytes.</span><span class="sxs-lookup"><span data-stu-id="74db3-119">Size of patch in bytes.</span></span>                       |



 

 

 



