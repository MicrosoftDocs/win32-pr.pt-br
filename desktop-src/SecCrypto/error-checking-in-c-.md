---
description: Em C++, cada método de serviços de certificados retorna diretamente um valor HRESULT que indica se a chamada de método foi bem-sucedida ou falhou. Se a chamada falhar, o valor de retorno indicará o motivo da falha.
ms.assetid: 4ab1b5ba-dd19-4802-aa9c-02bd5406681f
title: Verificação de erros em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f2a56acd41269ece0f9a5c7de4a2dff1960bb10
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505749"
---
# <a name="error-checking-in-c"></a><span data-ttu-id="f5acb-104">Verificação de erros em C++</span><span class="sxs-lookup"><span data-stu-id="f5acb-104">Error Checking in C++</span></span>

<span data-ttu-id="f5acb-105">Em C++, cada método de serviços de certificados retorna diretamente um valor **HRESULT** que indica se a chamada de método foi bem-sucedida ou falhou.</span><span class="sxs-lookup"><span data-stu-id="f5acb-105">In C++, every Certificate Services method directly returns an **HRESULT** value that indicates whether the method call succeeded or failed.</span></span> <span data-ttu-id="f5acb-106">Se a chamada falhar, o valor de retorno indicará o motivo da falha.</span><span class="sxs-lookup"><span data-stu-id="f5acb-106">If the call failed, the return value indicates why it failed.</span></span>

<span data-ttu-id="f5acb-107">O exemplo a seguir mostra como os valores de **HRESULT** retornados podem ser usados para verificação de erro.</span><span class="sxs-lookup"><span data-stu-id="f5acb-107">The following example shows how the returned **HRESULT** values can be used for error checking.</span></span> <span data-ttu-id="f5acb-108">Por exemplo, códigos de erro, consulte [valores comuns de HRESULT](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="f5acb-108">For example error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>


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



 

 



