---
description: A política de metadados de foto para a propriedade System. Photo. LensManufacturer.
ms.assetid: ee25da96-982f-475e-8957-e24ef7721b78
title: Política de metadados de foto System. Photo. LensManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6696e7113a14a9b5b26a26f38258f30a5ba82cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170870"
---
# <a name="systemphotolensmanufacturer-photo-metadata-policy"></a><span data-ttu-id="1d789-103">Política de metadados de foto System. Photo. LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="1d789-103">System.Photo.LensManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="1d789-104">A política de metadados de foto para a propriedade [System. Photo. LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) .</span><span class="sxs-lookup"><span data-stu-id="1d789-104">The photo metadata policy for the [System.Photo.LensManufacturer](../properties/props-system-photo-lensmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="1d789-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="1d789-105">PKEY</span></span>

<span data-ttu-id="1d789-106">PKEY \_ Photo \_ LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="1d789-106">PKEY\_Photo\_LensManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="1d789-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="1d789-107">Containers</span></span>

<span data-ttu-id="1d789-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="1d789-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="1d789-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d789-109">Read-Only</span></span>

<span data-ttu-id="1d789-110">No</span><span class="sxs-lookup"><span data-stu-id="1d789-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="1d789-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="1d789-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="1d789-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="1d789-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="1d789-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="1d789-113">Input Type</span></span>

<span data-ttu-id="1d789-114">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="1d789-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="1d789-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="1d789-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="1d789-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="1d789-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="1d789-117">Precedência de caminhos (JPEG)</span><span class="sxs-lookup"><span data-stu-id="1d789-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="1d789-118">Se o arquivo estiver no formato JPEG, o manipulador usará o caminho a seguir ao ler ou gravar os dados.</span><span class="sxs-lookup"><span data-stu-id="1d789-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="1d789-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="1d789-119">Order</span></span> | <span data-ttu-id="1d789-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="1d789-120">Path</span></span>                                 | <span data-ttu-id="1d789-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1d789-121">Disk Format</span></span> | <span data-ttu-id="1d789-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1d789-122">Required</span></span> |
|-------|--------------------------------------|-------------|----------|
| <span data-ttu-id="1d789-123">1</span><span class="sxs-lookup"><span data-stu-id="1d789-123">1</span></span>     | <span data-ttu-id="1d789-124">/xmp/MicrosoftPhoto:LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="1d789-124">/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="1d789-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="1d789-125">Unicode</span></span>     | <span data-ttu-id="1d789-126">Yes</span><span class="sxs-lookup"><span data-stu-id="1d789-126">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="1d789-127">Precedência de caminhos (TIFF)</span><span class="sxs-lookup"><span data-stu-id="1d789-127">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="1d789-128">Se o arquivo estiver no formato TIFF, o manipulador usará a ordem de precedência a seguir ao ler ou gravar os dados.</span><span class="sxs-lookup"><span data-stu-id="1d789-128">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="1d789-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="1d789-129">Order</span></span> | <span data-ttu-id="1d789-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="1d789-130">Path</span></span>                                     | <span data-ttu-id="1d789-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="1d789-131">Disk Format</span></span> | <span data-ttu-id="1d789-132">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="1d789-132">Required</span></span> |
|-------|------------------------------------------|-------------|----------|
| <span data-ttu-id="1d789-133">1</span><span class="sxs-lookup"><span data-stu-id="1d789-133">1</span></span>     | <span data-ttu-id="1d789-134">/ifd/xmp/MicrosoftPhoto:LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="1d789-134">/ifd/xmp/MicrosoftPhoto:LensManufacturer</span></span> | <span data-ttu-id="1d789-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="1d789-135">Unicode</span></span>     | <span data-ttu-id="1d789-136">Yes</span><span class="sxs-lookup"><span data-stu-id="1d789-136">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="1d789-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d789-137">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d789-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1d789-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d789-139">System. Photo. LensManufacturer</span><span class="sxs-lookup"><span data-stu-id="1d789-139">System.Photo.LensManufacturer</span></span>](../properties/props-system-photo-lensmanufacturer.md)
</dt> </dl>

 

 
