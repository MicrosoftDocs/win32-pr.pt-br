---
description: A política de metadados de foto para a propriedade System. Photo. Obturation.
ms.assetid: 3048eb9d-4ed4-4b5b-960e-9d0fd6704041
title: Política de metadados de foto System. Photo. Obturation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc02826b0602d0052f129640901ac3564a0eadb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813090"
---
# <a name="systemphotoaperture-photo-metadata-policy"></a><span data-ttu-id="6c5b8-103">Política de metadados de foto System. Photo. Obturation</span><span class="sxs-lookup"><span data-stu-id="6c5b8-103">System.Photo.Aperture Photo Metadata Policy</span></span>

<span data-ttu-id="6c5b8-104">A política de metadados de foto para a propriedade [System. Photo. Obturation](../properties/props-system-photo-aperture.md) .</span><span class="sxs-lookup"><span data-stu-id="6c5b8-104">The photo metadata policy for the [System.Photo.Aperture](../properties/props-system-photo-aperture.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6c5b8-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="6c5b8-105">PKEY</span></span>

<span data-ttu-id="6c5b8-106">\_Abertura de foto PKEY \_</span><span class="sxs-lookup"><span data-stu-id="6c5b8-106">PKEY\_Photo\_Aperture</span></span>

### <a name="containers"></a><span data-ttu-id="6c5b8-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="6c5b8-107">Containers</span></span>

<span data-ttu-id="6c5b8-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6c5b8-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6c5b8-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6c5b8-109">Read-Only</span></span>

<span data-ttu-id="6c5b8-110">Yes</span><span class="sxs-lookup"><span data-stu-id="6c5b8-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6c5b8-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="6c5b8-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6c5b8-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="6c5b8-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6c5b8-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="6c5b8-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="6c5b8-114">Esse valor é gerado em System. Photo. ApertureNumerator e System. Photo. ApertureDenominator.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-114">This value is generated from System.Photo.ApertureNumerator and System.Photo.ApertureDenominator.</span></span> <span data-ttu-id="6c5b8-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-115">It cannot be written directly.</span></span> <span data-ttu-id="6c5b8-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="6c5b8-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="6c5b8-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="6c5b8-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="6c5b8-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="6c5b8-118">Read Paths</span></span>



| <span data-ttu-id="6c5b8-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="6c5b8-119">Order</span></span> | <span data-ttu-id="6c5b8-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="6c5b8-120">Path</span></span>                          | <span data-ttu-id="6c5b8-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6c5b8-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="6c5b8-122">1</span><span class="sxs-lookup"><span data-stu-id="6c5b8-122">1</span></span>     | <span data-ttu-id="6c5b8-123">/App1/IFD/EXIF/{UShort = 37378}</span><span class="sxs-lookup"><span data-stu-id="6c5b8-123">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="6c5b8-124">2</span><span class="sxs-lookup"><span data-stu-id="6c5b8-124">2</span></span>     | <span data-ttu-id="6c5b8-125">/XMP/EXIF: Obturavalue</span><span class="sxs-lookup"><span data-stu-id="6c5b8-125">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="write-paths"></a><span data-ttu-id="6c5b8-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="6c5b8-126">Write Paths</span></span>



| <span data-ttu-id="6c5b8-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="6c5b8-127">Order</span></span> | <span data-ttu-id="6c5b8-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="6c5b8-128">Path</span></span>                          | <span data-ttu-id="6c5b8-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6c5b8-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="6c5b8-130">1</span><span class="sxs-lookup"><span data-stu-id="6c5b8-130">1</span></span>     | <span data-ttu-id="6c5b8-131">/App1/IFD/EXIF/{UShort = 37378}</span><span class="sxs-lookup"><span data-stu-id="6c5b8-131">/app1/ifd/exif/{ushort=37378}</span></span> |             |
| <span data-ttu-id="6c5b8-132">2</span><span class="sxs-lookup"><span data-stu-id="6c5b8-132">2</span></span>     | <span data-ttu-id="6c5b8-133">/XMP/EXIF: Obturavalue</span><span class="sxs-lookup"><span data-stu-id="6c5b8-133">/xmp/exif:ApertureValue</span></span>       |             |



 

### <a name="remove-paths"></a><span data-ttu-id="6c5b8-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="6c5b8-134">Remove Paths</span></span>



| <span data-ttu-id="6c5b8-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="6c5b8-135">Order</span></span> | <span data-ttu-id="6c5b8-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="6c5b8-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="6c5b8-137">1</span><span class="sxs-lookup"><span data-stu-id="6c5b8-137">1</span></span>     | <span data-ttu-id="6c5b8-138">/App1/IFD/EXIF/{UShort = 37378}</span><span class="sxs-lookup"><span data-stu-id="6c5b8-138">/app1/ifd/exif/{ushort=37378}</span></span> |
| <span data-ttu-id="6c5b8-139">2</span><span class="sxs-lookup"><span data-stu-id="6c5b8-139">2</span></span>     | <span data-ttu-id="6c5b8-140">/XMP/EXIF: obturavalue</span><span class="sxs-lookup"><span data-stu-id="6c5b8-140">/xmp/exif:aperturevalue</span></span>       |



 

### <a name="tiff-policies"></a><span data-ttu-id="6c5b8-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="6c5b8-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="6c5b8-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="6c5b8-142">Read Paths</span></span>



| <span data-ttu-id="6c5b8-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="6c5b8-143">Order</span></span> | <span data-ttu-id="6c5b8-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="6c5b8-144">Path</span></span>                        | <span data-ttu-id="6c5b8-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6c5b8-145">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="6c5b8-146">1</span><span class="sxs-lookup"><span data-stu-id="6c5b8-146">1</span></span>     | <span data-ttu-id="6c5b8-147">/IFD/EXIF/{UShort = 37378}</span><span class="sxs-lookup"><span data-stu-id="6c5b8-147">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="6c5b8-148">2</span><span class="sxs-lookup"><span data-stu-id="6c5b8-148">2</span></span>     | <span data-ttu-id="6c5b8-149">/IFD/XMP/EXIF: Obturavalue</span><span class="sxs-lookup"><span data-stu-id="6c5b8-149">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="6c5b8-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="6c5b8-150">Write Paths</span></span>



| <span data-ttu-id="6c5b8-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="6c5b8-151">Order</span></span> | <span data-ttu-id="6c5b8-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="6c5b8-152">Path</span></span>                        | <span data-ttu-id="6c5b8-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6c5b8-153">Disk Format</span></span> |
|-------|-----------------------------|-------------|
| <span data-ttu-id="6c5b8-154">1</span><span class="sxs-lookup"><span data-stu-id="6c5b8-154">1</span></span>     | <span data-ttu-id="6c5b8-155">/IFD/EXIF/{UShort = 37378}</span><span class="sxs-lookup"><span data-stu-id="6c5b8-155">/ifd/exif/{ushort=37378}</span></span>    |             |
| <span data-ttu-id="6c5b8-156">2</span><span class="sxs-lookup"><span data-stu-id="6c5b8-156">2</span></span>     | <span data-ttu-id="6c5b8-157">/IFD/XMP/EXIF: Obturavalue</span><span class="sxs-lookup"><span data-stu-id="6c5b8-157">/ifd/xmp/exif:ApertureValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="6c5b8-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="6c5b8-158">Remove Paths</span></span>



| <span data-ttu-id="6c5b8-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="6c5b8-159">Order</span></span> | <span data-ttu-id="6c5b8-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="6c5b8-160">Path</span></span>                        |
|-------|-----------------------------|
| <span data-ttu-id="6c5b8-161">1</span><span class="sxs-lookup"><span data-stu-id="6c5b8-161">1</span></span>     | <span data-ttu-id="6c5b8-162">/IFD/EXIF/{UShort = 37378}</span><span class="sxs-lookup"><span data-stu-id="6c5b8-162">/ifd/exif/{ushort=37378}</span></span>    |
| <span data-ttu-id="6c5b8-163">2</span><span class="sxs-lookup"><span data-stu-id="6c5b8-163">2</span></span>     | <span data-ttu-id="6c5b8-164">/IFD/XMP/EXIF: obturavalue</span><span class="sxs-lookup"><span data-stu-id="6c5b8-164">/ifd/xmp/exif:aperturevalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="6c5b8-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c5b8-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6c5b8-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6c5b8-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6c5b8-167">System. Photo. Obturation</span><span class="sxs-lookup"><span data-stu-id="6c5b8-167">System.Photo.Aperture</span></span>](../properties/props-system-photo-aperture.md)
</dt> </dl>

 

 
