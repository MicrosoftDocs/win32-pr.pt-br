---
title: ErrorItem.condition
description: A propriedade condition recupera um valor que indica a condição do erro.
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ErrorItem.condition Windows Media Player
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
ms.openlocfilehash: a5f4bfe2c4b2b517b0fd300a0c6465ae9f10147518937822212b621d808f0ded
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996636"
---
# <a name="erroritemcondition"></a>ErrorItem.condition

A **propriedade** condition recupera um valor que indica a condição do erro.

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é um Número somente **leitura** (**long**) que representa o código de condição.

## <a name="remarks"></a>Comentários

O código de condição é um valor usado pela Microsoft para fornecer informações adicionais para a equipe de suporte técnico.

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna 0.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player Série 9 ou posterior.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





