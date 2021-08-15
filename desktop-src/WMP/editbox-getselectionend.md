---
title: GetSelectionEnd de edição
description: O método getSelectionEnd recupera a posição final do texto selecionado no controle admy.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- GetSelectionEnd Windows Media Player de edição
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8dff56bda802286ed76ba3b448478dfa57d005c13baf229612e190bbf163b25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838840"
---
# <a name="editboxgetselectionend"></a>GetSelectionEnd de edição

O método **getSelectionEnd** recupera a posição final do texto selecionado no controle admy.

``` syntax
        elementID.getSelectionEnd()
```

## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **número** (**longo**).

## <a name="remarks"></a>Comentários

Se nenhum texto for selecionado, esse método retornará a posição do ponto de inserção.

Se o controle for Multiline, esse método retornará o índice de caracteres no controle, não o índice de linha.

Esse método só pode ser chamado depois que o controle se tornar visível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento admy**](editbox-element.md)
</dt> <dt>

[**GetSelectionStart de edição**](editbox-getselectionstart.md)
</dt> <dt>

[**ReplaceSelection de edição**](editbox-replaceselection.md)
</dt> <dt>

[**Autoseleção de myselecting**](editbox-setselection.md)
</dt> </dl>

 

 





