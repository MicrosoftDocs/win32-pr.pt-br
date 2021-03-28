---
description: Este tópico lista os métodos ExcludeClip da classe Graphics. Para obter uma lista completa de métodos para a classe Graphics, consulte gráficos.
ms.assetid: ee2b1bc7-6623-4144-b8fb-2ab9fbe28f59
title: Métodos Graphics. ExcludeClip (Gdiplusgraphics. h)
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 70011bfe1aba7ef8e7c14b58f61bfcbd9549c8fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "104989463"
---
# <a name="graphicsexcludeclip-methods"></a><span data-ttu-id="c5863-104">Métodos Graphics. ExcludeClip</span><span class="sxs-lookup"><span data-stu-id="c5863-104">Graphics.ExcludeClip methods</span></span>

<span data-ttu-id="c5863-105">Este tópico lista os métodos ExcludeClip da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="c5863-105">This topic lists the ExcludeClip methods of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="c5863-106">Para obter uma lista completa de métodos para a classe **Graphics** , consulte [**gráficos**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span><span class="sxs-lookup"><span data-stu-id="c5863-106">For a complete list of methods for the **Graphics** class, see [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics).</span></span>

### <a name="overload-list"></a><span data-ttu-id="c5863-107">Lista de sobrecargas</span><span class="sxs-lookup"><span data-stu-id="c5863-107">Overload list</span></span>



| <span data-ttu-id="c5863-108">Método</span><span class="sxs-lookup"><span data-stu-id="c5863-108">Method</span></span>                                                                         | <span data-ttu-id="c5863-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5863-109">Description</span></span>                                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5863-110">[**ExcludeClip (Rect&)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_))</span><span class="sxs-lookup"><span data-stu-id="c5863-110">[**ExcludeClip(Rect&)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_))</span></span>   | <span data-ttu-id="c5863-111">O método [**Graphics:: ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_)) atualiza a região de recorte para a parte de si mesmo que não faz a interseção do retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="c5863-111">The [**Graphics::ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstrect_)) method updates the clipping region to the portion of itself that does not intersect the specified rectangle.</span></span><br/>  |
| <span data-ttu-id="c5863-112">[**ExcludeClip (RectF&)**](/previous-versions//ms535975(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5863-112">[**ExcludeClip(RectF&)**](/previous-versions//ms535975(v=vs.85))</span></span> | <span data-ttu-id="c5863-113">O método [**Graphics:: ExcludeClip**](/previous-versions//ms535975(v=vs.85)) atualiza a região de recorte para a parte de si mesmo que não faz a interseção do retângulo especificado.</span><span class="sxs-lookup"><span data-stu-id="c5863-113">The [**Graphics::ExcludeClip**](/previous-versions//ms535975(v=vs.85)) method updates the clipping region to the portion of itself that does not intersect the specified rectangle.</span></span><br/> |
| <span data-ttu-id="c5863-114">[**ExcludeClip (região \* )**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion))</span><span class="sxs-lookup"><span data-stu-id="c5863-114">[**ExcludeClip(Region\*)**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion))</span></span>   | <span data-ttu-id="c5863-115">O método [**Graphics:: ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion)) atualiza a região de recorte com a parte de si mesma que não se sobrepõe à região especificada.</span><span class="sxs-lookup"><span data-stu-id="c5863-115">The [**Graphics::ExcludeClip**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-excludeclip(inconstregion)) method updates the clipping region with the portion of itself that does not overlap the specified region.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="c5863-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5863-116">Requirements</span></span>



| <span data-ttu-id="c5863-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5863-117">Requirement</span></span> | <span data-ttu-id="c5863-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c5863-118">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5863-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5863-119">Header</span></span><br/> | <dl> <span data-ttu-id="c5863-120"><dt>Gdiplusgraphics. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5863-120"><dt>Gdiplusgraphics.h</dt></span></span> </dl> |



 

 
