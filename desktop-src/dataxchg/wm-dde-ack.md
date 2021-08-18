---
title: WM_DDE_ACK mensagem (Dde.h)
description: A mensagem WM DDE ACK notifica um aplicativo Dados Dinâmicos Exchange (DDE) do recebimento e processamento das seguintes mensagens \_ \_ WM \_ \_ DDE WM DDE WM, WM \_ DDE \_ EXECUTE, WM \_ DDE \_ DATA, WM \_ \_ DDE ADVISE, WM \_ DDE \_ UNADVISE, WM DDE INITIATE ou \_ WM \_ \_ DDE REQUEST (em \_ alguns casos). Para postar essa mensagem, chame a função PostMessage com os parâmetros a seguir.
ms.assetid: aca47dbf-e1f2-4725-8364-0aa7fcd98bd9
keywords:
- WM_DDE_ACK de dados de Exchange
topic_type:
- apiref
api_name:
- WM_DDE_ACK
api_location:
- Dde.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1aad39115e1bdb68208a9ccbb0d83eea934ef2ff8c6521a0602e081c7ed811
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636236"
---
# <a name="wm_dde_ack-message"></a>Mensagem \_ WM DDE \_ ACK

A mensagem **WM \_ DDE \_ ACK** notifica um aplicativo DDE (Dados Dinâmicos Exchange) do recebimento e processamento das seguintes mensagens: [**WM \_ DDE WM DDE \_ WM WM**](wm-dde-poke.md)DE EXECUTE , WM [**\_ \_ DDE**](wm-dde-execute.md) [**\_ \_ DATA**](wm-dde-data.md), [**WM \_ DDE \_ ADVISE**](wm-dde-advise.md), [**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md), [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)ou [**WM \_ DDE \_ REQUEST**](wm-dde-request.md) (em alguns casos).

Para postar essa mensagem, chame a [**função PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) com os parâmetros a seguir.


```C++
#define WM_DDE_ACK     0x03E4
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Ao responder ao [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md), esse parâmetro é um handle para a janela do servidor que envia a mensagem.

Ao responder ao [**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md), esse parâmetro é um handle para a janela do servidor que posta a mensagem.

Ao responder a todas as outras mensagens, esse parâmetro é um lidar com a janela do cliente ou do servidor que está postando a mensagem.

</dd> <dt>

*lParam* 
</dt> <dd>

Ao responder ao [**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md), a palavra de ordem baixa contém um atom que identifica o aplicativo de resposta. A palavra de ordem alta contém um atom que identifica o tópico para o qual uma conversa está sendo estabelecida.

Ao responder a [**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md), a palavra de ordem baixa especifica uma estrutura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) que contém uma série de sinalizadores que indicam o status da resposta. A palavra de ordem alta é um identificador para um objeto de memória global que contém a cadeia de caracteres de comando que foi recebida na mensagem **WM \_ DDE \_ EXECUTE.**

Ao responder a todas as outras mensagens, a palavra de ordem baixa especifica uma estrutura [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) que contém uma série de sinalizadores que indicam o status da resposta. A palavra de ordem alta contém um atom global que identifica o nome do item de dados para o qual a resposta é enviada.

</dd> </dl>

## <a name="remarks"></a>Comentários

### <a name="posting"></a>Postar

Exceto em resposta à mensagem [**WM \_ DDE \_ INITIATE,**](wm-dde-initiate.md) o aplicativo posta a mensagem **WM \_ DDE \_ ACK** chamando a [**função PostMessage,**](/windows/desktop/api/winuser/nf-winuser-postmessagea) não chamando a [**função SendMessage.**](/windows/desktop/api/winuser/nf-winuser-sendmessage) Ao responder ao **WM \_ DDE \_ INITIATE**, o aplicativo envia a mensagem **WM \_ DDE \_ ACK** chamando **SendMessage**. Nesse caso, nem o atom de nome do aplicativo nem o atom de nome do tópico devem ser **NULL** (mesmo que a mensagem **WM \_ DDE \_ INITIATE** especifique **atoms NULL).**

Ao confirmar qualquer mensagem com um atom que o acompanha, o aplicativo postando **WM \_ DDE \_ ACK** pode reutilizar o atom que acompanhou a mensagem original ou pode excluí-la e criar uma nova.

Ao confirmar [**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md), o aplicativo que posta **WM \_ DDE \_ ACK** deve reutilizar o objeto de memória global identificado na mensagem EXECUTE do **WM \_ DDE \_** original.

Todas as mensagens **postadas do WM \_ DDE \_ ACK** devem criar ou reutilizar o parâmetro *lParam* chamando a função [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) ou a [**função ReuseDDElParam.**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)

Se um aplicativo tiver iniciado o encerramento de uma conversa postando [**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md) e estiver aguardando confirmação, o aplicativo em espera não deverá reconhecer (positiva ou negativamente) as mensagens subsequentes enviadas pelo outro aplicativo. O aplicativo em espera deve excluir os átomos ou objetos de memória compartilhada recebidos nessas mensagens intermediárias. Os objetos de memória não deverão ser liberados se o **sinalizador fRelease** estiver definido como **FALSE** em [**mensagens WM \_ DDE WM \_ DDE WM e**](wm-dde-poke.md) WM [**\_ DDE \_ DATA.**](wm-dde-data.md)

### <a name="receiving"></a>Recebimento

O aplicativo que recebe uma mensagem **WM \_ DDE \_ ACK** deve excluir todos os átomos que acompanham a mensagem. Se o aplicativo receber um **\_ WM DDE \_ ACK** em resposta a uma mensagem com um objeto de memória global que acompanha e o objeto tiver sido enviado com os **sinalizadores fRelease** definidos como **FALSE,** o aplicativo será responsável por excluir o objeto.

Se o aplicativo receber uma mensagem negativa **do WM \_ DDE \_ ACK** postada em resposta a uma mensagem [**WM \_ DDE \_ ADVISE,**](wm-dde-advise.md) o aplicativo deverá excluir o objeto de memória global postado com a mensagem DE CONSULTORIA do **WM \_ DDE \_** original. Se o aplicativo receber uma mensagem negativa **do WM \_ DDE \_ ACK** postada em resposta a uma mensagem [**WM \_ DDE \_ DATA**](wm-dde-data.md), [**WM \_ DDE WM DDE \_ WM OU**](wm-dde-poke.md)WM [**\_ DDE \_ EXECUTE**](wm-dde-execute.md) message, o aplicativo deverá excluir o objeto de memória global postado com a mensagem **ORIGINAL WM \_ DDE \_ DATA**, **WM \_ DDE WM DDE \_ WM OU** WM **\_ DDE \_ EXECUTE.**

O aplicativo que recebe uma mensagem postada do **\_ WM DDE \_ ACK** deve liberar o parâmetro *lParam* usando a [**função FreeDDElParam.**](/windows/desktop/api/Dde/nf-dde-freeddelparam)

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

[**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)
</dt> <dt>

[**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)
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

[**WM \_ DDE \_ ADVISE**](wm-dde-advise.md)
</dt> <dt>

[**WM \_ DDE \_ DATA**](wm-dde-data.md)
</dt> <dt>

[**WM \_ DDE \_ EXECUTE**](wm-dde-execute.md)
</dt> <dt>

[**WM \_ DDE \_ INITIATE**](wm-dde-initiate.md)
</dt> <dt>

[**WM \_ DDE \_ POKE**](wm-dde-poke.md)
</dt> <dt>

[**SOLICITAÇÃO \_ WM DDE \_**](wm-dde-request.md)
</dt> <dt>

[**WM \_ DDE \_ TERMINATE**](wm-dde-terminate.md)
</dt> <dt>

[**WM \_ DDE \_ UNADVISE**](wm-dde-unadvise.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Sobre Dados Dinâmicos Exchange](about-dynamic-data-exchange.md)
</dt> </dl>

 

