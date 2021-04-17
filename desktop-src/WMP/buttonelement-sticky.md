---
title: BUTTONelement. adesivo
description: O atributo adesivo especifica ou recupera um valor que indica se o BUTTONelement é uma alternância, ou seja, se é um botão de dois Estados ou de estado único.
ms.assetid: a7e74f70-9fa6-45a1-ab65-2db107e13551
keywords:
- BUTTONelement. adesivo do Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 713b26fdee3062fbe803d05e034bc9896cdd5563
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105762096"
---
# <a name="buttonelementsticky"></a>BUTTONelement. adesivo

O atributo **adesivo** especifica ou recupera um valor que indica se o **buttonelement** é uma alternância, ou seja, se é um botão de dois Estados ou de estado único.

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                               |
|-------|-------------------------------------------|
| true  | **Buttonelement** é adesivo.              |
| false | Padrão. **Buttonelement** não é adesivo. |



 

## <a name="remarks"></a>Comentários

Se o atributo **adesivo** for definido como true, o elemento Button será alterado para o estado Down quando for clicado e permanecerá nesse estado até ser clicado novamente. Quando o elemento Button estiver no estado down, o atributo **down** será true e a parte apropriada do grupo de botões **downImage** será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTONelement**](buttonelement-element.md)
</dt> <dt>

[**BOTÃO. para baixo**](buttonelement-down.md)
</dt> <dt>

[**BUTTON. downImage**](buttongroup-downimage.md)
</dt> </dl>

 

 





