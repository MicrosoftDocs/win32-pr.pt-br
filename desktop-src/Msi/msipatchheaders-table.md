---
description: A tabela MsiPatchHeaders contém os fluxos de cabeçalho de patch binários usados para validação de patch.
ms.assetid: aefdd365-1681-43e4-8470-04a5d6efd993
title: Tabela MsiPatchHeaders
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a3fa4e037a31f3e913f13ff9c96735ed6760dc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104169847"
---
# <a name="msipatchheaders-table"></a><span data-ttu-id="ed346-103">Tabela MsiPatchHeaders</span><span class="sxs-lookup"><span data-stu-id="ed346-103">MsiPatchHeaders Table</span></span>

<span data-ttu-id="ed346-104">A tabela MsiPatchHeaders contém os fluxos de cabeçalho de patch binários usados para validação de patch.</span><span class="sxs-lookup"><span data-stu-id="ed346-104">The MsiPatchHeaders table holds the binary patch header streams used for patch validation.</span></span>

<span data-ttu-id="ed346-105">A tabela MsiPatchHeaders é usada quando chaves de [tabela de arquivos](file-table.md) longos resultam em uma falha ao gerar o fluxo de cabeçalho de patch na tabela de [patches](patch-table.md).</span><span class="sxs-lookup"><span data-stu-id="ed346-105">The MsiPatchHeaders table is used when long [File table](file-table.md) keys result in a failure to generate the patch header stream in the [Patch table](patch-table.md).</span></span> <span data-ttu-id="ed346-106">Isso pode ser devido à limitação de nome de fluxo descrita em [limitações de OLE em fluxos](ole-limitations-on-streams.md).</span><span class="sxs-lookup"><span data-stu-id="ed346-106">This can be due to the stream name limitation described in [OLE Limitations on Streams](ole-limitations-on-streams.md).</span></span> <span data-ttu-id="ed346-107">Nesse caso, a tabela de patch pode fazer referência à tabela MsiPatchHeaders para criar o fluxo de cabeçalho de patch.</span><span class="sxs-lookup"><span data-stu-id="ed346-107">In this case, the Patch table can reference the MsiPatchHeaders table to create the patch header stream.</span></span>

<span data-ttu-id="ed346-108">A tabela MsiPatchHeaders tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="ed346-108">The MsiPatchHeaders table has the following columns.</span></span>



| <span data-ttu-id="ed346-109">Coluna</span><span class="sxs-lookup"><span data-stu-id="ed346-109">Column</span></span>    | <span data-ttu-id="ed346-110">Tipo</span><span class="sxs-lookup"><span data-stu-id="ed346-110">Type</span></span>                         | <span data-ttu-id="ed346-111">Chave</span><span class="sxs-lookup"><span data-stu-id="ed346-111">Key</span></span> | <span data-ttu-id="ed346-112">Nullable</span><span class="sxs-lookup"><span data-stu-id="ed346-112">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="ed346-113">StreamRef</span><span class="sxs-lookup"><span data-stu-id="ed346-113">StreamRef</span></span> | [<span data-ttu-id="ed346-114">Identificador</span><span class="sxs-lookup"><span data-stu-id="ed346-114">Identifier</span></span>](identifier.md) | <span data-ttu-id="ed346-115">S</span><span class="sxs-lookup"><span data-stu-id="ed346-115">Y</span></span>   | <span data-ttu-id="ed346-116">N</span><span class="sxs-lookup"><span data-stu-id="ed346-116">N</span></span>        |
| <span data-ttu-id="ed346-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed346-117">Header</span></span>    | [<span data-ttu-id="ed346-118">Binary</span><span class="sxs-lookup"><span data-stu-id="ed346-118">Binary</span></span>](binary.md)         | <span data-ttu-id="ed346-119">N</span><span class="sxs-lookup"><span data-stu-id="ed346-119">N</span></span>   | <span data-ttu-id="ed346-120">N</span><span class="sxs-lookup"><span data-stu-id="ed346-120">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="ed346-121">Colunas</span><span class="sxs-lookup"><span data-stu-id="ed346-121">Columns</span></span>

<dl> <dt>

<span data-ttu-id="ed346-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef</span><span class="sxs-lookup"><span data-stu-id="ed346-122"><span id="StreamRef"></span><span id="streamref"></span><span id="STREAMREF"></span>StreamRef</span></span>
</dt> <dd>

<span data-ttu-id="ed346-123">A chave primária da tabela que identifica exclusivamente um cabeçalho de patch específico.</span><span class="sxs-lookup"><span data-stu-id="ed346-123">The primary key for the table that uniquely identifies a particular patch header.</span></span>

</dd> <dt>

<span data-ttu-id="ed346-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Verga</span><span class="sxs-lookup"><span data-stu-id="ed346-124"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="ed346-125">Esta coluna é o cabeçalho de patch de fluxo binário usado para validação de patch.</span><span class="sxs-lookup"><span data-stu-id="ed346-125">This column is the binary stream patch header used for patch validation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed346-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed346-126">Remarks</span></span>

<span data-ttu-id="ed346-127">Essa tabela é processada pela [ação PatchFiles](patchfiles-action.md).</span><span class="sxs-lookup"><span data-stu-id="ed346-127">This table is processed by the [PatchFiles action](patchfiles-action.md).</span></span> <span data-ttu-id="ed346-128">Normalmente, essa tabela é adicionada ao pacote de instalação por uma transformação de um pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="ed346-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="ed346-129">Normalmente, ele não é criado diretamente em um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="ed346-129">It is usually not authored directly into an installation package.</span></span>

## <a name="validation"></a><span data-ttu-id="ed346-130">Validação</span><span class="sxs-lookup"><span data-stu-id="ed346-130">Validation</span></span>

<dl>

[<span data-ttu-id="ed346-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="ed346-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="ed346-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="ed346-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="ed346-133">ICE29</span><span class="sxs-lookup"><span data-stu-id="ed346-133">ICE29</span></span>](ice29.md)  
</dl>

 

 



