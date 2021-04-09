---
description: O atributo mudo especifica o estado de mudo do objeto.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: Atributo mudo
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4e43feb16d75312cedd0caf5c217af2dd71332
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087732"
---
# <a name="mute-attribute"></a>Atributo mudo

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `mute` atributo especifica o estado de mudo do objeto. Se o valor for **true**, nem o objeto nem seus filhos serão renderizados. Se o valor for **false**, o objeto será renderizado e seus filhos serão renderizados de acordo com seu próprio estado de mudo. O valor padrão é **false**.

## <a name="possible-values"></a>Valores possíveis

Os valores a seguir são definidos como TRUE: y, Y, t, T, 1. Os valores a seguir são definidos como FALSE: n, N, f, F, 0 (zero).

## <a name="applies-to"></a>Aplica-se A

[**clip**](clip-element.md), [**composto**](composite-element.md), [**efeito**](effect-element.md), [**grupo**](group-element.md), [**linha do tempo**](timeline-element.md), [**transição**](transition-element.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj:: setmudod**](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



