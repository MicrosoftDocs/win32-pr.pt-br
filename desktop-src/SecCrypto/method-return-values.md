---
description: O valor de retorno para métodos de interface C++ é sempre do tipo HRESULT; Esse valor pode ser verificado para determinar o êxito ou a falha.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Valores de retorno do método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3871cf00bd48c7fbe1432ec86b503fba7795592
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768432"
---
# <a name="method-return-values"></a><span data-ttu-id="ae3e3-103">Valores de retorno do método</span><span class="sxs-lookup"><span data-stu-id="ae3e3-103">Method Return Values</span></span>

<span data-ttu-id="ae3e3-104">O valor de retorno para métodos de interface C++ é sempre do tipo **HRESULT**; Esse valor pode ser verificado para determinar o êxito ou a falha.</span><span class="sxs-lookup"><span data-stu-id="ae3e3-104">The return value for C++ interface methods is always of type **HRESULT**; this value can be checked to determine success or failure.</span></span> <span data-ttu-id="ae3e3-105">O uso de parâmetros de "saída" permite que os valores sejam atribuídos a variáveis durante o método ou a chamada de propriedade.</span><span class="sxs-lookup"><span data-stu-id="ae3e3-105">The use of "output" parameters allows values to be assigned to variables during the method or property call.</span></span> <span data-ttu-id="ae3e3-106">O exemplo a seguir mostra uma chamada de método do C++ para enumerar provedores.</span><span class="sxs-lookup"><span data-stu-id="ae3e3-106">The following example shows a C++ method call to enumerate providers.</span></span>


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



<span data-ttu-id="ae3e3-107">No fragmento de código anterior, êxito ou falha é retornado para a variável "HR".</span><span class="sxs-lookup"><span data-stu-id="ae3e3-107">In the preceding code fragment, success or failure is returned to the "hr" variable.</span></span> <span data-ttu-id="ae3e3-108">Se a chamada foi bem-sucedida, HR será definido como S \_ OK e a variável bstrprovider conterá o nome do provedor enumerado.</span><span class="sxs-lookup"><span data-stu-id="ae3e3-108">If the call was successful, hr will be set to S\_OK and the variable bstrProvider will contain the name of the enumerated provider.</span></span>

<span data-ttu-id="ae3e3-109">Uma chamada de C++ para recuperar um valor de propriedade seria a seguinte.</span><span class="sxs-lookup"><span data-stu-id="ae3e3-109">A C++ call to retrieve a property value would be as follows.</span></span>


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



<span data-ttu-id="ae3e3-110">Uma chamada de C++ para definir um valor de propriedade seria a seguinte.</span><span class="sxs-lookup"><span data-stu-id="ae3e3-110">A C++ call to set a property value would be as follows.</span></span>


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



