---
title: Autoseleção de myselecting
description: O método setseleções seleciona o texto no controle caixa de edição do índice inicial especificado para o índice final especificado.
ms.assetid: 97b20a17-4b9c-4144-b448-8d7611c0e994
keywords:
- Admy. setselecting Windows Media Player
topic_type:
- apiref
api_name:
- EDITBOX.setSelection
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d7077de0ea59940c4afa551d22188d5583d0e4c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758217"
---
# <a name="editboxsetselection"></a>Autoseleção de myselecting

O método **setseleções** seleciona o texto no controle caixa de edição do índice inicial especificado para o índice final especificado.

``` syntax
        elementID.setSelection(start, end)
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="start"></span><span id="START"></span>*Comece*
</dt> <dd>

**Número** (**longo**) que contém o índice de caracteres da posição inicial do texto selecionado.

</dd> <dt>

<span id="end"></span><span id="END"></span>*completo*
</dt> <dd>

**Número** (**longo**) que contém o índice de caracteres da posição final do texto selecionado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Se o início for 0 e o final for 1, todo o texto no controle caixa de edição será selecionado. Se o início for 1, qualquer seleção atual será desmarcada.

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

[**ReplaceSelection de edição**](editbox-replaceselection.md)
</dt> </dl>

 

 





