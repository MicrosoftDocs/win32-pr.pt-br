---
title: Ambienteattributes. deslizeto
description: O método slideto move o controle para um novo local. O controle é movido de forma não linear no período de tempo especificado.
ms.assetid: 06dd610b-cb58-4b60-9f4b-8929c54c3c33
keywords:
- Ambiente. Deslize para o Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.slideTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: deb214046ace59094b6bd5c362dfa716b9fceb57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761492"
---
# <a name="ambientattributesslideto"></a>Ambienteattributes. deslizeto

O método **slideto** move o controle para um novo local. O controle é movido de forma não linear no período de tempo especificado.

``` syntax
        elementID.slideTo(newX, newY, moveTime)
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

<span id="moveTime"></span><span id="movetime"></span><span id="MOVETIME"></span>*mover para*
</dt> <dd>

**Número** (**longo**) que especifica o tempo, em milissegundos, que leva para que o controle seja movido para o novo local.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é diferente de **MoveTo**, que cria um movimento linear ao mover o controle. O movimento não linear criado por esse método é um movimento deslizante que acelera a partir de uma velocidade de zero no início do movimento e faz a desaceleração para zero no final, chegando a uma parada suave.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**Ambienteattributes. esquerda**](ambientattributes-left.md)
</dt> <dt>

[**Ambienteattributes. moveTo**](ambientattributes-moveto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





