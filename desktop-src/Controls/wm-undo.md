---
title: Mensagem de WM_UNDO (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de desfazer do WM para um controle de edição para desfazer a última operação. Quando essa mensagem é enviada a um controle de edição, o texto excluído anteriormente é restaurado ou o texto adicionado anteriormente é excluído.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- Controles de WM_UNDO de mensagens do Windows
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
ms.openlocfilehash: 3c5eb9182b6d8d3fc1360565f6661e989f3b6d0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455416"
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

## <a name="return-value"></a>Retornar valor

Se a mensagem tiver sucesso, o valor de retorno será **true**.

Se a mensagem falhar, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

**Edição avançada:** É recomendável que [**em \_ desfazer**](em-undo.md) seja usado em vez do **WM \_ desfazer**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



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

 

