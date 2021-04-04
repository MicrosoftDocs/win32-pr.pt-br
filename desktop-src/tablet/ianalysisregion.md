---
description: Expõe métodos e propriedades para uma região que representa uma área de um documento.
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: Interface IAnalysisRegion (IACom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c9c5e7653790e193c03b1cf4e0c489ea39c3eec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647239"
---
# <a name="ianalysisregion-interface"></a><span data-ttu-id="c4d29-103">Interface IAnalysisRegion</span><span class="sxs-lookup"><span data-stu-id="c4d29-103">IAnalysisRegion interface</span></span>

<span data-ttu-id="c4d29-104">Expõe métodos e propriedades para uma região que representa uma área de um documento.</span><span class="sxs-lookup"><span data-stu-id="c4d29-104">Exposes methods and properties for a region that represents an area of a document.</span></span>

## <a name="members"></a><span data-ttu-id="c4d29-105">Membros</span><span class="sxs-lookup"><span data-stu-id="c4d29-105">Members</span></span>

<span data-ttu-id="c4d29-106">A interface **IAnalysisRegion** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="c4d29-106">The **IAnalysisRegion** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="c4d29-107">**IAnalysisRegion** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c4d29-107">**IAnalysisRegion** also has these types of members:</span></span>

-   [<span data-ttu-id="c4d29-108">Métodos</span><span class="sxs-lookup"><span data-stu-id="c4d29-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="c4d29-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="c4d29-109">Methods</span></span>

<span data-ttu-id="c4d29-110">A interface **IAnalysisRegion** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="c4d29-110">The **IAnalysisRegion** interface has these methods.</span></span>



| <span data-ttu-id="c4d29-111">Método</span><span class="sxs-lookup"><span data-stu-id="c4d29-111">Method</span></span>                                                           | <span data-ttu-id="c4d29-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4d29-112">Description</span></span>                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c4d29-113">**8i**</span><span class="sxs-lookup"><span data-stu-id="c4d29-113">**Clone**</span></span>](ianalysisregion-clone.md)                           | <span data-ttu-id="c4d29-114">Cria uma cópia do **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="c4d29-114">Creates a copy of the **IAnalysisRegion**.</span></span><br/>                                                                                          |
| [<span data-ttu-id="c4d29-115">**ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="c4d29-115">**ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)     | <span data-ttu-id="c4d29-116">Restringe a área do **IAnalysisRegion** à parte de sua área que não faz a interseção do retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="c4d29-116">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified rectangle.</span></span><br/>           |
| [<span data-ttu-id="c4d29-117">**ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="c4d29-117">**ExcludeRegion**</span></span>](ianalysisregion-excluderegion.md)           | <span data-ttu-id="c4d29-118">Restringe a área do **IAnalysisRegion** à parte de sua área que não faz a interseção do **IAnalysisRegion** especificado.</span><span class="sxs-lookup"><span data-stu-id="c4d29-118">Restricts the area of the **IAnalysisRegion** to the portion of its area that does not intersect the specified **IAnalysisRegion**.</span></span><br/> |
| [<span data-ttu-id="c4d29-119">**GetBounds**</span><span class="sxs-lookup"><span data-stu-id="c4d29-119">**GetBounds**</span></span>](ianalysisregion-getbounds.md)                   | <span data-ttu-id="c4d29-120">Recupera o retângulo delimitador do **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="c4d29-120">Retrieves the bounding rectangle of the **IAnalysisRegion**.</span></span><br/>                                                                        |
| [<span data-ttu-id="c4d29-121">**GetRegionScans**</span><span class="sxs-lookup"><span data-stu-id="c4d29-121">**GetRegionScans**</span></span>](ianalysisregion-getregionscans.md)         | <span data-ttu-id="c4d29-122">Recupera uma matriz de retângulos que define a área do **IAnalysisRegion**.</span><span class="sxs-lookup"><span data-stu-id="c4d29-122">Retrieves an array of rectangles that defines the area of the **IAnalysisRegion**.</span></span><br/>                                                  |
| [<span data-ttu-id="c4d29-123">**IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="c4d29-123">**IntersectRectangle**</span></span>](ianalysisregion-intersectrectangle.md) | <span data-ttu-id="c4d29-124">Restringe a área desta **IAnalysisRegion** para a área criada por sua interseção com o retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="c4d29-124">Restricts the area of this **IAnalysisRegion** to the area created by its intersection with the specified rectangle.</span></span><br/>                |
| [<span data-ttu-id="c4d29-125">**IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="c4d29-125">**IntersectRegion**</span></span>](ianalysisregion-intersectregion.md)       | <span data-ttu-id="c4d29-126">Restringe a área de **IAnalysisRegion** para a área criada por sua interseção com o **IAnalysisRegion** especificado.</span><span class="sxs-lookup"><span data-stu-id="c4d29-126">Restricts the area of the **IAnalysisRegion** to the area created by its intersection with the specified **IAnalysisRegion**.</span></span><br/>       |
| [<span data-ttu-id="c4d29-127">**IntersectsWith**</span><span class="sxs-lookup"><span data-stu-id="c4d29-127">**IntersectsWith**</span></span>](ianalysisregion-intersectswith.md)         | <span data-ttu-id="c4d29-128">Determina se a área do **IAnalysisRegion** intersecciona com o retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="c4d29-128">Determines whether the area of the **IAnalysisRegion** intersects with the specified rectangle.</span></span><br/>                                     |
| [<span data-ttu-id="c4d29-129">**IsEmpty**</span><span class="sxs-lookup"><span data-stu-id="c4d29-129">**IsEmpty**</span></span>](ianalysisregion-isempty.md)                       | <span data-ttu-id="c4d29-130">Recupera um valor que indica se **IAnalysisRegion** representa uma região vazia.</span><span class="sxs-lookup"><span data-stu-id="c4d29-130">Retrieves a value indicating whether the **IAnalysisRegion** represents an empty region.</span></span><br/>                                            |
| [<span data-ttu-id="c4d29-131">**IsFinite**</span><span class="sxs-lookup"><span data-stu-id="c4d29-131">**IsInfinite**</span></span>](ianalysisregion-isinfinite.md)                 | <span data-ttu-id="c4d29-132">Recupera um valor que indica se **IAnalysisRegion** representa uma região infinita.</span><span class="sxs-lookup"><span data-stu-id="c4d29-132">Retrieves a value indicating whether the **IAnalysisRegion** represents an infinite region.</span></span><br/>                                         |
| [<span data-ttu-id="c4d29-133">**MakeEmpty**</span><span class="sxs-lookup"><span data-stu-id="c4d29-133">**MakeEmpty**</span></span>](ianalysisregion-makeempty.md)                   | <span data-ttu-id="c4d29-134">Reduz o **IAnalysisRegion** para representar uma área vazia.</span><span class="sxs-lookup"><span data-stu-id="c4d29-134">Reduces the **IAnalysisRegion** to represent an empty area.</span></span><br/>                                                                         |
| [<span data-ttu-id="c4d29-135">**MakeInfinite**</span><span class="sxs-lookup"><span data-stu-id="c4d29-135">**MakeInfinite**</span></span>](ianalysisregion-makeinfinite.md)             | <span data-ttu-id="c4d29-136">Expande o **IAnalysisRegion** para representar uma área infinita.</span><span class="sxs-lookup"><span data-stu-id="c4d29-136">Expands the **IAnalysisRegion** to represent an infinite area.</span></span><br/>                                                                      |
| [<span data-ttu-id="c4d29-137">**UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="c4d29-137">**UnionRectangle**</span></span>](ianalysisregion-unionrectangle.md)         | <span data-ttu-id="c4d29-138">Expande a área desta **IAnalysisRegion** para a área criada por sua união com o retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="c4d29-138">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified rectangle.</span></span><br/>                         |
| [<span data-ttu-id="c4d29-139">**UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="c4d29-139">**UnionRegion**</span></span>](ianalysisregion-unionregion.md)               | <span data-ttu-id="c4d29-140">Expande a área desta **IAnalysisRegion** para a área criada por sua união com o **IAnalysisRegion** especificado.</span><span class="sxs-lookup"><span data-stu-id="c4d29-140">Expands the area of this **IAnalysisRegion** to the area created by its union with the specified **IAnalysisRegion**.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="c4d29-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4d29-141">Remarks</span></span>

<span data-ttu-id="c4d29-142">Essa interface representa uma área que é construída a partir de regiões retangulares.</span><span class="sxs-lookup"><span data-stu-id="c4d29-142">This interface represents an area that is constructed from rectangular regions.</span></span> <span data-ttu-id="c4d29-143">O [**IInkAnalyzer**](iinkanalyzer.md) retorna ou interpreta as coordenadas de uma área dentro do espaço de coordenadas no qual recebe dados de traço.</span><span class="sxs-lookup"><span data-stu-id="c4d29-143">The [**IInkAnalyzer**](iinkanalyzer.md) returns or interprets an area's coordinates within the coordinate space in which it receives stroke data.</span></span>

<span data-ttu-id="c4d29-144">Para obter os limites atuais do **IAnalysisRegion**, use o método [**IAnalysisRegion:: GetBounds**](ianalysisregion-getbounds.md) ou o [**método IAnalysisRegion:: GetRegionScans**](ianalysisregion-getregionscans.md).</span><span class="sxs-lookup"><span data-stu-id="c4d29-144">To get the current bounds of the **IAnalysisRegion**, use [**IAnalysisRegion::GetBounds Method**](ianalysisregion-getbounds.md) or [**IAnalysisRegion::GetRegionScans Method**](ianalysisregion-getregionscans.md).</span></span>

<span data-ttu-id="c4d29-145">Para modificar a área de um **IAnalysisRegion** existente, use os métodos a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4d29-145">To modify the area of an existing **IAnalysisRegion**, use the following methods.</span></span>

-   [<span data-ttu-id="c4d29-146">**IAnalysisRegion::ExcludeRectangle**</span><span class="sxs-lookup"><span data-stu-id="c4d29-146">**IAnalysisRegion::ExcludeRectangle**</span></span>](ianalysisregion-excluderectangle.md)
-   [<span data-ttu-id="c4d29-147">**Método IAnalysisRegion:: ExcludeRegion**</span><span class="sxs-lookup"><span data-stu-id="c4d29-147">**IAnalysisRegion::ExcludeRegion Method**</span></span>](ianalysisregion-excluderegion.md)
-   [<span data-ttu-id="c4d29-148">**Método IAnalysisRegion:: IntersectRectangle**</span><span class="sxs-lookup"><span data-stu-id="c4d29-148">**IAnalysisRegion::IntersectRectangle Method**</span></span>](ianalysisregion-intersectrectangle.md)
-   [<span data-ttu-id="c4d29-149">**Método IAnalysisRegion:: IntersectRegion**</span><span class="sxs-lookup"><span data-stu-id="c4d29-149">**IAnalysisRegion::IntersectRegion Method**</span></span>](ianalysisregion-intersectregion.md)
-   [<span data-ttu-id="c4d29-150">**Método IAnalysisRegion:: MakeEmpty**</span><span class="sxs-lookup"><span data-stu-id="c4d29-150">**IAnalysisRegion::MakeEmpty Method**</span></span>](ianalysisregion-makeempty.md)
-   [<span data-ttu-id="c4d29-151">**Método IAnalysisRegion:: MakeInfinite**</span><span class="sxs-lookup"><span data-stu-id="c4d29-151">**IAnalysisRegion::MakeInfinite Method**</span></span>](ianalysisregion-makeinfinite.md)
-   [<span data-ttu-id="c4d29-152">**Método IAnalysisRegion:: UnionRectangle**</span><span class="sxs-lookup"><span data-stu-id="c4d29-152">**IAnalysisRegion::UnionRectangle Method**</span></span>](ianalysisregion-unionrectangle.md)
-   [<span data-ttu-id="c4d29-153">**Método IAnalysisRegion:: UnionRegion**</span><span class="sxs-lookup"><span data-stu-id="c4d29-153">**IAnalysisRegion::UnionRegion Method**</span></span>](ianalysisregion-unionregion.md)

<span data-ttu-id="c4d29-154">Essa interface é equivalente à classe System. Windows. Ink. AnalysisCore. AnalysisRegionBase na .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="c4d29-154">This interface is equivalent to the System.Windows.Ink.AnalysisCore.AnalysisRegionBase class in the .NET Framework.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4d29-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4d29-155">Requirements</span></span>



| <span data-ttu-id="c4d29-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4d29-156">Requirement</span></span> | <span data-ttu-id="c4d29-157">Valor</span><span class="sxs-lookup"><span data-stu-id="c4d29-157">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4d29-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4d29-158">Minimum supported client</span></span><br/> | <span data-ttu-id="c4d29-159">Somente aplicativos de área de trabalho do Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="c4d29-159">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="c4d29-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c4d29-160">Minimum supported server</span></span><br/> | <span data-ttu-id="c4d29-161">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="c4d29-161">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="c4d29-162">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4d29-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4d29-163"><dt>IACom. h (também requer IACom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="c4d29-163"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c4d29-164">DLL</span><span class="sxs-lookup"><span data-stu-id="c4d29-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4d29-165"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4d29-165"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="c4d29-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4d29-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4d29-167">**IInkAnalyzer**</span><span class="sxs-lookup"><span data-stu-id="c4d29-167">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="c4d29-168">Referência de análise de tinta</span><span class="sxs-lookup"><span data-stu-id="c4d29-168">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

