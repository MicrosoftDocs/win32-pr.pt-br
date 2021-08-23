---
title: TTM_RELAYEVENT mensagem (Commctrl.h)
description: Passa uma mensagem do mouse para um controle de dica de ferramenta para processamento.
ms.assetid: 76d6d0ed-f357-479e-83d8-03d2e988cbd3
keywords:
- TTM_RELAYEVENT controles de Windows mensagem
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
ms.openlocfilehash: 051a0b7ab8ecd93b15ceb9187eefd6f566b55d653b751889cd29acec58366716
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166359"
---
# <a name="ttm_relayevent-message"></a>Mensagem TTM \_ RELAYEVENT

Passa uma mensagem do mouse para um controle de dica de ferramenta para processamento.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero. **Windows 7 e posteriores:** Se a posição da dica de ferramenta for deslocada da posição do cursor (para não ser obstruída por um dedo ou um dispositivo que aponta), esse parâmetro poderá conter informações extras extra da mensagem [**WM \_ MOUSEMOVE.**](/windows/desktop/inputdev/wm-mousemove) Recupere essas informações extras com [**GetMessageExtraInfo.**](/windows/desktop/api/winuser/nf-winuser-getmessageextrainfo)

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura MSG**](/windows/win32/api/winuser/ns-winuser-msg) que contém a mensagem para retransmissão.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Um controle de dica de ferramenta processa apenas as seguintes mensagens passadas para ele pela **mensagem TTM \_ RELAYEVENT:**

-   WM \_ LBUTTONDOWN
-   WM \_ LBUTTONUP
-   WM \_ MBUTTONDOWN
-   WM \_ MBUTTONUP
-   WM \_ MOUSEMOVE
-   WM \_ NCMOUSEMOVE
-   WM \_ RBUTTONDOWN
-   WM \_ RBUTTONUP

Todas as outras mensagens são ignoradas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

