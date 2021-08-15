---
title: EQUALIZERSETTINGS.crossFade
description: O atributo crossFade especifica ou recupera um valor que indica se o esmaeçamento cruzado está habilitado.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS.crossFade Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ff38ee7634f31da7717bfca015ebaacd88796d9c8186faef155704a449bbb07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838621"
---
# <a name="equalizersettingscrossfade"></a>EQUALIZERSETTINGS.crossFade

O **atributo crossFade** especifica ou recupera um valor que indica se o esmaeçamento cruzado está habilitado.

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um booliana **de leitura/gravação.**



| Valor | Descrição                      |
|-------|----------------------------------|
| true  | O esmaeçando cruzado está habilitado.           |
| false | Padrão. O esmaeçando cruzado está desabilitado. |



 

## <a name="remarks"></a>Comentários

O esmaeçamento cruzado é um recurso de processamento de áudio que diminui gradualmente o volume de um item de mídia próximo ao final de sua reprodução, iniciando simultaneamente a reprodução do próximo item de mídia no volume mínimo e aumentando-o gradualmente para o volume normal. A sobreposição entre o início do segundo item de mídia e o final do primeiro item de mídia é especificada pelo **atributo crossFadeWindow.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.crossFadeWindow**](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





