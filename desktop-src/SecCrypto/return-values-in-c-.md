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
# <a name="return-values-in-c"></a>Valores de retorno em C++

Em C++, o valor de retorno é normalmente do tipo **HRESULT**. É desse valor de retorno que pode ser determinado se o método foi bem-sucedido ou não, e se não, qual foi o erro. Os serviços de certificados normalmente retorna S \_ OK para o **HRESULT** quando o método é concluído com êxito. Os valores programáticos que precisam ser retornados são retornados por meio de parâmetros "out" no método. O exemplo a seguir mostra uma chamada de método C++ para recuperar uma propriedade de solicitação:


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



No fragmento de código anterior, êxito ou falha é retornado para a variável **HRESULT** , *HR*. É imperativo verificar a variável **HRESULT** para êxito \[ tratado no código pela condição (S \_ OK! = hr) \] . Se o método for concluído com êxito, o valor da propriedade de solicitação será retornado no parâmetro **Variant** *varProp* .

 

 



