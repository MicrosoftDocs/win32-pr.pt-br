---
description: A política de metadados de foto para a propriedade System. GPS. AreaInformation.
ms.assetid: d9ecb00b-1f97-4f53-909f-30231104d398
title: Política de metadados de foto System. GPS. AreaInformation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e14837da9ffa8b688caf1a544e222043988cf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104296932"
---
# <a name="systemgpsareainformation-photo-metadata-policy"></a><span data-ttu-id="a5143-103">Política de metadados de foto System. GPS. AreaInformation</span><span class="sxs-lookup"><span data-stu-id="a5143-103">System.GPS.AreaInformation Photo Metadata Policy</span></span>

<span data-ttu-id="a5143-104">A política de metadados de foto para a propriedade [System. GPS. AreaInformation](../properties/props-system-gps-areainformation.md) .</span><span class="sxs-lookup"><span data-stu-id="a5143-104">The photo metadata policy for the [System.GPS.AreaInformation](../properties/props-system-gps-areainformation.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="a5143-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="a5143-105">PKEY</span></span>

<span data-ttu-id="a5143-106">PKEY \_ GPS \_ AreaInformation</span><span class="sxs-lookup"><span data-stu-id="a5143-106">PKEY\_GPS\_AreaInformation</span></span>

### <a name="containers"></a><span data-ttu-id="a5143-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="a5143-107">Containers</span></span>

<span data-ttu-id="a5143-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="a5143-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="a5143-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a5143-109">Read-Only</span></span>

<span data-ttu-id="a5143-110">No</span><span class="sxs-lookup"><span data-stu-id="a5143-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="a5143-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="a5143-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="a5143-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="a5143-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="a5143-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="a5143-113">Input Type</span></span>

<span data-ttu-id="a5143-114">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a5143-114">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="a5143-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="a5143-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="a5143-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="a5143-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="a5143-117">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="a5143-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a5143-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="a5143-118">Read Paths</span></span>



| <span data-ttu-id="a5143-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="a5143-119">Order</span></span> | <span data-ttu-id="a5143-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="a5143-120">Path</span></span>                         | <span data-ttu-id="a5143-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a5143-121">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="a5143-122">1</span><span class="sxs-lookup"><span data-stu-id="a5143-122">1</span></span>     | <span data-ttu-id="a5143-123">/App1/IFD/GPS/{UShort = 28}</span><span class="sxs-lookup"><span data-stu-id="a5143-123">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="a5143-124">2</span><span class="sxs-lookup"><span data-stu-id="a5143-124">2</span></span>     | <span data-ttu-id="a5143-125">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="a5143-125">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="a5143-126">Unicode</span><span class="sxs-lookup"><span data-stu-id="a5143-126">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a5143-127">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="a5143-127">Write Paths</span></span>



| <span data-ttu-id="a5143-128">Ordem</span><span class="sxs-lookup"><span data-stu-id="a5143-128">Order</span></span> | <span data-ttu-id="a5143-129">Caminho</span><span class="sxs-lookup"><span data-stu-id="a5143-129">Path</span></span>                         | <span data-ttu-id="a5143-130">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a5143-130">Disk Format</span></span> |
|-------|------------------------------|-------------|
| <span data-ttu-id="a5143-131">1</span><span class="sxs-lookup"><span data-stu-id="a5143-131">1</span></span>     | <span data-ttu-id="a5143-132">/App1/IFD/GPS/{UShort = 28}</span><span class="sxs-lookup"><span data-stu-id="a5143-132">/app1/ifd/gps/{ushort=28}</span></span>    |             |
| <span data-ttu-id="a5143-133">2</span><span class="sxs-lookup"><span data-stu-id="a5143-133">2</span></span>     | <span data-ttu-id="a5143-134">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="a5143-134">/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="a5143-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="a5143-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a5143-136">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="a5143-136">Remove Paths</span></span>



| <span data-ttu-id="a5143-137">Ordem</span><span class="sxs-lookup"><span data-stu-id="a5143-137">Order</span></span> | <span data-ttu-id="a5143-138">Caminho</span><span class="sxs-lookup"><span data-stu-id="a5143-138">Path</span></span>                         |
|-------|------------------------------|
| <span data-ttu-id="a5143-139">1</span><span class="sxs-lookup"><span data-stu-id="a5143-139">1</span></span>     | <span data-ttu-id="a5143-140">/App1/IFD/GPS/{UShort = 28}</span><span class="sxs-lookup"><span data-stu-id="a5143-140">/app1/ifd/gps/{ushort=28}</span></span>    |
| <span data-ttu-id="a5143-141">2</span><span class="sxs-lookup"><span data-stu-id="a5143-141">2</span></span>     | <span data-ttu-id="a5143-142">/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="a5143-142">/xmp/exif:GPSAreaInformation</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="a5143-143">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="a5143-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="a5143-144">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="a5143-144">Read Paths</span></span>



| <span data-ttu-id="a5143-145">Ordem</span><span class="sxs-lookup"><span data-stu-id="a5143-145">Order</span></span> | <span data-ttu-id="a5143-146">Caminho</span><span class="sxs-lookup"><span data-stu-id="a5143-146">Path</span></span>                             | <span data-ttu-id="a5143-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a5143-147">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="a5143-148">1</span><span class="sxs-lookup"><span data-stu-id="a5143-148">1</span></span>     | <span data-ttu-id="a5143-149">/IFD/GPS/{UShort = 28}</span><span class="sxs-lookup"><span data-stu-id="a5143-149">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="a5143-150">2</span><span class="sxs-lookup"><span data-stu-id="a5143-150">2</span></span>     | <span data-ttu-id="a5143-151">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="a5143-151">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="a5143-152">Unicode</span><span class="sxs-lookup"><span data-stu-id="a5143-152">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="a5143-153">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="a5143-153">Write Paths</span></span>



| <span data-ttu-id="a5143-154">Ordem</span><span class="sxs-lookup"><span data-stu-id="a5143-154">Order</span></span> | <span data-ttu-id="a5143-155">Caminho</span><span class="sxs-lookup"><span data-stu-id="a5143-155">Path</span></span>                             | <span data-ttu-id="a5143-156">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="a5143-156">Disk Format</span></span> |
|-------|----------------------------------|-------------|
| <span data-ttu-id="a5143-157">1</span><span class="sxs-lookup"><span data-stu-id="a5143-157">1</span></span>     | <span data-ttu-id="a5143-158">/IFD/GPS/{UShort = 28}</span><span class="sxs-lookup"><span data-stu-id="a5143-158">/ifd/gps/{ushort=28}</span></span>             |             |
| <span data-ttu-id="a5143-159">2</span><span class="sxs-lookup"><span data-stu-id="a5143-159">2</span></span>     | <span data-ttu-id="a5143-160">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="a5143-160">/ifd/xmp/exif:GPSAreaInformation</span></span> | <span data-ttu-id="a5143-161">Unicode</span><span class="sxs-lookup"><span data-stu-id="a5143-161">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="a5143-162">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="a5143-162">Remove Paths</span></span>



| <span data-ttu-id="a5143-163">Ordem</span><span class="sxs-lookup"><span data-stu-id="a5143-163">Order</span></span> | <span data-ttu-id="a5143-164">Caminho</span><span class="sxs-lookup"><span data-stu-id="a5143-164">Path</span></span>                             |
|-------|----------------------------------|
| <span data-ttu-id="a5143-165">1</span><span class="sxs-lookup"><span data-stu-id="a5143-165">1</span></span>     | <span data-ttu-id="a5143-166">/IFD/GPS/{UShort = 28}</span><span class="sxs-lookup"><span data-stu-id="a5143-166">/ifd/gps/{ushort=28}</span></span>             |
| <span data-ttu-id="a5143-167">2</span><span class="sxs-lookup"><span data-stu-id="a5143-167">2</span></span>     | <span data-ttu-id="a5143-168">/ifd/xmp/exif:GPSAreaInformation</span><span class="sxs-lookup"><span data-stu-id="a5143-168">/ifd/xmp/exif:GPSAreaInformation</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a5143-169">Comentários</span><span class="sxs-lookup"><span data-stu-id="a5143-169">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="a5143-170">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a5143-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5143-171">System. GPS. AreaInformation</span><span class="sxs-lookup"><span data-stu-id="a5143-171">System.GPS.AreaInformation</span></span>](../properties/props-system-gps-areainformation.md)
</dt> </dl>

 

 
