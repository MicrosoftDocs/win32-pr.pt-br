---
description: A política de metadados de foto para a propriedade System. GPS. ProcessingMethod.
ms.assetid: 840021a8-ec1d-4916-93b2-7cc1803e2d8c
title: Política de metadados de foto System. GPS. ProcessingMethod
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02bf1484eb8e8a53c65a9cd43c54b076e418d4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105810189"
---
# <a name="systemgpsprocessingmethod-photo-metadata-policy"></a><span data-ttu-id="680ce-103">Política de metadados de foto System. GPS. ProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="680ce-103">System.GPS.ProcessingMethod Photo Metadata Policy</span></span>

<span data-ttu-id="680ce-104">A política de metadados de foto para a propriedade [System. GPS. ProcessingMethod](../properties/props-system-gps-processingmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="680ce-104">The photo metadata policy for the [System.GPS.ProcessingMethod](../properties/props-system-gps-processingmethod.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="680ce-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="680ce-105">PKEY</span></span>

<span data-ttu-id="680ce-106">PKEY \_ GPS \_ ProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="680ce-106">PKEY\_GPS\_ProcessingMethod</span></span>

### <a name="containers"></a><span data-ttu-id="680ce-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="680ce-107">Containers</span></span>

<span data-ttu-id="680ce-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="680ce-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="680ce-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="680ce-109">Read-Only</span></span>

<span data-ttu-id="680ce-110">No</span><span class="sxs-lookup"><span data-stu-id="680ce-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="680ce-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="680ce-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="680ce-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="680ce-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="680ce-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="680ce-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="680ce-114">VT \_ LPWSTR é preferível, mas VT \_ LPSTR também é aceito.</span><span class="sxs-lookup"><span data-stu-id="680ce-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="680ce-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="680ce-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="680ce-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="680ce-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="680ce-117">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="680ce-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="680ce-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="680ce-118">Read Paths</span></span>



| <span data-ttu-id="680ce-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="680ce-119">Order</span></span> | <span data-ttu-id="680ce-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="680ce-120">Path</span></span>                          | <span data-ttu-id="680ce-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="680ce-121">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="680ce-122">1</span><span class="sxs-lookup"><span data-stu-id="680ce-122">1</span></span>     | <span data-ttu-id="680ce-123">/App1/IFD/GPS/{UShort = 27}</span><span class="sxs-lookup"><span data-stu-id="680ce-123">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="680ce-124">2</span><span class="sxs-lookup"><span data-stu-id="680ce-124">2</span></span>     | <span data-ttu-id="680ce-125">/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="680ce-125">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="680ce-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="680ce-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="680ce-127">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="680ce-127">Write Paths</span></span>



| <span data-ttu-id="680ce-128">Ordem</span><span class="sxs-lookup"><span data-stu-id="680ce-128">Order</span></span> | <span data-ttu-id="680ce-129">Caminho</span><span class="sxs-lookup"><span data-stu-id="680ce-129">Path</span></span>                          | <span data-ttu-id="680ce-130">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="680ce-130">Disk Format</span></span> |
|-------|-------------------------------|-------------|
| <span data-ttu-id="680ce-131">1</span><span class="sxs-lookup"><span data-stu-id="680ce-131">1</span></span>     | <span data-ttu-id="680ce-132">/App1/IFD/GPS/{UShort = 27}</span><span class="sxs-lookup"><span data-stu-id="680ce-132">/app1/ifd/gps/{ushort=27}</span></span>     |             |
| <span data-ttu-id="680ce-133">2</span><span class="sxs-lookup"><span data-stu-id="680ce-133">2</span></span>     | <span data-ttu-id="680ce-134">/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="680ce-134">/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="680ce-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="680ce-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="680ce-136">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="680ce-136">Remove Paths</span></span>



| <span data-ttu-id="680ce-137">Ordem</span><span class="sxs-lookup"><span data-stu-id="680ce-137">Order</span></span> | <span data-ttu-id="680ce-138">Caminho</span><span class="sxs-lookup"><span data-stu-id="680ce-138">Path</span></span>                          |
|-------|-------------------------------|
| <span data-ttu-id="680ce-139">1</span><span class="sxs-lookup"><span data-stu-id="680ce-139">1</span></span>     | <span data-ttu-id="680ce-140">/App1/IFD/GPS/{UShort = 27}</span><span class="sxs-lookup"><span data-stu-id="680ce-140">/app1/ifd/gps/{ushort=27}</span></span>     |
| <span data-ttu-id="680ce-141">2</span><span class="sxs-lookup"><span data-stu-id="680ce-141">2</span></span>     | <span data-ttu-id="680ce-142">/xmp/exif:gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="680ce-142">/xmp/exif:gpsprocessingmethod</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="680ce-143">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="680ce-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="680ce-144">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="680ce-144">Read Paths</span></span>



| <span data-ttu-id="680ce-145">Ordem</span><span class="sxs-lookup"><span data-stu-id="680ce-145">Order</span></span> | <span data-ttu-id="680ce-146">Caminho</span><span class="sxs-lookup"><span data-stu-id="680ce-146">Path</span></span>                              | <span data-ttu-id="680ce-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="680ce-147">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="680ce-148">1</span><span class="sxs-lookup"><span data-stu-id="680ce-148">1</span></span>     | <span data-ttu-id="680ce-149">/ifd/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="680ce-149">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="680ce-150">Unicode</span><span class="sxs-lookup"><span data-stu-id="680ce-150">unicode</span></span>     |
| <span data-ttu-id="680ce-151">2</span><span class="sxs-lookup"><span data-stu-id="680ce-151">2</span></span>     | <span data-ttu-id="680ce-152">/IFD/GPS/{UShort = 27}</span><span class="sxs-lookup"><span data-stu-id="680ce-152">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="write-paths"></a><span data-ttu-id="680ce-153">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="680ce-153">Write Paths</span></span>



| <span data-ttu-id="680ce-154">Ordem</span><span class="sxs-lookup"><span data-stu-id="680ce-154">Order</span></span> | <span data-ttu-id="680ce-155">Caminho</span><span class="sxs-lookup"><span data-stu-id="680ce-155">Path</span></span>                              | <span data-ttu-id="680ce-156">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="680ce-156">Disk Format</span></span> |
|-------|-----------------------------------|-------------|
| <span data-ttu-id="680ce-157">1</span><span class="sxs-lookup"><span data-stu-id="680ce-157">1</span></span>     | <span data-ttu-id="680ce-158">/ifd/xmp/exif:GPSProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="680ce-158">/ifd/xmp/exif:GPSProcessingMethod</span></span> | <span data-ttu-id="680ce-159">Unicode</span><span class="sxs-lookup"><span data-stu-id="680ce-159">unicode</span></span>     |
| <span data-ttu-id="680ce-160">2</span><span class="sxs-lookup"><span data-stu-id="680ce-160">2</span></span>     | <span data-ttu-id="680ce-161">/IFD/GPS/{UShort = 27}</span><span class="sxs-lookup"><span data-stu-id="680ce-161">/ifd/gps/{ushort=27}</span></span>              |             |



 

### <a name="remove-paths"></a><span data-ttu-id="680ce-162">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="680ce-162">Remove Paths</span></span>



| <span data-ttu-id="680ce-163">Ordem</span><span class="sxs-lookup"><span data-stu-id="680ce-163">Order</span></span> | <span data-ttu-id="680ce-164">Caminho</span><span class="sxs-lookup"><span data-stu-id="680ce-164">Path</span></span>                              |
|-------|-----------------------------------|
| <span data-ttu-id="680ce-165">1</span><span class="sxs-lookup"><span data-stu-id="680ce-165">1</span></span>     | <span data-ttu-id="680ce-166">/ifd/xmp/exif:gpsprocessingmethod</span><span class="sxs-lookup"><span data-stu-id="680ce-166">/ifd/xmp/exif:gpsprocessingmethod</span></span> |
| <span data-ttu-id="680ce-167">2</span><span class="sxs-lookup"><span data-stu-id="680ce-167">2</span></span>     | <span data-ttu-id="680ce-168">/IFD/GPS/{UShort = 27}</span><span class="sxs-lookup"><span data-stu-id="680ce-168">/ifd/gps/{ushort=27}</span></span>              |



 

## <a name="remarks"></a><span data-ttu-id="680ce-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="680ce-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="680ce-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="680ce-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="680ce-171">System. GPS. ProcessingMethod</span><span class="sxs-lookup"><span data-stu-id="680ce-171">System.GPS.ProcessingMethod</span></span>](../properties/props-system-gps-processingmethod.md)
</dt> </dl>

 

 
