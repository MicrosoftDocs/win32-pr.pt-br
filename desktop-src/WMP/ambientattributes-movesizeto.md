---
title: AmbientAttributes.moveSizeTo
description: O método moveSizeTo move o controle e especifica um novo tamanho para o controle no novo local. O controle move e resize de forma animada durante o período de tempo especificado.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- AmbientAttributes.moveSizeTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 936a6696dfcc99c5a181906eb970f84c7019af7905c466f09e820044f6220271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469946"
---
# <a name="ambientattributesmovesizeto"></a>AmbientAttributes.moveSizeTo

O **método moveSizeTo** move o controle e especifica um novo tamanho para o controle no novo local. O controle move e resize de forma animada durante o período de tempo especificado.

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
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

<span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*Newwidth*
</dt> <dd>

**Number** (**long**) especificando o novo valor para **o atributo de** largura do controle.

</dd> <dt>

<span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*
</dt> <dd>

**Number** (**long**) especificando o novo valor para o **atributo de altura** do controle .

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*moveTime*
</dt> <dd>

**Número** (**longo**) especificando o tempo, em milissegundos, que leva para o controle mudar para seu novo local.

</dd> <dt>

<span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*
</dt> <dd>

**Booliana** especificando o tipo de movimento criado ao mover o controle.



| Valor | Descrição                                                             |
|-------|-------------------------------------------------------------------------|
| true  | O movimento não é linear (movimento deslizante que acelera e desacelera). |
| false | O movimento é linear.                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O movimento do controle pode ser linear ou não linear. O movimento linear significa que o controle se move em uma velocidade constante para seu novo local, iniciando e parando de forma linear. Quando o movimento não linear é especificado, é criado um movimento deslizante que é acelerado de zero no início do movimento e desacelera de volta para zero no final, chegando a uma parada suave.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.height**](ambientattributes-height.md)
</dt> <dt>

[**AmbientAttributes.left**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> <dt>

[**AmbientAttributes.width**](ambientattributes-width.md)
</dt> </dl>

 

 





