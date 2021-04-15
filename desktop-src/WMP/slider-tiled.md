---
title: Controle deslizante. xadrez
description: O atributo de sublado especifica ou recupera um valor que indica se a imagem do controle deslizante será disposta ao lado.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- Controle deslizante. xadrez do Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1448f496ee45d6c8b01356499b9628c745d69f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753674"
---
# <a name="slidertiled"></a>Controle deslizante. xadrez

O atributo de **sublado** especifica ou recupera um valor que indica se a imagem do controle deslizante será disposta ao lado.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| true  | Padrão. O bitmap de imagem será repetido até ocupar a região inteira do controle. |
| false | A imagem não será enlado.                                                                |



 

## <a name="remarks"></a>Comentários

Esse atributo se aplica somente se você estiver usando imagens de primeiro e segundo plano para definir um controle deslizante. Se as imagens forem menores do que a área definida do controle deslizante, e o atributo de **ladrilho** for definido como true, as imagens serão repetidas até que preencham toda a duração do controle.

Talvez você queira usar esse atributo em conjunto com o atributo **borderize** . O atributo **borderize** permite que você defina uma borda que não é repetida durante a divisão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER. backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**Controle deslizante. Borderize**](slider-bordersize.md)
</dt> <dt>

[**SLIDER. foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





