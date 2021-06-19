---
description: O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções. Essas funções simples de API são encapsuladas pela classe GdiplusBase C++.
ms.assetid: b4fcc02c-1b0f-4731-8312-29894b1f722f
title: Funções de memória
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ed10574f9cc88c5b7ca8a2b0ed09924fe8c5192
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395821"
---
# <a name="memory-functions"></a><span data-ttu-id="ba44e-104">Funções de memória</span><span class="sxs-lookup"><span data-stu-id="ba44e-104">Memory Functions</span></span>

<span data-ttu-id="ba44e-105">O Windows GDI+ expõe uma API simples que consiste em cerca de 600 funções, que são implementadas em Gdiplus.dll e declaradas em Gdiplusflat. h.</span><span class="sxs-lookup"><span data-stu-id="ba44e-105">Windows GDI+ exposes a flat API that consists of about 600 functions, which are implemented in Gdiplus.dll and declared in Gdiplusflat.h.</span></span> <span data-ttu-id="ba44e-106">As funções na API Flat do GDI+ são encapsuladas por uma coleção de cerca de 40 classes C++.</span><span class="sxs-lookup"><span data-stu-id="ba44e-106">The functions in the GDI+ flat API are wrapped by a collection of about 40 C++ classes.</span></span> <span data-ttu-id="ba44e-107">É recomendável que você não chame diretamente as funções na API simples.</span><span class="sxs-lookup"><span data-stu-id="ba44e-107">It is recommended that you do not directly call the functions in the flat API.</span></span> <span data-ttu-id="ba44e-108">Sempre que você fizer chamadas para GDI+, deverá fazer isso chamando os métodos e funções fornecidos pelos invólucros do C++.</span><span class="sxs-lookup"><span data-stu-id="ba44e-108">Whenever you make calls to GDI+, you should do so by calling the methods and functions provided by the C++ wrappers.</span></span> <span data-ttu-id="ba44e-109">O Microsoft Product Support Services não fornecerá suporte para código que chama a API simples diretamente.</span><span class="sxs-lookup"><span data-stu-id="ba44e-109">Microsoft Product Support Services will not provide support for code that calls the flat API directly.</span></span> <span data-ttu-id="ba44e-110">Para obter mais informações sobre como usar esses métodos de wrapper, consulte [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span><span class="sxs-lookup"><span data-stu-id="ba44e-110">For more information on using these wrapper methods, see [GDI+ Flat API](-gdiplus-flatapi-flat.md).</span></span>

<span data-ttu-id="ba44e-111">As funções de API simples a seguir são encapsuladas pela classe [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++.</span><span class="sxs-lookup"><span data-stu-id="ba44e-111">The following flat API functions are wrapped by the [**GdiplusBase**](/windows/desktop/api/gdiplusbase/nl-gdiplusbase-gdiplusbase) C++ class.</span></span>

## <a name="memory-functions-and-corresponding-wrapper-methods"></a><span data-ttu-id="ba44e-112">Funções de memória e métodos de wrapper correspondentes</span><span class="sxs-lookup"><span data-stu-id="ba44e-112">Memory Functions and Corresponding Wrapper Methods</span></span>



| <span data-ttu-id="ba44e-113">Função Flat</span><span class="sxs-lookup"><span data-stu-id="ba44e-113">Flat function</span></span>                                          | <span data-ttu-id="ba44e-114">Método de wrapper</span><span class="sxs-lookup"><span data-stu-id="ba44e-114">Wrapper method</span></span>                                                                                                                                      | <span data-ttu-id="ba44e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba44e-115">Remarks</span></span>                                                                                                      |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba44e-116">GpStatus WINGDIPAPI GdipAlloc (tamanho \_ t tamanho)</span><span class="sxs-lookup"><span data-stu-id="ba44e-116">GpStatus WINGDIPAPI GdipAlloc(size\_t size)</span></span><br/> | [<span data-ttu-id="ba44e-117">**GpStatus WINGDIPAPI GdiplusBase void \* (novo operador) (tamanho \_ em \_ tamanho)**</span><span class="sxs-lookup"><span data-stu-id="ba44e-117">**GpStatus WINGDIPAPI GdiplusBase void\* (operator new)(size\_t in\_size)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatornew)<br/>      | <span data-ttu-id="ba44e-118">Aloca memória para um objeto Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="ba44e-118">Allocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="ba44e-119">GdipAlloc é declarado em GdiplusMem. h.</span><span class="sxs-lookup"><span data-stu-id="ba44e-119">GdipAlloc is declared in GdiplusMem.h.</span></span><br/>  |
| <span data-ttu-id="ba44e-120">GpStatus WINGDIPAPI GdipFree (void \* PTR);</span><span class="sxs-lookup"><span data-stu-id="ba44e-120">GpStatus WINGDIPAPI GdipFree(void\* ptr);</span></span><br/>   | [<span data-ttu-id="ba44e-121">**GpStatus WINGDIPAPI GdiplusBase void (operador Delete) (void \* em \_ pVoid)**</span><span class="sxs-lookup"><span data-stu-id="ba44e-121">**GpStatus WINGDIPAPI GdiplusBase void (operator delete)(void\* in\_pVoid)**</span></span>](/windows/win32/api/gdiplusbase/nf-gdiplusbase-gdiplusbase-operatordelete)<br/> | <span data-ttu-id="ba44e-122">Desaloca memória para um objeto Windows GDI+.</span><span class="sxs-lookup"><span data-stu-id="ba44e-122">Deallocates memory for one Windows GDI+ object.</span></span> <br/> <span data-ttu-id="ba44e-123">GdipFree é declarado em GdiplusMem. h.</span><span class="sxs-lookup"><span data-stu-id="ba44e-123">GdipFree is declared in GdiplusMem.h.</span></span><br/> |



 

 

 
