---
title: AmbientAttributes.slideTo
description: O método slideTo move o controle para um novo local. O controle se move de maneira não linear durante o período de tempo especificado.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- AmbientAttributes.slideTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3f199a2786adbd63313c3f500d589f9f51e2b8ca2fa8120a8fdf75021041115
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469906"
---
# <a name="ambientattributesslideto"></a>AmbientAttributes.slideTo

O **método slideTo** move o controle para um novo local. O controle se move de maneira não linear durante o período de tempo especificado.

``` syntax
        elementID.slideTo(newX, newY, moveTime)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*
</dt> <dd>

**Number** (**long**) especificando o novo valor para o **atributo esquerdo** do controle .

</dd> <dt>

<span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*
</dt> <dd>

**Number** (**long**) especificando o novo valor para o **atributo superior** do controle.

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Número** (**longo**) especificando o tempo, em milissegundos, que leva para o controle mudar para seu novo local.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é diferente de **moveTo**, que cria um movimento linear ao mover o controle. O movimento não linear criado por esse método é um movimento deslizante que acelera de uma velocidade de zero no início do movimento e desacelera de volta para zero no final, chegando a uma parada suave.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.moveTo**](ambientattributes-moveto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





