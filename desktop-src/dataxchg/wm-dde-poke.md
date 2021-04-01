---
title: Mensagem de WM_DDE_POKE (DDE. h)
description: Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de envio de DDE do WM \_ \_ em um aplicativo de servidor DDE.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- Troca de dados de mensagem WM_DDE_POKE
topic_type:
- apiref
api_name:
- WM_DDE_POKE
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 001697cbd5328b9c8d9eb72ebddff5f86ef6381c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645198"
---
# <a name="wm_dde_poke-message"></a>Mensagem de remediar DDE do WM \_ \_

Um aplicativo cliente troca dinâmica de dados (DDE) posta uma mensagem de envio de **\_ \_ DDE do WM** em um aplicativo de servidor DDE. Um cliente usa essa mensagem para solicitar que o servidor aceite um item de dados não solicitado. Espera-se que o servidor responda com uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) indicando se ele aceitou o item de dados.

Para postar essa mensagem, chame a função [**CreateMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para a janela do cliente que está postando a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior é um identificador para um objeto de memória global que contém uma estrutura [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) com os dados e informações adicionais.

A palavra de ordem superior contém um átomo global que identifica o item de dados para o qual os dados ou a notificação estão sendo enviados.

</dd> </dl>

## <a name="remarks"></a>Comentários

### <a name="posting"></a>Lançamento

O aplicativo cliente deve alocar memória para o objeto de memória global usando a função [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) . O aplicativo cliente deve excluir o objeto se qualquer uma das seguintes condições for verdadeira:

-   O aplicativo de servidor responde com uma mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) negativa.
-   O membro **fRelease** é **false**, mas o aplicativo de servidor responde com um [**\_ \_ ACK DDE do WM**](wm-dde-ack.md)positivo ou negativo.

O aplicativo cliente deve criar o Atom usando a função [**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma) .

O aplicativo cliente deve criar ou reutilizar o parâmetro de *lParam* de envio do **WM \_ DDE \_** , chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

### <a name="receiving"></a>Recebimento

O aplicativo de servidor deve postar a mensagem de [**\_ \_ ACK DDE do WM**](wm-dde-ack.md) para responder positivamente ou negativamente. Ao lançar o **WM \_ DDE \_ ACK**, o servidor pode reutilizar o Atom ou pode excluí-lo e criar um novo.

O servidor deve criar ou reutilizar o parâmetro de *lParam* [**\_ DDE \_ ACK do WM**](wm-dde-ack.md) chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a função [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) .

Para liberar o objeto de memória global, o servidor deve chamar a função [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) . Além disso, se o formato de dados for o [**CF \_ DSPMETAFILEPICT**](clipboard-formats.md) ou o **CF \_ METAFILEPICT**, o servidor também deverá chamar [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) com o identificador de metarquivo inserido. Esses dois formatos têm um nível extra de indireção; ou seja, um aplicativo deve bloquear o objeto para obter um ponteiro para um identificador e, em seguida, bloquear esse identificador para obter um ponteiro para uma estrutura [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) e, finalmente, chamar **DeleteMetaFile** com o identificador do membro **hMF** da estrutura **METAFILEPICT** .

Para liberar o objeto, o servidor deve chamar a função [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>DDE. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**GlobalAddAtom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
</dt> <dt>

[**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict)
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

**Conceitua**
</dt> <dt>

[Sobre troca dinâmica de dados](about-dynamic-data-exchange.md)
</dt> </dl>

 

