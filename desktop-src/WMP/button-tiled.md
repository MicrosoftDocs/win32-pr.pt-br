---
title: BOTÃO. xadrez
description: O atributo de sublado especifica ou recupera um valor que indica se a imagem do botão será colocada em lado.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- BOTÃO. xadrez Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6c1316f10ce9ae3135f4ac35ab214ecdd1096d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794509"
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

 

 





