---
description: O código de controle configura um soquete TCP para operações de menor latência e mais rápidas na interface de loopback.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: SIO_LOOPBACK_FAST_PATH de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8650cd267d321569aca584e7195fb1bdb79c83a33d931e59e8db37521b8933a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740405"
---
# <a name="sio_loopback_fast_path-control-code"></a>SIO_LOOPBACK_FAST_PATH de controle

## <a name="description"></a>Descrição

O código de controle PATH FAST **\_ LOOPBACK \_ \_** do SIO configura um soquete TCP para operações de menor latência e mais rápidas na interface de loopback.

**Importante**  O **CAMINHO DO \_ LOOPBACK FAST \_ \_ SIO** foi preterido e não é recomendável ser usado em seu código.

Para executar essa operação, chame a [**função WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) **ou WSPIoctl** com os parâmetros a seguir.

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

### <a name="dwiocontrolcode"></a>Dwiocontrolcode

O código de controle para a operação.
Use **SIO \_ LOOPBACK \_ FAST \_ PATH** para esta operação.

### <a name="lpvinbuffer"></a>Lpvinbuffer

Um ponteiro para o buffer de entrada.
Esse parâmetro contém um ponteiro para um valor booliana que indica se o soquete deve ser configurado para operações rápidas de loopback.

### <a name="cbinbuffer"></a>Cbinbuffer

O tamanho, em bytes, do buffer de entrada.

### <a name="lpvoutbuffer"></a>Lpvoutbuffer

Um ponteiro para o buffer de saída.
Esse parâmetro não éusado para esta operação.

### <a name="cboutbuffer"></a>cbOutBuffer

O tamanho, em bytes, do buffer de saída.
Esse parâmetro deve ser definido como zero.

### <a name="lpcbbytesreturned"></a>Lpcbbytesreturned

Um ponteiro para uma variável que recebe o tamanho, em bytes, dos dados armazenados no buffer de saída.

Se o buffer de saída for muito pequeno, a chamada falhará, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retornará [**WSAEINVAL**](windows-sockets-error-codes-2.md)e o parâmetro *lpcbBytesReturned* aponta para um **valor DWORD** de zero.

Se *lpOverlapped* for **NULL,** o valor **DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado em uma chamada bem-sucedida não poderá ser zero.

Se o *parâmetro lpOverlapped* não for **NULL** para soquetes sobrepondo, as operações que não puderem ser concluídas imediatamente serão iniciadas e a conclusão será indicada posteriormente.
O **valor DWORD** apontado pelo parâmetro *lpcbBytesReturned* retornado pode ser zero, pois o tamanho dos dados armazenados não pode ser determinado até que a operação sobrecarregada seja concluída.
O status de conclusão final pode ser recuperado quando o método de conclusão apropriado é sinalizado quando a operação é concluída.

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

Um ponteiro para uma [**estrutura WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) a ser usada pelo provedor em uma chamada subsequente para [**WPUQueueApc.**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)
O provedor deve armazenar a estrutura [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) referenciada (não o ponteiro para o mesmo) até depois que a [**função WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) retornar.

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
|**\_E/S WSA \_ PENDENTE** | A operação de E/S sobressalo está em andamento. Esse valor será retornado se uma operação sobrecarrada tiver sido iniciada com êxito e a conclusão for indicada posteriormente. |
| **OPERAÇÃO WSA \_ \_ ANULADA** | A operação de E/S foi anulada devido a uma saída de thread ou a uma solicitação de aplicativo. Esse erro será retornado se uma operação sobrecarrada tiver sido cancelada devido ao fechamento do soquete ou à execução do comando **\_ IOCTL SIO FLUSH.** |
| **Wsaeacces** | Foi feita uma tentativa de acessar um soquete de uma maneira proibida por suas permissões de acesso. Esse erro é retornado em várias condições para reservas de porta persistentes que incluem o seguinte: o usuário não tem os privilégios administrativos necessários no computador local ou o aplicativo não está em execução em um shell aprimorado como o Administrador integrado ( `RunAs administrator` ). |
| **WSAEFAULT** | O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada. Esse erro é retornado do parâmetro *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário. |
| **Wsaeinprogress** | Uma operação de bloqueio está atualmente em execução. Esse erro será retornado se a função for invocada quando um retorno de chamada estiver em andamento. |
| **Wsaeintr** | Uma operação de bloqueio foi interrompida por uma chamada para [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall). Esse erro será retornado se uma operação de bloqueio tiver sido interrompida. |
| **Wsaeinval** | Foi fornecido um argumento inválido. Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado. |
| **WSAENETDOWN** | Uma operação de soquete encontrou uma rede inoperante. Esse erro será retornado se o subsistema de rede tiver falhado. |
| **Wsaenotsock** | Foi tentada uma operação em algo que não é um soquete. Esse erro será retornado se o descritor *s* não for um soquete. |
| **Wsaeopnotsupp** | A operação tentada não tem suporte para o tipo de objeto referenciado. Esse erro será retornado se o comando IOCTL especificado não tiver suporte. Esse erro também será retornado se o **SIO \_ LOOPBACK \_ FAST \_ PATH** IOCTL não for suportado pelo provedor de transporte. |

## <a name="remarks"></a>Comentários

Um aplicativo pode usar o **SIO \_ LOOPBACK \_ FAST \_ PATH** IOCTL para reduzir a latência e melhorar o desempenho de operações de loopback em um soquete TCP.
Esse IOCTL solicita que a pilha TCP/IP use um caminho rápido especial para operações de loopback nesse soquete.
O **SIO \_ LOOPBACK \_ FAST \_ PATH** IOCTL só pode ser usado com soquetes TCP.
Esse IOCTL deve ser usado em ambos os lados da sessão de loopback.
Há suporte para o caminho rápido de loopback TCP usando a interface de loopback IPv4 ou IPv6.

O soquete que planeja iniciar a solicitação de conexão deve aplicar esse IOCTL antes de fazer a solicitação de conexão.
Portanto, o soquete usado pela função [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)ou [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) para iniciar a conexão deve aplicar esse IOCTL para usar o caminho rápido para operações de loopback.

O soquete que está escutando a solicitação de conexão deve aplicar esse IOCTL antes de aceitar a conexão.
Portanto, o soquete usado pela função listen deve aplicar esse IOCTL para que todos os soquetes aceitos usem o caminho rápido para loopback.
Todos os soquetes retornados pela função listen e passados para a função [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex)ou [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) serão marcados para usar o caminho rápido especial para operações de loopback.

Depois que um aplicativo estabelece a conexão em uma interface de loopback usando o caminho rápido, todos os pacotes durante o tempo de vida da conexão devem usar o caminho rápido.

A **aplicação de SIO \_ LOOPBACK \_ FAST \_ PATH** a um soquete que será conectado a um caminho não loopback não terá nenhum efeito.

Essa otimização de loopback TCP resulta em pacotes que fluem pela TL (Camada de Transporte) em vez do loopback tradicional pela Camada de Rede.
Essa otimização melhora a latência para pacotes de loopback.
Quando um aplicativo opta por uma configuração de nível de conexão para usar o caminho rápido de loopback, todos os pacotes seguirão o caminho de loopback.
Para comunicações de loopback, o congestionamento e o descarte de pacotes não são esperados.
A noção do controle de congestionamento e da entrega confiável no TCP será desnecessária.
No entanto, isso não é verdadeiro para o controle de fluxo.
Sem o controle de fluxo, o remetente pode sobrecarregar o buffer de recebimento, levando ao comportamento de loopback de TCP errado.
O controle de fluxo no caminho de loopback otimizado para TCP é mantido colocando solicitações de envio em uma fila.
Quando o buffer de recebimento estiver cheio, a pilha TCP/IP garante que os envios não serão concluídos até que a fila seja atendida mantendo o controle de fluxo.

as conexões de loopback de caminho rápido TCP na presença de um texto explicativo da WFP (plataforma de filtragem de Windows) para dados de conexão devem usar o caminho lento não otimizado para loopback.
Portanto, os filtros de WFP impedirão que esse novo caminho rápido de loopback seja usado.
quando um filtro WFP estiver habilitado, o sistema usará o caminho lento mesmo que o **SIO de \_ auto-retorno \_ do \_ caminho FAST** o IOCTL tenha sido definido.
Isso garante que os aplicativos de modo de usuário tenham o recurso de segurança WFP completo.

por padrão, **o \_ \_ \_ caminho de FAST de auto-retorno SIO** está desabilitado.

somente um subconjunto das opções de soquete TCP/IP tem suporte quando o **SIO de auto-retorno de \_ FAST de loopback \_ \_** é usado para habilitar o caminho rápido de auto-retorno em um soquete.
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
