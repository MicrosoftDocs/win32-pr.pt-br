---
title: BOTÃO. adesivo
description: O atributo adesivo especifica ou recupera um valor que indica se o botão é uma alternância, ou seja, se é um botão de dois Estados ou de estado único.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- BOTÃO. autoadesiva Windows Media Player
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
# <a name="buttonsticky"></a>BOTÃO. adesivo

O atributo **adesivo** especifica ou recupera um valor que indica se o **botão** é uma alternância, ou seja, se é um **botão** de dois Estados ou de estado único.

``` syntax
        elementID.sticky
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é um **booliano** de leitura/gravação.



| Valor | Descrição                        |
|-------|------------------------------------|
| true  | O **botão** é adesivo.              |
| false | Padrão. O **botão** não é adesivo. |



 

## <a name="remarks"></a>Comentários

Se **adesivo** estiver definido como true, o **botão** será alterado para o estado Down quando clicado e permanecerá nesse estado até que seja clicado novamente. Quando o **botão** estiver no estado inativo, o atributo **down** será true e o **downImage** será exibido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento BUTTON**](button-element.md)
</dt> <dt>

[**BOTÃO. para baixo**](button-down.md)
</dt> <dt>

[**BUTTON. downImage**](button-downimage.md)
</dt> </dl>

 

 





