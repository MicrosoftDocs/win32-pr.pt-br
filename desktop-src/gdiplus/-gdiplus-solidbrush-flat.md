---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Funções SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc7d75e99f46877ce990a985e47bc4b9021faaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967399"
---
# <a name="solidbrush-functions"></a><span data-ttu-id="5d819-103">Funções SolidBrush</span><span class="sxs-lookup"><span data-stu-id="5d819-103">SolidBrush Functions</span></span>

<span data-ttu-id="5d819-104">O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="5d819-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="5d819-105">As funções na API Flat do GDI+ são encapsuladas por uma coleção de cerca de 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="5d819-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="5d819-106">Recomendamos não chamar as funções na API simples diretamente.</span><span class="sxs-lookup"><span data-stu-id="5d819-106">We recommend not to call the functions in the flat API directly.</span></span> <span data-ttu-id="5d819-107">Sempre que você fizer chamadas para GDI+, recomendamos que faça isso chamando os métodos e funções fornecidos pelos invólucros do C++.</span><span class="sxs-lookup"><span data-stu-id="5d819-107">Whenever you make calls to GDI+, we recommend that you do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="5d819-108">O Microsoft Product Support Services não fornecerá suporte para código que chama a API simples diretamente.</span><span class="sxs-lookup"><span data-stu-id="5d819-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="5d819-109">Para obter mais informações sobre como usar esses métodos de wrapper, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="5d819-109">For more info on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="5d819-110">As funções de API simples a seguir são encapsuladas pela classe [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++.</span><span class="sxs-lookup"><span data-stu-id="5d819-110">The following flat API functions are wrapped by the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="5d819-111">Funções de pincel e métodos wrapper correspondentes</span><span class="sxs-lookup"><span data-stu-id="5d819-111">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="5d819-112">Função Flat</span><span class="sxs-lookup"><span data-stu-id="5d819-112">Flat function</span></span>                                                                               | <span data-ttu-id="5d819-113">Método de wrapper</span><span class="sxs-lookup"><span data-stu-id="5d819-113">Wrapper method</span></span>                                                                                       | <span data-ttu-id="5d819-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5d819-114">Remarks</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d819-115">**GpStatus WINGDIPAPI GdipCreateSolidFill (cor ARGB, pincel de GpSolidFill \* \* )**</span><span class="sxs-lookup"><span data-stu-id="5d819-115">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \*\*brush)**</span></span><br/>   | <span data-ttu-id="5d819-116">[**SolidBrush:: SolidBrush (IN const Color& Color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span><span class="sxs-lookup"><span data-stu-id="5d819-116">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span></span> | <span data-ttu-id="5d819-117">Cria um objeto [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) com base em uma cor</span><span class="sxs-lookup"><span data-stu-id="5d819-117">Creates a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object based on a color</span></span> |
| <span data-ttu-id="5d819-118">**GpStatus WINGDIPAPI GdipSetSolidFillColor (GpSolidFill \* Brush, cor ARGB)**</span><span class="sxs-lookup"><span data-stu-id="5d819-118">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \*brush, ARGB color)**</span></span><br/>   | [<span data-ttu-id="5d819-119">**SolidBrush:: setColor (na cor const& cor)**</span><span class="sxs-lookup"><span data-stu-id="5d819-119">**SolidBrush::SetColor(IN const Color& color)**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | <span data-ttu-id="5d819-120">Define a cor deste pincel sólido</span><span class="sxs-lookup"><span data-stu-id="5d819-120">Sets the color of this solid brush</span></span>                                                      |
| <span data-ttu-id="5d819-121">**GpStatus WINGDIPAPI GdipGetSolidFillColor (GpSolidFill \* Brush, \* cor ARGB)**</span><span class="sxs-lookup"><span data-stu-id="5d819-121">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \*brush, ARGB \*color)**</span></span><br/> | [<span data-ttu-id="5d819-122">**Const SolidBrush:: GetColor (fora da cor da cor \* )**</span><span class="sxs-lookup"><span data-stu-id="5d819-122">**SolidBrush::GetColor(OUT Color\* color) const**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | <span data-ttu-id="5d819-123">Obtém a cor deste pincel sólido</span><span class="sxs-lookup"><span data-stu-id="5d819-123">Gets the color of this solid brush</span></span>                                                      |



 

 

 
