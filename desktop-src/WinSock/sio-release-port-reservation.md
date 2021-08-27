---
description: O código de controle libera uma reserva de tempo de execução para um bloco de portas TCP ou UDP.
ms.assetid: 24D67A40-8CE9-4AF1-90BF-599D19C87B89
title: SIO_RELEASE_PORT_RESERVATION código de controle
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8d949e325292210ec7126da5ddf65c6ff30c5aa151cfaf85331fb7ebf3e5b346
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097486"
---
# <a name="sio_release_port_reservation-control-code"></a>SIO_RELEASE_PORT_RESERVATION código de controle

## <a name="description"></a>Descrição

O código de controle de **\_ reserva de \_ porta \_ de liberação sio** libera uma reserva de tempo de execução para um bloco de portas TCP ou UDP.
A reserva de tempo de execução a ser liberada deve ter sido obtida do processo emissora usando o [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.

Para executar essa operação, chame a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** com os parâmetros a seguir.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);

```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
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
Use **a \_ \_ \_ reserva de porta de liberação sio** para esta operação.

### <a name="lpvinbuffer"></a>lpvInBuffer

Um ponteiro para o buffer de entrada.
Esse parâmetro contém um ponteiro para uma estrutura de [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) com o token da reserva de porta TCP ou UDP a ser liberada.

### <a name="cbinbuffer"></a>cbInBuffer

O tamanho, em bytes, do buffer de entrada.
Esse parâmetro deve ter pelo menos o tamanho da estrutura de [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) .

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

## <a name="return-value"></a>Valor retornado

Se a operação for concluída com êxito, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará zero.

Se a operação falhar ou estiver pendente, a função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl** retornará **um \_ erro de soquete**.
Para obter informações de erro estendidas, chame [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Código do erro | Significado |
|------------|---------|
| **\_e/s de WSA \_ pendente** | A operação de e/s sobreposta está em andamento. Esse valor será retornado se uma operação sobreposta tiver sido iniciada com êxito e a conclusão será indicada mais tarde. |
| **operação de WSA \_ \_ anulada** | A operação de e/s foi anulada devido a uma saída de thread ou uma solicitação de aplicativo. Esse erro será retornado se uma operação sobreposta tiver sido cancelada devido ao fechamento do soquete ou à execução do comando **SIO_FLUSH** IOCTL. |
| **WSAEFAULT** | O sistema detectou um endereço de ponteiro inválido ao tentar usar um argumento de ponteiro em uma chamada. Esse erro é retornado do parâmetro *lpOverlapped* ou *lpCompletionRoutine* não está totalmente contido em uma parte válida do espaço de endereço do usuário. |
| **WSAEINPROGRESS** | Uma operação de bloqueio está atualmente em execução. Esse erro será retornado se a função for invocada quando um retorno de chamada estiver em andamento. |
| **WSAEINTR** | Uma operação de bloqueio foi interrompida por uma chamada para **WSACancelBlockingCall**. Esse erro será retornado se uma operação de bloqueio tiver sido interrompida. |
| **WSAEINVAL** | Foi fornecido um argumento inválido. Esse erro será retornado se o parâmetro *dwIoControlCode* não for um comando válido ou se um parâmetro de entrada especificado não for aceitável ou se o comando não for aplicável ao tipo de soquete especificado. |
| **WSAENETDOWN** | Uma operação de soquete encontrou uma rede inoperante. Esse erro será retornado se o subsistema de rede tiver falhado. |
| **WSAENOTSOCK** | Uma operação foi tentada em algo que não é um soquete. Esse erro será retornado se o descritor *s* não for um soquete. |
| **WSAEOPNOTSUPP** | Não há suporte para a operação tentada para o tipo de objeto referenciado. Esse erro será retornado se o comando IOCTL especificado não tiver suporte. Esse erro também será retornado se o IOCTL de **\_ reserva de \_ porta \_ de liberação sio** não tiver suporte do provedor de transporte. Esse erro também é retornado quando uma tentativa de usar o IOCTL de **\_ reserva de \_ porta \_ de liberação sio** é feita em um soquete diferente de UDP ou TCP. |

## <a name="remarks"></a>Comentários

o IOCTL de **\_ reserva de \_ porta \_ de liberação SIO** tem suporte no Windows Vista e versões posteriores do sistema operacional.

Os aplicativos e serviços que precisam reservar portas se enquadram em duas categorias.
A primeira categoria inclui componentes que precisam de uma porta específica como parte de sua operação.
Esses componentes geralmente preferem especificar a porta necessária no momento da instalação (em um manifesto do aplicativo, por exemplo).
A segunda categoria inclui componentes que precisam de qualquer porta disponível ou bloco de portas em tempo de execução.
Essas duas categorias correspondem a solicitações específicas e de reserva de porta curinga.
As solicitações de reserva específicas podem ser persistentes ou tempo de execução, enquanto as solicitações de reserva de porta curinga só têm suporte em tempo de execução.

O [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL é usado para solicitar uma reserva de tempo de execução para um bloco de portas TCP ou UDP.
Para reservas de porta de tempo de execução, o pool de portas requer que as reservas sejam consumidas do processo em cujo soquete a reserva foi concedida.
As reservas de porta de tempo de execução duram apenas desde o tempo de vida do soquete no qual o [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL foi chamado.
Por outro lado, as reservas de porta persistentes criadas usando a função [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) ou [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) podem ser consumidas por qualquer processo com a capacidade de obter reservas persistentes.

O **IOCTL \_ \_ \_ reserva de porta de liberação sio** é usado para liberar uma reserva de tempo de execução para um bloco de portas TCP ou UDP.

Se os parâmetros *lpOverlapped* e *lpCompletionRoutine* forem **nulos**, o soquete nessa função será tratado como um soquete não sobreposto.
Para um soquete não sobreposto, os parâmetros *lpOverlapped* e *lpCompletionRoutine* são ignorados, exceto que a função pode bloquear se o soquete *s* estiver no modo de bloqueio.
Se o soquete *s* estiver no modo sem bloqueio, essa função ainda será bloqueada, pois esse IOCTL específico não oferece suporte ao modo sem bloqueio.

Para soquetes sobrecarrados, as operações que não podem ser concluídas imediatamente serão iniciadas e a conclusão será indicada posteriormente.

Qualquer IOCTL pode ser bloqueado indefinidamente, dependendo da implementação do provedor de serviços.
Se o aplicativo não puder tolerar o bloqueio em uma chamada de função [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) ou **WSPIoctl,** a E/S sobresalo será aconselhada para IOCTLs que são especialmente prováveis de bloquear.

O IOCTL DE RESERVA DA PORTA DE LANÇAMENTO do SIO pode falhar com **A OPERAÇÃO WSAEINTR** ou **WSA \_ \_ ANULADA** nos seguintes casos: **\_ \_ \_**

* A solicitação é cancelada pelo Gerenciador de E/S.
* O soquete está fechado.

## <a name="examples"></a>Exemplos

O exemplo a seguir adquire uma reserva de porta de runtime e, em seguida, libera a reserva de porta de runtime.

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;          // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;     // Network byte order

    INET_PORT_RANGE portRange = { 0 };
    INET_PORT_RESERVATION_INSTANCE portRes = { 0 };

    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = 0;
    int iProtocol = 0;

    SOCKET sockRes = INVALID_SOCKET;

    DWORD bytesReturned = 0;

    // Validate the parameters
    if (argc != 6) {
        wprintf
            (L"usage: %s <addressfamily> <type> <protocol> <StartingPort> <NumberOfPorts>\n",
             argv[0]);
        wprintf(L"Opens a socket for the specified family, type, & protocol\n");
        wprintf
            (L"and then acquires a runtime port reservation for the protocol specified\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 2 2 17 5000 20\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_DGRAM=2 IPPROTO_UDP=17 StartPort=5000 NumPorts=20", argv[0]);

        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    startPort = _wtoi(argv[4]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[5]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    portRange.StartPort = startPortns;
    portRange.NumberOfPorts = (USHORT) numPorts;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) {
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    } else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ACQUIRE_PORT_RESERVATION, (LPVOID) & portRange,
                     sizeof (INET_PORT_RANGE), (LPVOID) & portRes,
                     sizeof (INET_PORT_RESERVATION_INSTANCE), &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf(L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) failed with error = %d\n",
                    WSAGetLastError());
            closesocket(sock);
            WSACleanup();
            return 1;
        } else {
            wprintf
                (L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                 bytesReturned);
            wprintf(L"  Starting port=%d,  Number of Ports=%d, Token=%I64d\n",
                    htons(portRes.Reservation.StartPort),
                    portRes.Reservation.NumberOfPorts, portRes.Token);

            iResult =
                WSAIoctl(sock, SIO_RELEASE_PORT_RESERVATION, (LPVOID) & portRes.Token,
                         sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
            if (iResult != 0) {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) failed with error = %d\n",
                     WSAGetLastError());
            } else {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                     bytesReturned);
            }
        }

        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for first socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
    }

    WSACleanup();

    return 0;
}
```

## <a name="see-also"></a>Confira também

[**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[**DeletePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[**DeletePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[**LookupPersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[**LookupPersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md)

[**SIO_ASSOCIATE_PORT_RESERVATION**](sio-associate-port-reservation.md)

[Soquete](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**Wsagetlasterror**](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[**Wsagetoverlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**Wsaioctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlapped**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
