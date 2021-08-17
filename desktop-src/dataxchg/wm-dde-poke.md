---
title: WM_DDE_POKE mensagem (Dde.h)
description: Um aplicativo Dados Dinâmicos Exchange cliente (DDE) publica uma mensagem WM \_ DDE WM DDE WM EM UM aplicativo \_ de servidor DDE.
ms.assetid: 848142b7-a7ef-4206-9bb3-b511388cfaaa
keywords:
- WM_DDE_POKE de dados de Exchange
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
ms.openlocfilehash: df1329c6667698a0b633deb2726c47469b515e8fcd78d735a3949e7c8e19a4dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117736283"
---
# <a name="wm_dde_poke-message"></a>Mensagem WM \_ DDE \_ WM DDE WM

Um aplicativo Dados Dinâmicos Exchange cliente (DDE) publica uma mensagem **WM \_ DDE \_ WM DDE ADM** em um aplicativo de servidor DDE. Um cliente usa essa mensagem para solicitar que o servidor aceite um item de dados não solicitado. Espera-se que o servidor responda com uma [**mensagem WM \_ DDE \_ ACK**](wm-dde-ack.md) indicando se ele aceitou o item de dados.

Para postar essa mensagem, chame a [**função PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.


```C++
#define WM_DDE_POKE        0x03E7
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para a janela do cliente que posta a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem baixa é um identificador para um objeto de memória global que contém uma estrutura [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke) com os dados e informações adicionais.

A palavra de ordem alta contém um atom global que identifica o item de dados para o qual os dados ou notificação estão sendo enviados.

</dd> </dl>

## <a name="remarks"></a>Comentários

### <a name="posting"></a>Postar

O aplicativo cliente deve alocar memória para o objeto de memória global usando a [**função GlobalAlloc.**](/windows/desktop/api/winbase/nf-winbase-globalalloc) O aplicativo cliente deverá excluir o objeto se uma das seguintes condições for verdadeira:

-   O aplicativo de servidor responde com uma mensagem [**negativa do WM \_ DDE \_ ACK.**](wm-dde-ack.md)
-   O **membro fRelease** é **FALSE,** mas o aplicativo de servidor responde com um [**WM \_ DDE ACK positivo ou \_ negativo.**](wm-dde-ack.md)

O aplicativo cliente deve criar o atom usando a [**função GlobalAddAtom.**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)

O aplicativo cliente deve criar ou reutilizar o parâmetro **WM \_ \_ DDE: lParam,** chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a [**função ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) 

### <a name="receiving"></a>Recebimento

O aplicativo de servidor deve postar a [**mensagem WM \_ DDE \_ ACK**](wm-dde-ack.md) para responder positiva ou negativamente. Ao postar **o WM \_ DDE \_ ACK**, o servidor pode reutilizar o atom ou pode excluí-lo e criar um novo.

O servidor deve criar ou reutilizar o parâmetro [**WM \_ DDE \_ ACK**](wm-dde-ack.md) *lParam* chamando a [**função PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a [**função ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

Para liberar o objeto de memória global, o servidor deve chamar a [**função GlobalFree.**](/windows/desktop/api/winbase/nf-winbase-globalfree) Além disso, se o formato de dados for [**CF \_ DSPMETAFILEPICT**](clipboard-formats.md) ou **CF \_ METAFILEPICT**, o servidor também deverá chamar [**DeleteMetaFile**](/windows/desktop/api/wingdi/nf-wingdi-deletemetafile) com o alçamento de metarquivo inserido. Esses dois formatos têm um nível extra de indcisão; ou seja, um aplicativo deve bloquear o objeto para obter um ponteiro para um identificador, bloquear esse identificador para obter um ponteiro para uma estrutura [**METAFILEPICT**](/windows/win32/api/wingdi/ns-wingdi-metafilepict) e, por fim, chamar **DeleteMetaFile** com o identificador do membro **hMF** da estrutura **METAFILEPICT.**

Para liberar o objeto, o servidor deve chamar a [**função FreeDDElParam.**](/windows/desktop/api/Dde/nf-dde-freeddelparam)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                 |
| Cabeçalho<br/>                   | <dl> <dt>Dde.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
</dt> <dt>

[**Globaladdatom**](/windows/desktop/api/Winbase/nf-winbase-globaladdatoma)
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

[**WM \_ DDE \_ ACK**](wm-dde-ack.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Sobre Dados Dinâmicos Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

