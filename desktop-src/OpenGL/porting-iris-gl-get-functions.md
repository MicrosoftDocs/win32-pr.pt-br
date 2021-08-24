---
title: Funções Get GL do íris de portabilidade
description: ÍRIS GL \ 0034; Get \ 0034; as funções usam o seguinte formulário
ms.assetid: 5bd6aa13-b41d-4f89-91dc-cc47481ac7b7
keywords:
- Portabilidade do íris GL, obter funções
- portando do íris GL, obter funções
- portando para OpenGL do íris GL, obter funções
- Portabilidade do OpenGL do íris GL, obter funções
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdfe9159e0207198fa94959729bd0c95439bb91b5dd55a8a1f9adf3b048d7bb1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485556"
---
# <a name="porting-iris-gl-get-functions"></a>Funções Get GL do íris de portabilidade

As funções de "Get" da íris GL assumem o seguinte formato:

``` syntax
int getthing();
```

e

``` syntax
int getthings( int *a, int *b);
```

O código da íris GL provavelmente incluirá chamadas de função Get parecidas com:

``` syntax
thing = getthing(); 
if (getthing() == THING) { /* some stuff here */ } 
getthings (&a, &b);
```

No OpenGL, você usa um dos quatro tipos de funções [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) a seguir em vez de funções Get GL equivalentes de íris.

-   **glGetBooleanv**
-   **glGetIntegerv**
-   **glGetFloatv**
-   **glGetDoublev**

As funções têm a seguinte sintaxe:

``` syntax
glGet<Datatype>v( value, *data );
```

em que *Value* é do tipo **GLenum** e os dados são do tipo **GLdatatype**. Quando você chama **glGet** e retorna um tipo diferente do tipo esperado, o tipo é convertido adequadamente. Para obter uma lista completa de parâmetros de **glGet** , consulte [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md).

 

 




