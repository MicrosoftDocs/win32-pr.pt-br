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
# <a name="method-return-values"></a>Valores de retorno do método

O valor de retorno para métodos de interface C++ é sempre do tipo **HRESULT**; Esse valor pode ser verificado para determinar o êxito ou a falha. O uso de parâmetros de "saída" permite que os valores sejam atribuídos a variáveis durante o método ou a chamada de propriedade. O exemplo a seguir mostra uma chamada de método do C++ para enumerar provedores.


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



No fragmento de código anterior, êxito ou falha é retornado para a variável "HR". Se a chamada foi bem-sucedida, HR será definido como S \_ OK e a variável bstrprovider conterá o nome do provedor enumerado.

Uma chamada de C++ para recuperar um valor de propriedade seria a seguinte.


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



Uma chamada de C++ para definir um valor de propriedade seria a seguinte.


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



