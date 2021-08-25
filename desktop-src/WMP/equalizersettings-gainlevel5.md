---
title: EQUALIZERSETTINGS.gainLevel5
description: O atributo gainLevel5 especifica ou recupera o nível de ganho da banda 5.
ms.assetid: 6077a4dc-b9b8-4e00-8b29-14afe5a44321
keywords:
- EQUALIZERSETTINGS.gainLevel5 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel5
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40a075a518eb27bbfe3ac29f8689afca323037373de518d27e95d1724f1c7364
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862866"
---
# <a name="equalizersettingsgainlevel5"></a>EQUALIZERSETTINGS.gainLevel5

O **atributo gainLevel5** especifica ou recupera o nível de ganho da banda 5.

``` syntax
        elementID.gainLevel5
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um número de leitura/gravação **(** **float**) com um valor normalmente variando de 20 a +20. Ele tem um valor padrão de zero.

## <a name="remarks"></a>Comentários

Esse atributo ajusta a parte do espectro de frequência de áudio centralizada em 500Hz.

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

 

 





