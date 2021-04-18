---
title: Obtendo interfaces ADSI de sua extensão
description: Uma extensão geralmente precisa obter dados do objeto de diretório ao qual ele se vincula.
ms.assetid: 2d2e6dc6-1eed-491b-9d6a-7f35c24a7ba8
ms.tgt_platform: multiple
keywords:
- ADSI de extensões, obtendo interfaces ADSI de sua extensão
- ADSI ADSI, código de exemplo C/C++, obtendo interfaces ADSI de sua extensão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1eeff55f2e382ce2816f59ee53dbd78033b79c
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "105755489"
---
# <a name="getting-adsi-interfaces-from-your-extension"></a><span data-ttu-id="a9a14-105">Obtendo interfaces ADSI de sua extensão</span><span class="sxs-lookup"><span data-stu-id="a9a14-105">Getting ADSI Interfaces From Your Extension</span></span>

<span data-ttu-id="a9a14-106">Uma extensão geralmente precisa obter dados do objeto de diretório ao qual ele se vincula.</span><span class="sxs-lookup"><span data-stu-id="a9a14-106">An extension often needs to get data from the directory object it binds to.</span></span> <span data-ttu-id="a9a14-107">Por exemplo, uma extensão para um objeto de **computador** pode querer obter o **dNSHostName** do objeto atual do diretório.</span><span class="sxs-lookup"><span data-stu-id="a9a14-107">For example, an extension for a **computer** object may want to get the **dnsHostName** of the current object from the directory.</span></span> <span data-ttu-id="a9a14-108">Isso pode ser facilmente obtido com a emissão de uma chamada de **QueryInterface** na interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para o agregador.</span><span class="sxs-lookup"><span data-stu-id="a9a14-108">This can be easily achieved by issuing a **QueryInterface** call on the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface for the aggregator.</span></span>


```C++
HRESULT hr;
IADs *pADs; ' ADSI Interface to get/set attributes.
 
hr = m_pOuterUnk->QueryInterface(IID_IADs,(void**)&pADs);
 
if ( SUCCEEDED(hr) )
{
    VARIANT var;
    VariantInit(&var);
    hr  = pADs ->Get(_bstr_t("dnsHostName"), &var);
    if ( SUCCEEDED(hr) )
    { 
        printf("%S\n", V_BSTR(&var));
    }
    VariantClear(&var);
    pADs->Release();
}
```



<span data-ttu-id="a9a14-109">Você deve liberar a interface imediatamente após usá-la.</span><span class="sxs-lookup"><span data-stu-id="a9a14-109">You should release the interface immediately after using it.</span></span> <span data-ttu-id="a9a14-110">Se a extensão tiver uma referência aberta ao agregador, você terá criado uma referência circular e o agregador não poderá liberar a extensão.</span><span class="sxs-lookup"><span data-stu-id="a9a14-110">If the extension has an open reference to the aggregator, you have created a circular reference and the aggregator cannot release the extension.</span></span> <span data-ttu-id="a9a14-111">Portanto, o agregador não pode ser liberado e o resultado é vazamentos de memória em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a9a14-111">Therefore, the aggregator cannot be released and the result is memory leaks in your application.</span></span>

 

 