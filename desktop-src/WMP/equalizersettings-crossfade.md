---
title: EQUALIZERSETTINGS. fading cruzado
description: O atributo fading cruzado especifica ou recupera um valor que indica se o esmaecimento cruzado está habilitado.
ms.assetid: 6c5a31f3-982e-4660-80ff-30b7a4290a15
keywords:
- EQUALIZERSETTINGS. fading cruzado Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.crossFade
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0472f90f94b5c4ba56948848476b6585502427c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760448"
---
# <a name="equalizersettingscrossfade"></a>EQUALIZERSETTINGS. fading cruzado

O atributo **fading cruzado** especifica ou recupera um valor que indica se o esmaecimento cruzado está habilitado.

``` syntax
        elementID.crossFade
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                      |
|-------|----------------------------------|
| true  | O esmaecimento cruzado está habilitado.           |
| false | Padrão. O esmaecimento cruzado está desabilitado. |



 

## <a name="remarks"></a>Comentários

Cross-esmaecimento é um recurso de processamento de áudio que diminui gradualmente o volume de um item de mídia próximo ao final de sua reprodução enquanto inicia simultaneamente a reprodução do próximo item de mídia no volume mínimo e o aumenta gradualmente para o volume normal. A sobreposição entre o início do segundo item de mídia e o final do primeiro item de mídia é especificado pelo atributo **crossFadeWindow** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EQUALIZERSETTINGS**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS.crossFadeWindow**](equalizersettings-crossfadewindow.md)
</dt> </dl>

 

 





