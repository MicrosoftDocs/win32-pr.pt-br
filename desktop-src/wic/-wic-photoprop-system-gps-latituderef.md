---
description: A política de metadados de foto para a propriedade System. GPS. LatitudeRef.
ms.assetid: 057015fd-38b7-4053-b611-72565975cc58
title: Política de metadados de foto System. GPS. LatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 782fbcecbed90c9c75c1ae5fe9d5409496f842a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171006"
---
# <a name="systemgpslatituderef-photo-metadata-policy"></a><span data-ttu-id="f21b5-103">Política de metadados de foto System. GPS. LatitudeRef</span><span class="sxs-lookup"><span data-stu-id="f21b5-103">System.GPS.LatitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="f21b5-104">A política de metadados de foto para a propriedade [System. GPS. LatitudeRef](../properties/props-system-gps-latitude.md) .</span><span class="sxs-lookup"><span data-stu-id="f21b5-104">The photo metadata policy for the [System.GPS.LatitudeRef](../properties/props-system-gps-latitude.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="f21b5-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="f21b5-105">PKEY</span></span>

<span data-ttu-id="f21b5-106">PKEY \_ GPS \_ LatitudeRef</span><span class="sxs-lookup"><span data-stu-id="f21b5-106">PKEY\_GPS\_LatitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="f21b5-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="f21b5-107">Containers</span></span>

<span data-ttu-id="f21b5-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="f21b5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="f21b5-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f21b5-109">Read-Only</span></span>

<span data-ttu-id="f21b5-110">No</span><span class="sxs-lookup"><span data-stu-id="f21b5-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="f21b5-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="f21b5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="f21b5-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="f21b5-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="f21b5-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="f21b5-113">Input Type</span></span>

<span data-ttu-id="f21b5-114">VT \_ LPWSTR é preferível, mas VT \_ LPSTR também é aceito.</span><span class="sxs-lookup"><span data-stu-id="f21b5-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="f21b5-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="f21b5-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="f21b5-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="f21b5-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="f21b5-117">Precedência de caminhos (JPEG)</span><span class="sxs-lookup"><span data-stu-id="f21b5-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="f21b5-118">Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="f21b5-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="f21b5-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="f21b5-119">Order</span></span> | <span data-ttu-id="f21b5-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="f21b5-120">Path</span></span>                         | <span data-ttu-id="f21b5-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="f21b5-121">Disk Format</span></span> | <span data-ttu-id="f21b5-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f21b5-122">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="f21b5-123">1</span><span class="sxs-lookup"><span data-stu-id="f21b5-123">1</span></span>     | <span data-ttu-id="f21b5-124">/xmp/exif:GPSLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="f21b5-124">/xmp/exif:GPSLatitudeRef</span></span>     | <span data-ttu-id="f21b5-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="f21b5-125">Unicode</span></span>     | <span data-ttu-id="f21b5-126">Yes</span><span class="sxs-lookup"><span data-stu-id="f21b5-126">Yes</span></span>      |
| <span data-ttu-id="f21b5-127">2</span><span class="sxs-lookup"><span data-stu-id="f21b5-127">2</span></span>     | <span data-ttu-id="f21b5-128">/App1/IFD/GPS/ \\ {UShort = 1 \\ }</span><span class="sxs-lookup"><span data-stu-id="f21b5-128">/app1/ifd/gps/\\{ushort=1\\}</span></span> | <span data-ttu-id="f21b5-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="f21b5-129">ASCII</span></span>       | <span data-ttu-id="f21b5-130">No</span><span class="sxs-lookup"><span data-stu-id="f21b5-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="f21b5-131">Precedência de caminhos (TIFF)</span><span class="sxs-lookup"><span data-stu-id="f21b5-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="f21b5-132">Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="f21b5-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="f21b5-133">Ordem</span><span class="sxs-lookup"><span data-stu-id="f21b5-133">Order</span></span> | <span data-ttu-id="f21b5-134">Caminho</span><span class="sxs-lookup"><span data-stu-id="f21b5-134">Path</span></span>                         | <span data-ttu-id="f21b5-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="f21b5-135">Disk Format</span></span> | <span data-ttu-id="f21b5-136">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="f21b5-136">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="f21b5-137">1</span><span class="sxs-lookup"><span data-stu-id="f21b5-137">1</span></span>     | <span data-ttu-id="f21b5-138">/ifd/xmp/exif:GPSLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="f21b5-138">/ifd/xmp/exif:GPSLatitudeRef</span></span> | <span data-ttu-id="f21b5-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="f21b5-139">Unicode</span></span>     | <span data-ttu-id="f21b5-140">Yes</span><span class="sxs-lookup"><span data-stu-id="f21b5-140">Yes</span></span>      |
| <span data-ttu-id="f21b5-141">2</span><span class="sxs-lookup"><span data-stu-id="f21b5-141">2</span></span>     | <span data-ttu-id="f21b5-142">/IFD/GPS/ \\ {UShort = 1 \\ }</span><span class="sxs-lookup"><span data-stu-id="f21b5-142">/ifd/gps/\\{ushort=1\\}</span></span>      | <span data-ttu-id="f21b5-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="f21b5-143">ASCII</span></span>       | <span data-ttu-id="f21b5-144">Não</span><span class="sxs-lookup"><span data-stu-id="f21b5-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="f21b5-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="f21b5-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="f21b5-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f21b5-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f21b5-147">System. GPS. LatitudeRef</span><span class="sxs-lookup"><span data-stu-id="f21b5-147">System.GPS.LatitudeRef</span></span>](../properties/props-system-gps-latitude.md)
</dt> </dl>

 

 
