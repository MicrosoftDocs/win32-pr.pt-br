---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. Essas funções de API simples são empacotadas pela classe C++ SolidBrush.
ms.assetid: b427b8ab-66fd-4f57-b08e-5f337a9ac9af
title: Funções SolidBrush
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc9feb2676c60b3f504315f75303aadb16a1cd1f
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395551"
---
# <a name="solidbrush-functions"></a><span data-ttu-id="d8daf-104">Funções SolidBrush</span><span class="sxs-lookup"><span data-stu-id="d8daf-104">SolidBrush Functions</span></span>

<span data-ttu-id="d8daf-105">O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas no Gdiplus.dll e declaradas em Gdiplusflat.h.</span><span class="sxs-lookup"><span data-stu-id="d8daf-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="d8daf-106">As funções na API simples GDI+ são envolvidas por uma coleção de cerca de 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="d8daf-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="d8daf-107">É recomendável não chamar as funções na API simples diretamente.</span><span class="sxs-lookup"><span data-stu-id="d8daf-107">We recommend not to call the functions in the flat API directly.</span></span> <span data-ttu-id="d8daf-108">Sempre que você fizer chamadas para GDI+, recomendamos que você faça isso chamando os métodos e funções fornecidos pelos wrappers do C++.</span><span class="sxs-lookup"><span data-stu-id="d8daf-108">Whenever you make calls to GDI+, we recommend that you do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="d8daf-109">Os Serviços de Suporte a Produtos da Microsoft não fornecerão suporte para o código que chama a API simples diretamente.</span><span class="sxs-lookup"><span data-stu-id="d8daf-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="d8daf-110">Para obter mais informações sobre como usar esses métodos de wrapper, consulte [API simples GDI+.](-gdiplus-flatapi-flat.md)</span><span class="sxs-lookup"><span data-stu-id="d8daf-110">For more info on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="d8daf-111">As funções de API simples a seguir são empacotadas pela [**classe C++ SolidBrush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush)</span><span class="sxs-lookup"><span data-stu-id="d8daf-111">The following flat API functions are wrapped by the [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="d8daf-112">Funções de pincel e métodos de wrapper correspondentes</span><span class="sxs-lookup"><span data-stu-id="d8daf-112">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="d8daf-113">Função simples</span><span class="sxs-lookup"><span data-stu-id="d8daf-113">Flat function</span></span>                                                                               | <span data-ttu-id="d8daf-114">Método Wrapper</span><span class="sxs-lookup"><span data-stu-id="d8daf-114">Wrapper method</span></span>                                                                                       | <span data-ttu-id="d8daf-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8daf-115">Remarks</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d8daf-116">**GpStatus WINGDIPAPI GdipCreateSolidFill(cor ARGB, pincel \* \* GpSolidFill)**</span><span class="sxs-lookup"><span data-stu-id="d8daf-116">**GpStatus WINGDIPAPI GdipCreateSolidFill(ARGB color, GpSolidFill \*\*brush)**</span></span><br/>   | <span data-ttu-id="d8daf-117">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span><span class="sxs-lookup"><span data-stu-id="d8daf-117">[**SolidBrush::SolidBrush(IN const Color& color)**](/windows/win32/api/gdiplusbrush/nf-gdiplusbrush-solidbrush-solidbrush(constsolidbrush_))</span></span> | <span data-ttu-id="d8daf-118">Cria um [**objeto SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) com base em uma cor</span><span class="sxs-lookup"><span data-stu-id="d8daf-118">Creates a [**SolidBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush) object based on a color</span></span> |
| <span data-ttu-id="d8daf-119">**GpStatus WINGDIPAPI GdipSetSolidFillColor(pincel GpSolidFill, \* cor ARGB)**</span><span class="sxs-lookup"><span data-stu-id="d8daf-119">**GpStatus WINGDIPAPI GdipSetSolidFillColor(GpSolidFill \*brush, ARGB color)**</span></span><br/>   | [<span data-ttu-id="d8daf-120">**SolidBrush::SetColor(IN const Color& color)**</span><span class="sxs-lookup"><span data-stu-id="d8daf-120">**SolidBrush::SetColor(IN const Color& color)**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-setcolor)     | <span data-ttu-id="d8daf-121">Define a cor desse pincel sólido</span><span class="sxs-lookup"><span data-stu-id="d8daf-121">Sets the color of this solid brush</span></span>                                                      |
| <span data-ttu-id="d8daf-122">**GpStatus WINGDIPAPI GdipGetSolidFillColor(pincel GpSolidFill, \* cor \* ARGB)**</span><span class="sxs-lookup"><span data-stu-id="d8daf-122">**GpStatus WINGDIPAPI GdipGetSolidFillColor(GpSolidFill \*brush, ARGB \*color)**</span></span><br/> | [<span data-ttu-id="d8daf-123">**SolidBrush::GetColor(OUT Color \* color) const**</span><span class="sxs-lookup"><span data-stu-id="d8daf-123">**SolidBrush::GetColor(OUT Color\* color) const**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-solidbrush-getcolor)   | <span data-ttu-id="d8daf-124">Obtém a cor desse pincel sólido</span><span class="sxs-lookup"><span data-stu-id="d8daf-124">Gets the color of this solid brush</span></span>                                                      |



 

 

 
