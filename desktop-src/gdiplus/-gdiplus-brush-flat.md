---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Funções de pincel (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7490cc641312014987b2fb847979de640c28c47e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296670"
---
# <a name="brush-functions-gdi"></a><span data-ttu-id="7cd2e-103">Funções de pincel (GDI+)</span><span class="sxs-lookup"><span data-stu-id="7cd2e-103">Brush Functions (GDI+)</span></span>

<span data-ttu-id="7cd2e-104">O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="7cd2e-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="7cd2e-105">As funções na API Flat do GDI+ são encapsuladas por uma coleção de cerca de 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="7cd2e-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="7cd2e-106">É recomendável que você não chame diretamente as funções na API simples.</span><span class="sxs-lookup"><span data-stu-id="7cd2e-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="7cd2e-107">Sempre que você fizer chamadas para GDI+, deverá fazer isso chamando os métodos e funções fornecidos pelos invólucros do C++.</span><span class="sxs-lookup"><span data-stu-id="7cd2e-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="7cd2e-108">O Microsoft Product Support Services não fornecerá suporte para código que chama a API simples diretamente.</span><span class="sxs-lookup"><span data-stu-id="7cd2e-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="7cd2e-109">Para obter mais informações sobre como usar esses métodos de wrapper, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="7cd2e-109">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="7cd2e-110">As seguintes funções simples de API são encapsuladas pela classe [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++.</span><span class="sxs-lookup"><span data-stu-id="7cd2e-110">The following flat API functions are wrapped by the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="7cd2e-111">Funções de pincel e métodos wrapper correspondentes</span><span class="sxs-lookup"><span data-stu-id="7cd2e-111">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="7cd2e-112">Função Flat</span><span class="sxs-lookup"><span data-stu-id="7cd2e-112">Flat function</span></span>                                                                        | <span data-ttu-id="7cd2e-113">Método de wrapper</span><span class="sxs-lookup"><span data-stu-id="7cd2e-113">Wrapper method</span></span>                                          | <span data-ttu-id="7cd2e-114">Description</span><span class="sxs-lookup"><span data-stu-id="7cd2e-114">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cd2e-115">GpStatus WINGDIPAPI GdipCloneBrush (GpBrush \* Brush, GpBrush \* \* cloneBrush)</span><span class="sxs-lookup"><span data-stu-id="7cd2e-115">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \*brush, GpBrush \*\*cloneBrush)</span></span>          | [<span data-ttu-id="7cd2e-116">**Pincel:: clone**</span><span class="sxs-lookup"><span data-stu-id="7cd2e-116">**Brush::Clone**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | <span data-ttu-id="7cd2e-117">O método [**Brush:: clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) cria um novo objeto de [**pincel**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) com base neste pincel.</span><span class="sxs-lookup"><span data-stu-id="7cd2e-117">The [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) method creates a new [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object based on this brush.</span></span> |
| <span data-ttu-id="7cd2e-118">GpStatus WINGDIPAPI GdipDeleteBrush (GpBrush \* Brush)</span><span class="sxs-lookup"><span data-stu-id="7cd2e-118">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush \*brush)</span></span>                                 | <span data-ttu-id="7cd2e-119">virtual ~ Brush ()</span><span class="sxs-lookup"><span data-stu-id="7cd2e-119">virtual ~Brush()</span></span>                                        | <span data-ttu-id="7cd2e-120">Limpa os recursos usados por um objeto de [**pincel**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) .</span><span class="sxs-lookup"><span data-stu-id="7cd2e-120">Cleans up resources used by a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span>                                                                    |
| <span data-ttu-id="7cd2e-121">GpStatus WINGDIPAPI GdipGetBrushType (GpBrush \* pincel, \* tipo GpBrushType)</span><span class="sxs-lookup"><span data-stu-id="7cd2e-121">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush \*brush, GpBrushType \*type)</span></span><br/> | [<span data-ttu-id="7cd2e-122">**Pincel:: GetType**</span><span class="sxs-lookup"><span data-stu-id="7cd2e-122">**Brush::GetType**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | <span data-ttu-id="7cd2e-123">O método [**Brush:: GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) Obtém o tipo desse pincel.</span><span class="sxs-lookup"><span data-stu-id="7cd2e-123">The [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) method gets the type of this brush.</span></span>                                                      |



 

 

 




