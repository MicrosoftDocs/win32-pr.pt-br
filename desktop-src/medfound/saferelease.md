---
description: SafeRelease
ms.assetid: 2e9af7bc-f478-4a9c-b28f-b0a72fa9ec75
title: SafeRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd0661b8515c1d8a79c81eef19f49cf8996fcbf3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790361"
---
# <a name="saferelease"></a><span data-ttu-id="08d75-103">SafeRelease</span><span class="sxs-lookup"><span data-stu-id="08d75-103">SafeRelease</span></span>


<span data-ttu-id="08d75-104">Muitos dos exemplos de código nesta documentação usam a função a seguir para liberar ponteiros de interface COM.</span><span class="sxs-lookup"><span data-stu-id="08d75-104">Many of the code examples in this documentation use the following function to release COM interface pointers.</span></span>


```C++
template <class T> void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}
```



> [!Note]  
> <span data-ttu-id="08d75-105">Essa função não está definida em um cabeçalho do SDK.</span><span class="sxs-lookup"><span data-stu-id="08d75-105">This function is not defined in an SDK header.</span></span> <span data-ttu-id="08d75-106">Para usar essa função, você deve defini-la em seu próprio código.</span><span class="sxs-lookup"><span data-stu-id="08d75-106">To use this function, you must define it in your own code.</span></span>

 

<span data-ttu-id="08d75-107">Essa função libera o ponteiro *ppt* e o define como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="08d75-107">This function releases the pointer *ppT* and sets it equal to **NULL**.</span></span>

<span data-ttu-id="08d75-108">Outra opção é usar uma classe de ponteiro inteligente, como **CComPtr**, que é definida no Active Template Library (ATL).</span><span class="sxs-lookup"><span data-stu-id="08d75-108">Another option is to use a smart pointer class, such as **CComPtr**, which is defined in the Active Template Library (ATL).</span></span>

## <a name="related-topics"></a><span data-ttu-id="08d75-109">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="08d75-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08d75-110">Sobre o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="08d75-110">About Media Foundation</span></span>](about-the-media-foundation-sdk.md)
</dt> <dt>

[<span data-ttu-id="08d75-111">**IUnknown:: versão**</span><span class="sxs-lookup"><span data-stu-id="08d75-111">**IUnknown::Release**</span></span>](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)
</dt> </dl>

 

 
