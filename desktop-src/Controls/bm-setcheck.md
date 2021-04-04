---
title: Mensagem de BM_SETCHECK (WinUser. h)
description: Define o estado de verificação de um botão de opção ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usando a \_ macro SetCheck do botão.
ms.assetid: 8294e6c4-caac-4c60-85ff-38698a1d2ae4
keywords:
- Controles de BM_SETCHECK de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_SETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c298fb865fe34946bfedc9f1d6d1924f6d32202
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008948"
---
# <a name="bm_setcheck-message"></a>\_Mensagem BM SETcheck

Define o estado de verificação de um botão de opção ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetCheck do botão**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O estado de verificação. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                                     | Significado                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BST_CHECKED"></span><span id="bst_checked"></span><dl> <dt>**BST \_ verificado**</dt> </dl>                   | Define o estado do botão como marcado.<br/>                                                                                                                                                                                           |
| <span id="BST_INDETERMINATE"></span><span id="bst_indeterminate"></span><dl> <dt>**BST \_ indeterminado**</dt> </dl> | Define o estado do botão como esmaecido, indicando um estado indeterminado. Use esse valor somente se o botão tiver o estilo [**BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE**](button-styles.md) .<br/> |
| <span id="BST_UNCHECKED"></span><span id="bst_unchecked"></span><dl> <dt>**BST não \_ verificado**</dt> </dl>             | Define o estado do botão como limpo.<br/>                                                                                                                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Essa mensagem sempre retorna zero.

## <a name="remarks"></a>Comentários

A **mensagem \_ SetCheck BM** não tem efeito sobre botões de push.

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

[**BM \_ GETcheck**](bm-getcheck.md)
</dt> <dt>

[**BM \_ GETstate**](bm-getstate.md)
</dt> <dt>

[**SetState BM \_**](bm-setstate.md)
</dt> </dl>

 

 





