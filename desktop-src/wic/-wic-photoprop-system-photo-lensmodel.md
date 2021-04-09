---
description: A política de metadados de foto para a propriedade System. Photo. LensModel.
ms.assetid: 39aeff17-e8d3-4ceb-86a1-1749d2ca98d6
title: Política de metadados de foto System. Photo. LensModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a5249136346407ab9fcd1e4802d6910d3e514a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011538"
---
# <a name="systemphotolensmodel-photo-metadata-policy"></a><span data-ttu-id="1b47e-103">Política de metadados de foto System. Photo. LensModel</span><span class="sxs-lookup"><span data-stu-id="1b47e-103">System.Photo.LensModel Photo Metadata Policy</span></span>

<span data-ttu-id="1b47e-104">A política de metadados de foto para a propriedade [System. Photo. LensModel](../properties/props-system-photo-lensmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="1b47e-104">The photo metadata policy for the [System.Photo.LensModel](../properties/props-system-photo-lensmodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1b47e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="1b47e-105">PKEY</span></span>

<span data-ttu-id="1b47e-106">PKEY \_ Photo \_ LensModel</span><span class="sxs-lookup"><span data-stu-id="1b47e-106">PKEY\_Photo\_LensModel</span></span>

### <a name="containers"></a><span data-ttu-id="1b47e-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="1b47e-107">Containers</span></span>

<span data-ttu-id="1b47e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1b47e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1b47e-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1b47e-109">Read-Only</span></span>

<span data-ttu-id="1b47e-110">No</span><span class="sxs-lookup"><span data-stu-id="1b47e-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1b47e-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="1b47e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1b47e-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="1b47e-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="1b47e-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="1b47e-113">Input Type</span></span>

<span data-ttu-id="1b47e-114">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1b47e-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1b47e-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="1b47e-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="1b47e-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="1b47e-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="1b47e-117">Precedência de caminhos (JPEG)</span><span class="sxs-lookup"><span data-stu-id="1b47e-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="1b47e-118">Se o arquivo estiver no formato JPEG, o manipulador usará o caminho a seguir ao ler ou gravar os dados.</span><span class="sxs-lookup"><span data-stu-id="1b47e-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="1b47e-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="1b47e-119">Order</span></span> | <span data-ttu-id="1b47e-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="1b47e-120">Path</span></span>                          | <span data-ttu-id="1b47e-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1b47e-121">Disk Format</span></span> | <span data-ttu-id="1b47e-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1b47e-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="1b47e-123">1</span><span class="sxs-lookup"><span data-stu-id="1b47e-123">1</span></span>     | <span data-ttu-id="1b47e-124">/xmp/MicrosoftPhoto:LensModel</span><span class="sxs-lookup"><span data-stu-id="1b47e-124">/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="1b47e-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="1b47e-125">Unicode</span></span>     | <span data-ttu-id="1b47e-126">Yes</span><span class="sxs-lookup"><span data-stu-id="1b47e-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="1b47e-127">Precedência de caminhos (TIFF)</span><span class="sxs-lookup"><span data-stu-id="1b47e-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="1b47e-128">Se o arquivo estiver no formato TIFF, o manipulador usará a ordem de precedência a seguir ao ler ou gravar os dados.</span><span class="sxs-lookup"><span data-stu-id="1b47e-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="1b47e-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="1b47e-129">Order</span></span> | <span data-ttu-id="1b47e-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="1b47e-130">Path</span></span>                              | <span data-ttu-id="1b47e-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1b47e-131">Disk Format</span></span> | <span data-ttu-id="1b47e-132">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1b47e-132">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="1b47e-133">1</span><span class="sxs-lookup"><span data-stu-id="1b47e-133">1</span></span>     | <span data-ttu-id="1b47e-134">/ifd/xmp/MicrosoftPhoto:LensModel</span><span class="sxs-lookup"><span data-stu-id="1b47e-134">/ifd/xmp/MicrosoftPhoto:LensModel</span></span> | <span data-ttu-id="1b47e-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="1b47e-135">Unicode</span></span>     | <span data-ttu-id="1b47e-136">Yes</span><span class="sxs-lookup"><span data-stu-id="1b47e-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="1b47e-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b47e-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1b47e-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b47e-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b47e-139">System. Photo. LensModel</span><span class="sxs-lookup"><span data-stu-id="1b47e-139">System.Photo.LensModel</span></span>](../properties/props-system-photo-lensmodel.md)
</dt> </dl>

 

 
