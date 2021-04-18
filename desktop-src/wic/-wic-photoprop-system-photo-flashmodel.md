---
description: A política de metadados de foto para a propriedade System. Photo. FlashModel.
ms.assetid: ef322823-1b87-40ea-a5e3-e7551f14e44d
title: Política de metadados de foto System. Photo. FlashModel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ade3769cb0d852239af84b769b85d5b3849589
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105763123"
---
# <a name="systemphotoflashmodel-photo-metadata-policy"></a><span data-ttu-id="17281-103">Política de metadados de foto System. Photo. FlashModel</span><span class="sxs-lookup"><span data-stu-id="17281-103">System.Photo.FlashModel Photo Metadata Policy</span></span>

<span data-ttu-id="17281-104">A política de metadados de foto para a propriedade [System. Photo. FlashModel](../properties/props-system-photo-flashmodel.md) .</span><span class="sxs-lookup"><span data-stu-id="17281-104">The photo metadata policy for the [System.Photo.FlashModel](../properties/props-system-photo-flashmodel.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="17281-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="17281-105">PKEY</span></span>

<span data-ttu-id="17281-106">PKEY \_ Photo \_ FlashModel</span><span class="sxs-lookup"><span data-stu-id="17281-106">PKEY\_Photo\_FlashModel</span></span>

### <a name="containers"></a><span data-ttu-id="17281-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="17281-107">Containers</span></span>

<span data-ttu-id="17281-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="17281-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="17281-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="17281-109">Read-Only</span></span>

<span data-ttu-id="17281-110">No</span><span class="sxs-lookup"><span data-stu-id="17281-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="17281-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="17281-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="17281-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="17281-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="17281-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="17281-113">Input Type</span></span>

<span data-ttu-id="17281-114">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="17281-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="17281-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="17281-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="17281-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="17281-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="17281-117">Precedência de caminhos (JPEG)</span><span class="sxs-lookup"><span data-stu-id="17281-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="17281-118">Se o arquivo estiver no formato JPEG, o manipulador usará o caminho a seguir ao ler ou gravar os dados.</span><span class="sxs-lookup"><span data-stu-id="17281-118">If the file is in JPEG format, the handler will use the following path when reading or writing the data.</span></span>



| <span data-ttu-id="17281-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="17281-119">Order</span></span> | <span data-ttu-id="17281-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="17281-120">Path</span></span>                           | <span data-ttu-id="17281-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="17281-121">Disk Format</span></span> | <span data-ttu-id="17281-122">Formato de Dados</span><span class="sxs-lookup"><span data-stu-id="17281-122">Data Format</span></span> | <span data-ttu-id="17281-123">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="17281-123">Required</span></span> |
|-------|--------------------------------|-------------|-------------|----------|
| <span data-ttu-id="17281-124">1</span><span class="sxs-lookup"><span data-stu-id="17281-124">1</span></span>     | <span data-ttu-id="17281-125">/xmp/MicrosoftPhoto:FlashModel</span><span class="sxs-lookup"><span data-stu-id="17281-125">/xmp/MicrosoftPhoto:FlashModel</span></span> | <span data-ttu-id="17281-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="17281-126">Unicode</span></span>     |             | <span data-ttu-id="17281-127">Yes</span><span class="sxs-lookup"><span data-stu-id="17281-127">Yes</span></span>      |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="17281-128">Precedência de caminhos (TIFF)</span><span class="sxs-lookup"><span data-stu-id="17281-128">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="17281-129">Se o arquivo estiver no formato TIFF, o manipulador usará a ordem de precedência a seguir ao ler ou gravar os dados.</span><span class="sxs-lookup"><span data-stu-id="17281-129">If the file is in TIFF format, the handler will use the following order of precedence when reading or writing the data.</span></span>



| <span data-ttu-id="17281-130">Ordem</span><span class="sxs-lookup"><span data-stu-id="17281-130">Order</span></span> | <span data-ttu-id="17281-131">Caminho</span><span class="sxs-lookup"><span data-stu-id="17281-131">Path</span></span>                               | <span data-ttu-id="17281-132">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="17281-132">Disk Format</span></span> | <span data-ttu-id="17281-133">Formato de Dados</span><span class="sxs-lookup"><span data-stu-id="17281-133">Data Format</span></span> | <span data-ttu-id="17281-134">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="17281-134">Required</span></span> |
|-------|------------------------------------|-------------|-------------|----------|
| <span data-ttu-id="17281-135">1</span><span class="sxs-lookup"><span data-stu-id="17281-135">1</span></span>     | <span data-ttu-id="17281-136">/ifd/xmp/MicrosoftPhoto:FlashModel</span><span class="sxs-lookup"><span data-stu-id="17281-136">/ifd/xmp/MicrosoftPhoto:FlashModel</span></span> | <span data-ttu-id="17281-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="17281-137">Unicode</span></span>     |             | <span data-ttu-id="17281-138">Yes</span><span class="sxs-lookup"><span data-stu-id="17281-138">Yes</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="17281-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="17281-139">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="17281-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="17281-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17281-141">System. Photo. FlashModel</span><span class="sxs-lookup"><span data-stu-id="17281-141">System.Photo.FlashModel</span></span>](../properties/props-system-photo-flashmodel.md)
</dt> </dl>

 

 
