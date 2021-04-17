---
title: ErrorItem.errorContext
description: A propriedade errorContext recupera um valor que indica o contexto do erro.
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- ErrorItem. errorContext Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813163"
---
# <a name="erroritemerrorcontext"></a>ErrorItem.errorContext

A propriedade **errorContext** recupera um valor que indica o contexto do erro.

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma **cadeia de caracteres** somente leitura que representa o código de contexto de erro.

## <a name="remarks"></a>Comentários

O contexto de erro é uma informação que é usada pela Microsoft para fornecer informações adicionais para a equipe de suporte técnico.

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna uma cadeia de caracteres vazia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/>                               |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





