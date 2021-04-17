---
description: A política de metadados de foto para a propriedade System. Photo. FocalLength.
ms.assetid: a282c31f-00dd-4df5-9b93-300bb9bc8f2d
title: Política de metadados de foto System. Photo. FocalLength
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7b36240713782c98d52e4fbf4dae5c0c06082
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812212"
---
# <a name="systemphotofocallength-photo-metadata-policy"></a><span data-ttu-id="cea84-103">Política de metadados de foto System. Photo. FocalLength</span><span class="sxs-lookup"><span data-stu-id="cea84-103">System.Photo.FocalLength Photo Metadata Policy</span></span>

<span data-ttu-id="cea84-104">A política de metadados de foto para a propriedade [System. Photo. FocalLength](../properties/props-system-photo-focallength.md) .</span><span class="sxs-lookup"><span data-stu-id="cea84-104">The photo metadata policy for the [System.Photo.FocalLength](../properties/props-system-photo-focallength.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="cea84-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="cea84-105">PKEY</span></span>

<span data-ttu-id="cea84-106">PKEY \_ Photo \_ FocalLength</span><span class="sxs-lookup"><span data-stu-id="cea84-106">PKEY\_Photo\_FocalLength</span></span>

### <a name="containers"></a><span data-ttu-id="cea84-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="cea84-107">Containers</span></span>

<span data-ttu-id="cea84-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="cea84-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="cea84-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cea84-109">Read-Only</span></span>

<span data-ttu-id="cea84-110">Yes</span><span class="sxs-lookup"><span data-stu-id="cea84-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="cea84-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="cea84-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="cea84-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="cea84-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="cea84-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="cea84-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="cea84-114">Esse valor é gerado em System. Photo. FocalLengthNumerator e System. Photo. FocalLengthDenominator.</span><span class="sxs-lookup"><span data-stu-id="cea84-114">This value is generated from System.Photo.FocalLengthNumerator and System.Photo.FocalLengthDenominator.</span></span> <span data-ttu-id="cea84-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="cea84-115">It cannot be written directly.</span></span> <span data-ttu-id="cea84-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="cea84-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="cea84-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="cea84-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="cea84-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="cea84-118">Read Paths</span></span>



| <span data-ttu-id="cea84-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="cea84-119">Order</span></span> | <span data-ttu-id="cea84-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="cea84-120">Path</span></span>                          | <span data-ttu-id="cea84-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="cea84-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="cea84-122">1</span><span class="sxs-lookup"><span data-stu-id="cea84-122">1</span></span>     | <span data-ttu-id="cea84-123">/App1/IFD/EXIF/{UShort = 37386}</span><span class="sxs-lookup"><span data-stu-id="cea84-123">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="cea84-124">2</span><span class="sxs-lookup"><span data-stu-id="cea84-124">2</span></span>     | <span data-ttu-id="cea84-125">/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="cea84-125">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="write-paths"></a><span data-ttu-id="cea84-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="cea84-126">Write Paths</span></span>



| <span data-ttu-id="cea84-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="cea84-127">Order</span></span> | <span data-ttu-id="cea84-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="cea84-128">Path</span></span>                          | <span data-ttu-id="cea84-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="cea84-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="cea84-130">1</span><span class="sxs-lookup"><span data-stu-id="cea84-130">1</span></span>     | <span data-ttu-id="cea84-131">/App1/IFD/EXIF/{UShort = 37386}</span><span class="sxs-lookup"><span data-stu-id="cea84-131">/app1/ifd/exif/{ushort=37386}</span></span> |             |
| <span data-ttu-id="cea84-132">2</span><span class="sxs-lookup"><span data-stu-id="cea84-132">2</span></span>     | <span data-ttu-id="cea84-133">/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="cea84-133">/xmp/exif:FocalLength</span></span>         |             |



 

### <a name="remove-paths"></a><span data-ttu-id="cea84-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="cea84-134">Remove Paths</span></span>



| <span data-ttu-id="cea84-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="cea84-135">Order</span></span> | <span data-ttu-id="cea84-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="cea84-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="cea84-137">1</span><span class="sxs-lookup"><span data-stu-id="cea84-137">1</span></span>     | <span data-ttu-id="cea84-138">/App1/IFD/EXIF/{UShort = 37386}</span><span class="sxs-lookup"><span data-stu-id="cea84-138">/app1/ifd/exif/{ushort=37386}</span></span> |
| <span data-ttu-id="cea84-139">2</span><span class="sxs-lookup"><span data-stu-id="cea84-139">2</span></span>     | <span data-ttu-id="cea84-140">/xmp/exif:focallength</span><span class="sxs-lookup"><span data-stu-id="cea84-140">/xmp/exif:focallength</span></span>         |



 

### <a name="tiff-policies"></a><span data-ttu-id="cea84-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="cea84-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="cea84-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="cea84-142">Read Paths</span></span>



| <span data-ttu-id="cea84-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="cea84-143">Order</span></span> | <span data-ttu-id="cea84-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="cea84-144">Path</span></span>                      | <span data-ttu-id="cea84-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="cea84-145">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="cea84-146">1</span><span class="sxs-lookup"><span data-stu-id="cea84-146">1</span></span>     | <span data-ttu-id="cea84-147">/IFD/EXIF/{UShort = 37386}</span><span class="sxs-lookup"><span data-stu-id="cea84-147">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="cea84-148">2</span><span class="sxs-lookup"><span data-stu-id="cea84-148">2</span></span>     | <span data-ttu-id="cea84-149">/ifd/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="cea84-149">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="cea84-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="cea84-150">Write Paths</span></span>



| <span data-ttu-id="cea84-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="cea84-151">Order</span></span> | <span data-ttu-id="cea84-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="cea84-152">Path</span></span>                      | <span data-ttu-id="cea84-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="cea84-153">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="cea84-154">1</span><span class="sxs-lookup"><span data-stu-id="cea84-154">1</span></span>     | <span data-ttu-id="cea84-155">/IFD/EXIF/{UShort = 37386}</span><span class="sxs-lookup"><span data-stu-id="cea84-155">/ifd/exif/{ushort=37386}</span></span>  |             |
| <span data-ttu-id="cea84-156">2</span><span class="sxs-lookup"><span data-stu-id="cea84-156">2</span></span>     | <span data-ttu-id="cea84-157">/ifd/xmp/exif:FocalLength</span><span class="sxs-lookup"><span data-stu-id="cea84-157">/ifd/xmp/exif:FocalLength</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="cea84-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="cea84-158">Remove Paths</span></span>



| <span data-ttu-id="cea84-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="cea84-159">Order</span></span> | <span data-ttu-id="cea84-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="cea84-160">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="cea84-161">1</span><span class="sxs-lookup"><span data-stu-id="cea84-161">1</span></span>     | <span data-ttu-id="cea84-162">/IFD/EXIF/{UShort = 37386}</span><span class="sxs-lookup"><span data-stu-id="cea84-162">/ifd/exif/{ushort=37386}</span></span>  |
| <span data-ttu-id="cea84-163">2</span><span class="sxs-lookup"><span data-stu-id="cea84-163">2</span></span>     | <span data-ttu-id="cea84-164">/ifd/xmp/exif:focallength</span><span class="sxs-lookup"><span data-stu-id="cea84-164">/ifd/xmp/exif:focallength</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="cea84-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="cea84-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="cea84-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cea84-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cea84-167">System. Photo. FocalLength</span><span class="sxs-lookup"><span data-stu-id="cea84-167">System.Photo.FocalLength</span></span>](../properties/props-system-photo-focallength.md)
</dt> </dl>

 

 
