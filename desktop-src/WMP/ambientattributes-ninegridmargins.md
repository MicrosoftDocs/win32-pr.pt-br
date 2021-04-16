---
title: Ambienteattributes. nineGridMargins
description: O atributo nineGridMargins especifica larguras de margem para o dimensionamento não uniforme do elemento de capa.
ms.assetid: b8a7efd0-6c12-4436-9d53-0dcfa1600aa5
keywords:
- NineGridMargins do Windows Media Player de ambiente.
topic_type:
- apiref
api_name:
- AmbientAttributes.nineGridMargins
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cf77c1fcfdb64fb9e4b0dde8753572255c17eda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105794529"
---
# <a name="ambientattributesninegridmargins"></a>Ambienteattributes. nineGridMargins

O atributo **nineGridMargins** especifica larguras de margem para o dimensionamento não uniforme do elemento de capa.

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma **cadeia de caracteres** de leitura/gravação que contém as larguras das margens no formato "*widthLeft*,*widthTop*,*widthRight*,*widthBottom*". Cada valor de largura é um número que representa a largura, em pixels, de uma margem para a nove grade.

## <a name="remarks"></a>Comentários

Uma *grade nove* é uma técnica usada para dividir elementos da interface do usuário em nove regiões retangulares organizadas em uma matriz 3 por 3. Quando um elemento é redimensionado, as nove regiões de grade podem cada escala por um fator diferente.

Cada um dos quatro valores de largura que você especifica representa a largura de uma linha ou coluna de três regiões adjacentes. Cada linha ou coluna formam o lado esquerdo, superior, lado direito ou inferior da grade nove.

[Ambienteattributes. resizeImages](ambientattributes-resizeimages.md) deve ser definido como true para que esse atributo funcione.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributos de ambiente**](ambient-attributes.md)
</dt> </dl>

 

 





