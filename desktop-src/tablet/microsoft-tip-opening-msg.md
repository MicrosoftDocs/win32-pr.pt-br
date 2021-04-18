---
description: Notifica a janela quando o painel de entrada de texto está sendo aberto.
ms.assetid: 6eadd648-bffb-4227-bdcd-cd733f692734
title: Mensagem de MICROSOFT_TIP_OPENING_MSG (PenInputPanel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f0938b8a00e39f54817b8ec52e86e00aae52111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105815549"
---
# <a name="microsoft_tip_opening_msg-message"></a>\_Mensagem do \_ msg de abertura do Microsoft Tip \_

Notifica a janela quando o painel de entrada de texto está sendo aberto.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Atualmente não usado, deve ser **nulo**.

</dd> <dt>

*lParam* 
</dt> <dd>

Atualmente não usado, deve ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Os aplicativos devem chamar [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) depois de manipular essa mensagem. Consulte **DefWindowProc** para obter informações sobre seus valores de retorno.

## <a name="remarks"></a>Comentários

Essa notificação permite que você saiba quando o painel de entrada está abrindo. Se você quiser executar uma ação quando isso acontecer, manipule a mensagem, execute a operação no manipulador e, em seguida, passe a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

> [!Note]  
> Essa mensagem também é enviada quando o painel de entrada de texto já está visível e o usuário alterna do teclado para a capa de manuscrito.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------------|
| Cliente<br/> | Windows Vista<br/>                                                                   |
| parâmetro<br/> | <dl> <dt>PenInputPanel. h</dt> </dl> |



 

