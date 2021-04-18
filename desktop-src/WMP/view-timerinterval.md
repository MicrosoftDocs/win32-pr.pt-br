---
title: VIEW. IntervaloDoCronômetro
description: O atributo IntervaloDoCronômetro especifica ou recupera o intervalo, em milissegundos, no qual o temporizador dispara eventos para o manipulador de eventos OnTimer.
ms.assetid: 1a69890f-5ea4-493a-8a9e-04fe60a41804
keywords:
- VIEW. IntervaloDoCronômetro Windows Media Player
topic_type:
- apiref
api_name:
- VIEW.timerInterval
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 790c95fbb2cded134222271d04c4c37dae412b8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780361"
---
# <a name="viewtimerinterval"></a>VIEW. IntervaloDoCronômetro

O atributo **IntervaloDoCronômetro** especifica ou recupera o intervalo, em milissegundos, no qual o temporizador dispara eventos para o manipulador de eventos **OnTimer** .

``` syntax
        elementID.timerInterval
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**longo**) com um valor padrão de 1000.



| Valor        | Descrição                    |
|--------------|--------------------------------|
| 0            | O evento de timer não é acionado. |
| 50 e acima | O intervalo em milissegundos.  |



 

Qualquer valor abaixo de 50 (incluindo números negativos, mas não incluindo zero) gera um erro e o valor anterior é mantido.

## <a name="remarks"></a>Comentários

Isso não será acionado automaticamente se nenhum manipulador de eventos **OnTimer** for implementado. Portanto, não há degradação de desempenho, embora o valor padrão seja diferente de zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento VIEW**](view-element.md)
</dt> <dt>

[**Exibir. OnTimer**](view-ontimer.md)
</dt> </dl>

 

 





