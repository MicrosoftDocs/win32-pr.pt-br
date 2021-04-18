---
description: A política de metadados de foto para a propriedade System. Photo. FNumber.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Política de metadados de foto System. Photo. FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c518ef2a05dde8fd7e812d1d76a79cbe3efb4217
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170298"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="45e67-103">Política de metadados de foto System. Photo. FNumber</span><span class="sxs-lookup"><span data-stu-id="45e67-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="45e67-104">A política de metadados de foto para a propriedade [System. Photo. FNumber](../properties/props-system-photo-fnumber.md) .</span><span class="sxs-lookup"><span data-stu-id="45e67-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="45e67-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="45e67-105">PKEY</span></span>

<span data-ttu-id="45e67-106">PKEY \_ Photo \_ FNumber</span><span class="sxs-lookup"><span data-stu-id="45e67-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="45e67-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="45e67-107">Containers</span></span>

<span data-ttu-id="45e67-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="45e67-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="45e67-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="45e67-109">Read-Only</span></span>

<span data-ttu-id="45e67-110">Yes</span><span class="sxs-lookup"><span data-stu-id="45e67-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="45e67-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="45e67-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="45e67-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="45e67-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="45e67-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="45e67-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="45e67-114">Esse valor é gerado em System. Photo. FNumberNumerator e System. Photo. FNumberDenominator.</span><span class="sxs-lookup"><span data-stu-id="45e67-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="45e67-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="45e67-115">It cannot be written directly.</span></span> <span data-ttu-id="45e67-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="45e67-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="45e67-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="45e67-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="45e67-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="45e67-118">Read Paths</span></span>



| <span data-ttu-id="45e67-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="45e67-119">Order</span></span> | <span data-ttu-id="45e67-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="45e67-120">Path</span></span>                          | <span data-ttu-id="45e67-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="45e67-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="45e67-122">1</span><span class="sxs-lookup"><span data-stu-id="45e67-122">1</span></span>     | <span data-ttu-id="45e67-123">/App1/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="45e67-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="45e67-124">2</span><span class="sxs-lookup"><span data-stu-id="45e67-124">2</span></span>     | <span data-ttu-id="45e67-125">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="45e67-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="45e67-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="45e67-126">Write Paths</span></span>



|       |                               |             |     |
|-------|-------------------------------|-------------|-----|
| <span data-ttu-id="45e67-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="45e67-127">Order</span></span> | <span data-ttu-id="45e67-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="45e67-128">Path</span></span>                          | <span data-ttu-id="45e67-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="45e67-129">Disk Format</span></span> |     |
| <span data-ttu-id="45e67-130">1</span><span class="sxs-lookup"><span data-stu-id="45e67-130">1</span></span>     | <span data-ttu-id="45e67-131">/App1/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="45e67-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |     |
| <span data-ttu-id="45e67-132">2</span><span class="sxs-lookup"><span data-stu-id="45e67-132">2</span></span>     | <span data-ttu-id="45e67-133">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="45e67-133">/xmp/exif:FNumber</span></span>             |             |     |



 

### <a name="remove-paths"></a><span data-ttu-id="45e67-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="45e67-134">Remove Paths</span></span>



| <span data-ttu-id="45e67-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="45e67-135">Order</span></span> | <span data-ttu-id="45e67-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="45e67-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="45e67-137">1</span><span class="sxs-lookup"><span data-stu-id="45e67-137">1</span></span>     | <span data-ttu-id="45e67-138">/App1/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="45e67-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="45e67-139">2</span><span class="sxs-lookup"><span data-stu-id="45e67-139">2</span></span>     | <span data-ttu-id="45e67-140">/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="45e67-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="45e67-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="45e67-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="45e67-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="45e67-142">Read Paths</span></span>



| <span data-ttu-id="45e67-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="45e67-143">Order</span></span> | <span data-ttu-id="45e67-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="45e67-144">Path</span></span>                     | <span data-ttu-id="45e67-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="45e67-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="45e67-146">1</span><span class="sxs-lookup"><span data-stu-id="45e67-146">1</span></span>     | <span data-ttu-id="45e67-147">/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="45e67-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="45e67-148">2</span><span class="sxs-lookup"><span data-stu-id="45e67-148">2</span></span>     | <span data-ttu-id="45e67-149">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="45e67-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="45e67-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="45e67-150">Write Paths</span></span>



| <span data-ttu-id="45e67-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="45e67-151">Order</span></span> | <span data-ttu-id="45e67-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="45e67-152">Path</span></span>                     | <span data-ttu-id="45e67-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="45e67-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="45e67-154">1</span><span class="sxs-lookup"><span data-stu-id="45e67-154">1</span></span>     | <span data-ttu-id="45e67-155">/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="45e67-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="45e67-156">2</span><span class="sxs-lookup"><span data-stu-id="45e67-156">2</span></span>     | <span data-ttu-id="45e67-157">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="45e67-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="45e67-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="45e67-158">Remove Paths</span></span>



| <span data-ttu-id="45e67-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="45e67-159">Order</span></span> | <span data-ttu-id="45e67-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="45e67-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="45e67-161">1</span><span class="sxs-lookup"><span data-stu-id="45e67-161">1</span></span>     | <span data-ttu-id="45e67-162">/IFD/EXIF/{UShort = 33437}</span><span class="sxs-lookup"><span data-stu-id="45e67-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="45e67-163">2</span><span class="sxs-lookup"><span data-stu-id="45e67-163">2</span></span>     | <span data-ttu-id="45e67-164">/ifd/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="45e67-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="45e67-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="45e67-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="45e67-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="45e67-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45e67-167">System. Photo. FNumber</span><span class="sxs-lookup"><span data-stu-id="45e67-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
