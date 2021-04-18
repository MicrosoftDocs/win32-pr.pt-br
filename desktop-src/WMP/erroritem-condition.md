---
title: ErrorItem. Condition
description: A Propriedade Condition recupera um valor que indica a condição do erro.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ErrorItem. Condition Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c498e7479a7a3e067dea2d8a562800351effd672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759715"
---
# <a name="erroritemcondition"></a>ErrorItem. Condition

A propriedade **Condition** recupera um valor que indica a condição do erro.

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um **número** somente leitura (**Long**) que representa o código de condição.

## <a name="remarks"></a>Comentários

O código de condição é um valor que é usado pela Microsoft para fornecer informações adicionais para a equipe de suporte técnico.

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





