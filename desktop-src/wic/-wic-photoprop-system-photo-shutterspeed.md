---
description: A política de metadados de foto para a propriedade System. Photo. ShutterSpeed.
ms.assetid: f320944c-978d-4a3c-9bf8-5c5652123e29
title: Política de metadados de foto System. Photo. ShutterSpeed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8df8c9e7fda5643fed022f67c3b6b7846e7a72f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759515"
---
# <a name="systemphotoshutterspeed-photo-metadata-policy"></a><span data-ttu-id="a4f76-103">Política de metadados de foto System. Photo. ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="a4f76-103">System.Photo.ShutterSpeed Photo Metadata Policy</span></span>

<span data-ttu-id="a4f76-104">A política de metadados de foto para a propriedade [System. Photo. ShutterSpeed](../properties/props-system-photo-shutterspeed.md) .</span><span class="sxs-lookup"><span data-stu-id="a4f76-104">The photo metadata policy for the [System.Photo.ShutterSpeed](../properties/props-system-photo-shutterspeed.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a4f76-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a4f76-105">PKEY</span></span>

<span data-ttu-id="a4f76-106">PKEY \_ Photo \_ ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="a4f76-106">PKEY\_Photo\_ShutterSpeed</span></span>

### <a name="containers"></a><span data-ttu-id="a4f76-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="a4f76-107">Containers</span></span>

<span data-ttu-id="a4f76-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a4f76-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a4f76-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a4f76-109">Read-Only</span></span>

<span data-ttu-id="a4f76-110">Yes</span><span class="sxs-lookup"><span data-stu-id="a4f76-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a4f76-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="a4f76-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a4f76-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="a4f76-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a4f76-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="a4f76-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="a4f76-114">Esse valor é gerado em System. Photo. ShutterSpeedNumerator e System. Photo. ShutterSpeedDenominator.</span><span class="sxs-lookup"><span data-stu-id="a4f76-114">This value is generated from System.Photo.ShutterSpeedNumerator and System.Photo.ShutterSpeedDenominator.</span></span> <span data-ttu-id="a4f76-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="a4f76-115">It cannot be written directly.</span></span> <span data-ttu-id="a4f76-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="a4f76-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="a4f76-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="a4f76-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="a4f76-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="a4f76-118">Read Paths</span></span>



| <span data-ttu-id="a4f76-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4f76-119">Order</span></span> | <span data-ttu-id="a4f76-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4f76-120">Path</span></span>                          | <span data-ttu-id="a4f76-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4f76-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a4f76-122">1</span><span class="sxs-lookup"><span data-stu-id="a4f76-122">1</span></span>     | <span data-ttu-id="a4f76-123">/App1/IFD/EXIF/{UShort = 37377}</span><span class="sxs-lookup"><span data-stu-id="a4f76-123">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="a4f76-124">2</span><span class="sxs-lookup"><span data-stu-id="a4f76-124">2</span></span>     | <span data-ttu-id="a4f76-125">/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="a4f76-125">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="a4f76-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="a4f76-126">Write Paths</span></span>



| <span data-ttu-id="a4f76-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4f76-127">Order</span></span> | <span data-ttu-id="a4f76-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4f76-128">Path</span></span>                          | <span data-ttu-id="a4f76-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4f76-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="a4f76-130">1</span><span class="sxs-lookup"><span data-stu-id="a4f76-130">1</span></span>     | <span data-ttu-id="a4f76-131">/App1/IFD/EXIF/{UShort = 37377}</span><span class="sxs-lookup"><span data-stu-id="a4f76-131">/app1/ifd/exif/{ushort=37377}</span></span> |             |
| <span data-ttu-id="a4f76-132">2</span><span class="sxs-lookup"><span data-stu-id="a4f76-132">2</span></span>     | <span data-ttu-id="a4f76-133">/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="a4f76-133">/xmp/exif:ShutterSpeedValue</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a4f76-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="a4f76-134">Remove Paths</span></span>



| <span data-ttu-id="a4f76-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4f76-135">Order</span></span> | <span data-ttu-id="a4f76-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4f76-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="a4f76-137">1</span><span class="sxs-lookup"><span data-stu-id="a4f76-137">1</span></span>     | <span data-ttu-id="a4f76-138">/App1/IFD/EXIF/{UShort = 37377}</span><span class="sxs-lookup"><span data-stu-id="a4f76-138">/app1/ifd/exif/{ushort=37377}</span></span> |
| <span data-ttu-id="a4f76-139">2</span><span class="sxs-lookup"><span data-stu-id="a4f76-139">2</span></span>     | <span data-ttu-id="a4f76-140">/xmp/exif:shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="a4f76-140">/xmp/exif:shutterspeedvalue</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="a4f76-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="a4f76-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a4f76-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="a4f76-142">Read Paths</span></span>



| <span data-ttu-id="a4f76-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4f76-143">Order</span></span> | <span data-ttu-id="a4f76-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4f76-144">Path</span></span>                            | <span data-ttu-id="a4f76-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4f76-145">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="a4f76-146">1</span><span class="sxs-lookup"><span data-stu-id="a4f76-146">1</span></span>     | <span data-ttu-id="a4f76-147">/IFD/EXIF/{UShort = 37377}</span><span class="sxs-lookup"><span data-stu-id="a4f76-147">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="a4f76-148">2</span><span class="sxs-lookup"><span data-stu-id="a4f76-148">2</span></span>     | <span data-ttu-id="a4f76-149">/ifd/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="a4f76-149">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="a4f76-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="a4f76-150">Write Paths</span></span>



| <span data-ttu-id="a4f76-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4f76-151">Order</span></span> | <span data-ttu-id="a4f76-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4f76-152">Path</span></span>                            | <span data-ttu-id="a4f76-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a4f76-153">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="a4f76-154">1</span><span class="sxs-lookup"><span data-stu-id="a4f76-154">1</span></span>     | <span data-ttu-id="a4f76-155">/IFD/EXIF/{UShort = 37377}</span><span class="sxs-lookup"><span data-stu-id="a4f76-155">/ifd/exif/{ushort=37377}</span></span>        |             |
| <span data-ttu-id="a4f76-156">2</span><span class="sxs-lookup"><span data-stu-id="a4f76-156">2</span></span>     | <span data-ttu-id="a4f76-157">/ifd/xmp/exif:ShutterSpeedValue</span><span class="sxs-lookup"><span data-stu-id="a4f76-157">/ifd/xmp/exif:ShutterSpeedValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="a4f76-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="a4f76-158">Remove Paths</span></span>



| <span data-ttu-id="a4f76-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="a4f76-159">Order</span></span> | <span data-ttu-id="a4f76-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="a4f76-160">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="a4f76-161">1</span><span class="sxs-lookup"><span data-stu-id="a4f76-161">1</span></span>     | <span data-ttu-id="a4f76-162">/IFD/EXIF/{UShort = 37377}</span><span class="sxs-lookup"><span data-stu-id="a4f76-162">/ifd/exif/{ushort=37377}</span></span>        |
| <span data-ttu-id="a4f76-163">2</span><span class="sxs-lookup"><span data-stu-id="a4f76-163">2</span></span>     | <span data-ttu-id="a4f76-164">/ifd/xmp/exif:shutterspeedvalue</span><span class="sxs-lookup"><span data-stu-id="a4f76-164">/ifd/xmp/exif:shutterspeedvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a4f76-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4f76-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4f76-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4f76-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4f76-167">System. Photo. ShutterSpeed</span><span class="sxs-lookup"><span data-stu-id="a4f76-167">System.Photo.ShutterSpeed</span></span>](../properties/props-system-photo-shutterspeed.md)
</dt> </dl>

 

 
