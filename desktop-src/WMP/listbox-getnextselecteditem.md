---
title: LISTBOX. getNextSelectedItem
description: O método getNextSelectedItem recupera o próximo item selecionado no controle caixa de listagem, começando no item após aquele com o índice especificado.
ms.assetid: 060d196d-2b14-4386-ba01-34256c137db5
keywords:
- Windows Media Player LISTBOX. getNextSelectedItem
topic_type:
- apiref
api_name:
- LISTBOX.getNextSelectedItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f4a5d95880b1300ebfb7f1732e7c20b6975ad82cf2d15514c58e68b9f9c42cc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003396"
---
# <a name="listboxgetnextselecteditem"></a>LISTBOX. getNextSelectedItem

O método **getNextSelectedItem** recupera o próximo item selecionado no controle caixa de listagem, começando no item após aquele com o índice especificado.

``` syntax
        elementID.getNextSelectedItem(startIndex)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*
</dt> <dd>

**Número** (**longo**) que contém o índice do item que precede o item que está sendo recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **número** (**Long**) que contém o índice do próximo item selecionado.

## <a name="remarks"></a>Comentários

Para iniciar a pesquisa desde o início, use 1 para o índice inicial.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





