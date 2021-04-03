---
description: O atributo Lock especifica se um objeto deve ser editado. Se o valor for TRUE, o aplicativo deverá tratar o objeto como bloqueado e não permitirá alterações nesse objeto ou em seus filhos. O valor padrão é FALSE.
ms.assetid: 1aa92665-ab3b-4f04-9e6b-905942c197ef
title: bloquear atributo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7716f047e0df47ffb5e84cb2de0e9fe345836b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646073"
---
# <a name="lock-attribute"></a>bloquear atributo

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `lock` atributo especifica se um objeto deve ser editado. Se o valor for **true**, o aplicativo deverá tratar o objeto como bloqueado e não permitirá alterações nesse objeto ou em seus filhos. O valor padrão é **false**.

## <a name="possible-values"></a>Valores possíveis

Valores possíveis os valores a seguir são definidos como TRUE: y, Y, t, T, 1. Os valores a seguir são definidos como FALSE: n, N, f, F, 0 (zero).

## <a name="applies-to"></a>Aplica-se A

[**clip**](clip-element.md), [**composto**](composite-element.md), [**efeito**](effect-element.md), [**grupo**](group-element.md), [**linha do tempo**](timeline-element.md), [**transição**](transition-element.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj:: setlocked**](iamtimelineobj-setlocked.md)
</dt> </dl>

 

 



