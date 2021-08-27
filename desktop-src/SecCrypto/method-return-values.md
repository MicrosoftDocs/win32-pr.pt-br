---
description: O valor de retorno para métodos de interface C++ é sempre do tipo HRESULT; esse valor pode ser verificado para determinar o êxito ou a falha.
ms.assetid: f6478e72-0fe9-4c3b-b08a-f71c9c943910
title: Valores de retorno do método
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073df1d306fb991d7e1347ff90a21d578bf42583c642a694de3160b405963a28
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100756"
---
# <a name="method-return-values"></a>Valores de retorno do método

O valor de retorno para métodos de interface C++ é sempre do tipo **HRESULT**; esse valor pode ser verificado para determinar o êxito ou a falha. O uso de parâmetros de "saída" permite que os valores sejam atribuídos a variáveis durante a chamada de método ou propriedade. O exemplo a seguir mostra uma chamada de método C++ para enumerar provedores.


```C++
UINT          ucEnumProvIndex = 0;
BSTR          bstrProvider = NULL;
HRESULT       hr;

// pEnroll is previously instantiated CEnroll interface pointer
hr = pEnroll->enumProviders(ucEnumProvIndex, 0, &bstrProvider);
```



No fragmento de código anterior, êxito ou falha é retornado para a variável "hr". Se a chamada for bem-sucedida, o rh será definido como S OK e a variável \_ bstrProvider conterá o nome do provedor enumerado.

Uma chamada C++ para recuperar um valor da propriedade seria a seguinte.


```C++
BSTR     bstrStoreName = NULL;
HRESULT  hr;

// pEnroll is previously instantiated CEnroll interface pointer

// get the storename
hr = pEnroll->get_CAStoreName( &bstrStoreName );

// (When done using bstrStoreName, free it by calling SysFreeString).
```



Uma chamada C++ para definir um valor da propriedade seria a seguinte.


```C++
// bstrNewName previously set to a valid store name
hr = pEnroll->put_CAStoreName( bstrNewName );
```



 

 



