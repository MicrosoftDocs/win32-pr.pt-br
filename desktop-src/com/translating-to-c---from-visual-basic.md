---
title: Convertendo para C++ de Visual Basic
description: Visual Basic manipula ponteiros implicitamente. Em C++, seu aplicativo é responsável por executar qualquer aritmética de ponteiro necessária.
ms.assetid: bbbcaba1-cf5a-4768-ad1d-22a040bfe384
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53de112f19b51be92657fb3293bb35e1d41ff9b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159771"
---
# <a name="translating-to-c-from-visual-basic"></a><span data-ttu-id="5b920-104">Convertendo para C++ de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="5b920-104">Translating to C++ from Visual Basic</span></span>

<span data-ttu-id="5b920-105">Visual Basic manipula ponteiros implicitamente.</span><span class="sxs-lookup"><span data-stu-id="5b920-105">Visual Basic handles pointers implicitly.</span></span> <span data-ttu-id="5b920-106">Em C++, seu aplicativo é responsável por executar qualquer aritmética de ponteiro necessária.</span><span class="sxs-lookup"><span data-stu-id="5b920-106">In C++, your application is responsible for performing any necessary pointer arithmetic.</span></span>

<span data-ttu-id="5b920-107">Por padrão, Visual Basic passa parâmetros por referência (como ponteiros).</span><span class="sxs-lookup"><span data-stu-id="5b920-107">By default, Visual Basic passes parameters by reference (as pointers).</span></span> <span data-ttu-id="5b920-108">Parâmetros que devem ser passados pelo valor somente são especificados pela palavra-chave **ByVal**.</span><span class="sxs-lookup"><span data-stu-id="5b920-108">Parameters that are meant to be passed by value only are specified by the keyword **ByVal**.</span></span> <span data-ttu-id="5b920-109">Por exemplo, um parâmetro  **inteiro** **ByVal** Â em Visual Basic é equivalente a um parâmetro **curto** em C++, enquanto um parâmetro de  **inteiro** **ByRef** em Visual Basic é equivalente a um **parâmetro \* curto** .</span><span class="sxs-lookup"><span data-stu-id="5b920-109">For example, a **ByVal** Â  **Integer** parameter in Visual Basic is equivalent to a **short** parameter in C++, whereas a **ByRef** Â  **Integer** parameter in Visual Basic is equivalent to a **short\*** parameter.</span></span>

<span data-ttu-id="5b920-110">Um parâmetro declarado **como cadeia de caracteres** em Visual Basic é declarado como um ponteiro para um **BSTR** em C++.</span><span class="sxs-lookup"><span data-stu-id="5b920-110">A parameter that is declared **As String** in Visual Basic is declared as a pointer to a **BSTR** in C++.</span></span> <span data-ttu-id="5b920-111">Definir um ponteiro de cadeia de caracteres como **nulo** em C++ é equivalente a definir a cadeia de caracteres para a constante **vbNullString** em Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="5b920-111">Setting a string pointer to **NULL** in C++ is equivalent to setting the string to the **vbNullString** constant in Visual Basic.</span></span> <span data-ttu-id="5b920-112">A passagem de uma cadeia de caracteres de comprimento zero ("") para uma função criada para receber **NULL** não funciona, porque isso passa um ponteiro para uma cadeia de caracteres de comprimento zero em vez de um ponteiro de zero.</span><span class="sxs-lookup"><span data-stu-id="5b920-112">Passing a zero-length string ("") to a function designed to receive **NULL** does not work, because this passes a pointer to a zero-length string instead of a zero pointer.</span></span>

<span data-ttu-id="5b920-113">C++ e Visual Basic diferem ligeiramente na forma como representam propriedades.</span><span class="sxs-lookup"><span data-stu-id="5b920-113">C++ and Visual Basic differ slightly in how they represent properties.</span></span> <span data-ttu-id="5b920-114">No C++, as propriedades são representadas como um conjunto de funções de acessador, uma que define o valor da propriedade e outra que recupera o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="5b920-114">In C++, properties are represented as a set of accessor functions, one that sets the property value and one that retrieves the property value.</span></span> <span data-ttu-id="5b920-115">Em Visual Basic, as propriedades são representadas como um único item que pode ser usado para recuperar ou definir o valor da propriedade.</span><span class="sxs-lookup"><span data-stu-id="5b920-115">In Visual Basic, properties are represented as a single item that can be used to retrieve or set the property value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5b920-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b920-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b920-117">Convertendo para C++</span><span class="sxs-lookup"><span data-stu-id="5b920-117">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 




