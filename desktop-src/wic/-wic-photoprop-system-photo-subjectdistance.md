---
description: A política de metadados de foto para a propriedade System. Photo. SubjectDistance.
ms.assetid: 8d5acd7e-7227-4a79-890a-43e6dace3864
title: Política de metadados de foto System. Photo. SubjectDistance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3335b17f45cce7dc60881dc7ea8d9ffecc711016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829494"
---
# <a name="systemphotosubjectdistance-photo-metadata-policy"></a><span data-ttu-id="73f0e-103">Política de metadados de foto System. Photo. SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="73f0e-103">System.Photo.SubjectDistance Photo Metadata Policy</span></span>

<span data-ttu-id="73f0e-104">A política de metadados de foto para a propriedade [System. Photo. SubjectDistance](../properties/props-system-photo-subjectdistance.md) .</span><span class="sxs-lookup"><span data-stu-id="73f0e-104">The photo metadata policy for the [System.Photo.SubjectDistance](../properties/props-system-photo-subjectdistance.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="73f0e-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="73f0e-105">PKEY</span></span>

<span data-ttu-id="73f0e-106">PKEY \_ Photo \_ SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="73f0e-106">PKEY\_Photo\_SubjectDistance</span></span>

### <a name="containers"></a><span data-ttu-id="73f0e-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="73f0e-107">Containers</span></span>

<span data-ttu-id="73f0e-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="73f0e-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="73f0e-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73f0e-109">Read-Only</span></span>

<span data-ttu-id="73f0e-110">Sim</span><span class="sxs-lookup"><span data-stu-id="73f0e-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="73f0e-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="73f0e-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="73f0e-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="73f0e-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="73f0e-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="73f0e-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="73f0e-114">Esse valor é gerado em System. Photo. SubjectDistanceNumerator e System. Photo. SubjectDistanceDenominator.</span><span class="sxs-lookup"><span data-stu-id="73f0e-114">This value is generated from System.Photo.SubjectDistanceNumerator and System.Photo.SubjectDistanceDenominator.</span></span> <span data-ttu-id="73f0e-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="73f0e-115">It cannot be written directly.</span></span> <span data-ttu-id="73f0e-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="73f0e-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="73f0e-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="73f0e-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="73f0e-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="73f0e-118">Read Paths</span></span>



| <span data-ttu-id="73f0e-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="73f0e-119">Order</span></span> | <span data-ttu-id="73f0e-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="73f0e-120">Path</span></span>                          | <span data-ttu-id="73f0e-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="73f0e-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="73f0e-122">1</span><span class="sxs-lookup"><span data-stu-id="73f0e-122">1</span></span>     | <span data-ttu-id="73f0e-123">/App1/IFD/EXIF/{UShort = 37382}</span><span class="sxs-lookup"><span data-stu-id="73f0e-123">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="73f0e-124">2</span><span class="sxs-lookup"><span data-stu-id="73f0e-124">2</span></span>     | <span data-ttu-id="73f0e-125">/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="73f0e-125">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="write-paths"></a><span data-ttu-id="73f0e-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="73f0e-126">Write Paths</span></span>



| <span data-ttu-id="73f0e-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="73f0e-127">Order</span></span> | <span data-ttu-id="73f0e-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="73f0e-128">Path</span></span>                          | <span data-ttu-id="73f0e-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="73f0e-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="73f0e-130">1</span><span class="sxs-lookup"><span data-stu-id="73f0e-130">1</span></span>     | <span data-ttu-id="73f0e-131">/App1/IFD/EXIF/{UShort = 37382}</span><span class="sxs-lookup"><span data-stu-id="73f0e-131">/app1/ifd/exif/{ushort=37382}</span></span> |             |
| <span data-ttu-id="73f0e-132">2</span><span class="sxs-lookup"><span data-stu-id="73f0e-132">2</span></span>     | <span data-ttu-id="73f0e-133">/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="73f0e-133">/xmp/exif:SubjectDistance</span></span>     |             |



 

### <a name="remove-paths"></a><span data-ttu-id="73f0e-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="73f0e-134">Remove Paths</span></span>



| <span data-ttu-id="73f0e-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="73f0e-135">Order</span></span> | <span data-ttu-id="73f0e-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="73f0e-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="73f0e-137">1</span><span class="sxs-lookup"><span data-stu-id="73f0e-137">1</span></span>     | <span data-ttu-id="73f0e-138">/App1/IFD/EXIF/{UShort = 37382}</span><span class="sxs-lookup"><span data-stu-id="73f0e-138">/app1/ifd/exif/{ushort=37382}</span></span> |
| <span data-ttu-id="73f0e-139">2</span><span class="sxs-lookup"><span data-stu-id="73f0e-139">2</span></span>     | <span data-ttu-id="73f0e-140">/xmp/exif:subjectdistance</span><span class="sxs-lookup"><span data-stu-id="73f0e-140">/xmp/exif:subjectdistance</span></span>     |



 

### <a name="tiff-policies"></a><span data-ttu-id="73f0e-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="73f0e-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="73f0e-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="73f0e-142">Read Paths</span></span>



| <span data-ttu-id="73f0e-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="73f0e-143">Order</span></span> | <span data-ttu-id="73f0e-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="73f0e-144">Path</span></span>                          | <span data-ttu-id="73f0e-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="73f0e-145">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="73f0e-146">1</span><span class="sxs-lookup"><span data-stu-id="73f0e-146">1</span></span>     | <span data-ttu-id="73f0e-147">/IFD/EXIF/{UShort = 37382}</span><span class="sxs-lookup"><span data-stu-id="73f0e-147">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="73f0e-148">2</span><span class="sxs-lookup"><span data-stu-id="73f0e-148">2</span></span>     | <span data-ttu-id="73f0e-149">/ifd/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="73f0e-149">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="73f0e-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="73f0e-150">Write Paths</span></span>



| <span data-ttu-id="73f0e-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="73f0e-151">Order</span></span> | <span data-ttu-id="73f0e-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="73f0e-152">Path</span></span>                          | <span data-ttu-id="73f0e-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="73f0e-153">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="73f0e-154">1</span><span class="sxs-lookup"><span data-stu-id="73f0e-154">1</span></span>     | <span data-ttu-id="73f0e-155">/IFD/EXIF/{UShort = 37382}</span><span class="sxs-lookup"><span data-stu-id="73f0e-155">/ifd/exif/{ushort=37382}</span></span>      |             |
| <span data-ttu-id="73f0e-156">2</span><span class="sxs-lookup"><span data-stu-id="73f0e-156">2</span></span>     | <span data-ttu-id="73f0e-157">/ifd/xmp/exif:SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="73f0e-157">/ifd/xmp/exif:SubjectDistance</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="73f0e-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="73f0e-158">Remove Paths</span></span>



| <span data-ttu-id="73f0e-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="73f0e-159">Order</span></span> | <span data-ttu-id="73f0e-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="73f0e-160">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="73f0e-161">1</span><span class="sxs-lookup"><span data-stu-id="73f0e-161">1</span></span>     | <span data-ttu-id="73f0e-162">/IFD/EXIF/{UShort = 37382}</span><span class="sxs-lookup"><span data-stu-id="73f0e-162">/ifd/exif/{ushort=37382}</span></span>      |
| <span data-ttu-id="73f0e-163">2</span><span class="sxs-lookup"><span data-stu-id="73f0e-163">2</span></span>     | <span data-ttu-id="73f0e-164">/ifd/xmp/exif:subjectdistance</span><span class="sxs-lookup"><span data-stu-id="73f0e-164">/ifd/xmp/exif:subjectdistance</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="73f0e-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="73f0e-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="73f0e-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73f0e-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73f0e-167">System. Photo. SubjectDistance</span><span class="sxs-lookup"><span data-stu-id="73f0e-167">System.Photo.SubjectDistance</span></span>](../properties/props-system-photo-subjectdistance.md)
</dt> </dl>

 

 
