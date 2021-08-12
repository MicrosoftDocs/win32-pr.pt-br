---
description: O atributo de ponto de corte especifica quando uma transição é cortada de uma fonte para outra, se a transição é renderizada como um corte. O valor é relativo ao início da transição.
ms.assetid: bdb0b8cd-025f-4b56-9cd4-f71c58ee809a
title: Atributo cutpoint
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7332d3ef1b608b192b18e0d32bc99bce547058754950847e0a9767eb500a1553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118654587"
---
# <a name="cutpoint-attribute"></a>Atributo cutpoint

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O atributo especifica quando uma transição é cortada de uma fonte para a próxima, se a transição `cutpoint` é renderizada como um corte. O valor é relativo ao início da transição.

## <a name="possible-values"></a>Valores possíveis

Deve ser uma cadeia de caracteres com o formato *hh:mm:ss.ff,* em que *hh* = horas, *mm* = minutos, *ss* = segundos e *ff* = frações de segundos. Exemplo: 1:04:30.512. As unidades à frente podem ser omitidas. Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.

## <a name="applies-to"></a>Aplica-se A

[**transição**](transition-element.md)

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineTrans::SetCutPoint**](iamtimelinetrans-setcutpoint.md)
</dt> </dl>

 

 



