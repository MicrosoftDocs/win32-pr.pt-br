---
title: EQUALIZERSETTINGS.gainLevel2
description: O atributo gainLevel2 especifica ou recupera o nível de ganho da banda 2.
ms.assetid: e602d9cc-42b3-402e-9df5-8b970d878904
keywords:
- EQUALIZERSETTINGS.gainLevel2 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe4979cb44fbd39b37acd29fe8e3303c879c45b40dfafc554180dad5301f0b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339826"
---
# <a name="equalizersettingsgainlevel2"></a>EQUALIZERSETTINGS.gainLevel2

O **atributo gainLevel2** especifica ou recupera o nível de ganho da banda 2.

``` syntax
        elementID.gainLevel2
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um número de leitura/gravação **(** **float**) com um valor normalmente variando de 20 a +20. Ele tem um valor padrão de zero.

## <a name="remarks"></a>Comentários

Esse atributo ajusta a parte do espectro de frequência de áudio centralizada em 62Hz.

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

 

 





