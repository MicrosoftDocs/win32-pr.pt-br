---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Funções de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86e748f8a68cc6f04deba3c9676638ee48ee2e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967759"
---
# <a name="memory-functions"></a><span data-ttu-id="83d78-103">Funções de memória</span><span class="sxs-lookup"><span data-stu-id="83d78-103">Memory Functions</span></span>

<span data-ttu-id="83d78-104">O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="83d78-104">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="83d78-105">As funções na API Flat do GDI+ são encapsuladas por uma coleção de cerca de 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="83d78-105">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="83d78-106">É recomendável que você não chame diretamente as funções na API simples.</span><span class="sxs-lookup"><span data-stu-id="83d78-106">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="83d78-107">Sempre que você fizer chamadas para GDI+, deverá fazer isso chamando os métodos e funções fornecidos pelos invólucros do C++.</span><span class="sxs-lookup"><span data-stu-id="83d78-107">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="83d78-108">O Microsoft Product Support Services não fornecerá suporte para código que chama a API simples diretamente.</span><span class="sxs-lookup"><span data-stu-id="83d78-108">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="83d78-109">Para obter mais informações sobre como usar esses métodos de wrapper, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="83d78-109">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="83d78-110">As funções de API simples a seguir são encapsuladas pela classe [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++.</span><span class="sxs-lookup"><span data-stu-id="83d78-110">The following flat API functions are wrapped by the [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++ class.</span></span>

## <a name="memory-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="83d78-111">Funções de memória e métodos de wrapper correspondentes</span><span class="sxs-lookup"><span data-stu-id="83d78-111">Memory Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="83d78-112">Função Flat</span><span class="sxs-lookup"><span data-stu-id="83d78-112">Flat function</span></span>                                          | <span data-ttu-id="83d78-113">Método de wrapper</span><span class="sxs-lookup"><span data-stu-id="83d78-113">Wrapper method</span></span>                                                                                                                                      | <span data-ttu-id="83d78-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="83d78-114">Remarks</span></span>                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83d78-115">GpStatus WINGDIPAPI GdipAlloc (tamanho \_ t tamanho)</span><span class="sxs-lookup"><span data-stu-id="83d78-115">GpStatus WINGDIPAPI GdipAlloc(size\_t size)</span></span><br/> | [<span data-ttu-id="83d78-116">**GpStatus WINGDIPAPI GdiplusBase void \* (novo operador) (tamanho \_ em \_ tamanho)**</span><span class="sxs-lookup"><span data-stu-id="83d78-116">**GpStatus WINGDIPAPI GdiplusBase void\* (operator new)(size\_t in\_size)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | <span data-ttu-id="83d78-117">Aloca memória para um objeto Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="83d78-117">Allocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="83d78-118">GdipAlloc é declarado em GdiplusMem. h.</span><span class="sxs-lookup"><span data-stu-id="83d78-118">GdipAlloc is declared in GdiplusMem.h.</span></span><br/>  |
| <span data-ttu-id="83d78-119">GpStatus WINGDIPAPI GdipFree (void \* PTR);</span><span class="sxs-lookup"><span data-stu-id="83d78-119">GpStatus WINGDIPAPI GdipFree(void\* ptr);</span></span><br/>   | [<span data-ttu-id="83d78-120">**GpStatus WINGDIPAPI GdiplusBase void (operador Delete) (void \* em \_ pVoid)**</span><span class="sxs-lookup"><span data-stu-id="83d78-120">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void\* in\_pVoid)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | <span data-ttu-id="83d78-121">Desaloca memória para um objeto Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="83d78-121">Deallocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="83d78-122">GdipFree é declarado em GdiplusMem. h.</span><span class="sxs-lookup"><span data-stu-id="83d78-122">GdipFree is declared in GdiplusMem.h.</span></span><br/> |



 

 

 
