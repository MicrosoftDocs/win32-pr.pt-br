---
title: ReplaceSelection de edição
description: O método replaceSelection substitui a seleção atual pelo texto especificado.
ms.assetid: 600650fb-f0c8-489a-9bf2-04f31705c6b0
keywords:
- Admy. replaceSelection Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.replaceSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6546f24c864d0b466acd17d9a42616c3f8ab01b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811334"
---
# <a name="editboxreplaceselection"></a>ReplaceSelection de edição

O método **replaceSelection** substitui a seleção atual pelo texto especificado.

``` syntax
        elementID.replaceSelection(newValue)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="newValue"></span><span id="newvalue"></span><span id="NEWVALUE"></span>*newValue*
</dt> <dd>

**Cadeia de caracteres** que contém o texto para substituir o texto selecionado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se não houver nenhum texto selecionado, o texto de substituição será inserido no local atual do ponto de inserção.

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

[**GetSelectionStart de edição**](editbox-getselectionstart.md)
</dt> <dt>

[**Autoseleção de myselecting**](editbox-setselection.md)
</dt> </dl>

 

 





