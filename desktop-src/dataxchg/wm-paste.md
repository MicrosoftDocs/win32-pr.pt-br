---
title: WM_PASTE mensagem (Winuser.h)
description: Um aplicativo envia uma mensagem WM PASTE para uma caixa de combinação ou controle de edição para copiar o conteúdo atual da área de transferência para o controle de edição na posição atual \_ do aparador. Os dados serão inseridos somente se a área de transferência contiver dados no formato CF \_ TEXT.
ms.assetid: 6830b511-986f-46ef-a977-7adedffe86ea
keywords:
- WM_PASTE de dados de Exchange
topic_type:
- apiref
api_name:
- WM_PASTE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a3cc1815349a2194d5dd7e2a65eb1c9ae77a2947f41361a90e92bae73357f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499116"
---
# <a name="wm_paste-message"></a>Mensagem WM \_ PASTE

Um aplicativo envia uma mensagem **WM \_ PASTE** para uma caixa de combinação ou controle de edição para copiar o conteúdo atual da área de transferência para o controle de edição na posição atual do aparador. Os dados serão inseridos somente se a área de transferência contiver dados no [**formato CF \_ TEXT.**](standard-clipboard-formats.md)


```C++
#define WM_PASTE                        0x0302
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Quando enviada para uma caixa de combinação, a **mensagem WM \_ PASTE** é manipulada por seu controle de edição. Essa mensagem não tem efeito quando enviada para uma caixa de combinação com o [**estilo \_ CBS DROPDOWNLIST.**](../controls/combo-box-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**WM \_ CLEAR**](wm-clear.md)
</dt> <dt>

[**CÓPIA DO WM \_**](wm-copy.md)
</dt> <dt>

[**WM \_ CUT**](wm-cut.md)
</dt> <dt>

[**WM \_ UNDO**](/windows/desktop/Controls/wm-undo)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Área de transferência](clipboard.md)
</dt> </dl>

 

