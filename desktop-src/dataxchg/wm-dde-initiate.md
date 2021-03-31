---
title: Mensagem de WM_DDE_INITIATE (DDE. h)
description: Um aplicativo cliente troca dinâmica de dados (DDE) envia uma mensagem de início do WM \_ DDE \_ para iniciar uma conversa com um aplicativo de servidor respondendo aos nomes de aplicativo e de tópico especificados.
ms.assetid: d486f584-75a3-4ffd-ba5d-f95f2692cd6c
keywords:
- Troca de dados de mensagem WM_DDE_INITIATE
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
ms.openlocfilehash: 36485db262c46d5364ee0ee26e7e6f39ccf0e677
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369546"
---
# <a name="wm_dde_initiate-message"></a>Mensagem de inicialização de \_ DDE do WM \_

Um aplicativo cliente troca dinâmica de dados (DDE) envia uma mensagem de **\_ \_ início do WM DDE** para iniciar uma conversa com um aplicativo de servidor respondendo aos nomes de aplicativo e de tópico especificados. Ao receber essa mensagem, todos os aplicativos de servidor com nomes que correspondem ao aplicativo especificado e que dão suporte ao tópico especificado devem confirmá-lo. (Para obter mais informações, consulte a mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) .)


```C++
#define WM_DDE_INITIATE        0x03E0
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela do cliente que está enviando a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior contém um Atom que identifica o aplicativo com o qual uma conversa é solicitada. O nome do aplicativo não pode conter barras (/) ou barras invertidas ( \) . Esses caracteres são reservados para implementações de rede. Se esse parâmetro for **NULL**, será solicitada uma conversa com todos os aplicativos.

A palavra de ordem superior contém um átomo que identifica o tópico para o qual uma conversa é solicitada. Se o tópico for **nulo**, as conversas de todos os tópicos disponíveis serão solicitadas.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se a palavra de ordem inferior de *lParam* for **nula**, qualquer aplicativo de servidor poderá responder. Se a palavra de ordem superior de *lParam* for **nula**, qualquer tópico será válido. Após receber uma solicitação de **\_ \_ inicialização de DDE do WM** com a palavra de ordem superior do parâmetro *lParam* definido como **NULL**, um servidor deve enviar uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) para cada um dos tópicos com suporte.

### <a name="sending"></a>Envio

O cliente transmite a mensagem para todas as janelas de nível superior definindo o primeiro parâmetro de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) para a **\_ difusão de hWnd**.

Se o aplicativo cliente já tiver obtido o identificador de janela do servidor desejado, ele poderá enviar o **WM \_ DDE \_ inicie** diretamente para a janela do servidor passando o identificador de janela do servidor como o primeiro parâmetro de [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage).

O aplicativo cliente aloca Atoms chamando a função [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

Quando [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) retorna, o aplicativo cliente deve excluir os átomos.

### <a name="receiving"></a>Recebimento

Para concluir a inicialização de uma conversa, o aplicativo de servidor deve responder com uma ou mais mensagens de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) , em que cada mensagem é para um tópico separado. Ao enviar a mensagem de **\_ \_ ACK DDE do WM** , o servidor deve criar novos átomos; ele não deve reutilizar os átomos enviados com o **WM \_ DDE \_ Iniciar**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>DDE. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**\_ACK de DDE do WM \_**](wm-dde-ack.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Sobre troca dinâmica de dados](about-dynamic-data-exchange.md)
</dt> </dl>

 

