---
description: A política de metadados de foto para a propriedade System. GPS. SpeedRef.
ms.assetid: 45fea6be-1e63-4244-a93d-d446e315ddd4
title: Política de metadados de foto System. GPS. SpeedRef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c454a016dd77345c0a85e0ca3df1ae52694bd81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764041"
---
# <a name="systemgpsspeedref-photo-metadata-policy"></a><span data-ttu-id="7c06b-103">Política de metadados de foto System. GPS. SpeedRef</span><span class="sxs-lookup"><span data-stu-id="7c06b-103">System.GPS.SpeedRef Photo Metadata Policy</span></span>

<span data-ttu-id="7c06b-104">A política de metadados de foto para a propriedade [System. GPS. SpeedRef](../properties/props-system-gps-speedref.md) .</span><span class="sxs-lookup"><span data-stu-id="7c06b-104">The photo metadata policy for the [System.GPS.SpeedRef](../properties/props-system-gps-speedref.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="7c06b-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="7c06b-105">PKEY</span></span>

<span data-ttu-id="7c06b-106">PKEY \_ GPS \_ SpeedRef</span><span class="sxs-lookup"><span data-stu-id="7c06b-106">PKEY\_GPS\_SpeedRef</span></span>

### <a name="containers"></a><span data-ttu-id="7c06b-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="7c06b-107">Containers</span></span>

<span data-ttu-id="7c06b-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="7c06b-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="7c06b-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7c06b-109">Read-Only</span></span>

<span data-ttu-id="7c06b-110">No</span><span class="sxs-lookup"><span data-stu-id="7c06b-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="7c06b-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="7c06b-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="7c06b-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="7c06b-112">VT\_LPWSTR</span></span>

### <a name="input-propvariant-type"></a><span data-ttu-id="7c06b-113">Tipo de PROPVARIANT de entrada</span><span class="sxs-lookup"><span data-stu-id="7c06b-113">Input PROPVARIANT Type</span></span>

<span data-ttu-id="7c06b-114">O ' VT \_ LPWSTR ' é preferencial, mas o ' VT \_ LPSTR ' também é aceito.</span><span class="sxs-lookup"><span data-stu-id="7c06b-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted..</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="7c06b-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="7c06b-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="7c06b-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="7c06b-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="7c06b-117">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="7c06b-117">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="7c06b-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="7c06b-118">Read Paths</span></span>



| <span data-ttu-id="7c06b-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="7c06b-119">Order</span></span> | <span data-ttu-id="7c06b-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="7c06b-120">Path</span></span>                      | <span data-ttu-id="7c06b-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7c06b-121">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="7c06b-122">1</span><span class="sxs-lookup"><span data-stu-id="7c06b-122">1</span></span>     | <span data-ttu-id="7c06b-123">/App1/IFD/GPS/{UShort = 12}</span><span class="sxs-lookup"><span data-stu-id="7c06b-123">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="7c06b-124">ascii</span><span class="sxs-lookup"><span data-stu-id="7c06b-124">ascii</span></span>       |
| <span data-ttu-id="7c06b-125">2</span><span class="sxs-lookup"><span data-stu-id="7c06b-125">2</span></span>     | <span data-ttu-id="7c06b-126">/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="7c06b-126">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="7c06b-127">Unicode</span><span class="sxs-lookup"><span data-stu-id="7c06b-127">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="7c06b-128">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="7c06b-128">Write Paths</span></span>



| <span data-ttu-id="7c06b-129">Ordem</span><span class="sxs-lookup"><span data-stu-id="7c06b-129">Order</span></span> | <span data-ttu-id="7c06b-130">Caminho</span><span class="sxs-lookup"><span data-stu-id="7c06b-130">Path</span></span>                      | <span data-ttu-id="7c06b-131">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7c06b-131">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="7c06b-132">1</span><span class="sxs-lookup"><span data-stu-id="7c06b-132">1</span></span>     | <span data-ttu-id="7c06b-133">/App1/IFD/GPS/{UShort = 12}</span><span class="sxs-lookup"><span data-stu-id="7c06b-133">/app1/ifd/gps/{ushort=12}</span></span> | <span data-ttu-id="7c06b-134">ascii</span><span class="sxs-lookup"><span data-stu-id="7c06b-134">ascii</span></span>       |
| <span data-ttu-id="7c06b-135">2</span><span class="sxs-lookup"><span data-stu-id="7c06b-135">2</span></span>     | <span data-ttu-id="7c06b-136">/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="7c06b-136">/xmp/exif:GPSSpeedRef</span></span>     | <span data-ttu-id="7c06b-137">Unicode</span><span class="sxs-lookup"><span data-stu-id="7c06b-137">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7c06b-138">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="7c06b-138">Remove Paths</span></span>



| <span data-ttu-id="7c06b-139">Ordem</span><span class="sxs-lookup"><span data-stu-id="7c06b-139">Order</span></span> | <span data-ttu-id="7c06b-140">Caminho</span><span class="sxs-lookup"><span data-stu-id="7c06b-140">Path</span></span>                      | <span data-ttu-id="7c06b-141">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7c06b-141">Disk format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="7c06b-142">1</span><span class="sxs-lookup"><span data-stu-id="7c06b-142">1</span></span>     | <span data-ttu-id="7c06b-143">/App1/IFD/GPS/{UShort = 12}</span><span class="sxs-lookup"><span data-stu-id="7c06b-143">/app1/ifd/gps/{ushort=12}</span></span> |             |
| <span data-ttu-id="7c06b-144">2</span><span class="sxs-lookup"><span data-stu-id="7c06b-144">2</span></span>     | <span data-ttu-id="7c06b-145">/xmp/exif:gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="7c06b-145">/xmp/exif:gpsspeedref</span></span>     |             |



 

### <a name="tiff-policies"></a><span data-ttu-id="7c06b-146">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="7c06b-146">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="7c06b-147">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="7c06b-147">Read Paths</span></span>



| <span data-ttu-id="7c06b-148">Ordem</span><span class="sxs-lookup"><span data-stu-id="7c06b-148">Order</span></span> | <span data-ttu-id="7c06b-149">Caminho</span><span class="sxs-lookup"><span data-stu-id="7c06b-149">Path</span></span>                      |         |
|-------|---------------------------|---------|
| <span data-ttu-id="7c06b-150">1</span><span class="sxs-lookup"><span data-stu-id="7c06b-150">1</span></span>     | <span data-ttu-id="7c06b-151">/IFD/GPS/{UShort = 12}</span><span class="sxs-lookup"><span data-stu-id="7c06b-151">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="7c06b-152">ascii</span><span class="sxs-lookup"><span data-stu-id="7c06b-152">ascii</span></span>   |
| <span data-ttu-id="7c06b-153">2</span><span class="sxs-lookup"><span data-stu-id="7c06b-153">2</span></span>     | <span data-ttu-id="7c06b-154">/ifd/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="7c06b-154">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="7c06b-155">Unicode</span><span class="sxs-lookup"><span data-stu-id="7c06b-155">unicode</span></span> |



 

### <a name="write-paths"></a><span data-ttu-id="7c06b-156">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="7c06b-156">Write Paths</span></span>



| <span data-ttu-id="7c06b-157">Ordem</span><span class="sxs-lookup"><span data-stu-id="7c06b-157">Order</span></span> | <span data-ttu-id="7c06b-158">Caminho</span><span class="sxs-lookup"><span data-stu-id="7c06b-158">Path</span></span>                      | <span data-ttu-id="7c06b-159">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="7c06b-159">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="7c06b-160">1</span><span class="sxs-lookup"><span data-stu-id="7c06b-160">1</span></span>     | <span data-ttu-id="7c06b-161">/IFD/GPS/{UShort = 12}</span><span class="sxs-lookup"><span data-stu-id="7c06b-161">/ifd/gps/{ushort=12}</span></span>      | <span data-ttu-id="7c06b-162">ascii</span><span class="sxs-lookup"><span data-stu-id="7c06b-162">ascii</span></span>       |
| <span data-ttu-id="7c06b-163">2</span><span class="sxs-lookup"><span data-stu-id="7c06b-163">2</span></span>     | <span data-ttu-id="7c06b-164">/ifd/xmp/exif:GPSSpeedRef</span><span class="sxs-lookup"><span data-stu-id="7c06b-164">/ifd/xmp/exif:GPSSpeedRef</span></span> | <span data-ttu-id="7c06b-165">Unicode</span><span class="sxs-lookup"><span data-stu-id="7c06b-165">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="7c06b-166">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="7c06b-166">Remove Paths</span></span>



| <span data-ttu-id="7c06b-167">Ordem</span><span class="sxs-lookup"><span data-stu-id="7c06b-167">Order</span></span> | <span data-ttu-id="7c06b-168">Caminho</span><span class="sxs-lookup"><span data-stu-id="7c06b-168">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="7c06b-169">1</span><span class="sxs-lookup"><span data-stu-id="7c06b-169">1</span></span>     | <span data-ttu-id="7c06b-170">/IFD/GPS/{UShort = 12}</span><span class="sxs-lookup"><span data-stu-id="7c06b-170">/ifd/gps/{ushort=12}</span></span>      |
| <span data-ttu-id="7c06b-171">2</span><span class="sxs-lookup"><span data-stu-id="7c06b-171">2</span></span>     | <span data-ttu-id="7c06b-172">/ifd/xmp/exif:gpsspeedref</span><span class="sxs-lookup"><span data-stu-id="7c06b-172">/ifd/xmp/exif:gpsspeedref</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7c06b-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c06b-173">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c06b-174">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7c06b-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c06b-175">System. GPS. SpeedRef</span><span class="sxs-lookup"><span data-stu-id="7c06b-175">System.GPS.SpeedRef</span></span>](../properties/props-system-gps-speedref.md)
</dt> </dl>

 

 
