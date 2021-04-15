---
title: CUSTOMSLIDER. Value
description: O atributo Value especifica ou recupera a posição atual do controle deslizante. | CUSTOMSLIDER. Value
ms.assetid: 29e17f48-1848-458d-9da4-316013b21980
keywords:
- CUSTOMSLIDER. Value Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89be4edd43fc79c8a8938a3861c982068760bcf3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761105"
---
# <a name="customslidervalue"></a>CUSTOMSLIDER. Value

O atributo **Value** especifica ou recupera a posição atual do controle deslizante.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**float**) com um valor padrão igual ao atributo **min** .

## <a name="remarks"></a>Comentários

O **valor** deve ser maior ou igual a **mín** . e menor ou igual a **máx**. Se o valor cai fora do intervalo, um aviso é emitido e o valor não é alterado.

## <a name="examples"></a>Exemplos

Consulte o atributo [positionImage](customslider-positionimage.md) para obter um exemplo ilustrando como os atributos do elemento **CUSTOMSLIDER** são usados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento CUSTOMSLIDER**](customslider-element.md)
</dt> </dl>

 

 





