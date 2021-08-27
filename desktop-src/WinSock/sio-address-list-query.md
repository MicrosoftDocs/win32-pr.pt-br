---
description: O código de controle obtém uma lista de endereços de transporte local da família de protocolo do soquete à qual o aplicativo pode ser associado.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: SIO_ADDRESS_LIST_QUERY de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 57d529ed4ea525b01e294efcacc1aa8dd2b118106177bd46cb64ffdf42a31a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097526"
---
# <a name="sio_address_list_query-control-code"></a>SIO_ADDRESS_LIST_QUERY de controle

## <a name="description"></a>Descrição

O **código de controle SIO ADDRESS LIST \_ \_ \_ QUERY** obtém uma lista de endereços de transporte local da família de protocolo do soquete à qual o aplicativo pode ser associado.
A lista de endereços varia de acordo com a família de endereços e alguns endereços são excluídos da lista.

Para executar essa operação, chame a [**função WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) **ou WSPIoctl** com os parâmetros a seguir.

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

### <a name="dwiocontrolcode"></a>Dwiocontrolcode

O código de controle para a operação.
Use **CONSULTA DE LISTA DE \_ \_ \_ ENDEREÇOS SIO** para esta operação.

### <a name="lpvinbuffer"></a>Lpvinbuffer

Um ponteiro para o buffer de entrada.
Esse parâmetro não éusado para esta operação.

### <a name="cbinbuffer"></a>Cbinbuffer

O tamanho, em bytes, do buffer de entrada.
Esse parâmetro não éusado para esta operação.

### <a name="lpvoutbuffer"></a>Lpvoutbuffer

Um ponteiro para o buffer de saída.

### <a name="cboutbuffer"></a>cbOutBuffer

O tamanho, em bytes, do buffer de saída.

### <a name="lpcbbytesreturned"></a>Lpcbbytesreturned

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.

### <a name="lpvoverlapped"></a>lpvOverlapped

Um ponteiro para uma [**estrutura WSAOVERLAPPED.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

Se o *soquete s* tiver sido criado sem o atributo sobrecodado, *o parâmetro lpOverlapped* será ignorado.

Se *s* foi aberto com o atributo sobre mapeado e o parâmetro *lpOverlapped* não é **NULL,** a operação é executada como uma operação sobressalo (assíncrona).
Nesse caso, *o parâmetro lpOverlapped* deve apontar para uma estrutura [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) válida.

Para operações sobreporadas, a [**função WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retorna imediatamente e o método de conclusão apropriado é sinalizado quando a operação é concluída.
Caso contrário, a função não retornará até que a operação seja concluída ou ocorra um erro.

### <a name="lpcompletionroutine"></a>Lpcompletionroutine

Tipo: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Um ponteiro para a rotina de conclusão chamada quando a operação foi concluída (ignorada para soquetes não sobre mapeados).

### <a name="lpthreadid"></a>lpThreadId

Um ponteiro para uma [**estrutura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usada pelo provedor em uma chamada subsequente para [**WPUQueueApc.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)
O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até depois que a [**função WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) retornar.

**Observação**  Esse parâmetro se aplica somente à **função WSPIoctl.**

### <a name="lperrno"></a>Lperrno

Um ponteiro para o código de erro.

**Observação**  Esse parâmetro se aplica somente à **função WSPIoctl.**

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com êxito, a [**função WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) **ou WSPIoctl** retornará zero.

Se a operação falhar ou estiver pendente, a [**função WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **SOCKET \_ ERROR**.
Para obter informações de erro estendidas, [**chame WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Código do erro | Significado |
|------------|---------|
| **\_E/S WSA \_ PENDENTE** | Uma operação sobrecarada foi iniciada com êxito e a conclusão será indicada posteriormente. |
| **OPERAÇÃO WSA \_ \_ ANULADA** | Uma operação sobrecarada foi cancelada devido ao fechamento do soquete ou à execução do comando **IOCTL SIO \_ FLUSH.** |
| **WSAEFAULT** | O *parâmetro lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário. |
| **Wsaeinprogress** | A função é invocada quando um retorno de chamada está em andamento. |
| **Wsaeintr** | Uma operação de bloqueio foi interrompida. |
| **Wsaeinval** | O *parâmetro dwIoControlCode* não é um comando válido ou um parâmetro de entrada especificado não é aceitável ou o comando não é aplicável ao tipo de soquete especificado. Esse erro será retornado se o *parâmetro cbInBuffer* não estiver definido como **NULL.** |
| **WSAENETDOWN** | O subsistema de rede falhou. |
| **WSAENOBUFS** | Nenhum espaço de buffer disponível. |
| **Wsaenoprotoopt** | Não há suporte para a opção de soquete no protocolo especificado. |
| **Wsaenotsock** | O descritor *s não* é um soquete. |
| **Wsaeopnotsupp** | Não há suporte para o comando IOCTL especificado. Esse erro será retornado se o IOCTL de CONSULTA DE LISTA DE ENDEREÇOS SIO não for suportado pelo provedor de transporte. **\_ \_ \_** |

## <a name="remarks"></a>Comentários

O IOCTL DE CONSULTA DE LISTA DE ENDEREÇOS SIO tem suporte Windows 2000 e versões posteriores do sistema operacional. **\_ \_ \_**

O **código de controle SIO ADDRESS LIST \_ \_ \_ QUERY** obtém uma lista de endereços de transporte local da família de protocolo do soquete à qual o aplicativo pode ser associado.
A lista de endereços varia de acordo com a família de endereços.

Para a família \_ de endereços AF INET6, todos os endereços são retornados, exceto pelo seguinte:

* Qualquer endereço IP em que o estado DEAM (detecção de endereço duplicado) não é IpDadStatePreferred.
* Qualquer endereço IP com um nível de escopo inferior a ScopeLevelSubnet em uma interface em que o tipo de interface **é IF TYPE SOFTWARE \_ \_ \_ LOOPBACK**.
Isso significa que os endereços de link local (fe80:*) e loopback (::1) em interfaces do tipo **IF \_ TYPE SOFTWARE \_ \_ LOOPBACK** são excluídos, mas não se esses endereços estão em uma interface com um tipo diferente.

Para a **família \_ de endereços INET** do AF, todos os endereços são retornados, exceto pelo seguinte:

* Qualquer endereço IP em que o estado DEAM (detecção de endereço duplicado) não é IpDadStatePreferred.
* Qualquer endereço IP em uma interface em que o tipo de interface **é IF TYPE SOFTWARE \_ \_ \_ LOOPBACK** e link é local.
Isso significa que os endereços link-local (169.254. ) e *loopback (127.*) em interfaces do tipo **IF TYPE SOFTWARE \_ \_ \_ LOOPBACK** serão excluídos, mas não se esses endereços estão em uma interface com um tipo diferente.

Para obter mais informações sobre o estado DO PAI, consulte a documentação do Auxiliar de IP sobre a enumeração [**IP \_ DAD \_ STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) e a estrutura IP [**ADAPTER \_ \_ UNICAST \_ ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) e a documentação do MIB sobre a estrutura [**MIB \_ UNICASTIPADDRESS \_ ROW.**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)
Para obter mais informações sobre o tipo de interface, consulte a documentação do Auxiliar de IP sobre a estrutura IP [**\_ ADAPTER \_ ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) e a função [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) e a documentação do MIB [**sobre**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) MIB_IF_ROW2 estrutura.
Para obter mais informações sobre o nível de escopo, consulte a documentação do Auxiliar de IP na estrutura [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) e a [**enumeração SCOPE \_ LEVEL.**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

A lista retornada no buffer de saída apontado pelo parâmetro *lpvOutBuffer* está na forma de uma estrutura [**SOCKET ADDRESS \_ \_ LIST.**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

Se o buffer de saída especificado no parâmetro *lpvOutBuffer* não for grande o suficiente para conter a lista de endereços, **SOCKET \_ ERROR** será retornado como resultado desse IOCTL e [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [WSAEFAULT.](windows-sockets-error-codes-2.md)
O tamanho necessário, em bytes, para o buffer de saída é retornado no *parâmetro lpcbBytesReturned* nesse caso.
Observe que o código de [erro WSAEFAULT](windows-sockets-error-codes-2.md) também será retornado se o parâmetro *lpvInBuffer*, *lpvOutBuffer* ou *lpcbBytesReturned* não estiver completamente contido em uma parte válida do espaço de endereço do usuário.

O IOCTL DE CONSULTA DE LISTA DE ENDEREÇOS SIO normalmente é chamado de forma síncrona com o parâmetro *lpvOverlapped* definido como **NULL,** pois a lista de endereços é retornada imediatamente. **\_ \_ \_**

**Observação**  Em Windows ambientes Plug-n-Play, os endereços podem ser adicionados e removidos dinamicamente.
Portanto, os aplicativos não podem contar com as informações retornadas pela **CONSULTA \_ LISTA \_ \_ DE** ENDEREÇOS SIO para serem persistentes.
Os aplicativos podem se registrar para notificações de alteração de endereço por meio do IOCTL DE ALTERAÇÃO DE LISTA DE ENDEREÇOS SIO, que fornece notificação por meio de um evento de ALTERAÇÃO de LISTA DE ENDEREÇOS de ENDEREÇO DE **\_ \_ \_ FD** ou E/S sobressalificado. **\_ \_ \_**
A seguinte sequência de ações pode ser usada para garantir que o aplicativo sempre tenha informações de lista de endereços atuais:

* Emitir o **IOCTL DE ALTERAÇÃO \_ DA LISTA DE \_ \_ ENDEREÇOS SIO**
* Emitir o **IOCTL DE CONSULTA DA LISTA DE \_ \_ \_ ENDEREÇOS SIO**
* Sempre que a chamada IOCTL DE ALTERAÇÃO DE LISTA DE ENDEREÇOS **SIO \_ \_ \_** notifica a aplicação de uma alteração de lista de endereços (seja por meio de E/S sobrecarada ou sinalizando o evento **FD \_ ADDRESS LIST \_ \_ CHANGE),** toda a sequência de ações deve ser repetida.

No SDK (Software Development Kit) do Microsoft Windows lançado para o Windows Vista e posterior, a organização dos arquivos de título foi alterada e o código de controle **SIO \_ ADDRESS LIST \_ \_ QUERY** é definido no arquivo de título *Ws2def.h.*
Observe que o *arquivo de título Ws2def.h* é incluído automaticamente no *Winsock2.h* e nunca deve ser usado diretamente.

## <a name="see-also"></a>Confira também

[**Getadaptersaddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[**Ip_adapter_addresses**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[**Ip_adapter_unicast_address**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[**IP_DAD_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[**MIB_UNICASTIPADDRESS_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[**SCOPE_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[**SOCKET_ADDRESS_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[**Soquete**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**Wsagetlasterror**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**Wsagetoverlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**Wsaioctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlapped**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
