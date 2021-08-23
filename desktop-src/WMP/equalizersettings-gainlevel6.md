---
title: EQUALIZERSETTINGS.gainLevel6
description: O atributo gainLevel6 especifica ou recupera o nível de ganho da banda 6. Ele tem um valor padrão de zero.
ms.assetid: da3e1df5-434b-44db-bcde-8ad9c9874627
keywords:
- EQUALIZERSETTINGS.gainLevel6 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel6
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7238fc2d90828bdae8e3a4c0ca7cf3700462cd27b7a180169e4a7293c1ae3472
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650926"
---
# <a name="equalizersettingsgainlevel6"></a>EQUALIZERSETTINGS.gainLevel6

O **atributo gainLevel6** especifica ou recupera o nível de ganho da banda 6. Ele tem um valor padrão de zero.

``` syntax
        elementID.gainLevel6
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um número de leitura/gravação **(** **float**) com um valor normalmente variando de 20 a +20. Ele tem um valor padrão de zero.

## <a name="remarks"></a>Comentários

Esse atributo ajusta a parte do espectro de frequência de áudio centralizada em 1kHz.

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

 

 





