---
description: A política de metadados de foto para a propriedade System. Photo. Peoplenames.
ms.assetid: 567d5542-fc7b-4d19-bc3c-b9d6e26e3387
title: Política de metadados de foto System. Photo. Peoplenames
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3de9f5adda67fcd0e555194500f109df078bdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754228"
---
# <a name="systemphotopeoplenames-photo-metadata-policy"></a><span data-ttu-id="65f5d-103">Política de metadados de foto System. Photo. Peoplenames</span><span class="sxs-lookup"><span data-stu-id="65f5d-103">System.Photo.PeopleNames Photo Metadata Policy</span></span>

<span data-ttu-id="65f5d-104">A política de metadados de foto para a propriedade [System. Photo. peoplenames](../properties/props-system-photo-peoplenames.md) .</span><span class="sxs-lookup"><span data-stu-id="65f5d-104">The photo metadata policy for the [System.Photo.PeopleNames](../properties/props-system-photo-peoplenames.md) property.</span></span>

### <a name="pkey"></a><span data-ttu-id="65f5d-105">PKEY</span><span class="sxs-lookup"><span data-stu-id="65f5d-105">PKEY</span></span>

<span data-ttu-id="65f5d-106">PKEY \_ fotos de \_ pessoas</span><span class="sxs-lookup"><span data-stu-id="65f5d-106">PKEY\_Photo\_PeopleNames</span></span>

### <a name="containers"></a><span data-ttu-id="65f5d-107">Contêineres</span><span class="sxs-lookup"><span data-stu-id="65f5d-107">Containers</span></span>

<span data-ttu-id="65f5d-108">JPEG, TIFF</span><span class="sxs-lookup"><span data-stu-id="65f5d-108">JPEG, TIFF</span></span>

### <a name="read-only"></a><span data-ttu-id="65f5d-109">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="65f5d-109">Read-Only</span></span>

<span data-ttu-id="65f5d-110">No</span><span class="sxs-lookup"><span data-stu-id="65f5d-110">No</span></span>

### <a name="output-propvariant-type"></a><span data-ttu-id="65f5d-111">Tipo de PROPVARIANT de saída</span><span class="sxs-lookup"><span data-stu-id="65f5d-111">Output PROPVARIANT Type</span></span>

<span data-ttu-id="65f5d-112">\_LPWStr do vetor VT VT \| \_</span><span class="sxs-lookup"><span data-stu-id="65f5d-112">VT\_VECTOR \| VT\_LPWSTR</span></span>

### <a name="input-type"></a><span data-ttu-id="65f5d-113">Tipo de entrada</span><span class="sxs-lookup"><span data-stu-id="65f5d-113">Input Type</span></span>

<span data-ttu-id="65f5d-114">StringMulti</span><span class="sxs-lookup"><span data-stu-id="65f5d-114">StringMulti</span></span>

### <a name="conflict-resolution-policy"></a><span data-ttu-id="65f5d-115">Política de resolução de conflito</span><span class="sxs-lookup"><span data-stu-id="65f5d-115">Conflict Resolution Policy</span></span>

<span data-ttu-id="65f5d-116">Os valores de esquemas diferentes são reconciliados.</span><span class="sxs-lookup"><span data-stu-id="65f5d-116">Values from different schemas are reconciled.</span></span>

### <a name="jpeg-policy"></a><span data-ttu-id="65f5d-117">Política JPEG</span><span class="sxs-lookup"><span data-stu-id="65f5d-117">JPEG Policy</span></span>

### <a name="read-paths"></a><span data-ttu-id="65f5d-118">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="65f5d-118">Read Paths</span></span>



| <span data-ttu-id="65f5d-119">Ordem</span><span class="sxs-lookup"><span data-stu-id="65f5d-119">Order</span></span> | <span data-ttu-id="65f5d-120">Caminho</span><span class="sxs-lookup"><span data-stu-id="65f5d-120">Path</span></span>                                                           | <span data-ttu-id="65f5d-121">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="65f5d-121">Disk Format</span></span> |
|-------|----------------------------------------------------------------|-------------|
| <span data-ttu-id="65f5d-122">1</span><span class="sxs-lookup"><span data-stu-id="65f5d-122">1</span></span>     | <span data-ttu-id="65f5d-123">/XMP/ <xmpstruct> MP: RegionInfo/ <xmpbag> MPRI: regiões</span><span class="sxs-lookup"><span data-stu-id="65f5d-123">/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions</span></span> | <span data-ttu-id="65f5d-124">ushort</span><span class="sxs-lookup"><span data-stu-id="65f5d-124">ushort</span></span>      |



 

### <a name="write-paths"></a><span data-ttu-id="65f5d-125">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="65f5d-125">Write Paths</span></span>

<span data-ttu-id="65f5d-126">Esta propriedade não pode ser gravada usando a política de metadados.</span><span class="sxs-lookup"><span data-stu-id="65f5d-126">This property cannot be written using the metadata policy.</span></span>

### <a name="remove-paths"></a><span data-ttu-id="65f5d-127">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="65f5d-127">Remove Paths</span></span>



| <span data-ttu-id="65f5d-128">Ordem</span><span class="sxs-lookup"><span data-stu-id="65f5d-128">Order</span></span> | <span data-ttu-id="65f5d-129">Caminho</span><span class="sxs-lookup"><span data-stu-id="65f5d-129">Path</span></span>                                |
|-------|-------------------------------------|
| <span data-ttu-id="65f5d-130">1</span><span class="sxs-lookup"><span data-stu-id="65f5d-130">1</span></span>     | <span data-ttu-id="65f5d-131">/XMP/ <xmpstruct> MP: RegionInfo</span><span class="sxs-lookup"><span data-stu-id="65f5d-131">/xmp/<xmpstruct>MP:RegionInfo</span></span> |



 

### <a name="tiff-policies"></a><span data-ttu-id="65f5d-132">Políticas TIFF</span><span class="sxs-lookup"><span data-stu-id="65f5d-132">TIFF Policies</span></span>

### <a name="read-paths"></a><span data-ttu-id="65f5d-133">Caminhos de leitura</span><span class="sxs-lookup"><span data-stu-id="65f5d-133">Read Paths</span></span>



| <span data-ttu-id="65f5d-134">Ordem</span><span class="sxs-lookup"><span data-stu-id="65f5d-134">Order</span></span> | <span data-ttu-id="65f5d-135">Caminho</span><span class="sxs-lookup"><span data-stu-id="65f5d-135">Path</span></span>                                                               | <span data-ttu-id="65f5d-136">Formato de disco</span><span class="sxs-lookup"><span data-stu-id="65f5d-136">Disk Format</span></span> |
|-------|--------------------------------------------------------------------|-------------|
| <span data-ttu-id="65f5d-137">1</span><span class="sxs-lookup"><span data-stu-id="65f5d-137">1</span></span>     | <span data-ttu-id="65f5d-138">/IFD/XMP/ <xmpstruct> MP: RegionInfo/ <xmpbag> MPRI: regiões</span><span class="sxs-lookup"><span data-stu-id="65f5d-138">/ifd/xmp/<xmpstruct>MP:RegionInfo/<xmpbag>MPRI:Regions</span></span> | <span data-ttu-id="65f5d-139">ushort</span><span class="sxs-lookup"><span data-stu-id="65f5d-139">ushort</span></span>      |



 

### <a name="write-paths"></a><span data-ttu-id="65f5d-140">Caminhos de gravação</span><span class="sxs-lookup"><span data-stu-id="65f5d-140">Write Paths</span></span>

<span data-ttu-id="65f5d-141">Esta propriedade não pode ser gravada usando a política de metadados.</span><span class="sxs-lookup"><span data-stu-id="65f5d-141">This property cannot be written using the metadata policy.</span></span>

### <a name="remove-paths"></a><span data-ttu-id="65f5d-142">Remover caminhos</span><span class="sxs-lookup"><span data-stu-id="65f5d-142">Remove Paths</span></span>



| <span data-ttu-id="65f5d-143">Ordem</span><span class="sxs-lookup"><span data-stu-id="65f5d-143">Order</span></span> | <span data-ttu-id="65f5d-144">Caminho</span><span class="sxs-lookup"><span data-stu-id="65f5d-144">Path</span></span>                                    |
|-------|-----------------------------------------|
| <span data-ttu-id="65f5d-145">1</span><span class="sxs-lookup"><span data-stu-id="65f5d-145">1</span></span>     | <span data-ttu-id="65f5d-146">/IFD/XMP/ <xmpstruct> MP: RegionInfo</span><span class="sxs-lookup"><span data-stu-id="65f5d-146">/ifd/xmp/<xmpstruct>MP:RegionInfo</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="65f5d-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="65f5d-147">Remarks</span></span>

## <a name="related-topics"></a><span data-ttu-id="65f5d-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65f5d-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65f5d-149">System. Photo. programmode</span><span class="sxs-lookup"><span data-stu-id="65f5d-149">System.Photo.ProgramMode</span></span>](../properties/props-system-photo-programmode.md)
</dt> </dl>

 

 
