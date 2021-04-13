---
description: Controlando gráficos de filtro usando C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Controlando gráficos de filtro usando C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ce6d78875c6b0d5f028ea89dfbd2b061285f1c1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370251"
---
# <a name="controlling-filter-graphs-using-c"></a>Controlando gráficos de filtro usando C

Se você estiver escrevendo um aplicativo DirectShow em C (em vez de C++), deverá usar um ponteiro vtable para chamar métodos. O exemplo a seguir ilustra como chamar o método **IUnknown:: QueryInterface** de um aplicativo escrito em C:


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



O seguinte mostra a chamada equivalente em C++:


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



Em C, as interfaces COM são definidas como estruturas. O membro **lpVtbl** é um ponteiro para uma tabela de métodos de interface (a vtable). Todos os métodos usam um parâmetro adicional, que é um ponteiro para a interface.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Apêndices](appendixes.md)
</dt> </dl>

 

 



