---
title: Mensagem de WM_UNDO (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de desfazer do WM para um controle de edição para desfazer a última operação. Quando essa mensagem é enviada a um controle de edição, o texto excluído anteriormente é restaurado ou o texto adicionado anteriormente é excluído.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- controles de Windows de mensagem de WM_UNDO
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b6e4bd0715b7eeb5f99f34f5142ac3198c5c1eae53cf4486c3efce9dace19a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119311336"
---
# <a name="wm_undo-message"></a>Mensagem de desfazer do WM \_

Um aplicativo envia uma mensagem de **\_ desfazer do WM** para um controle de edição para desfazer a última operação. Quando essa mensagem é enviada a um controle de edição, o texto excluído anteriormente é restaurado ou o texto adicionado anteriormente é excluído.

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

Se a mensagem tiver sucesso, o valor de retorno será **true**.

Se a mensagem falhar, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

**Edição avançada:** É recomendável que [**em \_ desfazer**](em-undo.md) seja usado em vez do **WM \_ desfazer**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Outros recursos**
</dt> <dt>

[**limpeza do WM \_**](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[**cópia do WM \_**](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[**recorte do WM \_**](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[**colar do WM \_**](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

