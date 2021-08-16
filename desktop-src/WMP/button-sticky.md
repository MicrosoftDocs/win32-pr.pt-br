---
title: BUTTON.sticky
description: O atributo sticky especifica ou recupera um valor que indica se BUTTON é uma alternância, ou seja, se é um BUTTON de dois estados ou de estado único.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- BUTTON.sticky Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9c6a2cf1523cf2384142bd6ffd47cb5e42e7851dc96b6e236343c5ba670aa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342741"
---
# <a name="buttonsticky"></a>BUTTON.sticky

O **atributo sticky** especifica ou recupera um valor que indica se **o BUTTON** é uma alternância, ou seja, se é um BUTTON de dois estados ou de estado **único.**

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um booliana **de leitura/gravação.**



| Valor | Descrição                        |
|-------|------------------------------------|
| true  | **BUTTON** é sticky.              |
| false | Padrão. **BUTTON** não é sticky. |



 

## <a name="remarks"></a>Comentários

Se **sticky** for definido como true, **o BOTÃO** será alterado para o estado para baixo quando clicado e permanecerá nesse estado até ser clicado novamente. Quando **o BUTTON** estiver no estado ino mesmo, o atributo **down** será true e **a downImage** será exibida.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BUTTON.down**](button-down.md)
</dt> <dt>

[**BUTTON.downImage**](button-downimage.md)
</dt> </dl>

 

 





