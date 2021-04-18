---
description: O código de controle obtém uma lista de endereços de transporte locais da família de protocolos do soquete à qual o aplicativo pode ser associado.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: SIO_ADDRESS_LIST_QUERY código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 7a728293afa51ceb58d61141e7184077478b787c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105762221"
---
# <a name="sio_address_list_query-control-code"></a>SIO_ADDRESS_LIST_QUERY código de controle

## <a name="description"></a>Descrição

O código de controle de **\_ consulta da \_ lista \_ de endereços sio** Obtém uma lista de endereços de transporte locais da família de protocolos do soquete à qual o aplicativo pode se associar.
A lista de endereços varia de acordo com a família de endereços e alguns endereços são excluídos da lista.

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a>Parâmetros

### <a name="s"></a>s

Um descritor que identifica um soquete.

### <a name="dwiocontrolcode"></a>dwIoControlCode

O código de controle para a operação.
Use **a \_ \_ \_ consulta de lista de endereços do sio** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada.
Este parâmetro não é usado para esta operação.

### <a name="cbinbuffer"></a>cbInBuffer

O tamanho, em bytes, do buffer de entrada.
Este parâmetro não é usado para esta operação.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Um ponteiro para o buffer de saída.

### <a name="cboutbuffer"></a>cbOutBuffer

O tamanho, em bytes, do buffer de saída.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.

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

Um ponteiro para uma estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usado pelo provedor em uma chamada subsequente para [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).
O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até que a função [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) seja retornada.

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
| **operação de WSA \_ \_ anulada** | Uma operação sobreposta foi cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush** IOCTL. |
| **WSAEFAULT** | O parâmetro *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário. |
| **WSAEINPROGRESS** | A função é invocada quando um retorno de chamada está em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida. |
| **WSAEINVAL** | O parâmetro *dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado. Esse erro será retornado se o parâmetro *cbInBuffer* não estiver definido como **NULL**. |
| **WSAENETDOWN** | Falha no subsistema de rede. |
| **WSAENOBUFS** | Não há espaço disponível no buffer. |
| **WSAENOPROTOOPT** | Não há suporte para a opção de soquete no protocolo especificado. |
| **WSAENOTSOCK** | O descritor *s* não é um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para o comando IOCTL especificado. Esse erro será retornado se a **\_ consulta de \_ lista \_ de endereços sio** IOCTL não tiver suporte do provedor de transporte. |

## <a name="remarks"></a>Comentários

A **\_ consulta de \_ lista \_ de endereços sio** do IOCTL tem suporte no Windows 2000 e em versões posteriores do sistema operacional.

O código de controle de **\_ consulta da \_ lista \_ de endereços sio** Obtém uma lista de endereços de transporte locais da família de protocolos do soquete à qual o aplicativo pode se associar.
A lista de endereços varia de acordo com a família de endereços.

Para a \_ família de endereços INET6 de AF, todos os endereços são retornados, exceto o seguinte:

* Qualquer endereço IP em que o estado de detecção de endereço duplicado (DAD) não é IpDadStatePreferred.
* Qualquer endereço IP com um nível de escopo inferior a ScopeLevelSubnet em uma interface em que o tipo de interface é **se for \_ tipo \_ \_ loopback de software**.
Isso significa que os endereços de link local (FE80: *) e loopback (:: 1) em interfaces do **\_ tipo \_ \_ loopback de software de tipos** são excluídos, mas não se esses endereços estiverem em uma interface com um tipo diferente.

Para a família de endereços **\_ inet** da série AF, todos os endereços são retornados, exceto o seguinte:

* Qualquer endereço IP em que o estado de detecção de endereço duplicado (DAD) não é IpDadStatePreferred.
* Qualquer endereço IP em uma interface em que o tipo de interface é **se o \_ tipo \_ \_ loopback de software** e link for local.
Isso significa que endereços de link local (169,254.*) e loopback (127.*) em interfaces **do \_ tipo \_ \_ loopback de software** são excluídos, mas não se esses endereços estiverem em uma interface com um tipo diferente.

Para obter mais informações sobre o estado de DAD, consulte a documentação do auxiliar de IP na estrutura de endereços [**IP \_ Dad \_**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) Enumeration e [**IP \_ Adapter \_ unicast \_ Address**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) e a documentação MIB na estrutura de [**\_ \_ linha MIB UNICASTIPADDRESS**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) .
Para obter mais informações sobre o tipo de interface, consulte a documentação auxiliar de IP na estrutura [**\_ \_ endereços de adaptador IP**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) e a função [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) e a documentação MIB na estrutura [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) .
Para obter mais informações sobre o nível de escopo, consulte a documentação auxiliar de IP na estrutura de [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) e a enumeração de [**\_ nível de escopo**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) .

A lista retornada no buffer de saída apontada pelo parâmetro *lpvOutBuffer* está na forma de uma estrutura de [**\_ \_ lista de endereços de soquete**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) .

Se o buffer de saída especificado no parâmetro *lpvOutBuffer* não for grande o suficiente para conter a lista de endereços, o **\_ erro de soquete** será retornado como resultado desse IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [WSAEFAULT](windows-sockets-error-codes-2.md).
O tamanho necessário, em bytes, para o buffer de saída é retornado no parâmetro *lpcbBytesReturned* nesse caso.
Observe que o código de erro [WSAEFAULT](windows-sockets-error-codes-2.md) também será retornado se o parâmetro *lpvInBuffer*, *lpvOutBuffer* ou *lpcbBytesReturned* não estiver completamente contido em uma parte válida do espaço de endereço de usuário.

A **\_ consulta de \_ lista \_ de endereços sio** IOCTL normalmente é chamada de forma síncrona com o parâmetro *lpvOverlapped* definido como **NULL**, pois a lista de endereços é retornada imediatamente.

**Observação**  Em ambientes Windows plug-n-play, os endereços podem ser adicionados e removidos dinamicamente.
Portanto, os aplicativos não podem contar com as informações retornadas pela **\_ consulta de \_ lista \_ de endereços sio** para serem persistentes.
Os aplicativos podem se registrar para notificações de alteração de endereço por meio do IOCTL de **\_ alteração da \_ lista \_ de endereços sio** , que fornece notificação por meio do evento de alteração da lista de endereços e/s sobreposta ou **FD \_ \_ \_** .
A seguinte sequência de ações pode ser usada para garantir que o aplicativo sempre tenha informações da lista de endereços atual:

* Emitir o IOCTL de **\_ alteração da \_ lista \_ de endereços sio**
* Emitir o IOCTL de **\_ consulta de \_ lista \_ de endereços sio**
* Sempre que a chamada de **\_ alteração da \_ lista \_ de endereços sio** notifica o aplicativo sobre uma alteração na lista de endereços (por meio de e/s sobreposta ou sinalizando o evento de **alteração da \_ lista de endereços \_ \_ FD** ), toda a sequência de ações deve ser repetida.

No SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior, a organização dos arquivos de cabeçalho foi alterada e o código de controle de consulta da lista de endereços do sio é definido no arquivo de cabeçalho *Ws2def. h* . **\_ \_ \_**
Observe que o arquivo de cabeçalho *Ws2def. h* é incluído automaticamente no *Winsock2. h* e nunca deve ser usado diretamente.

## <a name="see-also"></a>Confira também

[**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[**IP_ADAPTER_UNICAST_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[**IP_DAD_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[**MIB_UNICASTIPADDRESS_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[**SCOPE_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[**SOCKET_ADDRESS_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[**SSA**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
