---
title: EDITBOX.getSelectionStart
description: O método getSelectionStart recupera a posição inicial do texto selecionado no controle de caixa de edição.
ms.assetid: 2d7efe14-549c-4f73-96a7-b8ce88b881ad
keywords:
- EDITBOX.getSelectionStart Windows Media Player
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
# <a name="editboxgetselectionstart"></a>EDITBOX.getSelectionStart

O **método getSelectionStart** recupera a posição inicial do texto selecionado no controle de caixa de edição.

``` syntax
        elementID.getSelectionStart()
```

## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor Retornado

Esse método retorna um **Número** (**long**).

## <a name="remarks"></a>Comentários

Se nenhum texto for selecionado, esse método retornará a posição do ponto de inserção.

Se o controle for multilinha, esse método retornará o índice de caracteres no controle, não o índice de linha.

Esse método só pode ser chamado depois que o controle se torna visível.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------|
| Versão<br/> | Windows Media Player para Windows XP ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Elemento EDITBOX**](editbox-element.md)
</dt> <dt>

[**EDITBOX.getSelectionEnd**](editbox-getselectionend.md)
</dt> <dt>

[**EDITBOX.replaceSelection**](editbox-replaceselection.md)
</dt> <dt>

[**EDITBOX.setSelection**](editbox-setselection.md)
</dt> </dl>

 

 





