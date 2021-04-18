---
title: Ambienteattributes. moveSizeTo
description: O método moveSizeTo move o controle e especifica um novo tamanho para o controle no novo local. O controle é movido e redimensionado de maneira animada no período de tempo especificado.
ms.assetid: 89e3bf16-a123-4fb1-8c24-bc22a978e7f6
keywords:
- MoveSizeTo do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.moveSizeTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 406d48772e85a55ab82241518d499182931cc2fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810591"
---
# <a name="ambientattributesmovesizeto"></a>Ambienteattributes. moveSizeTo

O método **moveSizeTo** move o controle e especifica um novo tamanho para o controle no novo local. O controle é movido e redimensionado de maneira animada no período de tempo especificado.

``` syntax
        elementID.moveSizeTo(newX, newY, newWidth, newHeight, moveTime, fSlide)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="newX"></span><span id="newx"></span><span id="NEWX"></span>*newX*
</dt> <dd>

**Número** (**longo**) especificando o novo valor para o atributo **esquerdo** do controle.

</dd> <dt>

<span id="newY"></span><span id="newy"></span><span id="NEWY"></span>*newY*
</dt> <dd>

**Número** (**longo**) especificando o novo valor para o atributo **superior** do controle.

</dd> <dt>

<span id="newWidth"></span><span id="newwidth"></span><span id="NEWWIDTH"></span>*newWidth*
</dt> <dd>

**Número** (**longo**) especificando o novo valor para o atributo de **largura** do controle.

</dd> <dt>

<span id="newHeight"></span><span id="newheight"></span><span id="NEWHEIGHT"></span>*newHeight*
</dt> <dd>

**Número** (**longo**) especificando o novo valor para o atributo de **altura** do controle.

</dd> <dt>

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*mover para*
</dt> <dd>

**Número** (**longo**) que especifica o tempo, em milissegundos, que leva para que o controle seja movido para o novo local.

</dd> <dt>

<span id="fSlide"></span><span id="fslide"></span><span id="FSLIDE"></span>*fSlide*
</dt> <dd>

**Booliano** que especifica o tipo de movimento criado ao mover o controle.



| Valor | Descrição                                                             |
|-------|-------------------------------------------------------------------------|
| true  | O movimento não é linear (movimento deslizante que acelera e diminui). |
| false | O movimento é linear.                                                       |



 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

O movimento do controle pode ser linear ou não linear. Movimento linear significa que o controle se move em uma velocidade constante para seu novo local, iniciando e parando abruptamente. Quando o movimento não linear é especificado, é criado um movimento deslizante que acelera de zero no início do movimento e que é reduzido de volta para zero no final, chegando a uma parada suave.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**Ambiente. altura**](ambientattributes-height.md)
</dt> <dt>

[**Ambienteattributes. esquerda**](ambientattributes-left.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> <dt>

[**Ambiente. largura**](ambientattributes-width.md)
</dt> </dl>

 

 





