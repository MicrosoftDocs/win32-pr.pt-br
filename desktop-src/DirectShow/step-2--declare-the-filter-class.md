---
description: Declare uma classe C++ que herda a classe base que você escolheu como parte da escrita de um filtro de transformação.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: Etapa 2. Declarar a classe Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88be97e47d529ffa22c90e9c8c200160dbd5f261
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410059"
---
# <a name="step-2-declare-the-filter-class"></a>Etapa 2. Declarar a classe Filter

Esta é a etapa 2 do tutorial Escrevendo [filtros de transformação.](writing-transform-filters.md)

Comece declarando uma classe C++ que herda a classe base:


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



Cada uma das classes de filtro tem classes de pino associadas. Dependendo das necessidades específicas do filtro, talvez seja necessário substituir as classes de pino. No caso de **CTransformFilter**, os pinos delegam a maior parte de seu trabalho ao filtro, portanto, você provavelmente não precisa substituir os pinos.

Você deve gerar um CLSID exclusivo para o filtro. Você pode usar o utilitário Guidgen ou Uuidgen; nunca copie um GUID existente. Há várias maneiras de declarar um CLSID. O exemplo a seguir usa a **macro \_ DEFINE GUID:**


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



Em seguida, escreva um método de construtor para o filtro:


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



Observe que um dos parâmetros para o construtor [**CTransformFilter**](ctransformfilter-ctransformfilter.md) é o CLSID definido anteriormente.

Próximo: [Etapa 3. Suporte à negociação de tipo de mídia](step-3--support-media-type-negotiation.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Escrevendo filtros do DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



