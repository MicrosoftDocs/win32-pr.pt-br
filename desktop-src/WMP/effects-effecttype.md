---
title: EFFECTs. effecttype
description: O método effecttype recupera o nome do registro da visualização com o índice de registro especificado. Esse nome é uma ID exclusiva definida pelo autor da visualização.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- EFFECTs. effecttype Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3eda9cbd1a4634062683536f1f132393a2874691
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813166"
---
# <a name="effectseffecttype"></a>EFFECTs. effecttype

O método **effecttype** recupera o nome do registro da visualização com o índice de registro especificado. Esse nome é uma ID exclusiva definida pelo autor da visualização.

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*index*
</dt> <dd>

**Número** (**longo**) que contém o índice de uma visualização do registro.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna uma **cadeia de caracteres**.

## <a name="remarks"></a>Comentários

Esse método é útil para alternar entre visualizações no script. Uma interface do usuário pode exibir o conjunto de títulos, mas quando o usuário seleciona um, o script deve usar **currentEffectType** para alternar as visualizações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EFFECTs**](effects-element.md)
</dt> <dt>

[**EFFECTs. currentEffectType**](effects-currenteffecttype.md)
</dt> </dl>

 

 





