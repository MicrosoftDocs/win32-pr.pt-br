---
title: Mensagem de TTM_RELAYEVENT (commctrl. h)
description: Passa uma mensagem do mouse para um controle ToolTip para processamento.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- Controles de TTM_RELAYEVENT de mensagens do Windows
topic_type:
- apiref
api_name:
- TTM_RELAYEVENT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8648303a318f1f71eb16e8070235910ecfb8760
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298299"
---
# <a name="ttm_relayevent-message"></a>\_Mensagem TTM RELAYEVENT

Passa uma mensagem do mouse para um controle ToolTip para processamento.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero. **Windows 7 e posterior:** Se a posição da dica de ferramenta for deslocada da posição do cursor (na ordem não ser obstruída por um dedo ou um dispositivo apontador), esse parâmetro poderá conter informações extras da mensagem [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) . Recupere essas informações extras com [**GetMessageExtraInfo**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo).

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**msg**](/windows/win32/api/winuser/ns-winuser-msg) que contém a mensagem a ser retransmitida.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Um controle ToolTip processa apenas as seguintes mensagens passadas para ele pela mensagem **TTM \_ RELAYEVENT** :

-   LBUTTONDOWN do WM \_
-   LBUTTONUP do WM \_
-   MBUTTONDOWN do WM \_
-   MBUTTONUP do WM \_
-   admousemove do WM \_
-   NCMOUSEMOVE do WM \_
-   RBUTTONDOWN do WM \_
-   RBUTTONUP do WM \_

Todas as outras mensagens são ignoradas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

