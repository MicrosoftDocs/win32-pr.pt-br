---
description: Retorna um HRESULT. Nesse HRESULT, um valor de S \_ OK indica que o método foi executado com êxito.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Propriedades de controle de registro de certificado em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76525f26f318178f122cc0feee6221bbd948bba0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501582"
---
# <a name="certificate-enrollment-control-properties-in-c"></a><span data-ttu-id="388b6-104">Propriedades de controle de registro de certificado em C++</span><span class="sxs-lookup"><span data-stu-id="388b6-104">Certificate Enrollment Control Properties in C++</span></span>

<span data-ttu-id="388b6-105">Quando você define ou recupera uma propriedade de controle de registro de certificado em C++, a chamada do método retorna um **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="388b6-105">When you set or retrieve a Certificate Enrollment Control property in C++, the method call returns an **HRESULT**.</span></span> <span data-ttu-id="388b6-106">Nesse **HRESULT**, um valor de S \_ OK indica que o método foi executado com êxito.</span><span class="sxs-lookup"><span data-stu-id="388b6-106">In this an **HRESULT**, a value of S\_OK indicates that the method was successfully executed.</span></span>

<span data-ttu-id="388b6-107">Os programas escritos em C++ podem recuperar as propriedades do controle de registro de certificado por chamadas de método no formulário a seguir.</span><span class="sxs-lookup"><span data-stu-id="388b6-107">Programs written in C++ can retrieve the Certificate Enrollment Control properties by method calls in the following form.</span></span>


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



<span data-ttu-id="388b6-108">Em que *PropertyName* especifica o nome da propriedade que está sendo acessada e *pPropValue* é um ponteiro para uma variável do tipo de dados apropriado.</span><span class="sxs-lookup"><span data-stu-id="388b6-108">Where *propertyName* specifies the name of the property being accessed, and *pPropValue* is a pointer to a variable of the appropriate data type.</span></span> <span data-ttu-id="388b6-109">Após a conclusão bem-sucedida dessa chamada de método, *pPropValue* apontará para a variável que contém o valor da propriedade *PropertyName* .</span><span class="sxs-lookup"><span data-stu-id="388b6-109">After successful completion of this method call, *pPropValue* will point to the variable that contains the value of the *propertyName* property.</span></span>

<span data-ttu-id="388b6-110">Por exemplo, para recuperar o valor da propriedade **RootStoreType** , use o código a seguir.</span><span class="sxs-lookup"><span data-stu-id="388b6-110">For example, to retrieve the value for the **RootStoreType** property, you use the following code.</span></span>


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



<span data-ttu-id="388b6-111">Os programas escritos em C++ podem definir as propriedades do controle de registro de certificado chamando métodos no formulário a seguir.</span><span class="sxs-lookup"><span data-stu-id="388b6-111">Programs written in C++ can set the Certificate Enrollment Control properties by calling methods in the following form.</span></span>


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



<span data-ttu-id="388b6-112">Em que *PropertyName* especifica o nome da propriedade que está sendo acessada e *propvalue* é um valor do tipo de dados apropriado.</span><span class="sxs-lookup"><span data-stu-id="388b6-112">Where *propertyName* specifies the name of the property being accessed, and *PropValue* is a value of the appropriate data type.</span></span> <span data-ttu-id="388b6-113">Após a conclusão bem-sucedida dessa chamada de método, o novo valor da propriedade *PropertyName* será *propvalue*.</span><span class="sxs-lookup"><span data-stu-id="388b6-113">After successful completion of this method call, the new value of the *propertyName* property will be *PropValue*.</span></span>

<span data-ttu-id="388b6-114">Por exemplo, para definir o valor da propriedade para o **RootStoreType**, o código a seguir pode ser usado.</span><span class="sxs-lookup"><span data-stu-id="388b6-114">For example, to set the property value for the **RootStoreType**, the following code could be used.</span></span>


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



