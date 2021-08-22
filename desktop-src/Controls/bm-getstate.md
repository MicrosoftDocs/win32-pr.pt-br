---
title: BM_GETSTATE mensagem (Winuser.h)
description: Recupera o estado de um botão ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usar a \_ macro Button GetState.
ms.assetid: ca4c2f1a-b657-490a-ac8b-5f0cfef64d76
keywords:
- BM_GETSTATE controles Windows mensagem
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
ms.openlocfilehash: cd44921c61477e26cd5570fcbaa6f96a4e61f96ee22ad1c705bf553788d8cfba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674836"
---
# <a name="bm_getstate-message"></a>Mensagem \_ GETSTATE BM

Recupera o estado de um botão ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ Button GetState.**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate)

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

## <a name="return-value"></a>Valor retornado

O valor de retorno especifica o estado atual do botão. É uma combinação dos valores a seguir.



| Código de retorno                                                                                        | Descrição                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ CHECKED**</dt> </dl>        | O botão está marcado.<br/>                                                                                                                                                                                        |
| <dl> <dt>**BST \_ DROPDOWNPUSHED**</dt> </dl> | [Windows Vista](common-control-versions.md). O botão está no estado de lista listada. Aplica-se somente se o botão tiver o [**estilo \_ DROPDOWN TBSTYLE.**](toolbar-control-and-button-styles.md)<br/> |
| <dl> <dt>**FOCO \_ DE BST**</dt> </dl>          | O botão tem o foco do teclado.<br/>                                                                                                                                                                            |
| <dl> <dt>**BST \_ HOT**</dt> </dl>            | O botão está quente; ou seja, o mouse está sobre ele.<br/>                                                                                                                                                    |
| <dl> <dt>**BST \_ INDETERMINADO**</dt> </dl>  | O estado do botão é indeterminado. Aplica-se somente se o botão tiver o [**estilo BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE.**](button-styles.md)<br/>                    |
| <dl> <dt>**BST \_ PUSHED**</dt> </dl>         | O botão está sendo mostrado no estado pressionado.<br/>                                                                                                                                                                |
| <dl> <dt>**BST \_ UNCHECKED**</dt> </dl>      | Nenhum estado especial. Equivalente a zero.<br/>                                                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**BM \_ GETCHECK**](bm-getcheck.md)
</dt> <dt>

[**BM \_ SETSTATE**](bm-setstate.md)
</dt> </dl>

 

 





