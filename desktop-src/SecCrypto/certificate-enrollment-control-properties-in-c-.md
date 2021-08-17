---
description: Retorna um HRESULT. Nesse HRESULT, um valor de S \_ OK indica que o método foi executado com êxito.
ms.assetid: 6722a74a-1ec1-4c71-84c6-fb103aca149f
title: Propriedades de controle de registro de certificado em C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0941967b7b4be0bfa6d7db2f9b31e2971f8ca1d0deb9d9f92540a1ae5300791a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771915"
---
# <a name="certificate-enrollment-control-properties-in-c"></a>Propriedades de controle de registro de certificado em C++

Quando você define ou recupera uma propriedade de controle de registro de certificado em C++, a chamada do método retorna um **HRESULT**. Nesse **HRESULT**, um valor de S \_ OK indica que o método foi executado com êxito.

Os programas escritos em C++ podem recuperar as propriedades do controle de registro de certificado por chamadas de método no formulário a seguir.


```C++
#include <windows.h>

HRESULT get_propertyName( datatype * pPropValue);
```



Em que *PropertyName* especifica o nome da propriedade que está sendo acessada e *pPropValue* é um ponteiro para uma variável do tipo de dados apropriado. Após a conclusão bem-sucedida dessa chamada de método, *pPropValue* apontará para a variável que contém o valor da propriedade *PropertyName* .

Por exemplo, para recuperar o valor da propriedade **RootStoreType** , use o código a seguir.


```C++
// Get the store type.
// hr is an HRESULT.
// bstrStoreType is a BSTR variable.
hr = pEnroll->get_RootStoreType( &bstrStoreType );
```



Os programas escritos em C++ podem definir as propriedades do controle de registro de certificado chamando métodos no formulário a seguir.


```C++
#include <windows.h>

HRESULT put_propertyName( datatype PropValue);
```



Em que *PropertyName* especifica o nome da propriedade que está sendo acessada e *propvalue* é um valor do tipo de dados apropriado. Após a conclusão bem-sucedida dessa chamada de método, o novo valor da propriedade *PropertyName* será *propvalue*.

Por exemplo, para definir o valor da propriedade para o **RootStoreType**, o código a seguir pode ser usado.


```C++
// Set the store type.
// bstrNewType previously set to a valid store type
hr = pEnroll->put_RootStoreType( bstrNewType );
```



 

 



