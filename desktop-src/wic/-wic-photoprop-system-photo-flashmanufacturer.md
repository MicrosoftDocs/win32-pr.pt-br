---
description: A política de metadados de foto para a propriedade System. Photo. FlashManufacturer.
ms.assetid: f62e85ec-2dc6-456b-a43b-7b76d162b608
title: Política de metadados de foto System. Photo. FlashManufacturer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1e785dfd00662acf065021a3c80de5c587586c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011677"
---
# <a name="systemphotoflashmanufacturer-photo-metadata-policy"></a><span data-ttu-id="28221-103">Política de metadados de foto System. Photo. FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="28221-103">System.Photo.FlashManufacturer Photo Metadata Policy</span></span>

<span data-ttu-id="28221-104">A política de metadados de foto para a propriedade [System. Photo. FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) .</span><span class="sxs-lookup"><span data-stu-id="28221-104">The photo metadata policy for the [System.Photo.FlashManufacturer](../properties/props-system-photo-flashmanufacturer.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="28221-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="28221-105">PKEY</span></span>

<span data-ttu-id="28221-106">PKEY \_ Photo \_ FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="28221-106">PKEY\_Photo\_FlashManufacturer</span></span>

### <a name="containers"></a><span data-ttu-id="28221-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="28221-107">Containers</span></span>

<span data-ttu-id="28221-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="28221-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="28221-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="28221-109">Read-Only</span></span>

<span data-ttu-id="28221-110">No</span><span class="sxs-lookup"><span data-stu-id="28221-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="28221-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="28221-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="28221-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="28221-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="28221-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="28221-113">Input Type</span></span>

<span data-ttu-id="28221-114">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="28221-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="28221-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="28221-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="28221-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="28221-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="28221-117">Precedência de caminhos (JPEG)</span><span class="sxs-lookup"><span data-stu-id="28221-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="28221-118">Se o arquivo estiver no formato JPEG, o manipulador usará o caminho a seguir ao ler ou gravar os dados.</span><span class="sxs-lookup"><span data-stu-id="28221-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="28221-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="28221-119">Order</span></span> | <span data-ttu-id="28221-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="28221-120">Path</span></span>                                  | <span data-ttu-id="28221-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="28221-121">Disk Format</span></span> | <span data-ttu-id="28221-122">Formato de Dados</span><span class="sxs-lookup"><span data-stu-id="28221-122">Data Format</span></span> | <span data-ttu-id="28221-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="28221-123">Required</span></span> |
|-------|---------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="28221-124">1</span><span class="sxs-lookup"><span data-stu-id="28221-124">1</span></span>     | <span data-ttu-id="28221-125">/xmp/MicrosoftPhoto:FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="28221-125">/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="28221-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="28221-126">Unicode</span></span>     |             | <span data-ttu-id="28221-127">Yes</span><span class="sxs-lookup"><span data-stu-id="28221-127">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="28221-128">Precedência de caminhos (TIFF)</span><span class="sxs-lookup"><span data-stu-id="28221-128">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="28221-129">Se o arquivo estiver no formato TIFF, o manipulador usará a ordem de precedência a seguir ao ler ou gravar os dados.</span><span class="sxs-lookup"><span data-stu-id="28221-129">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="28221-130">Ordem</span><span class="sxs-lookup"><span data-stu-id="28221-130">Order</span></span> | <span data-ttu-id="28221-131">Caminho</span><span class="sxs-lookup"><span data-stu-id="28221-131">Path</span></span>                                      | <span data-ttu-id="28221-132">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="28221-132">Disk Format</span></span> | <span data-ttu-id="28221-133">Formato de Dados</span><span class="sxs-lookup"><span data-stu-id="28221-133">Data Format</span></span> | <span data-ttu-id="28221-134">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="28221-134">Required</span></span> |
|-------|-------------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="28221-135">1</span><span class="sxs-lookup"><span data-stu-id="28221-135">1</span></span>     | <span data-ttu-id="28221-136">/ifd/xmp/MicrosoftPhoto:FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="28221-136">/ifd/xmp/MicrosoftPhoto:FlashManufacturer</span></span> | <span data-ttu-id="28221-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="28221-137">Unicode</span></span>     |             | <span data-ttu-id="28221-138">Yes</span><span class="sxs-lookup"><span data-stu-id="28221-138">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="28221-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="28221-139">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="28221-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="28221-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28221-141">System. Photo. FlashManufacturer</span><span class="sxs-lookup"><span data-stu-id="28221-141">System.Photo.FlashManufacturer</span></span>](../properties/props-system-photo-flashmanufacturer.md)
</dt> </dl>

 

 
