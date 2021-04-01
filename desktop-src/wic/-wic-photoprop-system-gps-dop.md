---
description: A política de metadados de foto para a propriedade System. GPS. DOP.
ms.assetid: 62efd1cc-a2ae-4e53-a0f2-4822b8c91c42
title: Política de metadados de foto System. GPS. DOP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c33f3bfc6b958593748396124a8cfd1a7de73fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922641"
---
# <a name="systemgpsdop-photo-metadata-policy"></a><span data-ttu-id="b2e23-103">Política de metadados de foto System. GPS. DOP</span><span class="sxs-lookup"><span data-stu-id="b2e23-103">System.GPS.DOP Photo Metadata Policy</span></span>

<span data-ttu-id="b2e23-104">A política de metadados de foto para a propriedade [System. GPS. DOP](../properties/props-system-gps-dop.md) .</span><span class="sxs-lookup"><span data-stu-id="b2e23-104">The photo metadata policy for the [System.GPS.DOP](../properties/props-system-gps-dop.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="b2e23-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="b2e23-105">PKEY</span></span>

<span data-ttu-id="b2e23-106">\_DOP de GPS PKEY \_</span><span class="sxs-lookup"><span data-stu-id="b2e23-106">PKEY\_GPS\_DOP</span></span>

### <a name="containers"></a><span data-ttu-id="b2e23-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="b2e23-107">Containers</span></span>

<span data-ttu-id="b2e23-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="b2e23-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="b2e23-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b2e23-109">Read-Only</span></span>

<span data-ttu-id="b2e23-110">Sim</span><span class="sxs-lookup"><span data-stu-id="b2e23-110">Yes</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="b2e23-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="b2e23-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="b2e23-112">R8 de VT \_</span><span class="sxs-lookup"><span data-stu-id="b2e23-112">VT\_R8</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="b2e23-113">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="b2e23-113">Conflict Resolution Policy</span></span>

<span data-ttu-id="b2e23-114">Esse valor pode ser gravado escrevendo em System. GPS. DOPNumerator e System. GPS. DOPDenominator.</span><span class="sxs-lookup"><span data-stu-id="b2e23-114">This value can be written by writing to System.GPS.DOPNumerator and System.GPS.DOPDenominator.</span></span> <span data-ttu-id="b2e23-115">Ele não pode ser gravado diretamente.</span><span class="sxs-lookup"><span data-stu-id="b2e23-115">It cannot be written directly.</span></span> <span data-ttu-id="b2e23-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="b2e23-116">Values from different schemas are reconciled.</span></span>

### <a name="precedence-of-paths-jpeg"></a><span data-ttu-id="b2e23-117">Precedência de caminhos (JPEG)</span><span class="sxs-lookup"><span data-stu-id="b2e23-117">Precedence of Paths (JPEG)</span></span>

<span data-ttu-id="b2e23-118">Se o arquivo estiver no formato JPEG, o manipulador lerá, gravará e removerá os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="b2e23-118">If the file is in JPEG format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="b2e23-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="b2e23-119">Order</span></span> | <span data-ttu-id="b2e23-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="b2e23-120">Path</span></span>                          | <span data-ttu-id="b2e23-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b2e23-121">Disk Format</span></span>   | <span data-ttu-id="b2e23-122">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b2e23-122">Required</span></span> |
|-------|-------------------------------|---------------|----------|
| <span data-ttu-id="b2e23-123">1</span><span class="sxs-lookup"><span data-stu-id="b2e23-123">1</span></span>     | <span data-ttu-id="b2e23-124">/xmp/exif:GPSDOP</span><span class="sxs-lookup"><span data-stu-id="b2e23-124">/xmp/exif:GPSDOP</span></span>              | <span data-ttu-id="b2e23-125">Racional de XMP</span><span class="sxs-lookup"><span data-stu-id="b2e23-125">XMP rational</span></span>  | <span data-ttu-id="b2e23-126">Sim</span><span class="sxs-lookup"><span data-stu-id="b2e23-126">Yes</span></span>      |
| <span data-ttu-id="b2e23-127">2</span><span class="sxs-lookup"><span data-stu-id="b2e23-127">2</span></span>     | <span data-ttu-id="b2e23-128">/App1/IFD/GPS/ \\ {UShort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="b2e23-128">/app1/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="b2e23-129">Racional de EXIF</span><span class="sxs-lookup"><span data-stu-id="b2e23-129">EXIF rational</span></span> | <span data-ttu-id="b2e23-130">Não</span><span class="sxs-lookup"><span data-stu-id="b2e23-130">No</span></span>       |



 

### <a name="precedence-of-paths-tiff"></a><span data-ttu-id="b2e23-131">Precedência de caminhos (TIFF)</span><span class="sxs-lookup"><span data-stu-id="b2e23-131">Precedence of Paths (TIFF)</span></span>

<span data-ttu-id="b2e23-132">Se o arquivo estiver no formato TIFF, o manipulador lerá, gravará e removerá os dados na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="b2e23-132">If the file is in TIFF format, the handler will read, write, and remove the data in the following order:</span></span>



| <span data-ttu-id="b2e23-133">Ordem</span><span class="sxs-lookup"><span data-stu-id="b2e23-133">Order</span></span> | <span data-ttu-id="b2e23-134">Caminho</span><span class="sxs-lookup"><span data-stu-id="b2e23-134">Path</span></span>                     | <span data-ttu-id="b2e23-135">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="b2e23-135">Disk Format</span></span>   | <span data-ttu-id="b2e23-136">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="b2e23-136">Required</span></span> |
|-------|--------------------------|---------------|----------|
| <span data-ttu-id="b2e23-137">1</span><span class="sxs-lookup"><span data-stu-id="b2e23-137">1</span></span>     | <span data-ttu-id="b2e23-138">/ifd/xmp/exif:GPSDop</span><span class="sxs-lookup"><span data-stu-id="b2e23-138">/ifd/xmp/exif:GPSDop</span></span>     | <span data-ttu-id="b2e23-139">Racional de XMP</span><span class="sxs-lookup"><span data-stu-id="b2e23-139">XMP rational</span></span>  | <span data-ttu-id="b2e23-140">Sim</span><span class="sxs-lookup"><span data-stu-id="b2e23-140">Yes</span></span>      |
| <span data-ttu-id="b2e23-141">2</span><span class="sxs-lookup"><span data-stu-id="b2e23-141">2</span></span>     | <span data-ttu-id="b2e23-142">/IFD/GPS/ \\ {UShort = 11 \\ }</span><span class="sxs-lookup"><span data-stu-id="b2e23-142">/ifd/gps/\\{ushort=11\\}</span></span> | <span data-ttu-id="b2e23-143">Racional de EXIF</span><span class="sxs-lookup"><span data-stu-id="b2e23-143">EXIF rational</span></span> | <span data-ttu-id="b2e23-144">Não</span><span class="sxs-lookup"><span data-stu-id="b2e23-144">No</span></span>       |



 

## <a name="remarks"></a><span data-ttu-id="b2e23-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2e23-145">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="b2e23-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2e23-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2e23-147">System. GPS. DOP</span><span class="sxs-lookup"><span data-stu-id="b2e23-147">System.GPS.DOP</span></span>](../properties/props-system-gps-dop.md)
</dt> </dl>

 

 
