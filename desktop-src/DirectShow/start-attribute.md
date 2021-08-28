---
description: O atributo start especifica a hora de início de um objeto em relação ao objeto pai.
ms.assetid: 971de88e-c1ee-4e07-bf8e-3153e4fd11f3
title: Atributo start
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 227b04a8cd7dc366a9cf10a4930233cd834e2bea7faa64bb59c248049b9e9abe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650986"
---
# <a name="start-attribute"></a>Atributo start

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `start` atributo especifica a hora de início de um objeto em relação ao objeto pai.

## <a name="possible-values"></a>Valores possíveis

Deve ser uma cadeia de caracteres com o formato *hh:mm:ss.ff,* em que *hh* = horas, *mm* = minutos, *ss* = segundos e *ff* = frações de segundos. Exemplo: 1:04:30.512. As unidades à frente podem ser omitidas. Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.

## <a name="applies-to"></a>Aplica-se A

[**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



