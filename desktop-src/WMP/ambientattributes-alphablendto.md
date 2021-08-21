---
title: AmbientAttributes.alphaBlendTo
description: O método alphaBlendTo ajusta a propriedade alphaBlend durante um período de tempo.
ms.assetid: 5cb259bd-3010-4086-be9d-65022be297b7
keywords:
- AmbientAttributes.alphaBlendTo Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.alphaBlendTo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a8e0e29df897d070cd4d337e27a7f5f7f7e3a86c7f44a784afadb5bc203674ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055223"
---
# <a name="ambientattributesalphablendto"></a>AmbientAttributes.alphaBlendTo

O **método alphaBlendTo** ajusta a **propriedade alphaBlend** durante um período de tempo.

``` syntax
        elementID.alphaBlendTo(newVal, alphaTime)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="newVal"></span><span id="newval"></span><span id="NEWVAL"></span>*newVal*
</dt> <dd>

**Número** (longo) especificando o novo valor de opacidade. Varia de 0 (sem opacidade) a 255 (opacidade completa).

</dd> <dt>

<span id="alphaTime"></span><span id="alphatime"></span><span id="ALPHATIME"></span>*alphaTime*
</dt> <dd>

**Number** (**long**) especificando o tempo, em milissegundos, que leva o elemento para alterar a opacidade.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é útil para fazer com que os elementos apareçam ou desapareçam gradualmente.

Quando você usa **alphaBlendTo** com um **elemento TEXT** que não tem **o backgroundColor** especificado, uma cor da tela de fundo preta será usada. Se a cor de primeiro plano também for preta (que é o valor padrão para *TEXT.***foregroundColor**), seu texto pode se tornar ilegível. Para evitar isso, sempre especifique o **atributo backgroundColor** ou de definir **foregroundColor** como uma cor diferente de preto.

> [!Note]  
> Não há suporte para esse atributo no Windows 98.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.alphaBlend**](ambientattributes-alphablend.md)
</dt> <dt>

[**Elemento TEXT**](text-element.md)
</dt> <dt>

[**TEXT.backgroundColor**](text-backgroundcolor.md)
</dt> <dt>

[**TEXT.foregroundColor**](text-foregroundcolor.md)
</dt> </dl>

 

 





