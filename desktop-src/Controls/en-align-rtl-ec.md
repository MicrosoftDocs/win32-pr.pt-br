---
title: Código de notificação EN_ALIGN_RTL_EC (WinUser. h)
description: Enviado quando o usuário altera a direção do controle de edição para a direita para a esquerda. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de comando do WM \_ .
ms.assetid: c53bc808-48c6-4a8f-ae5d-af2164fe419a
keywords:
- EN_ALIGN_RTL_EC de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- EN_ALIGN_RTL_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eca94073b86ea44b192360e593f4b76d4227cf82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824301"
---
# <a name="en_align_rtl_ec-notification-code"></a>PT \_ alinhar \_ \_ código de notificação do EC DPE

Enviado quando o usuário altera a direção do controle de edição para a direita para a esquerda. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_ALIGN_RTL_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para o controle de edição que envia o código de notificação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se houver uma linguagem bidirecional instalada em seu sistema, por exemplo, árabe ou Hebraico, você poderá alterar a direção do controle de edição usando CTRL + LSHIFT (da esquerda para a direita) e CTRL + RSHIFT (da direita para a esquerda).

**Edição avançada:** Não há suporte para este código de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

