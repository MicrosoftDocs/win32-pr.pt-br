---
description: A política de metadados de foto para a propriedade System.Photo.FNumber.
ms.assetid: 434d52cb-c98d-4860-87f7-4aedab7f8188
title: Política de metadados de foto System.Photo.FNumber
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85443b849d9f810709f3e75c3082738e5377092f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443617"
---
# <a name="systemphotofnumber-photo-metadata-policy"></a><span data-ttu-id="70e61-103">Política de metadados de foto System.Photo.FNumber</span><span class="sxs-lookup"><span data-stu-id="70e61-103">System.Photo.FNumber Photo Metadata Policy</span></span>

<span data-ttu-id="70e61-104">A política de metadados de foto para a [propriedade System.Photo.FNumber.](../properties/props-system-photo-fnumber.md)</span><span class="sxs-lookup"><span data-stu-id="70e61-104">The photo metadata policy for the [System.Photo.FNumber](../properties/props-system-photo-fnumber.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="70e61-105">Pkey</span><span class="sxs-lookup"><span data-stu-id="70e61-105">PKEY</span></span>

<span data-ttu-id="70e61-106">PKEY \_ Photo \_ FNumber</span><span class="sxs-lookup"><span data-stu-id="70e61-106">PKEY\_Photo\_FNumber</span></span>

### <a name="containers"></a><span data-ttu-id="70e61-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="70e61-107">Containers</span></span>

<span data-ttu-id="70e61-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="70e61-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="70e61-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="70e61-109">Read-Only</span></span>

<span data-ttu-id="70e61-110">Sim</span><span class="sxs-lookup"><span data-stu-id="70e61-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="70e61-111">Tipo PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="70e61-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="70e61-112">VT \_ R8</span><span class="sxs-lookup"><span data-stu-id="70e61-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="70e61-113">Política de resolução de conflitos</span><span class="sxs-lookup"><span data-stu-id="70e61-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="70e61-114">Esse valor é gerado de System.Photo.FNumberNumerator e System.Photo.FNumberDenominator.</span><span class="sxs-lookup"><span data-stu-id="70e61-114">This value is generated from System.Photo.FNumberNumerator and System.Photo.FNumberDenominator.</span></span> <span data-ttu-id="70e61-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="70e61-115">It cannot be written directly.</span></span> <span data-ttu-id="70e61-116">Valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="70e61-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="70e61-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="70e61-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="70e61-118">Ler caminhos</span><span class="sxs-lookup"><span data-stu-id="70e61-118">Read Paths</span></span>



| <span data-ttu-id="70e61-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="70e61-119">Order</span></span> | <span data-ttu-id="70e61-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="70e61-120">Path</span></span>                          | <span data-ttu-id="70e61-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="70e61-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="70e61-122">1</span><span class="sxs-lookup"><span data-stu-id="70e61-122">1</span></span>     | <span data-ttu-id="70e61-123">/app1/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="70e61-123">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="70e61-124">2</span><span class="sxs-lookup"><span data-stu-id="70e61-124">2</span></span>     | <span data-ttu-id="70e61-125">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="70e61-125">/xmp/exif:FNumber</span></span>             |             |



 

### <a name="write-paths"></a><span data-ttu-id="70e61-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="70e61-126">Write Paths</span></span>



| <span data-ttu-id="70e61-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="70e61-127">Order</span></span> | <span data-ttu-id="70e61-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="70e61-128">Path</span></span>                          | <span data-ttu-id="70e61-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="70e61-129">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="70e61-130">1</span><span class="sxs-lookup"><span data-stu-id="70e61-130">1</span></span>     | <span data-ttu-id="70e61-131">/app1/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="70e61-131">/app1/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="70e61-132">2</span><span class="sxs-lookup"><span data-stu-id="70e61-132">2</span></span>     | <span data-ttu-id="70e61-133">/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="70e61-133">/xmp/exif:FNumber</span></span>             |             | 
 

### <a name="remove-paths"></a><span data-ttu-id="70e61-134">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="70e61-134">Remove Paths</span></span>



| <span data-ttu-id="70e61-135">Ordem</span><span class="sxs-lookup"><span data-stu-id="70e61-135">Order</span></span> | <span data-ttu-id="70e61-136">Caminho</span><span class="sxs-lookup"><span data-stu-id="70e61-136">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="70e61-137">1</span><span class="sxs-lookup"><span data-stu-id="70e61-137">1</span></span>     | <span data-ttu-id="70e61-138">/app1/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="70e61-138">/app1/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="70e61-139">2</span><span class="sxs-lookup"><span data-stu-id="70e61-139">2</span></span>     | <span data-ttu-id="70e61-140">/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="70e61-140">/xmp/exif:fnumber</span></span>             |



 

### <a name="tiff-policies"></a><span data-ttu-id="70e61-141">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="70e61-141">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="70e61-142">Ler caminhos</span><span class="sxs-lookup"><span data-stu-id="70e61-142">Read Paths</span></span>



| <span data-ttu-id="70e61-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="70e61-143">Order</span></span> | <span data-ttu-id="70e61-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="70e61-144">Path</span></span>                     | <span data-ttu-id="70e61-145">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="70e61-145">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="70e61-146">1</span><span class="sxs-lookup"><span data-stu-id="70e61-146">1</span></span>     | <span data-ttu-id="70e61-147">/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="70e61-147">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="70e61-148">2</span><span class="sxs-lookup"><span data-stu-id="70e61-148">2</span></span>     | <span data-ttu-id="70e61-149">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="70e61-149">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="write-paths"></a><span data-ttu-id="70e61-150">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="70e61-150">Write Paths</span></span>



| <span data-ttu-id="70e61-151">Ordem</span><span class="sxs-lookup"><span data-stu-id="70e61-151">Order</span></span> | <span data-ttu-id="70e61-152">Caminho</span><span class="sxs-lookup"><span data-stu-id="70e61-152">Path</span></span>                     | <span data-ttu-id="70e61-153">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="70e61-153">Disk Format</span></span> |
|-------|--------------------------|-------------|
| <span data-ttu-id="70e61-154">1</span><span class="sxs-lookup"><span data-stu-id="70e61-154">1</span></span>     | <span data-ttu-id="70e61-155">/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="70e61-155">/ifd/exif/{ushort=33437}</span></span> |             |
| <span data-ttu-id="70e61-156">2</span><span class="sxs-lookup"><span data-stu-id="70e61-156">2</span></span>     | <span data-ttu-id="70e61-157">/ifd/xmp/exif:FNumber</span><span class="sxs-lookup"><span data-stu-id="70e61-157">/ifd/xmp/exif:FNumber</span></span>    |             |



 

### <a name="remove-paths"></a><span data-ttu-id="70e61-158">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="70e61-158">Remove Paths</span></span>



| <span data-ttu-id="70e61-159">Ordem</span><span class="sxs-lookup"><span data-stu-id="70e61-159">Order</span></span> | <span data-ttu-id="70e61-160">Caminho</span><span class="sxs-lookup"><span data-stu-id="70e61-160">Path</span></span>                     |
|-------|--------------------------|
| <span data-ttu-id="70e61-161">1</span><span class="sxs-lookup"><span data-stu-id="70e61-161">1</span></span>     | <span data-ttu-id="70e61-162">/ifd/exif/{ushort=33437}</span><span class="sxs-lookup"><span data-stu-id="70e61-162">/ifd/exif/{ushort=33437}</span></span> |
| <span data-ttu-id="70e61-163">2</span><span class="sxs-lookup"><span data-stu-id="70e61-163">2</span></span>     | <span data-ttu-id="70e61-164">/ifd/xmp/exif:fnumber</span><span class="sxs-lookup"><span data-stu-id="70e61-164">/ifd/xmp/exif:fnumber</span></span>    |



 

## <a name="remarks"></a><span data-ttu-id="70e61-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="70e61-165">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="70e61-166">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70e61-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70e61-167">System.Photo.FNumber</span><span class="sxs-lookup"><span data-stu-id="70e61-167">System.Photo.FNumber</span></span>](../properties/props-system-photo-fnumber.md)
</dt> </dl>

 

 
