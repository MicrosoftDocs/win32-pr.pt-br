---
description: O código de controle configura um soquete TCP para menor latência e operações mais rápidas na interface de loopback.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: SIO_LOOPBACK_FAST_PATH código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f32cba8a081d2eb268a3e93a362ccec9bf414d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105798304"
---
# <a name="sio_loopback_fast_path-control-code"></a>SIO_LOOPBACK_FAST_PATH código de controle

## <a name="description"></a>Descrição

O código de controle de **\_ \_ \_ caminho rápido de auto-retorno sio** configura um soquete TCP para latência mais baixa e operações mais rápidas na interface de loopback.

**Importante**  O **\_ \_ \_ caminho rápido do loopback sio** foi preterido e não é recomendável usá-lo em seu código.

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
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
Use **o \_ \_ \_ caminho rápido de auto-retorno sio** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada.
Esse parâmetro contém um ponteiro para um valor booliano que indica se o soquete deve ser configurado para operações de auto-retorno rápido.

### <a name="cbinbuffer"></a>cbInBuffer

O tamanho, em bytes, do buffer de entrada.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Um ponteiro para o buffer de saída.
Este parâmetro não é usado para esta operação.

### <a name="cboutbuffer"></a>cbOutBuffer

O tamanho, em bytes, do buffer de saída.
Esse parâmetro deve ser definido como zero.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.

Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* apontará para um valor **DWORD** igual a zero.

Se *lpOverlapped* for **NULL**, o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.

Se o parâmetro *lpOverlapped* não for **nulo** para os soquetes sobrepostos, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada mais tarde.
O valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* que é retornado pode ser zero, já que o tamanho dos dados armazenados não pode ser determinado até que a operação sobreposta seja concluída.
O status final de conclusão pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.

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
|**\_e/s de WSA \_ pendente** | A operação de e/s sobreposta está em andamento. Esse valor será retornado se uma operação sobreposta tiver sido iniciada com êxito e a conclusão será indicada mais tarde. |
| **operação de WSA \_ \_ anulada** | A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo. Esse erro será retornado se uma operação sobreposta tiver sido cancelada devido ao fechamento do soquete ou à execução do comando **sio \_ flush IOCTL** . |
| **WSAEACCES** | Foi feita uma tentativa de acessar um soquete de uma maneira proibida por suas permissões de acesso. Esse erro é retornado sob várias condições para reservas de porta persistentes que incluem o seguinte: o usuário não tem os privilégios administrativos necessários no computador local ou o aplicativo não está sendo executado em um shell avançado como o administrador interno ( `RunAs administrator` ). |
| **WSAEFAULT** | O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada. Esse erro é retornado do parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço de usuário. |
| **WSAEINPROGRESS** | Uma operação de bloqueio está atualmente em execução. Esse erro será retornado se a função for invocada quando um retorno de chamada estiver em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida por uma chamada para [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Esse erro será retornado se uma operação de bloqueio tiver sido interrompida. |
| **WSAEINVAL** | Foi fornecido um argumento inválido. Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado. |
| **WSAENETDOWN** | Uma operação de soquete encontrou uma rede inoperante. Esse erro será retornado se o subsistema de rede tiver falhado. |
| **WSAENOTSOCK** | Uma operação foi tentada em algo que não é um soquete. Esse erro será retornado se o descritor *s* não for um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para a operação tentada para o tipo de objeto referenciado. Esse erro será retornado se o comando IOCTL especificado não tiver suporte. Esse erro também será retornado se o **sio \_ de \_ circuito \_ rápido de auto-retorno** não tiver suporte do provedor de transporte. |

## <a name="remarks"></a>Comentários

Um aplicativo pode usar o **sio \_ loopback \_ Fast \_ Path** IOCTL para reduzir a latência e melhorar o desempenho de operações de auto-retorno em um soquete TCP.
Esse IOCTL solicita que a pilha TCP/IP use um caminho rápido especial para operações de loopback neste soquete.
O IOCTL de **\_ \_ \_ caminho rápido de auto-retorno sio** só pode ser usado com soquetes TCP.
Esse IOCTL deve ser usado em ambos os lados da sessão de loopback.
O caminho rápido de loopback de TCP tem suporte usando a interface de loopback IPv4 ou IPv6.

O soquete que planeja iniciar a solicitação de conexão deve aplicar esse IOCTL antes de fazer a solicitação de conexão.
Portanto, o soquete usado pela função [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)ou [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) para iniciar a conexão deve aplicar esse IOCTL para usar o caminho rápido para operações de loopback.

O soquete que está escutando a solicitação de conexão deve aplicar esse IOCTL antes de aceitar a conexão.
Portanto, o soquete usado pela função Listen deve aplicar esse IOCTL para que qualquer soquete aceito use o caminho rápido para loopback.
Todos os soquetes retornados pela função Listen e passados para a função [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) serão marcados para usar o caminho rápido especial para operações de loopback.

Depois que um aplicativo estabelece a conexão em uma interface de loopback usando o caminho rápido, todos os pacotes para o tempo de vida da conexão devem usar o caminho rápido.

A aplicação do **\_ \_ \_ caminho rápido de auto-retorno sio** a um soquete que será conectado a um caminho de não loopback não terá nenhum efeito.

Essa otimização de auto-retorno de TCP resulta em pacotes que fluem pela camada de transporte (TL) em vez do loopback tradicional por meio da camada de rede.
Essa otimização melhora a latência de pacotes de loopback.
Quando um aplicativo opta por uma configuração de nível de conexão para usar o caminho rápido de loopback, todos os pacotes seguirão o caminho de loopback.
Para comunicações de loopback, o congestionamento e o descarte de pacotes não são esperados.
A noção do controle de congestionamento e da entrega confiável no TCP será desnecessária.
No entanto, isso não é verdadeiro para o controle de fluxo.
Sem o controle de fluxo, o remetente pode sobrecarregar o buffer de recebimento, levando ao comportamento de loopback de TCP errado.
O controle de fluxo no caminho de loopback otimizado para TCP é mantido colocando solicitações de envio em uma fila.
Quando o buffer de recebimento estiver cheio, a pilha TCP/IP garante que os envios não serão concluídos até que a fila seja atendida mantendo o controle de fluxo.

As conexões de loopback de caminho rápido TCP na presença de um texto explicativo da WFP (plataforma de filtragem do Windows) para dados de conexão devem usar o caminho lento não otimizado para loopback.
Portanto, os filtros de WFP impedirão que esse novo caminho rápido de loopback seja usado.
Quando um filtro WFP estiver habilitado, o sistema usará o caminho lento mesmo que o IOCTL **de \_ \_ \_ caminho rápido de auto-retorno sio** fosse definido.
Isso garante que os aplicativos de modo de usuário tenham o recurso de segurança WFP completo.

Por padrão, **o \_ \_ \_ caminho rápido de auto-retorno sio** está desabilitado.

Há suporte apenas para um subconjunto das opções de soquete TCP/IP quando o IOCTL de **\_ \_ \_ caminho rápido de loopback sio** é usado para habilitar o caminho rápido de loopback em um soquete.
A lista de opções com suporte inclui o seguinte:

* **TTL de IP \_**
* **IP \_ unicast \_ se**
* **\_Saltos de unicast IPv6 \_**
* **Unicast IPV6 \_ \_ se**
* **\_V6ONLY IPv6**
* **por isso, \_ \_ aceite condicional**
* **\_EXCLUSIVEADDRUSE**
* **Portanto \_ , \_ escalabilidade de porta**
* **\_RCVBUF**
* **\_REUSEADDR**
* **\_BSDURGENT TCP**

## <a name="see-also"></a>Confira também

[**Opções de soquete IPPROTO_IP**](/windows/desktop/winsock/ipproto-ip-socket-options)

[**Opções de Soquete IPPROTO_IPV6**](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[**Opções de soquete IPPROTO_TCP**](/windows/desktop/winsock/ipproto-tcp-socket-options)

[**SSA**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**Opções de Soquete SOL_SOCKET**](/windows/desktop/winsock/sol-socket-socket-options)

[**WSAGetLastError**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
