---
title: Mensagem de WM_DDE_DATA (DDE. h)
description: um aplicativo de servidor troca dinâmica de dados (DDE) posta uma \_ mensagem de dados dde do WM \_ em um aplicativo cliente dde para passar um item de dados para o cliente ou notificar o cliente sobre a disponibilidade de um item de dados.
ms.assetid: ed6a65d3-b2a3-45f2-9600-291ce2ec8c0a
keywords:
- WM_DDE_DATA Exchange de dados da mensagem
topic_type:
- apiref
api_name:
- WM_DDE_DATA
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0200737a9b25a123954498941ad117e5465f58f5313daa8caf90674751355ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736273"
---
# <a name="wm_dde_data-message"></a>\_Mensagem de dados DDE do WM \_

um aplicativo de servidor troca dinâmica de dados (DDE) posta uma mensagem de **\_ \_ dados dde do WM** em um aplicativo cliente dde para passar um item de dados para o cliente ou notificar o cliente sobre a disponibilidade de um item de dados.

Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.


```C++
#define WM_DDE_DATA        0x03E05
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela do servidor postando a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior é um identificador para um objeto de memória global que contém uma estrutura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) com os dados e informações adicionais. O identificador deve ser definido como **nulo** se o servidor estiver notificando o cliente que o valor do item de dados foi alterado durante um link de dados quente. Um link quente é estabelecido pelo cliente que envia uma mensagem de [**\_ \_ aviso de DDE do WM**](wm-dde-advise.md) com o conjunto de bits **fDeferUpd** .

A palavra de ordem superior contém um átomo que identifica o item de dados para o qual os dados ou a notificação são enviados.

</dd> </dl>

## <a name="remarks"></a>Comentários

### <a name="posting"></a>Lançamento

O aplicativo de servidor aloca o objeto de memória global usando a função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . Ele aloca o Atom usando a função [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

O servidor deve criar ou reutilizar o parâmetro de *lParam* de **\_ \_ dados DDE do WM** chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Se o aplicativo receptor (cliente) responder com uma mensagem [**de \_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa, o aplicativo de postagem (servidor) deverá excluir o objeto de memória global; caso contrário, o cliente deverá excluir o objeto depois de extrair seu conteúdo chamando a função [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) .

Se o aplicativo de servidor definir o membro **fRelease** da estrutura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) como **false**, o servidor será responsável por excluir o objeto no recebimento de uma confirmação positiva ou negativa.

O aplicativo de servidor não deve definir os membros **fAckReq** e **FRelease** da estrutura [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata) como **false**. Se ambos os membros forem definidos como **false**, será impossível para o servidor determinar quando excluir o objeto.

### <a name="receiving"></a>Recebimento

Se **fAckReq** for **true**, o aplicativo cliente deverá postar a mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) para responder positiva ou negativamente. Ao lançar o **WM \_ DDE \_ ACK**, o cliente pode reutilizar o Atom ou pode excluí-lo e criar um novo.

O cliente deve criar ou reutilizar o parâmetro de *lParam* [**\_ DDE \_ ACK do WM**](wm-dde-ack.md) chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Se **fAckReq** for **false**, o aplicativo cliente deverá excluir o Atom.

Se o aplicativo de lançamento especificou o objeto de memória global como **nulo**, o aplicativo receptor pode solicitar que o servidor envie os dados postando uma mensagem de [**\_ \_ solicitação DDE do WM**](wm-dde-request.md) .

Depois de processar uma mensagem de **\_ \_ dados DDE do WM** em que o objeto de memória global não é **nulo**, o cliente deve liberar o objeto, a menos que uma das seguintes condições seja verdadeira:

-   O membro **fRelease** é **false**.
-   O membro **fRelease** é **true**, mas o aplicativo cliente responde com uma mensagem [**de \_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Dde. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)
</dt> <dt>

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)
</dt> <dt>

[**\_ACK de DDE do WM \_**](wm-dde-ack.md)
</dt> <dt>

[**\_aviso de DDE do WM \_**](wm-dde-advise.md)
</dt> <dt>

[**o WM \_ DDE. \_**](wm-dde-poke.md)
</dt> <dt>

[**\_solicitação de DDE do WM \_**](wm-dde-request.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Sobre troca dinâmica de dados](about-dynamic-data-exchange.md)
</dt> </dl>

 

