---
title: EFFECTS.currentEffect
description: O atributo currentEffect especifica ou recupera a visualização atual.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- EFFECTS.currentEffect Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d9ac47ef88d1a0bce4982f71ce2e20e33f48933c9916bbb1e62085b5a1e5178
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996866"
---
# <a name="effectscurrenteffect"></a>EFFECTS.currentEffect

O **atributo currentEffect** especifica ou recupera a visualização atual.

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um objeto de **leitura/gravação.** O valor padrão é a primeira visualização na ordem de autor. Se não houver visualizações na capa, o padrão será a primeira visualização no Registro.

## <a name="remarks"></a>Comentários

Você pode usar esse objeto para acessar visualizações personalizadas criadas. Por exemplo, você pode expor uma propriedade por meio da interface **IDispatch** em sua visualização. Em seguida, você pode alterar o valor da propriedade da sua capa tornando a visualização o efeito atual e, em seguida, usando o objeto **currentEffect** para definir um novo valor para a propriedade . Por exemplo, se sua visualização expõe uma propriedade chamada backgroundColor, o código JScript seguinte especifica um novo valor:


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EFFECTS**](effects-element.md)
</dt> <dt>

[**EFFECTS.currentEffectTitle**](effects-currenteffecttitle.md)
</dt> <dt>

[**EFFECTS.currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





