---
title: VIEW.timerInterval
description: O atributo timerInterval especifica ou recupera o intervalo, em milissegundos, no qual o temporizador dispara eventos para o manipulador de eventos ontimer.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- VIEW.timerInterval Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f43b2b7bbd87663a35c43db733d3e11ff0dca5bc3ddfd00e57022b4df7122c3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001306"
---
# <a name="viewtimerinterval"></a>VIEW.timerInterval

O **atributo timerInterval** especifica ou recupera o intervalo, em milissegundos, no qual o temporizador dispara eventos para o manipulador de eventos **ontimer.**

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um  número de leitura/gravação (**longo**) com um valor padrão de 1000.



| Valor        | Descrição                    |
|--------------|--------------------------------|
| 0            | O evento de temporizador não é a incêndio. |
| 50 e acima | O intervalo em milissegundos.  |



 

Qualquer valor abaixo de 50 (incluindo números negativos, mas sem incluir zero) gera um erro e o valor anterior é mantido.

## <a name="remarks"></a>Comentários

Isso não será a disparar automaticamente se nenhum manipulador de eventos **ontimer** for implementado. Portanto, não há degradação de desempenho, embora o valor padrão seja não zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> <dt>

[**VIEW.ontimer**](view-ontimer.md)
</dt> </dl>

 

 





