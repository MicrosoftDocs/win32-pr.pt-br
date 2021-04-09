---
description: A política de metadados de foto para a propriedade System. GPS. Date.
ms.assetid: 75047658-b6f3-454e-961a-89016c244bf6
title: Política de metadados de foto System. GPS. Date
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c736c79cd76d2d070d727dc024925717b386cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171521"
---
# <a name="systemgpsdate-photo-metadata-policy"></a><span data-ttu-id="0b6b0-103">Política de metadados de foto System. GPS. Date</span><span class="sxs-lookup"><span data-stu-id="0b6b0-103">System.GPS.Date Photo Metadata Policy</span></span>

<span data-ttu-id="0b6b0-104">A política de metadados de foto para a propriedade [System. GPS. Date](../properties/props-system-gps-date.md) .</span><span class="sxs-lookup"><span data-stu-id="0b6b0-104">The photo metadata policy for the [System.GPS.Date](../properties/props-system-gps-date.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="0b6b0-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="0b6b0-105">PKEY</span></span>

<span data-ttu-id="0b6b0-106">PKEY \_ data de GPS \_</span><span class="sxs-lookup"><span data-stu-id="0b6b0-106">PKEY\_GPS\_Date</span></span>

### <a name="containers"></a><span data-ttu-id="0b6b0-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="0b6b0-107">Containers</span></span>

<span data-ttu-id="0b6b0-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="0b6b0-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="0b6b0-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0b6b0-109">Read-Only</span></span>

<span data-ttu-id="0b6b0-110">No</span><span class="sxs-lookup"><span data-stu-id="0b6b0-110">No</span></span>

### <a name="input-type"></a><span data-ttu-id="0b6b0-111">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="0b6b0-111">Input Type</span></span>

<span data-ttu-id="0b6b0-112">Cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-112">String.</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="0b6b0-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="0b6b0-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="0b6b0-114">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-114">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policies"></a><span data-ttu-id="0b6b0-115">Políticas JPEG</span><span class="sxs-lookup"><span data-stu-id="0b6b0-115">JPEG Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0b6b0-116">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="0b6b0-116">Read Paths</span></span>



| <span data-ttu-id="0b6b0-117">Ordem</span><span class="sxs-lookup"><span data-stu-id="0b6b0-117">Order</span></span> | <span data-ttu-id="0b6b0-118">Caminho</span><span class="sxs-lookup"><span data-stu-id="0b6b0-118">Path</span></span>                      | <span data-ttu-id="0b6b0-119">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0b6b0-119">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="0b6b0-120">1</span><span class="sxs-lookup"><span data-stu-id="0b6b0-120">1</span></span>     | <span data-ttu-id="0b6b0-121">/App1/IFD/GPS/{UShort = 29}</span><span class="sxs-lookup"><span data-stu-id="0b6b0-121">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="0b6b0-122">ascii</span><span class="sxs-lookup"><span data-stu-id="0b6b0-122">ascii</span></span>       |
| <span data-ttu-id="0b6b0-123">2</span><span class="sxs-lookup"><span data-stu-id="0b6b0-123">2</span></span>     | <span data-ttu-id="0b6b0-124">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="0b6b0-124">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="0b6b0-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="0b6b0-125">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0b6b0-126">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="0b6b0-126">Write Paths</span></span>



| <span data-ttu-id="0b6b0-127">Ordem</span><span class="sxs-lookup"><span data-stu-id="0b6b0-127">Order</span></span> | <span data-ttu-id="0b6b0-128">Caminho</span><span class="sxs-lookup"><span data-stu-id="0b6b0-128">Path</span></span>                      | <span data-ttu-id="0b6b0-129">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0b6b0-129">Disk Format</span></span> |
|-------|---------------------------|-------------|
| <span data-ttu-id="0b6b0-130">1</span><span class="sxs-lookup"><span data-stu-id="0b6b0-130">1</span></span>     | <span data-ttu-id="0b6b0-131">/App1/IFD/GPS/{UShort = 29}</span><span class="sxs-lookup"><span data-stu-id="0b6b0-131">/app1/ifd/gps/{ushort=29}</span></span> | <span data-ttu-id="0b6b0-132">ascii</span><span class="sxs-lookup"><span data-stu-id="0b6b0-132">ascii</span></span>       |
| <span data-ttu-id="0b6b0-133">2</span><span class="sxs-lookup"><span data-stu-id="0b6b0-133">2</span></span>     | <span data-ttu-id="0b6b0-134">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="0b6b0-134">/xmp/exif:GPSTimeStamp</span></span>    | <span data-ttu-id="0b6b0-135">Unicode</span><span class="sxs-lookup"><span data-stu-id="0b6b0-135">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0b6b0-136">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="0b6b0-136">Remove Paths</span></span>



| <span data-ttu-id="0b6b0-137">Ordem</span><span class="sxs-lookup"><span data-stu-id="0b6b0-137">Order</span></span> | <span data-ttu-id="0b6b0-138">Caminho</span><span class="sxs-lookup"><span data-stu-id="0b6b0-138">Path</span></span>                      |
|-------|---------------------------|
| <span data-ttu-id="0b6b0-139">1</span><span class="sxs-lookup"><span data-stu-id="0b6b0-139">1</span></span>     | <span data-ttu-id="0b6b0-140">/App1/IFD/GPS/{UShort = 29}</span><span class="sxs-lookup"><span data-stu-id="0b6b0-140">/app1/ifd/gps/{ushort=29}</span></span> |
| <span data-ttu-id="0b6b0-141">2</span><span class="sxs-lookup"><span data-stu-id="0b6b0-141">2</span></span>     | <span data-ttu-id="0b6b0-142">/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="0b6b0-142">/xmp/exif:GPSTimeStamp</span></span>    |



 

### <a name="tiff-policies"></a><span data-ttu-id="0b6b0-143">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="0b6b0-143">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="0b6b0-144">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="0b6b0-144">Read Paths</span></span>



| <span data-ttu-id="0b6b0-145">Ordem</span><span class="sxs-lookup"><span data-stu-id="0b6b0-145">Order</span></span> | <span data-ttu-id="0b6b0-146">Caminho</span><span class="sxs-lookup"><span data-stu-id="0b6b0-146">Path</span></span>                       | <span data-ttu-id="0b6b0-147">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0b6b0-147">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="0b6b0-148">1</span><span class="sxs-lookup"><span data-stu-id="0b6b0-148">1</span></span>     | <span data-ttu-id="0b6b0-149">/IFD/GPS/{UShort = 29}</span><span class="sxs-lookup"><span data-stu-id="0b6b0-149">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="0b6b0-150">ascii</span><span class="sxs-lookup"><span data-stu-id="0b6b0-150">ascii</span></span>       |
| <span data-ttu-id="0b6b0-151">2</span><span class="sxs-lookup"><span data-stu-id="0b6b0-151">2</span></span>     | <span data-ttu-id="0b6b0-152">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="0b6b0-152">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="0b6b0-153">Unicode</span><span class="sxs-lookup"><span data-stu-id="0b6b0-153">unicode</span></span>     |



 

### <a name="write-paths"></a><span data-ttu-id="0b6b0-154">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="0b6b0-154">Write Paths</span></span>



| <span data-ttu-id="0b6b0-155">Ordem</span><span class="sxs-lookup"><span data-stu-id="0b6b0-155">Order</span></span> | <span data-ttu-id="0b6b0-156">Caminho</span><span class="sxs-lookup"><span data-stu-id="0b6b0-156">Path</span></span>                       | <span data-ttu-id="0b6b0-157">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="0b6b0-157">Disk Format</span></span> |
|-------|----------------------------|-------------|
| <span data-ttu-id="0b6b0-158">1</span><span class="sxs-lookup"><span data-stu-id="0b6b0-158">1</span></span>     | <span data-ttu-id="0b6b0-159">/IFD/GPS/{UShort = 29}</span><span class="sxs-lookup"><span data-stu-id="0b6b0-159">/ifd/gps/{ushort=29}</span></span>       | <span data-ttu-id="0b6b0-160">ascii</span><span class="sxs-lookup"><span data-stu-id="0b6b0-160">ascii</span></span>       |
| <span data-ttu-id="0b6b0-161">2</span><span class="sxs-lookup"><span data-stu-id="0b6b0-161">2</span></span>     | <span data-ttu-id="0b6b0-162">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="0b6b0-162">/ifd/xmp/exif:GPSTimeStamp</span></span> | <span data-ttu-id="0b6b0-163">Unicode</span><span class="sxs-lookup"><span data-stu-id="0b6b0-163">unicode</span></span>     |



 

### <a name="remove-paths"></a><span data-ttu-id="0b6b0-164">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="0b6b0-164">Remove Paths</span></span>



| <span data-ttu-id="0b6b0-165">Ordem</span><span class="sxs-lookup"><span data-stu-id="0b6b0-165">Order</span></span> | <span data-ttu-id="0b6b0-166">Caminho</span><span class="sxs-lookup"><span data-stu-id="0b6b0-166">Path</span></span>                       |
|-------|----------------------------|
| <span data-ttu-id="0b6b0-167">1</span><span class="sxs-lookup"><span data-stu-id="0b6b0-167">1</span></span>     | <span data-ttu-id="0b6b0-168">/IFD/GPS/{UShort = 29}</span><span class="sxs-lookup"><span data-stu-id="0b6b0-168">/ifd/gps/{ushort=29}</span></span>       |
| <span data-ttu-id="0b6b0-169">2</span><span class="sxs-lookup"><span data-stu-id="0b6b0-169">2</span></span>     | <span data-ttu-id="0b6b0-170">/ifd/xmp/exif:GPSTimeStamp</span><span class="sxs-lookup"><span data-stu-id="0b6b0-170">/ifd/xmp/exif:GPSTimeStamp</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0b6b0-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="0b6b0-171">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b6b0-172">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0b6b0-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b6b0-173">System. GPS. Date</span><span class="sxs-lookup"><span data-stu-id="0b6b0-173">System.GPS.Date</span></span>](../properties/props-system-gps-date.md)
</dt> </dl>

 

 
