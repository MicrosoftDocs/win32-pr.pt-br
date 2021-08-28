---
title: EQUALIZERSETTINGS.gainLevel3
description: O atributo gainLevel3 especifica ou recupera o nível de ganho da banda 3.
ms.assetid: 508d00c6-2429-4f35-b7ab-bf30f774e614
keywords:
- EQUALIZERSETTINGS.gainLevel3 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8e719cd59a253ded35ad10e067f537d6f7d3a68d0d0b05a4cf79d0cd976f5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123646"
---
# <a name="equalizersettingsgainlevel3"></a>EQUALIZERSETTINGS.gainLevel3

O **atributo gainLevel3** especifica ou recupera o nível de ganho da banda 3.

``` syntax
        elementID.gainLevel3
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um número de leitura/gravação **(** **float**) com um valor normalmente variando de 20 a +20. Ele tem um valor padrão de zero.

## <a name="remarks"></a>Comentários

Esse atributo ajusta a parte do espectro de frequência de áudio centralizada em 125Hz.

Se esse atributo não for especificado, o valor anterior será mantido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS. gainLevels**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 





