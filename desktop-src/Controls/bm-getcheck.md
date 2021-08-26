---
title: BM_GETCHECK mensagem (Winuser.h)
description: Obtém o estado de verificação de um botão de rádio ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetCheck do botão.
ms.assetid: a25b2c8d-0b32-4807-bfb4-e277675924f1
keywords:
- BM_GETCHECK controles de Windows mensagem
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
ms.openlocfilehash: e5eb87d98752bd0cd447d48c648bc4a55e93c3f8eb418a81a07e04113a86633a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921286"
---
# <a name="bm_getcheck-message"></a>Mensagem \_ GETCHECK do BM

Obtém o estado de verificação de um botão de rádio ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ GetCheck do**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) botão.

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

O valor de retorno de um botão criado com o estilo [**BS \_ AUTOCHECKBOX**](button-styles.md), [**BS \_ AUTORADIOBUTTON**](button-styles.md), [**BS \_ AUTO3STATE,**](button-styles.md) [**BS \_ CHECKBOX**](button-styles.md), [**BS \_ RADIOBUTTON**](button-styles.md)ou [**BS \_ 3STATE**](button-styles.md) pode ser um dos seguintes.



| Código de retorno                                                                                       | Descrição                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**BST \_ CHECKED**</dt> </dl>       | O botão está marcado.<br/>                                                                                                                                                                                     |
| <dl> <dt>**BST \_ INDETERMINADO**</dt> </dl> | O botão está es cinza, indicando um estado indeterminado (aplica-se somente se o botão tiver o [**estilo BS \_ 3STATE**](button-styles.md) ou [**BS \_ AUTO3STATE).**](button-styles.md)<br/> |
| <dl> <dt>**BST \_ UNCHECKED**</dt> </dl>     | O botão está limpo<br/>                                                                                                                                                                                      |



 

## <a name="remarks"></a>Comentários

Se o botão tiver um estilo diferente daqueles listados, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**BM \_ GETSTATE**](bm-getstate.md)
</dt> <dt>

[**BM \_ SETCHECK**](bm-setcheck.md)
</dt> </dl>

 

 





