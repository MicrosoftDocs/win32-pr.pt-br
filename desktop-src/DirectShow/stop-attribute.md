---
description: O atributo Stop especifica a hora de parada de um objeto, em relação ao objeto pai.
ms.assetid: 1bda3472-abda-4672-9b82-311163e56fe0
title: parar atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15f8ccae1ff4a9a067ccf8ee90438cfb87e3260d41a7fac009afb4b4153e4ddf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050167"
---
# <a name="stop-attribute"></a>parar atributo

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `stop` atributo especifica a hora de parada de um objeto, em relação ao objeto pai.

## <a name="possible-values"></a>Valores possíveis

Deve ser uma cadeia de caracteres com o formato *hh: mm: SS. FF* , em que *hh* = hours, *mm* = minutos, *SS* = segundos e *FF* = frações de segundos. Exemplo: 1:04:30.512. As unidades à esquerda podem ser omitidas. Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.

## <a name="applies-to"></a>Aplica-se A

[**clip**](clip-element.md), [**efeito**](effect-element.md), [**transição**](transition-element.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineObj::SetStartStop**](iamtimelineobj-setstartstop.md)
</dt> </dl>

 

 



