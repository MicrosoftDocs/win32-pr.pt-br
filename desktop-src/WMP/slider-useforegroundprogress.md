---
title: SLIDER.useForegroundProgress
description: O atributo useForegroundProgress especifica ou recupera um valor que indica se a barra de progresso em primeiro plano será usada.
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- SLIDER.useForegroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 563f5776791ba0f140dfe907facf85965bddbdc8fc69f35185f72e3de95518fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832552"
---
# <a name="slideruseforegroundprogress"></a>SLIDER.useForegroundProgress

O **atributo useForegroundProgress** especifica ou recupera um valor que indica se a barra de progresso em primeiro plano será usada.

``` syntax
        elementID.useForegroundProgress
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um booliana **de leitura/gravação.**



| Valor | Descrição                              |
|-------|------------------------------------------|
| true  | Use o progresso em primeiro plano.                 |
| false | Padrão. Não use o progresso em primeiro plano. |



 

## <a name="remarks"></a>Comentários

Esse atributo permite o uso do atributo **foregroundProgress,** que é usado principalmente para acompanhar o progresso do download de um arquivo de mídia enquanto acompanha simultaneamente a posição de reprodução atual do arquivo usando o atributo **value.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento SLIDER**](slider-element.md)
</dt> <dt>

[**SLIDER.foregroundProgress**](slider-foregroundprogress.md)
</dt> <dt>

[**SLIDER.value**](slider-value.md)
</dt> </dl>

 

 





