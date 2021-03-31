---
description: A tabela PatchPackage descreve todos os pacotes de patch que foram aplicados a este produto. Para cada pacote de patch, o identificador exclusivo do patch é fornecido juntamente com informações sobre a imagem de mídia em que o patch está localizado.
ms.assetid: 212d99dd-c80c-42ca-9dfa-819ae1813006
title: Tabela PatchPackage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13bf9fc03012ca54a0b2144e97c828c968c68da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172010"
---
# <a name="patchpackage-table"></a><span data-ttu-id="08d83-104">Tabela PatchPackage</span><span class="sxs-lookup"><span data-stu-id="08d83-104">PatchPackage Table</span></span>

<span data-ttu-id="08d83-105">A tabela PatchPackage descreve todos os pacotes de patch que foram aplicados a este produto.</span><span class="sxs-lookup"><span data-stu-id="08d83-105">The PatchPackage table describes all patch packages that have been applied to this product.</span></span> <span data-ttu-id="08d83-106">Para cada pacote de patch, o identificador exclusivo do patch é fornecido juntamente com informações sobre a imagem de mídia em que o patch está localizado.</span><span class="sxs-lookup"><span data-stu-id="08d83-106">For each patch package, the unique identifier for the patch is provided along with information about the media image the on which the patch is located.</span></span>

<span data-ttu-id="08d83-107">A tabela PatchPackage tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="08d83-107">The PatchPackage table has the following columns.</span></span>



| <span data-ttu-id="08d83-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="08d83-108">Column</span></span>  | <span data-ttu-id="08d83-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="08d83-109">Type</span></span>                   | <span data-ttu-id="08d83-110">Chave</span><span class="sxs-lookup"><span data-stu-id="08d83-110">Key</span></span> | <span data-ttu-id="08d83-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="08d83-111">Nullable</span></span> |
|---------|------------------------|-----|----------|
| <span data-ttu-id="08d83-112">PatchID</span><span class="sxs-lookup"><span data-stu-id="08d83-112">PatchId</span></span> | [<span data-ttu-id="08d83-113">GUID</span><span class="sxs-lookup"><span data-stu-id="08d83-113">GUID</span></span>](guid.md)       | <span data-ttu-id="08d83-114">S</span><span class="sxs-lookup"><span data-stu-id="08d83-114">Y</span></span>   | <span data-ttu-id="08d83-115">N</span><span class="sxs-lookup"><span data-stu-id="08d83-115">N</span></span>        |
| <span data-ttu-id="08d83-116">Mídia\_</span><span class="sxs-lookup"><span data-stu-id="08d83-116">Media\_</span></span> | [<span data-ttu-id="08d83-117">Inteiro</span><span class="sxs-lookup"><span data-stu-id="08d83-117">Integer</span></span>](integer.md) | <span data-ttu-id="08d83-118">N</span><span class="sxs-lookup"><span data-stu-id="08d83-118">N</span></span>   | <span data-ttu-id="08d83-119">N</span><span class="sxs-lookup"><span data-stu-id="08d83-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="08d83-120">Colunas</span><span class="sxs-lookup"><span data-stu-id="08d83-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="08d83-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchID</span><span class="sxs-lookup"><span data-stu-id="08d83-121"><span id="PatchId"></span><span id="patchid"></span><span id="PATCHID"></span>PatchId</span></span>
</dt> <dd>

<span data-ttu-id="08d83-122">Esta coluna contém um identificador exclusivo para esse patch específico.</span><span class="sxs-lookup"><span data-stu-id="08d83-122">This column contains a unique identifier for this particular patch.</span></span>

</dd> <dt>

<span data-ttu-id="08d83-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Meio\_</span><span class="sxs-lookup"><span data-stu-id="08d83-123"><span id="Media_"></span><span id="media_"></span><span id="MEDIA_"></span>Media\_</span></span>
</dt> <dd>

<span data-ttu-id="08d83-124">Esta coluna é uma chave estrangeira para a coluna DiskId da [tabela de mídia](media-table.md) e indica o disco que contém o pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="08d83-124">This column is a foreign key to the DiskId column of the [Media Table](media-table.md) and indicates the disk containing the patch package.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08d83-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="08d83-125">Remarks</span></span>

<span data-ttu-id="08d83-126">A tabela PatchPackage é necessária em cada pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="08d83-126">The PatchPackage table is required in every patch package.</span></span> <span data-ttu-id="08d83-127">Se a tabela estiver ausente, as tentativas de instalar o patch falharão com "erro 2768: a transformação no pacote de patch é inválida."</span><span class="sxs-lookup"><span data-stu-id="08d83-127">If the table is missing, attempts to install the patch fail with "Error 2768: Transform in patch package is invalid."</span></span> <span data-ttu-id="08d83-128">Normalmente, essa tabela é adicionada ao pacote de instalação por uma transformação de um pacote de patch.</span><span class="sxs-lookup"><span data-stu-id="08d83-128">This table is usually added to the install package by a transform from a patch package.</span></span> <span data-ttu-id="08d83-129">Normalmente, ele não é criado diretamente em um pacote de instalação.</span><span class="sxs-lookup"><span data-stu-id="08d83-129">It is usually not authored directly into an install package.</span></span>

## <a name="validation"></a><span data-ttu-id="08d83-130">Validação</span><span class="sxs-lookup"><span data-stu-id="08d83-130">Validation</span></span>

<dl>

[<span data-ttu-id="08d83-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="08d83-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="08d83-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="08d83-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



