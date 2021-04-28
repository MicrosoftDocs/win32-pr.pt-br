---
title: Códigos de erro em COM
description: Códigos de erro em COM
ms.assetid: ed430863-f416-4611-81b4-0c31d819944a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733cbe0799a22b0f0c01ee9cb226ad7e0b8660da
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103954"
---
# <a name="error-codes-in-com"></a><span data-ttu-id="88fa4-103">Códigos de erro em COM</span><span class="sxs-lookup"><span data-stu-id="88fa4-103">Error Codes in COM</span></span>

<span data-ttu-id="88fa4-104">Para indicar êxito ou falha, métodos COM e funções retornam um valor do tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="88fa4-104">To indicate success or failure, COM methods and functions return a value of type **HRESULT**.</span></span> <span data-ttu-id="88fa4-105">Um **HRESULT** é um inteiro de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="88fa4-105">An **HRESULT** is a 32-bit integer.</span></span> <span data-ttu-id="88fa4-106">O bit de ordem superior do **HRESULT** sinaliza êxito ou falha.</span><span class="sxs-lookup"><span data-stu-id="88fa4-106">The high-order bit of the **HRESULT** signals success or failure.</span></span> <span data-ttu-id="88fa4-107">Zero (0) indica êxito e 1 indica falha.</span><span class="sxs-lookup"><span data-stu-id="88fa4-107">Zero (0) indicates success and 1 indicates failure.</span></span>

<span data-ttu-id="88fa4-108">Isso produz os seguintes intervalos numéricos:</span><span class="sxs-lookup"><span data-stu-id="88fa4-108">This produces the following numeric ranges:</span></span>

-   <span data-ttu-id="88fa4-109">Códigos de êxito: 0x0 – 0x7FFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="88fa4-109">Success codes: 0x0–0x7FFFFFFF.</span></span>
-   <span data-ttu-id="88fa4-110">Códigos de erro: 0x80000000 – 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="88fa4-110">Error codes: 0x80000000–0xFFFFFFFF.</span></span>

<span data-ttu-id="88fa4-111">Um pequeno número de métodos COM não retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88fa4-111">A small number of COM methods do not return an **HRESULT** value.</span></span> <span data-ttu-id="88fa4-112">Por exemplo, os métodos [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) e [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) retornam valores longos não assinados.</span><span class="sxs-lookup"><span data-stu-id="88fa4-112">For example, the [**AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) and [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) methods return unsigned long values.</span></span> <span data-ttu-id="88fa4-113">Mas cada método COM que retorna um código de erro faz isso retornando um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="88fa4-113">But every COM method that returns an error code does so by returning an **HRESULT** value.</span></span>

<span data-ttu-id="88fa4-114">Para verificar se um método COM é executado COM sucesso, examine o bit de ordem superior do **HRESULT** retornado.</span><span class="sxs-lookup"><span data-stu-id="88fa4-114">To check whether a COM method succeeds, examine the high-order bit of the returned **HRESULT**.</span></span> <span data-ttu-id="88fa4-115">Os cabeçalhos de SDK do Windows fornecem duas macros que tornam isso mais fácil: a macro com [**êxito**](/windows/desktop/api/winerror/nf-winerror-succeeded) e a macro [**com falha**](/windows/desktop/api/winerror/nf-winerror-failed) .</span><span class="sxs-lookup"><span data-stu-id="88fa4-115">The Windows SDK headers provide two macros that make this easier: the [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) macro and the [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro.</span></span> <span data-ttu-id="88fa4-116">A macro **Succeeded** retornará **true** se um **HRESULT** for um código de êxito e **false** se for um código de erro.</span><span class="sxs-lookup"><span data-stu-id="88fa4-116">The **SUCCEEDED** macro returns **TRUE** if an **HRESULT** is a success code and **FALSE** if it is an error code.</span></span> <span data-ttu-id="88fa4-117">O exemplo a seguir verifica se [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) tem sucesso.</span><span class="sxs-lookup"><span data-stu-id="88fa4-117">The following example checks whether [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) succeeds.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (SUCCEEDED(hr))
{
    // The function succeeded.
}
else
{
    // Handle the error.
}
```



<span data-ttu-id="88fa4-118">Às vezes, é mais conveniente testar a condição inversa.</span><span class="sxs-lookup"><span data-stu-id="88fa4-118">Sometimes it is more convenient to test the inverse condition.</span></span> <span data-ttu-id="88fa4-119">A macro [**com falha**](/windows/desktop/api/winerror/nf-winerror-failed) faz o oposto do [**êxito**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span><span class="sxs-lookup"><span data-stu-id="88fa4-119">The [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) macro does the opposite of [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded).</span></span> <span data-ttu-id="88fa4-120">Retorna **true** para um código de erro e **false** para um código de êxito.</span><span class="sxs-lookup"><span data-stu-id="88fa4-120">It returns **TRUE** for an error code and **FALSE** for a success code.</span></span>


```C++
HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | 
    COINIT_DISABLE_OLE1DDE);

if (FAILED(hr))
{
    // Handle the error.
}
else
{
    // The function succeeded.
}
```



<span data-ttu-id="88fa4-121">Mais adiante neste módulo, veremos alguns conselhos práticos sobre como estruturar seu código para manipular erros COM.</span><span class="sxs-lookup"><span data-stu-id="88fa4-121">Later in this module, we will look at some practical advice for how to structure your code to handle COM errors.</span></span> <span data-ttu-id="88fa4-122">(Consulte [tratamento de erros no com](error-handling-in-com.md).)</span><span class="sxs-lookup"><span data-stu-id="88fa4-122">(See [Error Handling in COM](error-handling-in-com.md).)</span></span>

## <a name="next"></a><span data-ttu-id="88fa4-123">Avançar</span><span class="sxs-lookup"><span data-stu-id="88fa4-123">Next</span></span>

[<span data-ttu-id="88fa4-124">Criando um objeto em COM</span><span class="sxs-lookup"><span data-stu-id="88fa4-124">Creating an Object in COM</span></span>](creating-an-object-in-com.md)

 

 
