---
description: O atributo mstart especifica a hora de início de um clipe, em relação ao arquivo de mídia original.
ms.assetid: ed63f448-8ca3-4733-afc0-2d743f82bebe
title: Atributo mstart
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c65ffcb7d3da41f3e1f1232e37a6f5786755980eb63a8bbc554bbe726f453e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050946"
---
# <a name="mstart-attribute"></a>Atributo mstart

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `mstart` atributo especifica a hora de início de um clipe, em relação ao arquivo de mídia original.

## <a name="applies-to"></a>Aplica-se A

[**clip**](clip-element.md)

## <a name="possible-values"></a>Valores possíveis

Deve ser uma cadeia de caracteres com o formato *hh:mm:ss.ff,* em que *hh* = horas, *mm* = minutos, *ss* = segundos e *ff* = frações de segundos. Exemplo: 1:04:30.512. As unidades à frente podem ser omitidas. Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



