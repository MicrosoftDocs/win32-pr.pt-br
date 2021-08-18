---
title: EFFECTS.currentEffectType
description: O atributo currentEffectType especifica ou recupera o nome do Registro da visualização atual. Esse nome é uma ID exclusiva definida pelo autor da visualização.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- EFFECTS.currentEffectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8df55ae806781fa0924349cfe472f355cdabd2be6723148fc6100dc39efd9062
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996746"
---
# <a name="effectscurrenteffecttype"></a>EFFECTS.currentEffectType

O **atributo currentEffectType** especifica ou recupera o nome do Registro da visualização atual. Esse nome é uma ID exclusiva definida pelo autor da visualização.

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de caracteres de **leitura/gravação.**

## <a name="remarks"></a>Comentários

Você pode usar esse atributo em tempo de executar para alterar o efeito exibido no momento. Para fazer isso, execute estas etapas:

1.  Use **effectCount** para recuperar a contagem de efeitos registrados.
2.  Em um loop, recupere o nome de cada efeito registrado usando **effectType**.
3.  Especifique um dos nomes recuperados para **currentEffectType** para definir o efeito atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EFFECTS**](effects-element.md)
</dt> <dt>

[**EFFECTS.currentEffect**](effects-currenteffect.md)
</dt> <dt>

[**EFFECTS.effectCount**](effects-effectcount.md)
</dt> <dt>

[**EFFECTS.effectType**](effects-effecttype.md)
</dt> </dl>

 

 





