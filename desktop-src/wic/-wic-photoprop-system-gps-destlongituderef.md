---
description: A política de metadados de foto para a propriedade System. GPS. DestLongitudeRef.
ms.assetid: 2a0abb9b-41e3-49ba-a60b-3096d9c032bd
title: Política de metadados de foto System. GPS. DestLongitudeRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8139fcf5218d9863393888d7ab7b188a53e7f55f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762517"
---
# <a name="systemgpsdestlongituderef-photo-metadata-policy"></a><span data-ttu-id="9e12b-103">Política de metadados de foto System. GPS. DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="9e12b-103">System.GPS.DestLongitudeRef Photo Metadata Policy</span></span>

<span data-ttu-id="9e12b-104">A política de metadados de foto para a propriedade [System. GPS. DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) .</span><span class="sxs-lookup"><span data-stu-id="9e12b-104">The photo metadata policy for the [System.GPS.DestLongitudeRef](../properties/props-system-gps-destlongituderef.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="9e12b-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="9e12b-105">PKEY</span></span>

<span data-ttu-id="9e12b-106">PKEY \_ GPS. DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="9e12b-106">PKEY\_GPS.DestLongitudeRef</span></span>

### <a name="containers"></a><span data-ttu-id="9e12b-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="9e12b-107">Containers</span></span>

<span data-ttu-id="9e12b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="9e12b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="9e12b-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9e12b-109">Read-Only</span></span>

<span data-ttu-id="9e12b-110">No</span><span class="sxs-lookup"><span data-stu-id="9e12b-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="9e12b-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="9e12b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="9e12b-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="9e12b-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="9e12b-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="9e12b-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="9e12b-114">VT \_ LPWSTR é preferível, mas VT \_ LPSTR também é aceito.</span><span class="sxs-lookup"><span data-stu-id="9e12b-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="9e12b-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="9e12b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="9e12b-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="9e12b-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="9e12b-117">Precedência de caminhos (JPEG)</span><span class="sxs-lookup"><span data-stu-id="9e12b-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="9e12b-118">Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="9e12b-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="9e12b-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="9e12b-119">Order</span></span> | <span data-ttu-id="9e12b-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="9e12b-120">Path</span></span>                          | <span data-ttu-id="9e12b-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9e12b-121">Disk Format</span></span> | <span data-ttu-id="9e12b-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9e12b-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="9e12b-123">1</span><span class="sxs-lookup"><span data-stu-id="9e12b-123">1</span></span>     | <span data-ttu-id="9e12b-124">/xmp/exif:GPSDestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="9e12b-124">/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="9e12b-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="9e12b-125">Unicode</span></span>     | <span data-ttu-id="9e12b-126">Yes</span><span class="sxs-lookup"><span data-stu-id="9e12b-126">Yes</span></span>      |
| <span data-ttu-id="9e12b-127">2</span><span class="sxs-lookup"><span data-stu-id="9e12b-127">2</span></span>     | <span data-ttu-id="9e12b-128">/App1/IFD/GPS/ \\ {UShort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="9e12b-128">/app1/ifd/gps/\\{ushort=21\\}</span></span> | <span data-ttu-id="9e12b-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="9e12b-129">ASCII</span></span>       | <span data-ttu-id="9e12b-130">No</span><span class="sxs-lookup"><span data-stu-id="9e12b-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="9e12b-131">Precedência de caminhos (TIFF)</span><span class="sxs-lookup"><span data-stu-id="9e12b-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="9e12b-132">Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="9e12b-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="9e12b-133">Ordem</span><span class="sxs-lookup"><span data-stu-id="9e12b-133">Order</span></span> | <span data-ttu-id="9e12b-134">Caminho</span><span class="sxs-lookup"><span data-stu-id="9e12b-134">Path</span></span>                              | <span data-ttu-id="9e12b-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="9e12b-135">Disk Format</span></span> | <span data-ttu-id="9e12b-136">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="9e12b-136">Required</span></span> |
|-------|-----------------------------------|-------------|----------|
| <span data-ttu-id="9e12b-137">1</span><span class="sxs-lookup"><span data-stu-id="9e12b-137">1</span></span>     | <span data-ttu-id="9e12b-138">/ifd/xmp/exif:GPSDestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="9e12b-138">/ifd/xmp/exif:GPSDestLongitudeRef</span></span> | <span data-ttu-id="9e12b-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="9e12b-139">Unicode</span></span>     | <span data-ttu-id="9e12b-140">Yes</span><span class="sxs-lookup"><span data-stu-id="9e12b-140">Yes</span></span>      |
| <span data-ttu-id="9e12b-141">2</span><span class="sxs-lookup"><span data-stu-id="9e12b-141">2</span></span>     | <span data-ttu-id="9e12b-142">/IFD/GPS/ \\ {UShort = 21 \\ }</span><span class="sxs-lookup"><span data-stu-id="9e12b-142">/ifd/gps/\\{ushort=21\\}</span></span>          | <span data-ttu-id="9e12b-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="9e12b-143">ASCII</span></span>       | <span data-ttu-id="9e12b-144">Não</span><span class="sxs-lookup"><span data-stu-id="9e12b-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="9e12b-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e12b-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e12b-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9e12b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e12b-147">System. GPS. DestLongitudeRef</span><span class="sxs-lookup"><span data-stu-id="9e12b-147">System.GPS.DestLongitudeRef</span></span>](../properties/props-system-gps-destlongituderef.md)
</dt> </dl>

 

 
