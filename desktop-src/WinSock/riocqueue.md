---
description: Especifica um descritor de fila de conclusão usado para notificação de conclusão de e/s por envio e recebimento de solicitações com as extensões de e/s registradas do Winsock.
ms.assetid: 9196F8AF-3C48-445D-B2D5-E22A99759D92
title: RIO_CQ (Mswsockdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69ca4376c5b130cccaefd7170f62878f31fd1457
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763339"
---
# <a name="rio_cq"></a>RIO de \_ CQ

O **typedef \_ CQ do Rio** especifica um descritor de fila de conclusão usado para notificação de conclusão de e/s por envio e recebimento de solicitações com as extensões de e/s registradas do Winsock.


```C++
typedef struct RIO_CQ_t* RIO_CQ, **PRIO_CQ;
```



<dl> <dt>

**RIO de \_ CQ**
</dt> <dd>

Um tipo de dados que especifica um descritor de fila de conclusão usado para notificação de conclusão de e/s por solicitações de envio e recebimento.

</dd> </dl>

## <a name="remarks"></a>Comentários

O objeto **rio \_ CQ** é usado para a notificação de conclusão de e/s de envio e recebimento de solicitações de rede pelas extensões de e/s registradas pelo Winsock.

Um aplicativo pode usar a função [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) para solicitar notificação quando uma fila de preenchimento do **rio \_ CQ** não está vazia. Um aplicativo também pode sondar o status a qualquer momento de uma fila de conclusão **rio \_ CQ** em uma forma sem bloqueio usando a função [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) .

O objeto **Rio de \_ CQ** é criado usando a função [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) . No momento da criação, o aplicativo deve especificar o tamanho da fila, o que determina quantas entradas de conclusão ela pode conter. Quando um aplicativo chama a função [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) para obter um identificador [**rio \_ RQ**](riorqueue.md) , o aplicativo deve especificar um identificador **Rio de \_ CQ** para as conclusões de envio e um identificador **rio \_ CQ** para as conclusões de recebimento. Esses identificadores podem ser idênticos quando a mesma fila deve ser usada para a conclusão de envio e recebimento. A função **RIOCreateRequestQueue** também requer um número máximo de operações pendentes de envio e recebimento, que são cobradas em relação à capacidade da fila ou filas de conclusão associadas. Se as filas não tiverem capacidade suficiente restante, a chamada **RIOCreateRequestQueue** falhará com [WSAENOBUFS](windows-sockets-error-codes-2.md).

O comportamento de notificação para uma fila de conclusão é definido quando o **Rio de \_ CQ** é criado.

Para uma fila de conclusão que usa um evento, o **tipo** membro da estrutura de [**\_ \_ conclusão de notificação do Rio**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) é definido como **\_ \_ conclusão do evento Rio**. O membro **Event. EventHandle** deve conter o identificador de um evento criado pela função [**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent) ou [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) . Para receber a conclusão de [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , o aplicativo deve aguardar o identificador de evento especificado usando [**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents) ou uma rotina de espera semelhante. Se o aplicativo planeja redefinir e reutilizar o evento, o aplicativo pode reduzir a sobrecarga definindo o membro **Event. NotifyReset** com um valor diferente de zero. Isso faz com que o evento seja redefinido automaticamente pela função **RIONotify** quando a notificação ocorre. Isso reduz a necessidade de chamar a função [**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent) para redefinir o evento entre chamadas para a função **RIONotify** .

Para uma fila de conclusão que usa uma porta de conclusão de e/s, o membro de **tipo** da estrutura de [**\_ \_ conclusão de notificação Rio**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion) é definido como a **\_ \_ conclusão Rio IOCP**. O membro **IOCP. IocpHandle** deve conter o identificador para uma porta de conclusão de e/s criada pela função [**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport) . Para receber a conclusão de [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) , o aplicativo deve chamar a função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) ou [**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex) . O aplicativo deve fornecer um objeto [**sobreposto**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped) dedicado para a fila de conclusão e também pode usar o membro **IOCP. CompletionKey** para distinguir solicitações **RIONotify** na fila de conclusão de outras conclusões de e/s, incluindo preenchimentos **RIONotify** para outras filas de conclusão.

> [!Note]  
> Para fins de eficiência, o acesso às filas de conclusão (as estruturas do **rio \_ CQ** ) e as filas de solicitação (do [**rio \_ RQ**](riorqueue.md) ) não são protegidos por primitivos de sincronização. Se você precisar acessar uma fila de conclusão ou de solicitação de vários threads, o acesso deve ser coordenado por uma seção crítica, bloqueio de gravação de leitor fino ou mecanismo semelhante. Esse bloqueio não é necessário para o acesso por um único thread. Threads diferentes podem acessar filas de solicitações/conclusão separadas sem bloqueios. A necessidade de sincronização ocorre somente quando vários threads tentam acessar a mesma fila. A sincronização também será necessária se vários threads emitirem o envio e receberem no mesmo soquete, pois as operações de envio e recebimento usam a fila de solicitações do soquete.

 

Se vários threads tentarem acessar o mesmo **Rio de \_ CQ** usando [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), o acesso deverá ser coordenado por uma seção crítica, bloqueio de gravador de leitor fino ou mecanismo de exclusão mútua semelhante. Se as filas de conclusão não forem compartilhadas, a exclusão mútua não será necessária.

Quando uma fila de conclusão não for mais necessária, um aplicativo poderá fechá-la usando a função [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) .

O **typedef \_ CQ do Rio** é definido no arquivo de cabeçalho *Mswsockdef. h* que é incluído automaticamente no arquivo de cabeçalho *mswsock. h* . O arquivo de cabeçalho *Mswsockdef. h* nunca deve ser usado diretamente.

## <a name="thread-safety"></a>Acesso thread-safe

Se vários threads tentarem acessar o mesmo **Rio de \_ CQ** usando [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion), o acesso deverá ser coordenado por uma seção crítica, bloqueio de gravador de leitor fino ou mecanismo de exclusão mútua semelhante. Se as filas de conclusão não forem compartilhadas, a exclusão mútua não será necessária.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Mswsockdef. h (incluir mswsock. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CreateIoCompletionPort**](/windows/win32/api/ioapiset/nf-ioapiset-createiocompletionport)
</dt> <dt>

[**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus)
</dt> <dt>

[**GetQueuedCompletionStatusEx**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatusex)
</dt> <dt>

[**SOBREPÕE**](/windows/win32/api/minwinbase/ns-minwinbase-overlapped)
</dt> <dt>

[**\_conclusão da notificação do Rio \_**](/windows/desktop/api/Mswsock/ns-mswsock-rio_notification_completion)
</dt> <dt>

[**\_tipo de \_ conclusão de notificação rio \_**](/windows/desktop/api/Mswsock/ne-mswsock-rio_notification_completion_type)
</dt> <dt>

[**RIO de \_ RQ**](riorqueue.md)
</dt> <dt>

[**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85))
</dt> <dt>

[**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion)
</dt> <dt>

[**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify)
</dt> <dt>

[**WSACreateEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsacreateevent)
</dt> <dt>

[**WSAResetEvent**](/windows/desktop/api/Winsock2/nf-winsock2-wsaresetevent)
</dt> <dt>

[**WSAWaitForMultipleEvents**](/windows/desktop/api/Winsock2/nf-winsock2-wsawaitformultipleevents)
</dt> </dl>

 

 
