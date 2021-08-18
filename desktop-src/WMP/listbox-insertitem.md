---
title: LISTBOX. insertItem
description: O método insertItem insere o texto especificado no índice especificado no controle da caixa de listagem.
ms.assetid: c45eb75e-074d-4f3f-bfdd-6c3cbbd71f54
keywords:
- Windows Media Player LISTBOX. insertItem
topic_type:
- apiref
api_name:
- LISTBOX.insertItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0344bbc9fbe4f8f2b680866f70c0fe16398ad08cbf4a916c454223fdff04614e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135299"
---
# <a name="listboxinsertitem"></a>LISTBOX. insertItem

O método **insertItem** insere o texto especificado no índice especificado no controle da caixa de listagem.

``` syntax
        elementID.insertItem(index, text)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*index*
</dt> <dd>

**Número** (**longo**) que contém o índice da linha a ser recuperada.

</dd> <dt>

<span id="text"></span><span id="TEXT"></span>*texto*
</dt> <dd>

**Cadeia de caracteres** que contém o texto a ser inserido.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Quando uma linha é inserida, os índices de linha para as linhas abaixo da linha inserida aumentam em uma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





