---
title: EFFECTs. currentEffect
description: O atributo currentEffect especifica ou recupera a visualização atual.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- EFFECTs. currentEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105796429"
---
# <a name="effectscurrenteffect"></a>EFFECTs. currentEffect

O atributo **currentEffect** especifica ou recupera a visualização atual.

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é um **objeto** de leitura/gravação. O valor padrão é a primeira visualização na ordem de criação. Se não houver visualizações criadas na capa, o padrão será a primeira visualização no registro.

## <a name="remarks"></a>Comentários

Você pode usar esse objeto para acessar visualizações personalizadas que você criou. Por exemplo, você pode expor uma propriedade por meio da interface **IDispatch** em sua visualização. Em seguida, você pode alterar o valor da propriedade de sua capa, tornando a visualização o efeito atual e, em seguida, usando o objeto **currentEffect** para definir um novo valor para a propriedade. Por exemplo, se sua visualização expõe uma propriedade chamada backgroundColor, o seguinte código JScript especifica um novo valor:


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EFFECTs**](effects-element.md)
</dt> <dt>

[**EFFECTs. currentEffectTitle**](effects-currenteffecttitle.md)
</dt> <dt>

[**EFFECTs. currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





