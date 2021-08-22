---
description: O atributo mstop especifica a hora de parada de um clipe, em relação ao arquivo de mídia original.
ms.assetid: 01559d29-9c7b-4842-a1f7-16552adbda43
title: Atributo mstop
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9d432c3ed9ff80a9252def74fb553ed307668b36e660d96963baae0f4d0db04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072930"
---
# <a name="mstop-attribute"></a>Atributo mstop

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `mstop` atributo especifica a hora de parada de um clipe, em relação ao arquivo de mídia original.

## <a name="applies-to"></a>Aplica-se A

[**clip**](clip-element.md)

## <a name="possible-values"></a>Valores possíveis

Deve ser uma cadeia de caracteres com o formato *hh: mm: SS. FF* , em que *hh* = hours, *mm* = minutos, *SS* = segundos e *FF* = frações de segundos. Exemplo: 1:04:30.512. As unidades à esquerda podem ser omitidas. Por exemplo, 3:00 (três minutos) e 45 (45 segundos) são válidos.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetMediaTimes**](iamtimelinesrc-setmediatimes.md)
</dt> </dl>

 

 



