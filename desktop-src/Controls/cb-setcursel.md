---
title: Mensagem de CB_SETCURSEL (WinUser. h)
description: Um aplicativo envia uma \_ mensagem do CB setcurse para selecionar uma cadeia de caracteres na lista de uma caixa de combinação.
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- Controles de CB_SETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bd130204e6dc8bb4166c21bc9c4d52950182c5c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009351"
---
# <a name="cb_setcursel-message"></a>Mensagem do CB \_ SETcurseal

Um aplicativo envia uma mensagem do **CB \_ setcurse** para selecionar uma cadeia de caracteres na lista de uma caixa de combinação. Se necessário, a lista rola a cadeia de caracteres para a exibição. O texto no controle de edição da caixa de combinação é alterado para refletir a nova seleção e qualquer seleção anterior na lista é removida.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice de base zero da cadeia de caracteres a ser selecionada. Se esse parâmetro for-1, qualquer seleção atual na lista será removida e o controle de edição será limpo.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem for bem-sucedida, o valor de retorno será o índice do item selecionado. Se *wParam* for maior do que o número de itens na lista ou se *wParam* for-1, o valor de retorno será CB \_ Err e a seleção será desmarcada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**localização da CB \_**](cb-findstring.md)
</dt> <dt>

[**iscursel de CB \_**](cb-getcursel.md)
</dt> <dt>

[**seleção do CB \_**](cb-selectstring.md)
</dt> </dl>

 

 





