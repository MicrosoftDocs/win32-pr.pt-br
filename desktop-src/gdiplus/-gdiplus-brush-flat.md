---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. Essas funções de API simples são empacotadas pela classe Brush C++.
ms.assetid: def64d31-9a4b-4365-a618-b87735ce38f1
title: Funções brush (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffe23588c44d8a3a6412cd0c2bc1327b98bbbd95
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395081"
---
# <a name="brush-functions-gdi"></a><span data-ttu-id="f8545-104">Funções brush (GDI+)</span><span class="sxs-lookup"><span data-stu-id="f8545-104">Brush Functions (GDI+)</span></span>

<span data-ttu-id="f8545-105">O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas no Gdiplus.dll e declaradas em Gdiplusflat.h.</span><span class="sxs-lookup"><span data-stu-id="f8545-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="f8545-106">As funções na API simples GDI+ são envolvidas por uma coleção de cerca de 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="f8545-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="f8545-107">É recomendável que você não chame diretamente as funções na API simples.</span><span class="sxs-lookup"><span data-stu-id="f8545-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="f8545-108">Sempre que fizer chamadas ao GDI+, você deverá fazer isso chamando os métodos e funções fornecidos pelos wrappers do C++.</span><span class="sxs-lookup"><span data-stu-id="f8545-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="f8545-109">Os Serviços de Suporte a Produtos da Microsoft não fornecerão suporte para o código que chama a API simples diretamente.</span><span class="sxs-lookup"><span data-stu-id="f8545-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="f8545-110">Para obter mais informações sobre como usar esses métodos de wrapper, consulte [API simples GDI+.](-gdiplus-flatapi-flat.md)</span><span class="sxs-lookup"><span data-stu-id="f8545-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="f8545-111">As funções de API simples a seguir são empacotadas pela [**classe Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++.</span><span class="sxs-lookup"><span data-stu-id="f8545-111">The following flat API functions are wrapped by the [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) C++ class.</span></span>

## <a name="brush-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="f8545-112">Funções de pincel e métodos de wrapper correspondentes</span><span class="sxs-lookup"><span data-stu-id="f8545-112">Brush Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="f8545-113">Função simples</span><span class="sxs-lookup"><span data-stu-id="f8545-113">Flat function</span></span>                                                                        | <span data-ttu-id="f8545-114">Método Wrapper</span><span class="sxs-lookup"><span data-stu-id="f8545-114">Wrapper method</span></span>                                          | <span data-ttu-id="f8545-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="f8545-115">Description</span></span>                                                                                                                                          |
|--------------------------------------------------------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8545-116">GpStatus WINGDIPAPI GdipCloneBrush(pincel GpBrush, \* \* \* cloneBrushBrush)</span><span class="sxs-lookup"><span data-stu-id="f8545-116">GpStatus WINGDIPAPI GdipCloneBrush(GpBrush \*brush, GpBrush \*\*cloneBrush)</span></span>          | [<span data-ttu-id="f8545-117">**Brush::Clone**</span><span class="sxs-lookup"><span data-stu-id="f8545-117">**Brush::Clone**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone)     | <span data-ttu-id="f8545-118">O [**método Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) cria um novo [**objeto Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) com base nesse pincel.</span><span class="sxs-lookup"><span data-stu-id="f8545-118">The [**Brush::Clone**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-clone) method creates a new [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object based on this brush.</span></span> |
| <span data-ttu-id="f8545-119">GpStatus WINGDIPAPI GdipDeleteBrush(pincel \* GpBrush)</span><span class="sxs-lookup"><span data-stu-id="f8545-119">GpStatus WINGDIPAPI GdipDeleteBrush(GpBrush \*brush)</span></span>                                 | <span data-ttu-id="f8545-120">virtual ~Brush()</span><span class="sxs-lookup"><span data-stu-id="f8545-120">virtual ~Brush()</span></span>                                        | <span data-ttu-id="f8545-121">Limpa os recursos usados por um [**objeto Brush.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush)</span><span class="sxs-lookup"><span data-stu-id="f8545-121">Cleans up resources used by a [**Brush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush) object.</span></span>                                                                    |
| <span data-ttu-id="f8545-122">GpStatus WINGDIPAPI GdipGetBrushType(pincel GpBrush, \* tipo GpBrushType) \*</span><span class="sxs-lookup"><span data-stu-id="f8545-122">GpStatus WINGDIPAPI GdipGetBrushType(GpBrush \*brush, GpBrushType \*type)</span></span><br/> | [<span data-ttu-id="f8545-123">**Brush::GetType**</span><span class="sxs-lookup"><span data-stu-id="f8545-123">**Brush::GetType**</span></span>](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) | <span data-ttu-id="f8545-124">O [**método Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) obtém o tipo desse pincel.</span><span class="sxs-lookup"><span data-stu-id="f8545-124">The [**Brush::GetType**](/windows/desktop/api/Gdiplusbrush/nf-gdiplusbrush-brush-gettype) method gets the type of this brush.</span></span>                                                      |



 

 

 




