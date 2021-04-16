---
title: GetSelectionEnd de edição
description: O método getSelectionEnd recupera a posição final do texto selecionado no controle admy.
ms.assetid: 82a445da-3c50-41b7-8ac8-da6c860056ba
keywords:
- Admy. getSelectionEnd Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.getSelectionEnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f27c2974360e7e77becfa67a27b4e96b529ad1e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811113"
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

 

 





