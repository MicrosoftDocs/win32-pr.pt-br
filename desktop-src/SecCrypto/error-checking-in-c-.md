---
description: Em C++, cada método de serviços de certificados retorna diretamente um valor HRESULT que indica se a chamada de método foi bem-sucedida ou falhou. Se a chamada falhar, o valor de retorno indicará o motivo da falha.
ms.assetid: 4ab1b5ba-dd19-4802-aa9c-02bd5406681f
title: Verificação de erros em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc3e374c6f0bd933c2e4de7a477fea02b4e1538a7a1fa9b4de78e45fd896b192
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874066"
---
# <a name="error-checking-in-c"></a>Verificação de erros em C++

Em C++, cada método de serviços de certificados retorna diretamente um valor **HRESULT** que indica se a chamada de método foi bem-sucedida ou falhou. Se a chamada falhar, o valor de retorno indicará o motivo da falha.

O exemplo a seguir mostra como os valores de **HRESULT** retornados podem ser usados para verificação de erro. Por exemplo, códigos de erro, consulte [valores comuns de HRESULT](common-hresult-values.md).


```C++
HRESULT hr;
BSTR strAttributeName;
BSTR strAttributeValue = NULL;

if(!(strAttributeName = SysAllocString(L"TheAttribute")))
{
     printf("Could not allocate memory for attribute name.\n");
     exit(1);
}

hr = pICertServerPolicy->GetRequestAttribute(
                                strAttributeName,
                                &strAttributeValue);
if(S_OK != hr)          // Check to determine whether method failed
{
    if (E_INVALIDARG == hr)
    {
        //... Do something to recover from errors and so on.
    }
}
// Free BSTRs when finished.
if (NULL != strAttributeName)
    SysFreeString(strAttributeName);
if (NULL != strAttributeValue)
    SysFreeString(strAttributeValue);
```



 

 



