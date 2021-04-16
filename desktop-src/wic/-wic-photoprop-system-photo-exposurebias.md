---
description: A política de metadados de foto para a propriedade System. Photo. ExposureBias.
ms.assetid: 00ebe037-0116-4d75-868b-d75b3e58a84d
title: Política de metadados de foto System. Photo. ExposureBias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709aa21da7cec56d36b5de643681a592873717bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105787012"
---
# <a name="systemphotoexposurebias-photo-metadata-policy"></a><span data-ttu-id="933c5-103">Política de metadados de foto System. Photo. ExposureBias</span><span class="sxs-lookup"><span data-stu-id="933c5-103">System.Photo.ExposureBias Photo Metadata Policy</span></span>

<span data-ttu-id="933c5-104">A política de metadados de foto para a propriedade [System. Photo. ExposureBias](../properties/props-system-photo-exposurebias.md) .</span><span class="sxs-lookup"><span data-stu-id="933c5-104">The photo metadata policy for the [System.Photo.ExposureBias](../properties/props-system-photo-exposurebias.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="933c5-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="933c5-105">PKEY</span></span>

<span data-ttu-id="933c5-106">PKEY \_ Photo \_ ExposureBias</span><span class="sxs-lookup"><span data-stu-id="933c5-106">PKEY\_Photo\_ExposureBias</span></span>

### <a name="containers"></a><span data-ttu-id="933c5-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="933c5-107">Containers</span></span>

<span data-ttu-id="933c5-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="933c5-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="933c5-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="933c5-109">Read-Only</span></span>

<span data-ttu-id="933c5-110">Yes</span><span class="sxs-lookup"><span data-stu-id="933c5-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="933c5-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="933c5-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="933c5-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="933c5-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="933c5-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="933c5-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="933c5-114">Esse valor é gerado em System. Photo. ExposureBiasNumerator e System. Photo. ExposureBiasDenominator.</span><span class="sxs-lookup"><span data-stu-id="933c5-114">This value is generated from System.Photo.ExposureBiasNumerator and System.Photo.ExposureBiasDenominator.</span></span> <span data-ttu-id="933c5-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="933c5-115">It cannot be written directly.</span></span> <span data-ttu-id="933c5-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="933c5-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="933c5-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="933c5-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="933c5-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="933c5-118">Read Paths</span></span>



| <span data-ttu-id="933c5-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="933c5-119">Order</span></span> | <span data-ttu-id="933c5-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="933c5-120">Path</span></span>                          | <span data-ttu-id="933c5-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="933c5-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="933c5-122">1</span><span class="sxs-lookup"><span data-stu-id="933c5-122">1</span></span>     | <span data-ttu-id="933c5-123">/App1/IFD/EXIF/{UShort = 37380}</span><span class="sxs-lookup"><span data-stu-id="933c5-123">/app1/ifd/exif/{ushort=37380}</span></span> |             |
| <span data-ttu-id="933c5-124">2</span><span class="sxs-lookup"><span data-stu-id="933c5-124">2</span></span>     | <span data-ttu-id="933c5-125">/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="933c5-125">/xmp/exif:ExposureBiasValue</span></span>   |             |



 

### <a name="write-paths"></a><span data-ttu-id="933c5-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="933c5-126">Write Paths</span></span>



| <span data-ttu-id="933c5-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="933c5-127">Order</span></span> | <span data-ttu-id="933c5-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="933c5-128">Path</span></span>                          | <span data-ttu-id="933c5-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="933c5-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="933c5-130">1</span><span class="sxs-lookup"><span data-stu-id="933c5-130">1</span></span>     | <span data-ttu-id="933c5-131">/App1/IFD/EXIF/{UShort = 37380}</span><span class="sxs-lookup"><span data-stu-id="933c5-131">/app1/ifd/exif/{ushort=37380}</span></span> |             |
| <span data-ttu-id="933c5-132">2</span><span class="sxs-lookup"><span data-stu-id="933c5-132">2</span></span>     | <span data-ttu-id="933c5-133">/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="933c5-133">/xmp/exif:ExposureBiasValue</span></span>   |             |



 

### <a name="remove-paths"></a><span data-ttu-id="933c5-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="933c5-134">Remove Paths</span></span>



| <span data-ttu-id="933c5-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="933c5-135">Order</span></span> | <span data-ttu-id="933c5-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="933c5-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="933c5-137">1</span><span class="sxs-lookup"><span data-stu-id="933c5-137">1</span></span>     | <span data-ttu-id="933c5-138">/App1/IFD/EXIF/{UShort = 37380}</span><span class="sxs-lookup"><span data-stu-id="933c5-138">/app1/ifd/exif/{ushort=37380}</span></span> |
| <span data-ttu-id="933c5-139">2</span><span class="sxs-lookup"><span data-stu-id="933c5-139">2</span></span>     | <span data-ttu-id="933c5-140">/xmp/exif:exposurebiasvalue</span><span class="sxs-lookup"><span data-stu-id="933c5-140">/xmp/exif:exposurebiasvalue</span></span>   |



 

### <a name="tiff-policies"></a><span data-ttu-id="933c5-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="933c5-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="933c5-142">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="933c5-142">Read Paths</span></span>



| <span data-ttu-id="933c5-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="933c5-143">Order</span></span> | <span data-ttu-id="933c5-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="933c5-144">Path</span></span>                            | <span data-ttu-id="933c5-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="933c5-145">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="933c5-146">1</span><span class="sxs-lookup"><span data-stu-id="933c5-146">1</span></span>     | <span data-ttu-id="933c5-147">/IFD/EXIF/{UShort = 37380}</span><span class="sxs-lookup"><span data-stu-id="933c5-147">/ifd/exif/{ushort=37380}</span></span>        |             |
| <span data-ttu-id="933c5-148">2</span><span class="sxs-lookup"><span data-stu-id="933c5-148">2</span></span>     | <span data-ttu-id="933c5-149">/ifd/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="933c5-149">/ifd/xmp/exif:ExposureBiasValue</span></span> |             |



 

### <a name="write-paths"></a><span data-ttu-id="933c5-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="933c5-150">Write Paths</span></span>



| <span data-ttu-id="933c5-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="933c5-151">Order</span></span> | <span data-ttu-id="933c5-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="933c5-152">Path</span></span>                            | <span data-ttu-id="933c5-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="933c5-153">Disk Format</span></span> |
|-------|---------------------------------|-------------|
| <span data-ttu-id="933c5-154">1</span><span class="sxs-lookup"><span data-stu-id="933c5-154">1</span></span>     | <span data-ttu-id="933c5-155">/IFD/EXIF/{UShort = 37380}</span><span class="sxs-lookup"><span data-stu-id="933c5-155">/ifd/exif/{ushort=37380}</span></span>        |             |
| <span data-ttu-id="933c5-156">2</span><span class="sxs-lookup"><span data-stu-id="933c5-156">2</span></span>     | <span data-ttu-id="933c5-157">/ifd/xmp/exif:ExposureBiasValue</span><span class="sxs-lookup"><span data-stu-id="933c5-157">/ifd/xmp/exif:ExposureBiasValue</span></span> |             |



 

### <a name="remove-paths"></a><span data-ttu-id="933c5-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="933c5-158">Remove Paths</span></span>



| <span data-ttu-id="933c5-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="933c5-159">Order</span></span> | <span data-ttu-id="933c5-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="933c5-160">Path</span></span>                            |
|-------|---------------------------------|
| <span data-ttu-id="933c5-161">1</span><span class="sxs-lookup"><span data-stu-id="933c5-161">1</span></span>     | <span data-ttu-id="933c5-162">/IFD/EXIF/{UShort = 37380}</span><span class="sxs-lookup"><span data-stu-id="933c5-162">/ifd/exif/{ushort=37380}</span></span>        |
| <span data-ttu-id="933c5-163">2</span><span class="sxs-lookup"><span data-stu-id="933c5-163">2</span></span>     | <span data-ttu-id="933c5-164">/ifd/xmp/exif:exposurebiasvalue</span><span class="sxs-lookup"><span data-stu-id="933c5-164">/ifd/xmp/exif:exposurebiasvalue</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="933c5-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="933c5-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="933c5-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="933c5-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="933c5-167">System. Photo. ExposureBias</span><span class="sxs-lookup"><span data-stu-id="933c5-167">System.Photo.ExposureBias</span></span>](../properties/props-system-photo-exposurebias.md)
</dt> </dl>

 

 
