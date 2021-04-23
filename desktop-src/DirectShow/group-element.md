---
description: O elemento Group define um grupo, o objeto de nível superior em uma linha do tempo.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Elemento Group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31502cef89c8383e935f409d76b9e31ca53a2da1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909244"
---
# <a name="group-element"></a>Elemento Group

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O elemento **Group** define um grupo, o objeto de nível superior em uma linha do tempo.

## <a name="attributes"></a>Atributos

[**bitdepth**](bitdepth-attribute.md), [**buffer**](buffering-attribute.md), [**taxa de quadros**](framerate-attribute.md), [**altura**](height-attribute.md), [**bloqueio**](lock-attribute.md), [**mudo**](mute-attribute.md), [**nome**](name-attribute.md), [**modo de exibição**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**tipo**](type-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**nome de usuário**](username-attribute.md), [**largura**](width-attribute.md)

## <a name="parentchild-information"></a>Informações de pai/filho



| Label | Valor |
|----------|----------------------------------------------------------------------------------------------------------|
| Pai   | [**linha do tempo**](timeline-element.md)                                                                     |
| Children | [**composto**](composite-element.md), [**efeito**](effect-element.md), [**faixa**](track-element.md) |



 

## <a name="remarks"></a>Comentários

Dentro de um `group` elemento, a prioridade de camadas aninhadas é determinada implicitamente pela ordem em que aparecem dentro do elemento. A primeira camada tem a prioridade 0 e as camadas subsequentes têm valores de prioridade crescentes.

## <a name="examples"></a>Exemplos


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



