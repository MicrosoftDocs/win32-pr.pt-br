---
title: BOTÃO. xadrez
description: O atributo de sublado especifica ou recupera um valor que indica se a imagem do botão será colocada em lado.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- BOTÃO. Windows Media Player ao lado
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32f4f1dda0b5a79749cfbffaa30f29522ff318a763ad50fcd005479afa9c8997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581370"
---
# <a name="buttontiled"></a>BOTÃO. xadrez

O atributo de **sublado** especifica ou recupera um valor que indica se a imagem do **botão** será colocada em lado.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                       |
|-------|-----------------------------------|
| true  | O lado da imagem será enfeita.              |
| false | Padrão. A imagem não será enlado. |



 

## <a name="remarks"></a>Comentários

Se a imagem for menor do que a região real do controle, o agrupamento da imagem será repetido até que ela preencha toda a região. Se uma imagem não for especificada ou não puder ser recuperada, os **ladrilhos** serão definidos como false.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BOTÃO. imagem**](button-image.md)
</dt> </dl>

 

 





