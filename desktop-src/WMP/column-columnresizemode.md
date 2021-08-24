---
title: COLUMN.columnResizeMode
description: O atributo columnResizeMode especifica ou recupera o modo de resize para essa coluna.
ms.assetid: 95ece2a3-20a6-4b9d-a2eb-fc69fc612f29
keywords:
- COLUMN.columnResizeMode Windows Media Player
topic_type:
- apiref
api_name:
- COLUMN.columnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c59046aa76c01a1439e5db8f0fb6850e7df74d874cba555d1f9c3829f09d9598
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763996"
---
# <a name="columncolumnresizemode"></a>COLUMN.columnResizeMode

O **atributo columnResizeMode** especifica ou recupera o modo de resize para essa coluna.

``` syntax
        elementID.columnResizeMode
```

## <a name="possible-values"></a>Valores possíveis

Esse atributo é uma cadeia de **caracteres** de leitura/gravação que contém um dos valores a seguir.



| Valor          | Descrição                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | Padrão. A coluna é relize para acomodar todos os dados na coluna e no header.                         |
| AutosizeData   | A coluna é relize para acomodar todos os dados somente na coluna.                                                 |
| Fixo          | A coluna é um tamanho fixo.                                                                                    |
| Trechos      | A coluna é reorganizada para usar o espaço restante no controle **PLAYLIST** depois que todas as outras colunas são resized. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento COLUMN**](column-element.md)
</dt> </dl>

 

 





