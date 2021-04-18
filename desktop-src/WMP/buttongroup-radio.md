---
title: BOTÃO de opção. Radio
description: O atributo Radio especifica ou recupera um valor que indica se o botão é composto por botões de opção.
ms.assetid: f84479f8-af4f-4ca8-991e-1c2ab39d7110
keywords:
- O Windows Media Player. Radio
topic_type:
- apiref
api_name:
- BUTTONGROUP.radio
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e1765a7756aedcebc2b7b030634d8598a5cd89e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784907"
---
# <a name="buttongroupradio"></a>BOTÃO de opção. Radio

O atributo **Radio** especifica ou recupera um valor que indica se o **botão** é composto por botões de opção.

``` syntax
        elementID.radio
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                                      |
|-------|--------------------------------------------------|
| true  | O tipo de **botão** é estilo de rádio.              |
| false | Padrão. O **botão** de opção não é estilo de rádio. |



 

## <a name="remarks"></a>Comentários

Se **Radio** for definido como true, todos os elementos **buttonelement** no grupo de **botões** serão adesivos, mas apenas um botão por vez estará no estado inoperante.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BUTTONelement. adesivo**](buttonelement-sticky.md)
</dt> <dt>

[**Elemento de botão**](buttongroup-element.md)
</dt> </dl>

 

 





