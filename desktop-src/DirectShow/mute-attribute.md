---
description: O atributo mute especifica o estado de mute do objeto.
ms.assetid: 9a6dccf5-ae00-4ee0-8df3-bf817fe1a164
title: Atributo mute
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6d89632e632ec4dbf0fe76a915e073baa769044fa1eaad455c16dd3065dc1c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791036"
---
# <a name="mute-attribute"></a>Atributo mute

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `mute` atributo especifica o estado de mute do objeto. Se o valor for **TRUE,** nem o objeto nem seus filhos serão renderizados. Se o valor for **FALSE,** o objeto será renderizado e seus filhos serão renderizados de acordo com seu próprio estado de mudo. O valor padrão é **FALSE**.

## <a name="possible-values"></a>Valores possíveis

Os seguintes valores são definidos como TRUE: y, Y, t, T, 1. Os seguintes valores são definidos como FALSE: n, N, f, F, 0 (zero).

## <a name="applies-to"></a>Aplica-se A

[**clip**](clip-element.md), [**composite**](composite-element.md), [**effect**](effect-element.md), [**group**](group-element.md), [**timeline**](timeline-element.md), [**transition**](transition-element.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetMuted**](iamtimelineobj-setmuted.md)
</dt> </dl>

 

 



