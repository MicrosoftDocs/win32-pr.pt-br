---
title: WM_DDE_INITIATE mensagem (Dde.h)
description: Um aplicativo troca dinâmica de dados cliente (DDE) envia uma mensagem WM DDE INITIATE para iniciar uma conversa com um aplicativo de servidor que responde aos nomes de aplicativo e \_ \_ tópico especificados.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- WM_DDE_INITIATE troca de dados de mensagens
topic_type:
- apiref
api_name:
- WM_DDE_INITIATE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf65e222c7711d429db44e391d4f03c35997e219
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386719"
---
# <a name="wm_dde_initiate-message"></a>Mensagem WM \_ DDE \_ INITIATE

Um troca dinâmica de dados cliente (DDE) envia uma mensagem **WM \_ DDE \_ INITIATE** para iniciar uma conversa com um aplicativo de servidor que responde aos nomes de aplicativo e tópico especificados. Ao receber essa mensagem, todos os aplicativos de servidor com nomes que corresponderem ao aplicativo especificado e que deem suporte ao tópico especificado devem confirmá-lo. (Para obter mais informações, consulte a [**mensagem WM \_ DDE \_ ACK.)**](wm-dde-ack.md)


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para a janela do cliente que envia a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem baixa contém um atom que identifica o aplicativo com o qual uma conversa é solicitada. O nome do aplicativo não pode conter barras (/) ou barras in backslashes ( \\ ). Esses caracteres são reservados para implementações de rede. Se esse parâmetro for **NULL,** uma conversa com todos os aplicativos será solicitada.

A palavra de ordem alta contém um atom que identifica o tópico para o qual uma conversa é solicitada. Se o tópico for **NULL,** serão solicitadas conversas para todos os tópicos disponíveis.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se a palavra de ordem baixa *de lParam* for **NULL,** qualquer aplicativo de servidor poderá responder. Se a palavra de ordem alta de *lParam* for **NULL,** qualquer tópico será válido. Ao receber uma solicitação WM DDE INITIATE com a palavra de ordem alta do parâmetro *lParam* definida como **NULL**, um servidor deve enviar uma mensagem WM **\_ \_ DDE** [**\_ \_ ACK**](wm-dde-ack.md) para cada um dos tópicos aos que ele dá suporte.

### <a name="sending"></a>Envio

O cliente transmite a mensagem para todas as janelas de nível superior definindo o primeiro parâmetro de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) como **HWND \_ BROADCAST.**

Se o aplicativo cliente já tiver obtido o handle de janela do servidor desejado, ele poderá enviar **WM \_ DDE \_ INITIATE** diretamente para a janela do servidor passando o alça de janela do servidor como o primeiro parâmetro [**de SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).

O aplicativo cliente aloca átomos chamando a [**função GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

Quando [**SendMessage retorna,**](/windows/desktop/api/winuser/nf-winuser-sendmessage) o aplicativo cliente deve excluir os átomos.

### <a name="receiving"></a>Recebimento

Para concluir o início de uma conversa, o aplicativo de servidor deve responder com uma ou mais mensagens [**WM \_ DDE \_ ACK,**](wm-dde-ack.md) em que cada mensagem é para um tópico separado. Ao enviar **a mensagem WM \_ DDE \_ ACK,** o servidor deve criar novos átomos; ele não deve reutilizar os átomos enviados com **WM \_ DDE \_ INITIATE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Dde.h (inclua Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Sobre troca dinâmica de dados](about-dynamic-data-exchange.md)
</dt> </dl>

 

