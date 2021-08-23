---
title: SLIDER.til
description: O atributo lado a lado especifica ou recupera um valor que indica se a imagem do controle deslizante será lado a lado.
ms.assetid: 159a2972-a0eb-4e43-a083-e124e56782f5
keywords:
- CONTROLE DESLIZANTE.bloco Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a97be7ee857574b24585ffd7ffd9b63acdfad0a37762445699daa3a06f94e97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832532"
---
# <a name="slidertiled"></a>SLIDER.til

O **atributo lado** a lado especifica ou recupera um valor que indica se a imagem do controle deslizante será lado a lado.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um booliana **de leitura/gravação.**



| Valor | Descrição                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| true  | Padrão. O bitmap de imagem será repetido até preencher toda a região do controle. |
| false | A imagem não será lado a lado.                                                                |



 

## <a name="remarks"></a>Comentários

Esse atributo se aplica somente se você estiver usando imagens de primeiro plano e de plano de fundo para definir um controle deslizante. Se as imagens são menores do que a  área definida do controle deslizante e o atributo lado a lado é definido como true, as imagens serão repetidas até preencher todo o comprimento do controle.

Talvez você queira usar esse atributo em conjunto com o **atributo borderSize.** O **atributo borderSize** permite que você defina uma borda que não é repetida durante o bloco.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER.borderSize**](slider-bordersize.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





