---
title: Ambienteattributes. moveTo
description: O método moveTo move o controle para um novo local em uma velocidade linear.
ms.assetid: 8670aa7b-a5c1-4d93-9f48-452bc53e65e6
keywords:
- Windows Media Player de ambiente. moveTo
topic_type:
- apiref
api_name:
- AmbientAttributes.moveTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af481526c0923c527bb14aa4700a6c6fe5ea3613
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794530"
---
# <a name="ambientattributesmoveto"></a>Ambienteattributes. moveTo

O método **MoveTo** move o controle para um novo local em uma velocidade linear.

``` syntax
        elementID.moveTo(newLeft, newTop, time)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="newLeft"></span><span id="newleft"></span><span id="NEWLEFT"></span>*newLeft*
</dt> <dd>

**Número** (**longo**) especificando o novo valor para o atributo **esquerdo** do controle.

</dd> <dt>

<span id="newTop"></span><span id="newtop"></span><span id="NEWTOP"></span>*newTop*
</dt> <dd>

**Número** (**longo**) especificando o novo valor para o atributo **superior** do controle.

</dd> <dt>

<span id="time"></span><span id="TIME"></span>*momento*
</dt> <dd>

**Número** (**longo**) que especifica o tempo, em milissegundos, que leva para que o controle seja movido para o novo local.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é útil para elementos de **subexibição** animados (por exemplo, se o usuário clicar em uma bandeja e os controles deslizarem).

Esse método cria um movimento linear ao mover o controle. Isso é diferente de **slideto**, que cria um movimento não linear.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**Ambienteattributes. esquerda**](ambientattributes-left.md)
</dt> <dt>

[**Ambienteattributes. deslizeto**](ambientattributes-slideto.md)
</dt> <dt>

[**AmbientAttributes.top**](ambientattributes-top.md)
</dt> </dl>

 

 





