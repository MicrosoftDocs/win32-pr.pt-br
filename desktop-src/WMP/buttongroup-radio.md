---
title: BUTTONGROUP.radio
description: O atributo de rádio especifica ou recupera um valor que indica se BUTTONGROUP é composto por botões de rádio.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- BUTTONGROUP.radio Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56a8a9f85a3dce5ef070519f436c28ec157f7aa467a9115bcd8e2ccefa6444f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997766"
---
# <a name="buttongroupradio"></a>BUTTONGROUP.radio

O **atributo** de rádio especifica ou recupera um valor que indica se **BUTTONGROUP** é composto por botões de rádio.

``` syntax
        elementID.radio
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um booliana **de leitura/gravação.**



| Valor | Descrição                                      |
|-------|--------------------------------------------------|
| true  | O **BUTTONGROUP é** o estilo de rádio.              |
| false | Padrão. O **BUTTONGROUP não** é um estilo de rádio. |



 

## <a name="remarks"></a>Comentários

Se **a rádio** for definida como true, todos os elementos **BUTTONELEMENT** no **BUTTONGROUP** serão ativos, mas apenas um botão de cada vez estará no estado de inatividade.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BUTTONELEMENT.sticky**](buttonelement-sticky.md)
</dt> <dt>

[**Elemento BUTTONGROUP**](buttongroup-element.md)
</dt> </dl>

 

 





