---
title: Mensagem de BM_GETSTATE (WinUser. h)
description: Recupera o estado de um botão ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetState do botão.
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- Controles de BM_GETSTATE de mensagens do Windows
topic_type:
- apiref
api_name:
- BM_GETSTATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3b5e69f067acfc13cd8661be8a585fcfc8e6fe4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918042"
---
# <a name="bm_getstate-message"></a>\_Mensagem GETstate do BM

Recupera o estado de um botão ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetState do botão**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) .

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

O valor de retorno especifica o estado atual do botão. É uma combinação dos valores a seguir.



| Código de retorno                                                                                        | Descrição                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ verificado**</dt> </dl>        | O botão está marcado.<br/>                                                                                                                                                                                        |
| <dl> <dt>**BST \_ DROPDOWNPUSHED**</dt> </dl> | [Windows Vista](common-control-versions.md). O botão está no estado suspenso. Aplica-se somente se o botão tiver o estilo [**\_ suspenso TBSTYLE**](toolbar-control-and-button-styles.md) .<br/> |
| <dl> <dt>**foco de BST \_**</dt> </dl>          | O botão tem o foco do teclado.<br/>                                                                                                                                                                            |
| <dl> <dt>**BST \_ quente**</dt> </dl>            | O botão está quente; ou seja, o mouse está focalizando-o.<br/>                                                                                                                                                    |
| <dl> <dt>**BST \_ indeterminado**</dt> </dl>  | O estado do botão é indeterminado. Aplica-se somente se o botão tiver o estilo [**BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE**](button-styles.md) .<br/>                    |
| <dl> <dt>**BST \_ enviado por push**</dt> </dl>         | O botão está sendo exibido no estado enviado por push.<br/>                                                                                                                                                                |
| <dl> <dt>**BST não \_ verificado**</dt> </dl>      | Nenhum estado especial. Equivalente a zero.<br/>                                                                                                                                                                         |



 

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

[**SetState BM \_**](bm-setstate.md)
</dt> </dl>

 

 





