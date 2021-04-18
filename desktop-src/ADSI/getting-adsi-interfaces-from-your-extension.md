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
# <a name="getting-adsi-interfaces-from-your-extension"></a>Obtendo interfaces ADSI de sua extensão

Uma extensão geralmente precisa obter dados do objeto de diretório ao qual ele se vincula. Por exemplo, uma extensão para um objeto de **computador** pode querer obter o **dNSHostName** do objeto atual do diretório. Isso pode ser facilmente obtido com a emissão de uma chamada de **QueryInterface** na interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) para o agregador.


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



Você deve liberar a interface imediatamente após usá-la. Se a extensão tiver uma referência aberta ao agregador, você terá criado uma referência circular e o agregador não poderá liberar a extensão. Portanto, o agregador não pode ser liberado e o resultado é vazamentos de memória em seu aplicativo.

 

 