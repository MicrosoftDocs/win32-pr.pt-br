---
title: EQUALIZERSETTINGS.gainLevels
description: O atributo gainLevels especifica ou recupera o nível de lucro da faixa correspondente ao índice fornecido.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- EQUALIZERSETTINGS. gainLevels Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800143"
---
# <a name="equalizersettingsgainlevels"></a>EQUALIZERSETTINGS.gainLevels

O atributo **gainLevels** especifica ou recupera o nível de lucro da faixa correspondente ao índice fornecido.

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **número** de leitura/gravação (**float**) com um valor normalmente que varia de 20 a + 20.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*a banda*
</dt> <dd>

**Número**(**longo**) entre 1 e 10 indicando o índice da banda.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse atributo usa um parâmetro, mas seu valor é especificado no código do script da mesma forma que outros valores de atributo. Ele não pode ser especificado no elemento EQUALIZERSETTINGS, nem pode ser usado com o atributo de escuta **wmpprop** . Em vez disso, os atributos de nível de lucro numerados são fornecidos para essas situações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**Atributos de escuta**](listening-attributes.md)
</dt> </dl>

 

 





