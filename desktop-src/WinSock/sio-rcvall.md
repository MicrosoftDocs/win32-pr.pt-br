---
description: O código de controle permite que um soquete receba todos os pacotes IPv4 ou IPv6 passando por uma interface de rede.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: SIO_RCVALL código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ddff631f1fa4b6b9f9af74f71e2b1eb38a2bf48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812415"
---
# <a name="sio_rcvall-control-code"></a>SIO_RCVALL código de controle

## <a name="description"></a>Descrição
O código de controle **sio \_ RCVALL** permite que um soquete receba todos os pacotes IPv4 ou IPv6 passando por uma interface de rede.

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a>Parâmetros

### <a name="s"></a>s

Um descritor que identifica um soquete.

### <a name="dwiocontrolcode"></a>dwIoControlCode

O código de controle para a operação.
Use **sio \_ RCVALL** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada que deve conter o valor da opção.
Os valores possíveis para a opção **sio \_ RCVALL** IOCTL são especificados na enumeração **RCVALL_VALUE** definida no arquivo de cabeçalho *Mstcpip. h* .

Os valores possíveis para **sio \_ RCVALL** são os seguintes:

| Valor | Significado |
|-------|---------|
| **RCVALL \_ desativado** | Desabilite essa opção para que um soquete não receba todos os pacotes IPv4 ou IPv6 passando por uma interface de rede. |
| **RCVALL \_ em** | Habilite essa opção para que um soquete receba todos os pacotes IPv4 ou IPv6 passando por uma interface de rede. Essa opção habilita o modo promíscuo na NIC (placa de interface de rede), se a NIC der suporte ao modo promíscuo. Em um segmento de LAN com um hub de rede, uma NIC que dá suporte ao modo promíscuo capturará todo o tráfego IPv4 ou IPv6 na LAN, incluindo o tráfego entre outros computadores no mesmo segmento de LAN. Todos os pacotes capturados (IPv4 ou IPv6, dependendo do soquete) serão entregues ao soquete bruto. Essa opção não capturará outros pacotes (ARP, IPX e pacotes NetBEUI, por exemplo) na interface. O Netmon usa o mesmo modo para a interface de rede, mas não usa essa opção para capturar o tráfego. |
| **RCVALL \_ SOCKETLEVELONLY** | Este recurso não está implementado no momento; portanto, definir essa opção não tem nenhum efeito. |
| **RCVALL \_ IPLEVEL** | Habilite essa opção para que um soquete IPv4 ou IPv6 receba todos os pacotes no nível de IP passando por uma interface de rede. Essa opção não habilita o modo promíscuo na placa de interface de rede. Essa opção afeta apenas o processamento de pacotes no nível de IP. A NIC ainda recebe apenas os pacotes direcionados para seus endereços unicast e multicast configurados. No entanto, um soquete com essa opção habilitada receberá não apenas os pacotes direcionados para endereços IP específicos, mas receberá todos os pacotes IPv4 ou IPv6 recebidos pela NIC. Essa opção não capturará outros pacotes (ARP, IPX e pacotes NetBEUI, por exemplo) recebidos na interface. |

### <a name="cbinbuffer"></a>cbInBuffer

O tamanho, em bytes, do buffer de entrada.
Esse parâmetro deve ser igual ou maior que o tamanho do **RCVALL_VALUE** valor de enumeração apontado pelo parâmetro *lpvInBuffer* .

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Um ponteiro para o buffer de saída.
Este parâmetro não é usado para esta operação.

### <a name="cboutbuffer"></a>cbOutBuffer

O tamanho, em bytes, do buffer de saída.
Este parâmetro não é usado para esta operação.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.
Este parâmetro não é usado para esta operação.

### <a name="lpvoverlapped"></a>lpvOverlapped

Um ponteiro para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) .

Se o soquete *s* foi criado sem o atributo sobreposto, o parâmetro *lpOverlapped* será ignorado.

Se *s* foi aberto com o atributo Overlapped e o parâmetro *LpOverlapped* não for **nulo**, a operação será executada como uma operação sobreposta (assíncrona).
Nesse caso, o parâmetro *lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.

Para operações sobrepostas, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente, e o método de conclusão apropriado é sinalizado quando a operação é concluída.
Caso contrário, a função não retorna até que a operação seja concluída ou um erro ocorra.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobrepostos).

### <a name="lpthreadid"></a>lpThreadId

Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).
O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.

**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .

### <a name="lperrno"></a>lpErrno

Um ponteiro para o código de erro.

**Observação**  Esse parâmetro se aplica somente à função **WSPIoctl** .

## <a name="return-value"></a>Retornar valor

Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.

Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.
Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Código do erro | Significado |
|------------|---------|
| **\_e/s de WSA \_ pendente** | Uma operação sobreposta foi iniciada com êxito e a conclusão será indicada em um momento posterior. |
| **operação de WSA \_ \_ anulada** | Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **SIO_FLUSH** IOCTL. |
| **WSAEFAULT** | O parâmetro *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário. |
| **WSAEINPROGRESS** | A função é invocada quando um retorno de chamada está em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida. |
| **WSAEINVAL** | O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado. Esse erro também será retornado se o parâmetro *cbInBuffer* for menor que o `sizeof(UCHAR)` ou o parâmetro *lpvInBuffer* apontar para um valor que não seja um **RCVALL_VALUE** valor de enumeração. Esse erro também pode ser retornado se a interface de rede associada ao soquete não puder ser encontrada. Isso pode ocorrer se a interface de rede associada ao soquete for excluída ou removida (um dispositivo de rede PCMCIA ou USB de remoção, por exemplo). |
| **WSAENETDOWN** | Falha no subsistema de rede. |
| **WSAENOBUFS** | Não há espaço disponível no buffer. |
| **WSAENOPROTOOPT** | Não há suporte para a opção de soquete no protocolo especificado. |
| **WSAENOTSOCK** | O descritor *s* não é um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para o comando IOCTL especificado. Esse erro será retornado se o **sio \_ RCVALL** IOCTL não tiver suporte do provedor de transporte. |

## <a name="remarks"></a>Comentários

O **sio \_ RCVALL** IOCTL tem suporte no Windows 2000 e em versões posteriores do sistema operacional.

O IOCTL **sio \_ RCVALL** permite que um soquete receba todos os pacotes IPv4 ou IPv6 em uma interface de rede.
O identificador de soquete passado para a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** deve ser um dos seguintes:

* Um soquete IPv4 que foi criado com a família de endereços definida como AF_INET, o tipo de soquete definido como SOCK_RAW e o protocolo definido como IPPROTO_IP.
* Um soquete IPv6 que foi criado com a família de endereços definida como AF_INET6, o tipo de soquete definido como SOCK_RAW e o protocolo definido como IPPROTO_IPV6.

Para obter mais informações sobre soquetes brutos, consulte [**soquetes brutos TCP/IP**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).

O soquete também deve estar associado a uma interface IPv4 ou IPv6 local explícita, o que significa que você não pode fazer a ligação com **\_ qualquer endereço** ou **in6addr \_**.

Depois que o soquete é associado e o IOCTL é concluído com êxito, as chamadas para as funções [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) ou [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) retornam datagrams IPv4 que passam pela interface IPv4 fornecida ou retornam datagrams IPv6 passando pela interface IPv6 fornecida.
Observe que você deve fornecer um buffer suficientemente grande.
Definir esse IOCTL só capturará pacotes IPv4 ou IPv6 em uma determinada interface.
Esse IOCTL não capturará outros pacotes (ARP, IPX e pacotes NetBEUI, por exemplo) na interface.

Um soquete associado a uma interface local específica com o IOCTL **sio \_ RCVALL** receberá apenas os pacotes que passam pela interface.
Ele não receberá pacotes recebidos em outra interface e será encaminhado em outra interface diferente do soquete associado com **sio \_ RCVALL** IOCTL.

No Windows Server 2008 e versões anteriores, a configuração de IOCTL **sio \_ RCVALL** não capturaria pacotes locais enviados de uma interface de rede.
Isso incluiu os pacotes recebidos em outra interface e encaminhou a interface de rede especificada para o **sio \_ RCVALL** IOCTL.

No Windows 7 e no Windows Server 2008 R2, isso foi alterado para que os pacotes locais enviados de uma interface de rede também sejam capturados.
Isso inclui os pacotes recebidos em outra interface e, em seguida, encaminhado o adaptador de rede associado ao soquete com **sio \_ RCVALL** IOCTL.

Definir esse IOCTL requer privilégio de administrador no computador local.

Esse recurso é, às vezes, chamado de modo promíscuo.
Qualquer alteração direta da aplicação dessa opção em uma interface e, em seguida, a outra interface com uma única chamada usando esse IOCTL não é suportada.
Um aplicativo deve primeiro usar este IOCTL para desativar o comportamento na primeira interface e, em seguida, usar este IOCTL para habilitar o comportamento em uma nova interface.

## <a name="see-also"></a>Confira também

[**SSA**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**Soquetes brutos TCP/IP**](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
