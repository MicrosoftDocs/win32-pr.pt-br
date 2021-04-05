---
title: Mensagem de BM_GETCHECK (WinUser. h)
description: Obtém o estado de verificação de um botão de opção ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usar o botão \_ getcheck macro.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- Controles de BM_GETCHECK de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_GETCHECK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1aa89dc256ea9e0036259239d1c74e1e82b272
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086252"
---
# <a name="bm_getcheck-message"></a>Mensagem de BM \_ GETcheck

Obtém o estado de verificação de um botão de opção ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usar o [**botão \_ getcheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) macro.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno de um botão criado com o estilo [**\_ AUTOCHECKBOX BS**](button-styles.md), [**BS \_ AUTORADIOBUTTON**](button-styles.md), [**BS \_ AUTO3STATE**](button-styles.md), [**BS \_ CheckBox**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)ou [**BS \_ 3STATE**](button-styles.md) pode ser um dos seguintes.



| Código de retorno                                                                                       | Descrição                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ verificado**</dt> </dl>       | O botão está marcado.<br/>                                                                                                                                                                                     |
| <dl> <dt>**BST \_ indeterminado**</dt> </dl> | O botão fica acinzentado, indicando um estado indeterminado (aplica-se somente se o botão tiver o estilo [**BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE**](button-styles.md) ).<br/> |
| <dl> <dt>**BST não \_ verificado**</dt> </dl>     | O botão está desmarcado<br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a>Comentários

Se o botão tiver um estilo diferente daqueles listados, o valor de retorno será zero.

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

[**BM \_ GETstate**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETcheck**](bm-setcheck.md)
</dt> </dl>

 

 





