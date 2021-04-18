---
description: A política de metadados de foto para a propriedade System. GPS. MapDatum.
ms.assetid: be31e98f-5114-4693-a9ef-37fea334875b
title: Política de metadados de foto System. GPS. MapDatum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb7a279c79da3d2b1dd20563af35bd34233a1a2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759517"
---
# <a name="systemgpsmapdatum-photo-metadata-policy"></a><span data-ttu-id="6b427-103">Política de metadados de foto System. GPS. MapDatum</span><span class="sxs-lookup"><span data-stu-id="6b427-103">System.GPS.MapDatum Photo Metadata Policy</span></span>

<span data-ttu-id="6b427-104">A política de metadados de foto para a propriedade [System. GPS. MapDatum](../properties/props-system-gps-mapdatum.md) .</span><span class="sxs-lookup"><span data-stu-id="6b427-104">The photo metadata policy for the [System.GPS.MapDatum](../properties/props-system-gps-mapdatum.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="6b427-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="6b427-105">PKEY</span></span>

<span data-ttu-id="6b427-106">PKEY \_ GPS \_ MapDatum</span><span class="sxs-lookup"><span data-stu-id="6b427-106">PKEY\_GPS\_MapDatum</span></span>

### <a name="containers"></a><span data-ttu-id="6b427-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="6b427-107">Containers</span></span>

<span data-ttu-id="6b427-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="6b427-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="6b427-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6b427-109">Read-Only</span></span>

<span data-ttu-id="6b427-110">No</span><span class="sxs-lookup"><span data-stu-id="6b427-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="6b427-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="6b427-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="6b427-112">LPWStr do VT \_</span><span class="sxs-lookup"><span data-stu-id="6b427-112">VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="6b427-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="6b427-113">Input Type</span></span>

<span data-ttu-id="6b427-114">VT \_ LPWSTR é preferível, mas VT \_ LPSTR também é aceito</span><span class="sxs-lookup"><span data-stu-id="6b427-114">VT\_LPWSTR is preferred, but VT\_LPSTR is also accepted</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="6b427-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="6b427-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="6b427-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="6b427-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="6b427-117">Precedência de caminhos (JPEG)</span><span class="sxs-lookup"><span data-stu-id="6b427-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="6b427-118">Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="6b427-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="6b427-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="6b427-119">Order</span></span> | <span data-ttu-id="6b427-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="6b427-120">Path</span></span>                          | <span data-ttu-id="6b427-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6b427-121">Disk Format</span></span> | <span data-ttu-id="6b427-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6b427-122">Required</span></span> |
|-------|-------------------------------|-------------|----------|
| <span data-ttu-id="6b427-123">1</span><span class="sxs-lookup"><span data-stu-id="6b427-123">1</span></span>     | <span data-ttu-id="6b427-124">/xmp/exif:GPSMapDatum</span><span class="sxs-lookup"><span data-stu-id="6b427-124">/xmp/exif:GPSMapDatum</span></span>         | <span data-ttu-id="6b427-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="6b427-125">Unicode</span></span>     | <span data-ttu-id="6b427-126">Yes</span><span class="sxs-lookup"><span data-stu-id="6b427-126">Yes</span></span>      |
| <span data-ttu-id="6b427-127">2</span><span class="sxs-lookup"><span data-stu-id="6b427-127">2</span></span>     | <span data-ttu-id="6b427-128">/App1/IFD/GPS/ \\ {UShort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="6b427-128">/app1/ifd/gps/\\{ushort=18\\}</span></span> | <span data-ttu-id="6b427-129">ASCII</span><span class="sxs-lookup"><span data-stu-id="6b427-129">ASCII</span></span>       | <span data-ttu-id="6b427-130">No</span><span class="sxs-lookup"><span data-stu-id="6b427-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="6b427-131">Precedência de caminhos (TIFF)</span><span class="sxs-lookup"><span data-stu-id="6b427-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="6b427-132">Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="6b427-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="6b427-133">Ordem</span><span class="sxs-lookup"><span data-stu-id="6b427-133">Order</span></span> | <span data-ttu-id="6b427-134">Caminho</span><span class="sxs-lookup"><span data-stu-id="6b427-134">Path</span></span>                      | <span data-ttu-id="6b427-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="6b427-135">Disk Format</span></span> | <span data-ttu-id="6b427-136">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="6b427-136">Required</span></span> |
|-------|---------------------------|-------------|----------|
| <span data-ttu-id="6b427-137">1</span><span class="sxs-lookup"><span data-stu-id="6b427-137">1</span></span>     | <span data-ttu-id="6b427-138">/ifd/xmp/exif:GPSMapDatum</span><span class="sxs-lookup"><span data-stu-id="6b427-138">/ifd/xmp/exif:GPSMapDatum</span></span> | <span data-ttu-id="6b427-139">Unicode</span><span class="sxs-lookup"><span data-stu-id="6b427-139">Unicode</span></span>     | <span data-ttu-id="6b427-140">Yes</span><span class="sxs-lookup"><span data-stu-id="6b427-140">Yes</span></span>      |
| <span data-ttu-id="6b427-141">2</span><span class="sxs-lookup"><span data-stu-id="6b427-141">2</span></span>     | <span data-ttu-id="6b427-142">/IFD/GPS/ \\ {UShort = 18 \\ }</span><span class="sxs-lookup"><span data-stu-id="6b427-142">/ifd/gps/\\{ushort=18\\}</span></span>  | <span data-ttu-id="6b427-143">ASCII</span><span class="sxs-lookup"><span data-stu-id="6b427-143">ASCII</span></span>       | <span data-ttu-id="6b427-144">Não</span><span class="sxs-lookup"><span data-stu-id="6b427-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="6b427-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b427-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b427-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6b427-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b427-147">System. GPS. MapDatum</span><span class="sxs-lookup"><span data-stu-id="6b427-147">System.GPS.MapDatum</span></span>](../properties/props-system-gps-mapdatum.md)
</dt> </dl>

 

 
