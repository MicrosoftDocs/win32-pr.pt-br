---
description: O atributo de taxa de quadros especifica uma taxa de quadros, em quadros por segundo.
ms.assetid: 541a86e3-7736-4de4-b509-f8d61ef9bc58
title: Atributo de taxa de quadros (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2939126dbd849538bb30fcf7729e5f91dafa292b6db512398c915c8f8de2c9a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015654"
---
# <a name="framerate-attribute-directshow"></a>Atributo de taxa de quadros (DirectShow)

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `framerate` atributo especifica uma taxa de quadros, em quadros por segundo.

## <a name="possible-values"></a>Valores possíveis

Valor de ponto flutuante. O valor deve incluir o zero à esquerda antes da casa decimal. Por exemplo, 0,3, não. 3. Não use mais de sete dígitos decimais.

## <a name="applies-to"></a>Aplica-se A

[**clip**](clip-element.md), [**grupo**](group-element.md), [**linha do tempo**](timeline-element.md)

## <a name="remarks"></a>Comentários

Para o elemento **clip** , esse atributo especifica a taxa de quadros padrão da origem. Especifique o atributo para imagens que ainda andDIB sequências. Para uma imagem ainda, defina o valor como zero. Para uma sequência DIB, use um valor diferente de zero. O valor padrão é zero.

Para o elemento **Group** , esse atributo especifica a taxa de quadros de saída para o grupo.

Para o elemento **Timeline** , esse atributo especifica a taxa de quadros padrão para todos os grupos.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Atributos XTL](xtl-attributes.md)
</dt> <dt>

[**IAMTimelineSrc::SetDefaultFPS**](iamtimelinesrc-setdefaultfps.md)
</dt> <dt>

[**IAMTimelineGroup::SetOutputFPS**](iamtimelinegroup-setoutputfps.md)
</dt> <dt>

[**IAMTimeline::SetDefaultFPS**](iamtimeline-setdefaultfps.md)
</dt> </dl>

 

 



