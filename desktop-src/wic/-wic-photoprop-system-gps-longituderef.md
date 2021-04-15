---
description: A política de metadados de foto para a propriedade System. GPS. LongitudeRef.
ms.assetid: 6e7b3b87-70e5-4c6a-a9b3-959eab38f1f0
title: Política de metadados de foto System. GPS. LongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72a93d37b59ca7c77bc05e049860cf4e2608eb60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105760723"
---
# <a name="systemgpslongituderef-photo-metadata-policy"></a><span data-ttu-id="041a5-103">Política de metadados de foto System. GPS. LongitudeRef</span><span class="sxs-lookup"><span data-stu-id="041a5-103">System.GPS.LongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="041a5-104">A política de metadados de foto para a propriedade [System. GPS. LongitudeRef](../properties/props-system-gps-longituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="041a5-104">The photo metadata policy for the [System.GPS.LongitudeRef](../properties/props-system-gps-longituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="041a5-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="041a5-105">PKEY</span></span>

<span data-ttu-id="041a5-106">PKEY \_ GPS \_ LongitudeRef</span><span class="sxs-lookup"><span data-stu-id="041a5-106">PKEY\_GPS\_LongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="041a5-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="041a5-107">Containers</span></span>

<span data-ttu-id="041a5-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="041a5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="041a5-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="041a5-109">Read-Only</span></span>

<span data-ttu-id="041a5-110">No</span><span class="sxs-lookup"><span data-stu-id="041a5-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="041a5-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="041a5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="041a5-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="041a5-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="041a5-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="041a5-113">Input Type</span></span>

<span data-ttu-id="041a5-114">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="041a5-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="041a5-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="041a5-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="041a5-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="041a5-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="041a5-117">Precedência de caminhos (JPEG)</span><span class="sxs-lookup"><span data-stu-id="041a5-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="041a5-118">Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="041a5-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="041a5-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="041a5-119">Order</span></span> | <span data-ttu-id="041a5-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="041a5-120">Path</span></span>                         | <span data-ttu-id="041a5-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="041a5-121">Disk Format</span></span> | <span data-ttu-id="041a5-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="041a5-122">Required</span></span> |
|-------|------------------------------|-------------|----------|
| <span data-ttu-id="041a5-123">1</span><span class="sxs-lookup"><span data-stu-id="041a5-123">1</span></span>     | <span data-ttu-id="041a5-124">/xmp/exif:GPSLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="041a5-124">/xmp/exif:GPSLongitudeRef</span></span>    | <span data-ttu-id="041a5-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="041a5-125">Unicode</span></span>     | <span data-ttu-id="041a5-126">Yes</span><span class="sxs-lookup"><span data-stu-id="041a5-126">Yes</span></span>      |
| <span data-ttu-id="041a5-127">2</span><span class="sxs-lookup"><span data-stu-id="041a5-127">2</span></span>     | <span data-ttu-id="041a5-128">/App1/IFD/GPS/ \\ {UShort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="041a5-128">/app1/ifd/gps/\\{ushort=3\\}</span></span> | <span data-ttu-id="041a5-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="041a5-129">ASCII</span></span>       | <span data-ttu-id="041a5-130">No</span><span class="sxs-lookup"><span data-stu-id="041a5-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="041a5-131">Precedência de caminhos (TIFF)</span><span class="sxs-lookup"><span data-stu-id="041a5-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="041a5-132">Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="041a5-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="041a5-133">Ordem</span><span class="sxs-lookup"><span data-stu-id="041a5-133">Order</span></span> | <span data-ttu-id="041a5-134">Caminho</span><span class="sxs-lookup"><span data-stu-id="041a5-134">Path</span></span>                          | <span data-ttu-id="041a5-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="041a5-135">Disk Format</span></span> | <span data-ttu-id="041a5-136">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="041a5-136">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="041a5-137">1</span><span class="sxs-lookup"><span data-stu-id="041a5-137">1</span></span>     | <span data-ttu-id="041a5-138">/ifd/xmp/exif:GPSLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="041a5-138">/ifd/xmp/exif:GPSLongitudeRef</span></span> | <span data-ttu-id="041a5-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="041a5-139">Unicode</span></span>     | <span data-ttu-id="041a5-140">Yes</span><span class="sxs-lookup"><span data-stu-id="041a5-140">Yes</span></span>      |
| <span data-ttu-id="041a5-141">2</span><span class="sxs-lookup"><span data-stu-id="041a5-141">2</span></span>     | <span data-ttu-id="041a5-142">/IFD/GPS/ \\ {UShort = 3 \\ }</span><span class="sxs-lookup"><span data-stu-id="041a5-142">/ifd/gps/\\{ushort=3\\}</span></span>       | <span data-ttu-id="041a5-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="041a5-143">ASCII</span></span>       | <span data-ttu-id="041a5-144">Não</span><span class="sxs-lookup"><span data-stu-id="041a5-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="041a5-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="041a5-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="041a5-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="041a5-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="041a5-147">System. GPS. LongitudeRef</span><span class="sxs-lookup"><span data-stu-id="041a5-147">System.GPS.LongitudeRef</span></span>](../properties/props-system-gps-longituderef.md)
</dt> </dl>

 

 
