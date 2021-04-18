---
description: A \_ opção de soquete EXCLUSIVEADDRUSE impede que outros soquetes sejam ligados à força no mesmo endereço e porta.
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: Opção de soquete SO_EXCLUSIVEADDRUSE (Winsock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d4747150f918a7e9c4ce37ec209e7261d1a00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105773031"
---
# <a name="so_exclusiveaddruse-socket-option"></a>\_Opção de soquete EXCLUSIVEADDRUSE

A \_ opção de soquete EXCLUSIVEADDRUSE impede que outros soquetes sejam ligados à força no mesmo endereço e porta.

## <a name="syntax"></a>Sintaxe

A \_ opção de EXCLUSIVEADDRUSE impede que outros soquetes sejam vinculados à força ao mesmo endereço e porta, uma prática habilitada pela \_ opção de soquete REUSEADDR. Essa reutilização pode ser executada por aplicativos mal-intencionados para interromper o aplicativo. A \_ opção EXCLUSIVEADDRUSE é muito útil para serviços do sistema que exigem alta disponibilidade.

O exemplo de código a seguir ilustra como definir essa opção.


```C++
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>             // Needed for _wtoi

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
    WSADATA wsaData;
    int iResult = 0;
    int iError = 0;

    SOCKET s = INVALID_SOCKET;
    SOCKADDR_IN saLocal;
    int iOptval = 0;

    int iFamily = AF_UNSPEC;
    int iType = 0;
    int iProtocol = 0;

    int iPort = 0;

    // Validate the parameters
    if (argc != 5) {
        wprintf(L"usage: %ws <addressfamily> <type> <protocol> <port>\n", argv[0]);
        wprintf(L"    opens a socket for the specified family, type, & protocol\n");
        wprintf(L"    sets the SO_EXCLUSIVEADDRUSE socket option on the socket\n");
        wprintf(L"    then tries to bind the port specified on the command-line\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17 5150\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17  PORT=5150\n",
                argv[0]);
        wprintf(L"   %ws 2 1 17 5150\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_STREAM=1 IPPROTO_TCP=6  PORT=5150\n", argv[0]);
        wprintf(L"   See the documentation for the socket function for other values\n");
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    iPort = _wtoi(argv[4]);

    if (iFamily != AF_INET && iFamily != AF_INET6) {
        wprintf(L"Address family must be either AF_INET (2) or AF_INET6 (23)\n");
        return 1;
    }

    if (iPort <= 0 || iPort >= 65535) {
        wprintf(L"Port specified must be greater than 0 and less than 65535\n");
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }
    // Create the socket
    s = socket(iFamily, iType, iProtocol);
    if (s == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    // Set the exclusive address option
    iOptval = 1;
    iResult = setsockopt(s, SOL_SOCKET, SO_EXCLUSIVEADDRUSE,
                         (char *) &iOptval, sizeof (iOptval));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"setsockopt for SO_EXCLUSIVEADDRUSE failed with error: %ld\n",
                WSAGetLastError());
    }

    saLocal.sin_family = (ADDRESS_FAMILY) iFamily;
    saLocal.sin_port = htons( (u_short) iPort);
    saLocal.sin_addr.s_addr = htonl(INADDR_ANY);

    // Bind the socket
    iResult = bind(s, (SOCKADDR *) & saLocal, sizeof (saLocal));
    if (iResult == SOCKET_ERROR) {

        // Most errors related to setting SO_EXCLUSIVEADDRUSE
        //    will occur at bind.
        iError = WSAGetLastError();
        if (iError == WSAEACCES)
            wprintf(L"bind failed with WSAEACCES (access denied)\n");
        else
            wprintf(L"bind failed with error: %ld\n", iError);

    } else {
        wprintf(L"bind on socket with SO_EXCLUSIVEADDRUSE succeeded to port: %ld\n",
                iPort);
    }

    // cleanup
    closesocket(s);
    WSACleanup();

    return 0;
}

```



Para ter qualquer efeito, a \_ opção for EXCLUSIVADDRUSE deve ser definida antes de a função [**BIND**](/windows/desktop/api/winsock/nf-winsock-bind) ser chamada (isso também se aplica à \_ opção REUSEADDR, por isso). A tabela 1 lista os efeitos da definição da \_ opção EXCLUSIVEADDRUSE. O caractere curinga indica a associação ao endereço curinga, como 0.0.0.0 para IPv4 e:: para IPv6. Específico indica a associação a uma interface específica, como a associação de um endereço IP atribuído a um adaptador. Specific2 indica a associação a um endereço específico diferente do endereço associado a no caso específico.

> [!Note]  
> O caso de Specific2 é aplicável somente quando a primeira ligação é executada com um endereço específico; para o caso em que o primeiro soquete está associado ao curinga, a entrada para específico abrange todos os casos de endereço específicos.

 

Por exemplo, considere um computador com duas interfaces IP: 10.0.0.1 e 10.99.99.99. Se a primeira ligação for 10.0.0.1 e a porta 5150 com a \_ opção EXCLUSIVEADDRUSE definida, a segunda ligação a 10.99.99.99 e a porta 5150 com qualquer ou nenhuma opção definida terá sucesso. No entanto, se o primeiro soquete estiver associado ao endereço curinga (0.0.0.0) e à porta 5150 com \_ o EXCLUSIVEADDRUSE definido, qualquer associação subsequente à mesma porta, independentemente do endereço IP, falhará com WSAEADDRINUSE (10048) ou WSAEACCESS (10013), dependendo de quais opções foram definidas no segundo soquete de ligação.

### <a name="bind-behavior-with-various-options-set"></a>Comportamento de ligação com várias opções definidas



Segunda Associação

Primeira ligação

*\_EXCLUSIVEADDRUSE*

*Nenhuma opção* ou *\_ REUSEADDR*

*Amplia*

*Específicas*

*Amplia*

*Específicas*

$ {ROWSPAN3} $*so \_ EXCLUSIVEADDRUSE*$ {remove} $  

*Amplia*

Falha (10048)

Falha (10048)

Falha (10048)

Falha (10048)

*Específicas*

Falha (10048)

Falha (10048)

Falha (10048)

Falha (10048)

*Specific2*

N/D

Êxito

N/D

Êxito

$ {ROWSPAN3} $*sem opções*$ {remover} $  

*Amplia*

Falha (10048)

Falha (10048)

Falha (10048)

Falha (10048)

*Específicas*

Falha (10048)

Falha (10048)

Falha (10048)

Falha (10048)

*Specific2*

N/D

Êxito

N/D

Êxito

$ {ROWSPAN3} $*so \_ REUSEADDR*$ {remove} $  

*Amplia*

Falha (10013)

Falha (10013)

Êxito\*

Êxito

*Específicas*

Falha (10013)

Falha (10013)

Êxito

Êxito\*

*Specific2*

N/D

Êxito

N/D

Êxito

\* O comportamento é indefinido para qual soquete receberá pacotes.



 

No caso em que a primeira ligação não define nenhuma opção ou tão \_ REUSEADDR, e a segunda ligação executa um \_ REUSEADDR, o segundo soquete excedeu a porta e o comportamento em relação ao qual o soquete receberá os pacotes que serão indeterminados. Portanto, \_ o EXCLUSIVEADDRUSE foi introduzido para resolver essa situação.

Um soquete com o \_ EXCLUSIVEADDRUSE set não pode ser sempre reutilizado imediatamente após o fechamento do soquete. Por exemplo, se um soquete de escuta com o sinalizador exclusivo definido aceitar uma conexão após a qual o soquete de escuta está fechado, outro Soquete não poderá se associar à mesma porta que o primeiro soquete de escuta com o sinalizador exclusivo até que a conexão aceita não esteja mais ativa.

Essa situação pode ser bastante complicada; Embora o soquete tenha sido fechado, o transporte subjacente pode não encerrar sua conexão. Mesmo após o soquete ser fechado, o sistema deve enviar todos os dados armazenados em buffer, transmitir uma desconexão normal para o par e aguardar uma desconexão normal do par. Portanto, é possível que o transporte subjacente nunca libere a conexão, como quando o mesmo anuncia uma janela de tamanho zero ou outros ataques. No exemplo anterior, o soquete de escuta foi fechado após a aceitação de uma conexão de cliente. Agora, mesmo que a conexão do cliente seja fechada, a porta ainda poderá não ser reutilizada se a conexão do cliente permanecer em um estado ativo devido a dados não confirmados e assim por diante.

Para evitar essa situação, os aplicativos devem garantir um desligamento normal: chamar o [**desligamento**](/windows/desktop/api/winsock/nf-winsock-shutdown) com o sinalizador de envio de SD \_ e esperar em um loop de [**recepção**](/windows/desktop/api/winsock/nf-winsock-recv) até que zero bytes sejam retornados. Isso evita o problema associado à reutilização da porta, garante que todos os dados foram recebidos pelo par e garante o ponto em que todos os seus dados foram recebidos com êxito.

A opção de modo \_ remanescente pode ser definida em um soquete para impedir que a porta esteja entrando em um dos Estados de espera ativos; no entanto, isso não é recomendável porque pode levar a efeitos indesejados, pois pode fazer com que a conexão seja redefinida. Por exemplo, se os dados tiverem sido recebidos, mas ainda não confirmados pelo par, e o computador local fechar o soquete com o \_ conjunto remanescente, a conexão será redefinida e o par descartará os dados não confirmados. Além disso, é difícil escolher um horário adequado para o remanescente; um valor muito pequeno resulta em muitas conexões anuladas, enquanto um tempo limite grande pode deixar o sistema vulnerável a ataques de negação de serviço estabelecendo muitas conexões e, assim, paralisando vários threads de aplicativo.

> [!Note]  
> Um soquete que está usando a \_ opção EXCLUSIVEADDRUSE deve ser desligado corretamente antes de fechá-lo. A falha em fazer isso pode causar um ataque de negação de serviço se o serviço associado precisar ser reiniciado.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Winsock2. h</dt> </dl> |



 

 




