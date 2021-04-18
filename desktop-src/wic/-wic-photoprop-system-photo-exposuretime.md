---
description: A política de metadados de foto para a propriedade System. Photo. Exposiçãotime.
ms.assetid: 26f6ff27-b326-46f8-b4be-b091acbec575
title: Política de metadados de foto System. Photo. Exposiçãotime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea9078befd0cbc26272ff14ae023b1b22cb4f0f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768678"
---
# <a name="systemphotoexposuretime-photo-metadata-policy"></a><span data-ttu-id="34e01-103">Política de metadados de foto System. Photo. Exposiçãotime</span><span class="sxs-lookup"><span data-stu-id="34e01-103">System.Photo.ExposureTime Photo Metadata Policy</span></span>

<span data-ttu-id="34e01-104">A política de metadados de foto para a propriedade [System. Photo. exposiçãotime](../properties/props-system-photo-exposuretime.md) .</span><span class="sxs-lookup"><span data-stu-id="34e01-104">The photo metadata policy for the [System.Photo.ExposureTime](../properties/props-system-photo-exposuretime.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="34e01-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="34e01-105">PKEY</span></span>

<span data-ttu-id="34e01-106">PKEY \_ fotos \_</span><span class="sxs-lookup"><span data-stu-id="34e01-106">PKEY\_Photo\_ExposureTime</span></span>

### <a name="containers"></a><span data-ttu-id="34e01-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="34e01-107">Containers</span></span>

<span data-ttu-id="34e01-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="34e01-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="34e01-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="34e01-109">Read-Only</span></span>

<span data-ttu-id="34e01-110">Yes</span><span class="sxs-lookup"><span data-stu-id="34e01-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="34e01-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="34e01-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="34e01-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="34e01-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="34e01-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="34e01-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="34e01-114">Esse valor é gerado em System. Photo. ExposureTimeNumerator e System. Photo. ExposureTimeDenominator.</span><span class="sxs-lookup"><span data-stu-id="34e01-114">This value is generated from System.Photo.ExposureTimeNumerator and System.Photo.ExposureTimeDenominator.</span></span> <span data-ttu-id="34e01-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="34e01-115">It cannot be written directly.</span></span> <span data-ttu-id="34e01-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="34e01-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="34e01-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="34e01-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="34e01-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="34e01-118">Read Paths</span></span>



| <span data-ttu-id="34e01-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="34e01-119">Order</span></span> | <span data-ttu-id="34e01-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="34e01-120">Path</span></span>                          | <span data-ttu-id="34e01-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="34e01-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="34e01-122">1</span><span class="sxs-lookup"><span data-stu-id="34e01-122">1</span></span>     | <span data-ttu-id="34e01-123">/App1/IFD/EXIF/{UShort = 33434}</span><span class="sxs-lookup"><span data-stu-id="34e01-123">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="34e01-124">2</span><span class="sxs-lookup"><span data-stu-id="34e01-124">2</span></span>     | <span data-ttu-id="34e01-125">/XMP/EXIF: Exposiçãotime</span><span class="sxs-lookup"><span data-stu-id="34e01-125">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="write-paths"></a><span data-ttu-id="34e01-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="34e01-126">Write Paths</span></span>



| <span data-ttu-id="34e01-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="34e01-127">Order</span></span> | <span data-ttu-id="34e01-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="34e01-128">Path</span></span>                          | <span data-ttu-id="34e01-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="34e01-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="34e01-130">1</span><span class="sxs-lookup"><span data-stu-id="34e01-130">1</span></span>     | <span data-ttu-id="34e01-131">/App1/IFD/EXIF/{UShort = 33434}</span><span class="sxs-lookup"><span data-stu-id="34e01-131">/app1/ifd/exif/{ushort=33434}</span></span> |             |
| <span data-ttu-id="34e01-132">2</span><span class="sxs-lookup"><span data-stu-id="34e01-132">2</span></span>     | <span data-ttu-id="34e01-133">/XMP/EXIF: Exposiçãotime</span><span class="sxs-lookup"><span data-stu-id="34e01-133">/xmp/exif:ExposureTime</span></span>        |             |



 

### <a name="remove-paths"></a><span data-ttu-id="34e01-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="34e01-134">Remove Paths</span></span>



| <span data-ttu-id="34e01-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="34e01-135">Order</span></span> | <span data-ttu-id="34e01-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="34e01-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="34e01-137">1</span><span class="sxs-lookup"><span data-stu-id="34e01-137">1</span></span>     | <span data-ttu-id="34e01-138">/App1/IFD/EXIF/{UShort = 33434}</span><span class="sxs-lookup"><span data-stu-id="34e01-138">/app1/ifd/exif/{ushort=33434}</span></span> |
| <span data-ttu-id="34e01-139">2</span><span class="sxs-lookup"><span data-stu-id="34e01-139">2</span></span>     | <span data-ttu-id="34e01-140">/XMP/EXIF: exposiçãotime</span><span class="sxs-lookup"><span data-stu-id="34e01-140">/xmp/exif:exposuretime</span></span>        |



 

### <a name="tiff-policies"></a><span data-ttu-id="34e01-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="34e01-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="34e01-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="34e01-142">Read Paths</span></span>



| <span data-ttu-id="34e01-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="34e01-143">Order</span></span> | <span data-ttu-id="34e01-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="34e01-144">Path</span></span>                       | <span data-ttu-id="34e01-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="34e01-145">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="34e01-146">1</span><span class="sxs-lookup"><span data-stu-id="34e01-146">1</span></span>     | <span data-ttu-id="34e01-147">/IFD/EXIF/{UShort = 33434}</span><span class="sxs-lookup"><span data-stu-id="34e01-147">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="34e01-148">2</span><span class="sxs-lookup"><span data-stu-id="34e01-148">2</span></span>     | <span data-ttu-id="34e01-149">/IFD/XMP/EXIF: Exposiçãotime</span><span class="sxs-lookup"><span data-stu-id="34e01-149">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="34e01-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="34e01-150">Write Paths</span></span>



| <span data-ttu-id="34e01-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="34e01-151">Order</span></span> | <span data-ttu-id="34e01-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="34e01-152">Path</span></span>                       | <span data-ttu-id="34e01-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="34e01-153">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="34e01-154">1</span><span class="sxs-lookup"><span data-stu-id="34e01-154">1</span></span>     | <span data-ttu-id="34e01-155">/IFD/EXIF/{UShort = 33434}</span><span class="sxs-lookup"><span data-stu-id="34e01-155">/ifd/exif/{ushort=33434}</span></span>   |             |
| <span data-ttu-id="34e01-156">2</span><span class="sxs-lookup"><span data-stu-id="34e01-156">2</span></span>     | <span data-ttu-id="34e01-157">/IFD/XMP/EXIF: Exposiçãotime</span><span class="sxs-lookup"><span data-stu-id="34e01-157">/ifd/xmp/exif:ExposureTime</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="34e01-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="34e01-158">Remove Paths</span></span>



| <span data-ttu-id="34e01-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="34e01-159">Order</span></span> | <span data-ttu-id="34e01-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="34e01-160">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="34e01-161">1</span><span class="sxs-lookup"><span data-stu-id="34e01-161">1</span></span>     | <span data-ttu-id="34e01-162">/IFD/EXIF/{UShort = 33434}</span><span class="sxs-lookup"><span data-stu-id="34e01-162">/ifd/exif/{ushort=33434}</span></span>   |
| <span data-ttu-id="34e01-163">2</span><span class="sxs-lookup"><span data-stu-id="34e01-163">2</span></span>     | <span data-ttu-id="34e01-164">/IFD/XMP/EXIF: exposiçãotime</span><span class="sxs-lookup"><span data-stu-id="34e01-164">/ifd/xmp/exif:exposuretime</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="34e01-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="34e01-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="34e01-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34e01-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34e01-167">Sistema. Photo. Exposiçãotime</span><span class="sxs-lookup"><span data-stu-id="34e01-167">System.Photo.ExposureTime</span></span>](../properties/props-system-photo-exposuretime.md)
</dt> </dl>

 

 
