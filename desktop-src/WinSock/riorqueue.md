---
description: Especifica um descritor de soquete usado pelas solicitações de envio e recebimento com as extensões de e/s registradas do Winsock.
ms.assetid: 50E9516C-6078-4466-A593-3F29E4783740
title: RIO_RQ (Mswsockdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c25abebbe40842532f3cca180868b5b3786e756d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296597"
---
# <a name="rio_rq"></a>RIO de \_ RQ

O **typedef \_ RQ de Rio** especifica um descritor de soquete usado pelas solicitações de envio e recebimento com as extensões de e/s registradas do Winsock.


```C++
typedef struct RIO_RQ_t* RIO_RQ, **PRIO_RQ;
```



<dl> <dt>

**RIO de \_ RQ**
</dt> <dd>

Um tipo de dados que especifica um descritor de soquete usado pelas solicitações de envio e recebimento.

</dd> </dl>

## <a name="remarks"></a>Comentários

As extensões de e/s registradas no Winsock operam principalmente em um objeto **rio \_ RQ** em vez de um soquete. Um aplicativo obtém um **Rio de \_ RQ** para um soquete existente usando a função [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) . O soquete de entrada deve ter sido criado chamando-se a função [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) com o sinalizador **WSA \_ sinalizador \_ Rio** definido no parâmetro *dwFlags* .

Depois de obter um objeto **Rio de \_ RQ** , o descritor de soquete subjacente permanece válido. Um aplicativo pode continuar a usar o soquete subjacente para definir e consultar opções de soquete, emitir IOCTLs e, por fim, fechar o soquete.

> [!Note]  
> Para fins de eficiência, o acesso às filas de conclusão (as estruturas do [**rio \_ CQ**](riocqueue.md) ) e as filas de solicitação (do **rio \_ RQ** ) não são protegidos por primitivos de sincronização. Se você precisar acessar uma fila de conclusão ou de solicitação de vários threads, o acesso deve ser coordenado por uma seção crítica, bloqueio de gravação de leitor fino ou mecanismo semelhante. Esse bloqueio não é necessário para o acesso por um único thread. Threads diferentes podem acessar filas de solicitações/conclusão separadas sem bloqueios. A necessidade de sincronização ocorre somente quando vários threads tentam acessar a mesma fila. A sincronização também será necessária se vários threads emitirem o envio e receberem no mesmo soquete, pois as operações de envio e recebimento usam a fila de solicitações do soquete.

 

O [**typedef \_ RQ do Rio**](riocqueue.md) é definido no arquivo de cabeçalho *Mswsockdef. h* que é incluído automaticamente no arquivo de cabeçalho *mswsock. h* . O arquivo de cabeçalho *Mswsockdef. h* nunca deve ser usado diretamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                        |
| parâmetro<br/>                   | <dl> <dt>Mswsockdef. h (incluir mswsock. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue)
</dt> <dt>

[**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive)
</dt> <dt>

[**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex)
</dt> <dt>

[**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85))
</dt> <dt>

[**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend)
</dt> <dt>

[**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85))
</dt> <dt>

[**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)
</dt> </dl>

 

 
