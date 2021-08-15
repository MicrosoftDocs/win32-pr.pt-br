---
title: GetSelectionStart de edição
description: O método getSelectionStart recupera a posição inicial do texto selecionado no controle admy.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- GetSelectionStart Windows Media Player de edição
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionStart
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c555cc7231440e15275dcd44a2508f1d8cc5ba53a8137db861cc71b61528ac3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118340027"
---
# <a name="editboxgetselectionstart"></a>GetSelectionStart de edição

O método **getSelectionStart** recupera a posição inicial do texto selecionado no controle admy.

``` syntax
        elementID.getSelectionStart()
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

[**GetSelectionEnd de edição**](editbox-getselectionend.md)
</dt> <dt>

[**ReplaceSelection de edição**](editbox-replaceselection.md)
</dt> <dt>

[**Autoseleção de myselecting**](editbox-setselection.md)
</dt> </dl>

 

 





