---
title: EFFECTs. currentEffectType
description: O atributo currentEffectType especifica ou recupera o nome do registro da visualização atual. Esse nome é uma ID exclusiva definida pelo autor da visualização.
ms.assetid: 29469272-468d-49b4-a934-e7dc00583efa
keywords:
- EFFECTs. currentEffectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7c7671c4a5dce9df81cf8f9d770d71eba3325e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760450"
---
# <a name="effectscurrenteffecttype"></a>EFFECTs. currentEffectType

O atributo **currentEffectType** especifica ou recupera o nome do registro da visualização atual. Esse nome é uma ID exclusiva definida pelo autor da visualização.

``` syntax
        elementID.currentEffectType
```

## <a name="possible-values"></a>Valores possíveis

Este atributo é uma **cadeia de caracteres** de leitura/gravação.

## <a name="remarks"></a>Comentários

Você pode usar esse atributo em tempo de execução para alterar o efeito exibido no momento. Para fazer isso, siga estas etapas:

1.  Use **effectCount** para recuperar a contagem de efeitos registrados.
2.  Em um loop, recupere o nome de cada efeito registrado usando **effecttype**.
3.  Especifique um dos nomes que você recuperou para **currentEffectType** para definir o efeito atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EFFECTs**](effects-element.md)
</dt> <dt>

[**EFFECTs. currentEffect**](effects-currenteffect.md)
</dt> <dt>

[**EFFECTs. effectCount**](effects-effectcount.md)
</dt> <dt>

[**EFFECTs. effecttype**](effects-effecttype.md)
</dt> </dl>

 

 





