---
title: Ambienteattributes. alphaBlendTo
description: O método alphaBlendTo ajusta a propriedade alphaBlend ao longo de um período de tempo.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- AlphaBlendTo do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16b21e78de3510e2e4a58c7214995f7888f778c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800172"
---
# <a name="ambientattributesalphablendto"></a>Ambienteattributes. alphaBlendTo

O método **alphaBlendTo** ajusta a propriedade **alphaBlend** ao longo de um período de tempo.

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*
</dt> <dd>

**Número** (longo) que especifica o novo valor de opacidade. Varia de 0 (sem opacidade) a 255 (opacidade total).

</dd> <dt>

<span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphatime*
</dt> <dd>

**Número** (**longo**) que especifica o tempo, em milissegundos, que leva o elemento para alterar a opacidade.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é útil para fazer com que os elementos apareçam gradualmente ou desapareçam.

Quando você usa **alphaBlendTo** com um elemento de **texto** que não tem o **backgroundColor** especificado, uma cor de plano de fundo de preto será usada. Se a cor de primeiro plano também for preta (que é o valor padrão para *texto*.**foregroundColor**), seu texto pode se tornar ilegível. Para evitar isso, sempre especifique o atributo **backgroundColor** ou defina **foregroundColor** como uma cor diferente de preto.

> [!Note]  
> Não há suporte para esse atributo no Windows 98.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**Ambienteattributes. alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**Elemento de texto**](text-element.md)
</dt> <dt>

[**TEXT. backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TEXT. foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





