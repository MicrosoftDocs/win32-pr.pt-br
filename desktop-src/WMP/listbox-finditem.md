---
title: LISTBOX. findItem
description: O método findItem pesquisa uma determinada cadeia de caracteres começando com o item após o índice de item especificado.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- LISTBOX. findItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161f4dd8b93fe4fed6a794dffde3e58e840c74e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760511"
---
# <a name="listboxfinditem"></a>LISTBOX. findItem

O método **findItem** pesquisa uma determinada cadeia de caracteres começando com o item após o índice de item especificado.

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*
</dt> <dd>

**Número** (**longo**) que contém o índice do item no qual iniciar a pesquisa.

</dd> <dt>

<span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*
</dt> <dd>

**Cadeia de caracteres** que contém o texto a ser pesquisado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **número** (**Long**) que contém o índice do item que contém a cadeia de caracteres.

## <a name="remarks"></a>Comentários

Para iniciar a pesquisa na primeira linha do controle caixa de listagem, use 1 como o *startIndex*. Para continuar pesquisando texto após a primeira linha ser encontrada, use o índice de linha retornado como *startIndex* e a pesquisa será iniciada na próxima linha. Esse método irá procurar subcadeias de caracteres e não diferencia maiúsculas de minúsculas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





