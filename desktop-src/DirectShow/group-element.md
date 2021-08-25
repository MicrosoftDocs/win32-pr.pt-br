---
description: O elemento group define um grupo, o objeto de nível superior em uma linha do tempo.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Elemento group (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eda120363540eaf467ebb9beaea4705c4b430077c55b5b05c46197d90920b40a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997826"
---
# <a name="group-element"></a>Elemento group

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O **elemento** group define um grupo, o objeto de nível superior em uma linha do tempo.

## <a name="attributes"></a>Atributos

[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md) [**,**](framerate-attribute.md)taxa de quadros , [**altura**](height-attribute.md) [**,**](lock-attribute.md)bloqueio , [**mute**](mute-attribute.md), [**name**](name-attribute.md), previewmode , [**samplingrate**](previewmode-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md) [](samplingrate-attribute.md)

## <a name="parentchild-information"></a>Informações pai/filho



| Rótulo | Valor |
|----------|----------------------------------------------------------------------------------------------------------|
| Pai   | [**Cronograma**](timeline-element.md)                                                                     |
| Children | [**composto**](composite-element.md), [**efeito**](effect-element.md), [**faixa**](track-element.md) |



 

## <a name="remarks"></a>Comentários

Dentro de `group` um elemento, a prioridade das camadas aninhadas é determinada implicitamente pela ordem em que aparecem dentro do elemento. A primeira camada tem prioridade 0 e as camadas subsequentes têm valores de prioridade crescentes.

## <a name="examples"></a>Exemplos


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



