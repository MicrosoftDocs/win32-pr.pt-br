---
title: BOTÃO. adesivo
description: O atributo adesivo especifica ou recupera um valor que indica se o botão é uma alternância, ou seja, se é um botão de dois Estados ou de estado único.
ms.assetid: aa0b48b4-29ce-440c-aeb9-dce31ab3cb63
keywords:
- BOTÃO. autoadesiva do Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.sticky
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8de9b4e1a8e4bab04e5729cb45662164e2dfa2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813379"
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

 

 





