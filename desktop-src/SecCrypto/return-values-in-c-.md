---
description: Em C++, o valor de retorno é normalmente do tipo HRESULT.
ms.assetid: 7abf1b3e-b94b-4846-a813-5eab5b34324c
title: Valores de retorno em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff7a5417019468945054f24701636fcece1d3d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169483"
---
# <a name="return-values-in-c"></a><span data-ttu-id="029a5-103">Valores de retorno em C++</span><span class="sxs-lookup"><span data-stu-id="029a5-103">Return Values in C++</span></span>

<span data-ttu-id="029a5-104">Em C++, o valor de retorno é normalmente do tipo **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="029a5-104">In C++, the return value is typically of type **HRESULT**.</span></span> <span data-ttu-id="029a5-105">É desse valor de retorno que pode ser determinado se o método foi bem-sucedido ou não, e se não, qual foi o erro.</span><span class="sxs-lookup"><span data-stu-id="029a5-105">It is from this return value that it can be determined whether the method succeeded or not, and if not, what the error was.</span></span> <span data-ttu-id="029a5-106">Os serviços de certificados normalmente retorna S \_ OK para o **HRESULT** quando o método é concluído com êxito.</span><span class="sxs-lookup"><span data-stu-id="029a5-106">Certificate Services typically returns S\_OK for the **HRESULT** when the method has completed successfully.</span></span> <span data-ttu-id="029a5-107">Os valores programáticos que precisam ser retornados são retornados por meio de parâmetros "out" no método.</span><span class="sxs-lookup"><span data-stu-id="029a5-107">Programmatic values that need to be returned are returned through "out" parameters in the method.</span></span> <span data-ttu-id="029a5-108">O exemplo a seguir mostra uma chamada de método C++ para recuperar uma propriedade de solicitação:</span><span class="sxs-lookup"><span data-stu-id="029a5-108">The following example shows a C++ method call to retrieve a request property:</span></span>


```C++
BSTR      bstrPropName = NULL;
VARIANT   varProp;
HRESULT   hr;

VariantInit(&varProp);

bstrPropName = SysAllocString(L"RequestID");
if (NULL == bstrPropName)
{
    printf("Failed SysAllocString\n");
    // Take application-specific error action.
    exit(1);
}

// Retrieve the request property.
// pCertServerPolicy is a pointer to a previously
// instantiated ICertServerPolicy object.
hr = pCertServerPolicy->GetRequestProperty(bstrPropName,
                                           PROPTYPE_LONG,
                                           &varProp);
if (S_OK != hr)
{
    printf("Failed GetRequestProperty [%x]\n", hr);
    // Take application-specific error action.
    // ...
}
else
{
    // Successfully retrieved property; use varProp as needed.
    // ...
}

// Done processing.
VariantClear(&varProp);
if (NULL != bstrPropName)
    SysFreeString(bstrPropName);
```



<span data-ttu-id="029a5-109">No fragmento de código anterior, êxito ou falha é retornado para a variável **HRESULT** , *HR*.</span><span class="sxs-lookup"><span data-stu-id="029a5-109">In the preceding code fragment, success or failure is returned to the **HRESULT** variable, *hr*.</span></span> <span data-ttu-id="029a5-110">É imperativo verificar a variável **HRESULT** para êxito \[ tratado no código pela condição (S \_ OK! = hr) \] .</span><span class="sxs-lookup"><span data-stu-id="029a5-110">It is imperative to check the **HRESULT** variable for success \[handled in the code by the condition (S\_OK != hr)\].</span></span> <span data-ttu-id="029a5-111">Se o método for concluído com êxito, o valor da propriedade de solicitação será retornado no parâmetro **Variant** *varProp* .</span><span class="sxs-lookup"><span data-stu-id="029a5-111">If the method completed successfully, the request property value is returned in the **VARIANT** *varProp* parameter.</span></span>

 

 



