---
title: ErrorItem.customUrl
description: A propriedade customURL recupera a URL de um site que exibe informações específicas sobre falha de download do codec.
ms.assetid: 51028f45-2ce6-4e57-86bd-d7c2d8fb3af8
keywords:
- ErrorItem.customUrl Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.customUrl
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acccf086fc9b620243667aadac50ec2f727ab6951b2770cd2c8b21d5ea41b683
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118577832"
---
# <a name="erroritemcustomurl"></a>ErrorItem.customUrl

A **propriedade customURL** recupera a URL de um site que exibe informações específicas sobre falha de download do codec.

``` syntax
player.error.item(
        index
        ).customURL
      
```

## <a name="possible-values"></a>Valores possíveis

Essa propriedade é uma Cadeia de Caracteres somente **leitura.**

## <a name="remarks"></a>Comentários

**Windows Media Player 10 Mobile:** Essa propriedade sempre retorna uma cadeia de caracteres vazia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7.0 ou posterior.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Objeto ErrorItem**](erroritem-object.md)
</dt> </dl>

 

 





