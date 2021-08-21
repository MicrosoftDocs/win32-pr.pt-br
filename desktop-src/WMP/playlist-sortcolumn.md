---
title: PLAYLIST. sortColumn
description: O método sortColumn classifica os dados na coluna especificada.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- Windows Media Player de PLAYLIST. sortColumn
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34dfce7306ceb39d64665538a21dbaef965ea799141a2756c2fea5bbe23ea9cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335649"
---
# <a name="playlistsortcolumn"></a>PLAYLIST. sortColumn

O método **SortColumn** classifica os dados na coluna especificada.

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*pilha*
</dt> <dd>

**Número** (**longo**) indicando o índice da coluna a ser classificada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método classifica a coluna especificada da mesma maneira que os botões de cabeçalho de coluna no elemento **playlist** . Se a coluna ainda não tiver sido classificada, ela será classificada em ordem alfanumérica. Se ele tiver sido classificado, sua ordem será invertida.

Para que esse método funcione, o atributo **allowColumnSorting** deve ser definido como true.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------------------------|
| Versão<br/> | Windows Media Player versão 7,0 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. allowColumnSorting**](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





