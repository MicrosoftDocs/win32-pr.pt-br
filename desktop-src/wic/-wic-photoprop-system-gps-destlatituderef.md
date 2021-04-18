---
description: A política de metadados de foto para a propriedade System. GPS. DestLatitudeRef.
ms.assetid: 8a13642a-0d29-4193-9784-f716bc428c72
title: Política de metadados de foto System. GPS. DestLatitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838e4688f0c3342091e5995885689a44fab38739
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780207"
---
# <a name="systemgpsdestlatituderef-photo-metadata-policy"></a><span data-ttu-id="c0c7c-103">Política de metadados de foto System. GPS. DestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0c7c-103">System.GPS.DestLatitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="c0c7c-104">A política de metadados de foto para a propriedade [System. GPS. DestLatitudeRef](../properties/props-system-gps-destlatituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="c0c7c-104">The photo metadata policy for the [System.GPS.DestLatitudeRef](../properties/props-system-gps-destlatituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="c0c7c-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="c0c7c-105">PKEY</span></span>

<span data-ttu-id="c0c7c-106">PKEY \_ GPS \_ DestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0c7c-106">PKEY\_GPS\_DestLatitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="c0c7c-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="c0c7c-107">Containers</span></span>

<span data-ttu-id="c0c7c-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="c0c7c-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="c0c7c-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c0c7c-109">Read-Only</span></span>

<span data-ttu-id="c0c7c-110">No</span><span class="sxs-lookup"><span data-stu-id="c0c7c-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="c0c7c-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="c0c7c-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="c0c7c-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="c0c7c-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="c0c7c-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="c0c7c-113">Input Type</span></span>

<span data-ttu-id="c0c7c-114">VT \_ LPWSTR é preferencial, mas VT \_ LPSTR é aceito.</span><span class="sxs-lookup"><span data-stu-id="c0c7c-114">VT\_LPWSTR is preferred, but VT\_LPSTR is accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="c0c7c-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="c0c7c-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="c0c7c-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="c0c7c-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="c0c7c-117">Precedência de caminhos (JPEG)</span><span class="sxs-lookup"><span data-stu-id="c0c7c-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="c0c7c-118">Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="c0c7c-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="c0c7c-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="c0c7c-119">Order</span></span> | <span data-ttu-id="c0c7c-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="c0c7c-120">Path</span></span>                          | <span data-ttu-id="c0c7c-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c0c7c-121">Disk Format</span></span> | <span data-ttu-id="c0c7c-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c0c7c-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="c0c7c-123">1</span><span class="sxs-lookup"><span data-stu-id="c0c7c-123">1</span></span>     | <span data-ttu-id="c0c7c-124">/xmp/exif:GPSDestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0c7c-124">/xmp/exif:GPSDestLatitudeRef</span></span>  | <span data-ttu-id="c0c7c-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="c0c7c-125">Unicode</span></span>     | <span data-ttu-id="c0c7c-126">Yes</span><span class="sxs-lookup"><span data-stu-id="c0c7c-126">Yes</span></span>      |
| <span data-ttu-id="c0c7c-127">2</span><span class="sxs-lookup"><span data-stu-id="c0c7c-127">2</span></span>     | <span data-ttu-id="c0c7c-128">/App1/IFD/GPS/ \\ {UShort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="c0c7c-128">/app1/ifd/gps/\\{ushort=19\\}</span></span> | <span data-ttu-id="c0c7c-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="c0c7c-129">ASCII</span></span>       | <span data-ttu-id="c0c7c-130">No</span><span class="sxs-lookup"><span data-stu-id="c0c7c-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="c0c7c-131">Precedência de caminhos (TIFF)</span><span class="sxs-lookup"><span data-stu-id="c0c7c-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="c0c7c-132">Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="c0c7c-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="c0c7c-133">Ordem</span><span class="sxs-lookup"><span data-stu-id="c0c7c-133">Order</span></span> | <span data-ttu-id="c0c7c-134">Caminho</span><span class="sxs-lookup"><span data-stu-id="c0c7c-134">Path</span></span>                             | <span data-ttu-id="c0c7c-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="c0c7c-135">Disk Format</span></span> | <span data-ttu-id="c0c7c-136">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c0c7c-136">Required</span></span> |
|-------|----------------------------------|-------------|----------|
| <span data-ttu-id="c0c7c-137">1</span><span class="sxs-lookup"><span data-stu-id="c0c7c-137">1</span></span>     | <span data-ttu-id="c0c7c-138">/ifd/xmp/exif:GPSDestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0c7c-138">/ifd/xmp/exif:GPSDestLatitudeRef</span></span> | <span data-ttu-id="c0c7c-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="c0c7c-139">Unicode</span></span>     | <span data-ttu-id="c0c7c-140">Yes</span><span class="sxs-lookup"><span data-stu-id="c0c7c-140">Yes</span></span>      |
| <span data-ttu-id="c0c7c-141">2</span><span class="sxs-lookup"><span data-stu-id="c0c7c-141">2</span></span>     | <span data-ttu-id="c0c7c-142">/IFD/GPS/ \\ {UShort = 19 \\ }</span><span class="sxs-lookup"><span data-stu-id="c0c7c-142">/ifd/gps/\\{ushort=19\\}</span></span>         | <span data-ttu-id="c0c7c-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="c0c7c-143">ASCII</span></span>       | <span data-ttu-id="c0c7c-144">Não</span><span class="sxs-lookup"><span data-stu-id="c0c7c-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="c0c7c-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0c7c-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0c7c-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0c7c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0c7c-147">System. GPS. DestLatitudeRef</span><span class="sxs-lookup"><span data-stu-id="c0c7c-147">System.GPS.DestLatitudeRef</span></span>](../properties/props-system-gps-destlatituderef.md)
</dt> </dl>

 

 
