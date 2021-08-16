---
description: Controlando grafos de filtro usando C
ms.assetid: 56e41f0a-2ea6-422c-8d3f-7849e91e3731
title: Controlando grafos de filtro usando C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e234413f7642d7349c2bf378d1aded97b399e252117b0793f90335de8643912e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119073750"
---
# <a name="controlling-filter-graphs-using-c"></a>Controlando grafos de filtro usando C

Se você estiver escrevendo um DirectShow em C (em vez de C++), deverá usar um ponteiro vtable para chamar métodos. O exemplo a seguir ilustra como chamar o **método IUnknown::QueryInterface** de um aplicativo escrito em C:


```C++
pGraph->lpVtbl->QueryInterface(pGraph, &IID_IMediaEvent, (void **)&pEvent);
```



Veja a seguir a chamada equivalente em C++:


```C++
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



Em C, as interfaces COM são definidas como estruturas. O **membro lpVtbl** é um ponteiro para uma tabela de métodos de interface (a vtable). Todos os métodos levam um parâmetro adicional, que é um ponteiro para a interface .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Apêndices](appendixes.md)
</dt> </dl>

 

 



