---
title: EFFECTS.effectType
description: O método effectType recupera o nome do Registro da visualização com o índice do Registro especificado. Esse nome é uma ID exclusiva definida pelo autor da visualização.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- EFFECTS.effectType Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a452f9218c7004d1078ae6b9e878421a7cad301f3ee913ef6296aaa1c681b736
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117749228"
---
# <a name="effectseffecttype"></a>EFFECTS.effectType

O **método effectType** recupera o nome do Registro da visualização com o índice do Registro especificado. Esse nome é uma ID exclusiva definida pelo autor da visualização.

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*Índice*
</dt> <dd>

**Número** (**longo**) que contém o índice do Registro de uma visualização.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna uma **Cadeia de Caracteres**.

## <a name="remarks"></a>Comentários

Esse método é útil para alternar entre visualizações no script. Uma interface do usuário pode exibir o conjunto de títulos, mas quando o usuário seleciona um, o script deve usar **currentEffectType** para alternar as visualizações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EFFECTS**](effects-element.md)
</dt> <dt>

[**EFFECTS.currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





