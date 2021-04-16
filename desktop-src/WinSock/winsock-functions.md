---
description: A lista a seguir fornece descrições concisas de cada função do Winsock. Para obter informações adicionais sobre qualquer função, clique no nome da função.
ms.assetid: edafb5f9-09fe-4f8e-9651-4002b6f622f4
title: Funções do Winsock
ms.topic: article
ms.date: 10/01/2019
ms.openlocfilehash: 9bf2205c970eeaaf4e64867565d58680b28298c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105772602"
---
# <a name="winsock-functions"></a>Funções do Winsock

A lista a seguir fornece descrições concisas de cada função do Winsock. Para obter informações adicionais sobre qualquer função, clique no nome da função.

| Função | Descrição |
|-|-|
| [**aceitar**](/windows/win32/api/Winsock2/nf-winsock2-accept) | Permite uma tentativa de conexão de entrada em um soquete. |
| [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) | Aceita uma nova conexão, retorna o endereço local e remoto e recebe o primeiro bloco de dados enviados pelo aplicativo cliente. |
| [**associa**](/windows/win32/api/winsock/nf-winsock-bind) | Associa um endereço local a um soquete. |
| [**fechamento**](/windows/win32/api/winsock/nf-winsock-closesocket) | Fecha um soquete existente. |
| [**Connect**](/windows/win32/api/Winsock2/nf-winsock2-connect) | Estabelece uma conexão com um soquete especificado. |
| [**ConnectEx**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_connectex) | Estabelece uma conexão com um soquete especificado e, opcionalmente, envia dados depois que a conexão é estabelecida. Com suporte apenas em soquetes orientados a conexão. |
| [**DisconnectEx**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) | Fecha uma conexão em um soquete e permite que o identificador de soquete seja reutilizado. |
| [**EnumProtocols**](/windows/win32/api/Nspapi/nf-nspapi-enumprotocolsa) | Recupera informações sobre um conjunto especificado de protocolos de rede que estão ativos em um host local. |
| [**freeaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) | Libera informações de endereço que a função [**Getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) aloca dinamicamente em estruturas [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) . |
| [**FreeAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex) | Libera informações de endereço que a função [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) aloca dinamicamente em estruturas [**addrinfoex**](/windows/win32/api/Ws2def/ns-ws2def-addrinfoexw) . |
| [**FreeAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow) | Libera informações de endereço que a função [**GetAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) aloca dinamicamente em estruturas [**addrinfoW**](/windows/win32/api/Ws2def/ns-ws2def-addrinfow) . |
| [**Gai \_ strerror**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-gai_strerrora) | Ajuda na impressão de mensagens de erro com base nos erros de EAI \_ \* retornados pela função [**Getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . |
| [**GetAcceptExSockaddrs**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs) | Analisa os dados obtidos de uma chamada para a função [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) . |
| [**GetAddressByName**](/windows/win32/api/Nspapi/nf-nspapi-getaddressbynamea) | Consulta um namespace, ou um conjunto de namespaces padrão, para recuperar informações de endereço de rede para um serviço de rede especificado. Esse processo é conhecido como resolução de nome de serviço. Um serviço de rede também pode usar a função para obter informações de endereço local que ele pode usar com a função [**BIND**](/windows/win32/api/winsock/nf-winsock-bind) . |
| [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) | Fornece conversão independente de protocolo de um nome de host ANSI para um endereço. |
| [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) | Fornece resolução de nomes independente de protocolo com parâmetros adicionais para qualificar quais provedores de espaço de nome devem tratar a solicitação. |
| [**GetAddrInfoExCancel**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexcancel) | Cancela uma operação assíncrona pela função [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) . |
| [**GetAddrInfoExOverlappedResult**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexoverlappedresult) | Obtém o código de retorno para uma estrutura **sobreposta** usada por uma operação assíncrona para a função [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) . |
| [**GetAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) | Fornece conversão independente de protocolo de um nome de host Unicode para um endereço. |
| [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) | Recupera as informações do host correspondentes a um endereço de rede. |
| [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) | Recupera informações do host correspondentes a um nome de host de um banco de dados de host. Preterido: use [**Getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) em vez disso. |
| [**GetHostName**](/windows/win32/api/winsock/nf-winsock-gethostname) | Recupera o nome de host padrão para o computador local. |
| [**GetHostNameW**](/windows/win32/api/Winsock2/nf-winsock2-gethostnamew) | Recupera o nome de host padrão para o computador local como uma cadeia de caracteres Unicode. |
| [**getipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getipv4sourcefilter) | Recupera o estado do filtro multicast para um soquete IPv4. |
| [**GetNameByType**](/windows/win32/api/Nspapi/nf-nspapi-getnamebytypea) | Recupera o nome de um serviço de rede para o tipo de serviço especificado. |
| [**getnameinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) | Fornece resolução de nomes de um endereço IPv4 ou IPv6 para um nome de host ANSI e de um número de porta para o nome do serviço ANSI. |
| [**GetNameInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfow) | Fornece resolução de nomes de um endereço IPv4 ou IPv6 para um nome de host Unicode e de um número de porta para o nome do serviço Unicode. |
| [**getemparelhaname**](/windows/win32/api/winsock/nf-winsock-getpeername) | Recupera o endereço do par ao qual um soquete está conectado. |
| [**getprotobyname**](/windows/win32/api/winsock/nf-winsock-getprotobyname) | Recupera as informações de protocolo correspondentes a um nome de protocolo. |
| [**getprotobynumber**](/windows/win32/api/winsock/nf-winsock-getprotobynumber) | Recupera informações de protocolo correspondentes a um número de protocolo. |
| [**getservbyname**](/windows/win32/api/winsock/nf-winsock-getservbyname) | Recupera informações de serviço correspondentes a um nome de serviço e protocolo. |
| [**getservbyport**](/windows/win32/api/winsock/nf-winsock-getservbyport) | Recupera informações de serviço correspondentes a uma porta e um protocolo. |
| [**GetService**](/windows/win32/api/Nspapi/nf-nspapi-getservicea) | Recupera informações sobre um serviço de rede no contexto de um conjunto de namespaces padrão ou um namespace especificado. |
| [**getsockname**](/windows/win32/api/winsock/nf-winsock-getsockname) | Recupera o nome local de um soquete. |
| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) | Recupera uma opção de soquete. |
| [**getsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getsourcefilter) | Recupera o estado do filtro multicast para um soquete IPv4 ou IPv6. |
| [**GetTypeByName**](/windows/win32/api/Nspapi/nf-nspapi-gettypebynamea) | Recupera um GUID de tipo de serviço para um serviço de rede especificado pelo nome. |
| [**htond**](/windows/win32/api/Winsock2/nf-winsock2-htond) | Converte um **Double** do host em uma ordem de bytes de rede TCP/IP (que é big-endian). |
| [**htonf**](/windows/win32/api/Winsock2/nf-winsock2-htonf) | Converte um **float** do host para a ordem de bytes de rede TCP/IP (que é big-endian). |
| [**htonl**](/windows/win32/api/winsock/nf-winsock-htonl) | Converte um **u \_ longo** do host para a ordem de bytes de rede TCP/IP (que é big-endian). |
| [**htonll**](/windows/win32/api/Winsock2/nf-winsock2-htonll) | Converte um **\_ \_ Int64 não assinado** do host para a ordem de bytes de rede TCP/IP (que é big-endian). |
| [**htons**](/windows/win32/api/winsock/nf-winsock-htons) | Converte um **u \_ curto** do host em uma ordem de bytes de rede TCP/IP (que é big-endian). |
| [**\_endereço inet**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) | Converte uma cadeia de caracteres que contém um endereço de protocolo de Internet (IPv4) pontilhado em um endereço apropriado para a estrutura [**de \_**](/windows/win32/api/winsock2/ns-winsock2-in_addr) endereço. |
| [**\_NTOA inet**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) | Converte um endereço de rede da Internet (IPv4) em uma cadeia de caracteres no formato pontilhado padrão da Internet. |
| [**InetNtop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw) | Converte um endereço de rede de Internet IPv4 ou IPv6 em uma cadeia de caracteres no formato padrão da Internet. A versão ANSI dessa função é [**inet \_ ntop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw). |
| [**InetPton**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw) | Converte um endereço de rede de Internet IPv4 ou IPv6 em seu formulário de apresentação de texto padrão em seu formato binário numérico. A versão ANSI dessa função é [**inet \_ pton**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw). |
| [**ioctlsocket**](/windows/win32/api/winsock/nf-winsock-ioctlsocket) | Controla o modo de e/s de um soquete. |
| [**ouvir**](/windows/win32/api/Winsock2/nf-winsock2-listen) | Coloca um soquete em um estado em que está escutando uma conexão de entrada. |
| [**ntohd**](/windows/win32/api/Winsock2/nf-winsock2-ntohd) | Converte um **\_ \_ Int64 não assinado** da ordem da rede TCP/IP para hospedar a ordem de bytes (que é little-endian em processadores Intel) e retorna um **Double**. |
| [**ntohf**](/windows/win32/api/Winsock2/nf-winsock2-ntohf) | Converte um **\_ \_ Int32 não assinado** de uma ordem de rede TCP/IP para hospedar a ordem de bytes (que é little-endian em processadores Intel) e retorna um **float**. |
| [**ntohl**](/windows/win32/api/winsock/nf-winsock-ntohl) | Converte um u \_ longo da ordem da rede TCP/IP para hospedar a ordem de bytes (que é little-endian em processadores Intel). |
| [**ntohll**](/windows/win32/api/Winsock2/nf-winsock2-ntohll) | Converte um **\_ \_ Int64 não assinado** da ordem da rede TCP/IP para hospedar a ordem de bytes (que é little-endian em processadores Intel). |
| [**ntohs**](/windows/win32/api/winsock/nf-winsock-ntohs) | Converte um u \_ curto da ordem de bytes de rede TCP/IP para a ordem de bytes do host (que é little-endian em processadores Intel). |
| [**recebidos**](/windows/win32/api/winsock/nf-winsock-recv) | Recebe dados de um Soquete conectado ou ligado. |
| [**recvfrom**](/windows/win32/api/winsock/nf-winsock-recvfrom) | Recebe um datagrama e armazena o endereço de origem. |
| [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) | Fecha uma fila de conclusão existente usada para notificação de conclusão de e/s por envio e recebimento de solicitações com as extensões de e/s registradas do Winsock. |
| [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Cria uma fila de conclusão de e/s de um tamanho específico para uso com as extensões de e/s registradas do Winsock. |
| [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) | Cria um descritor de soquete de e/s registrado usando um soquete especificado e filas de conclusão de e/s para uso com as extensões de e/s registradas do Winsock. |
| [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Remove entradas de uma fila de conclusão de e/s para uso com as extensões de e/s registradas no Winsock. |
| [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) | Cancela o registro de um buffer registrado usado com as extensões de e/s registradas do Winsock. |
| [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) | Registra o método a ser usado para o comportamento de notificação com uma fila de conclusão de e/s para uso com as extensões de e/s registradas do Winsock. |
| [**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive) | Recebe dados de rede em um soquete TCP de e/s registrado conectado ou um soquete de UDP de e/s registrado para uso com as extensões de e/s registradas do Winsock. |
| [**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex) | Recebe dados de rede em um soquete TCP de e/s registrado conectado ou um soquete de UDP de e/s registrado e vinculado com opções adicionais para uso com as extensões de e/s registradas do Winsock. |
| [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) | Registra o [**rio \_ bufferid**](rio-bufferid.md), um descritor de buffer registrado, com um buffer especificado para uso com as extensões de e/s registradas do Winsock. |
| [**RIOResizeCompletionQueue**](/previous-versions/windows/desktop/legacy/hh437202(v=vs.85)) | Redimensiona uma fila de conclusão de e/s para ser maior ou menor para uso com as extensões de e/s registradas no Winsock. |
| [**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85)) | Redimensiona uma fila de solicitações para ser maior ou menor para uso com as extensões de e/s registradas do Winsock. |
| [**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend) | Envia dados de rede em um soquete TCP de e/s registrado conectado ou um soquete de UDP de e/s registrado e associado para uso com as extensões de e/s registradas do Winsock. |
| [**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)) | Envia dados de rede em um soquete TCP de e/s registrado conectado ou um soquete UDP de e/s registrado e vinculado com opções adicionais para uso com as extensões de e/s registradas do Winsock. |
| [**Não**](/windows/win32/api/Winsock2/nf-winsock2-select) | Determina o status de um ou mais soquetes, aguardando, se necessário, para executar e/s síncrona. |
| [**Enviar**](/windows/win32/api/Winsock2/nf-winsock2-send) | Envia dados em um Soquete conectado. |
| [**Enviar**](/windows/win32/api/winsock/nf-winsock-sendto) | Envia dados para um destino específico. |
| [**SetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa) | Registra um nome de host e serviço junto com os endereços associados com um provedor de namespace específico. |
| [**setipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setipv4sourcefilter) | Define o estado do filtro multicast para um soquete IPv4. |
| [**Setservice**](/windows/win32/api/Nspapi/nf-nspapi-setservicea) | Registra ou remove do registro um serviço de rede em um ou mais namespaces. Também é possível adicionar ou remover um tipo de serviço de rede em um ou mais namespaces. |
| [**SetSocketMediaStreamingMode**](/windows/win32/api/Socketapi/nf-socketapi-setsocketmediastreamingmode) | Indica se a rede deve ser usada para transferir mídia de streaming que requer qualidade de serviço. |
| [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) | Define uma opção de soquete. |
| [**setsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setsourcefilter) | Define o estado do filtro multicast para um soquete IPv4 ou IPv6. |
| [**desligar**](/windows/win32/api/winsock/nf-winsock-shutdown) | Desabilita envios ou recebimentos em um soquete. |
| [**SSA**](/windows/win32/api/Winsock2/nf-winsock2-socket) | Cria um soquete que está associado a um provedor de serviços específico. |
| [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) | Transmite dados de arquivo por um identificador de Soquete conectado. |
| [**TransmitPackets**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_transmitpackets) | Transmite dados na memória ou dados de arquivo por um Soquete conectado. |
| [**WSAAccept**](/windows/win32/api/Winsock2/nf-winsock2-wsaaccept) | Aceita condicionalmente uma conexão com base no valor de retorno de uma função de condição, fornece a qualidade das especificações de fluxo de serviço e permite a transferência de dados de conexão. |
| [**WSAAddressToString**](/windows/win32/api/Winsock2/nf-winsock2-wsaaddresstostringa) | Converte todos os componentes de uma estrutura [**SOCKADDR**](sockaddr-2.md) em uma representação de cadeia de caracteres legível do endereço. |
| [**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr) | Recupera de forma assíncrona informações do host que correspondem a um endereço. |
| [**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname) | Recupera de forma assíncrona informações do host que correspondem a um nome de host. |
| [**WSAAsyncGetProtoByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobyname) | Recupera de forma assíncrona as informações de protocolo que correspondem a um nome de protocolo. |
| [**WSAAsyncGetProtoByNumber**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobynumber) | Recupera de forma assíncrona as informações de protocolo que correspondem a um número de protocolo. |
| [**WSAAsyncGetServByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyname) | Recupera de forma assíncrona as informações de serviço que correspondem a um nome de serviço e a uma porta. |
| [**WSAAsyncGetServByPort**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyport) | Recupera de forma assíncrona as informações de serviço que correspondem a uma porta e um protocolo. |
| [**WSAAsyncSelect**](/windows/win32/api/winsock/nf-winsock-wsaasyncselect) | Solicita notificação baseada em mensagem do Windows de eventos de rede para um soquete. |
| [**WSACancelAsyncRequest**](/windows/win32/api/winsock/nf-winsock-wsacancelasyncrequest) | Cancela uma operação assíncrona incompleta. |
| [**WSACleanup**](/windows/win32/api/winsock/nf-winsock-wsacleanup) | Encerra o uso do32.DLL Ws2 \_ . |
| [**WSACloseEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacloseevent) | Fecha um identificador de objeto de evento aberto. |
| [**WSAConnect**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnect) | Estabelece uma conexão com outro aplicativo de soquete, troca dados de conexão e especifica a qualidade de serviço necessária com base na estrutura [**FLOWSPEC**](/windows/win32/api/qos/ns-qos-flowspec) especificada. |
| [**WSAConnectByList**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbylist) | Estabelece uma conexão com uma coleção de pontos de extremidade possíveis representados por um conjunto de endereços de destino (nomes de host e portas). |
| [**WSAConnectByName**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbynamea) | Estabelece uma conexão com outro aplicativo de soquete em um host e uma porta especificados |
| [**WSACreateEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacreateevent) | Cria um novo objeto de evento. |
| [**WSADeleteSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) | Remove a associação entre um nome de destino par e um endereço IP para um soquete. |
| [**WSADuplicateSocket**](/windows/win32/api/Winsock2/nf-winsock2-wsaduplicatesocketa) | Retorna uma estrutura que pode ser usada para criar um novo descritor de soquete para um Soquete compartilhado. |
| [**WSAEnumNameSpaceProviders**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) | Recupera informações sobre namespaces disponíveis. |
| [**WSAEnumNameSpaceProvidersEx**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) | Recupera informações sobre namespaces disponíveis. |
| [**WSAEnumNetworkEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnetworkevents) | Descobre ocorrências de eventos de rede para o soquete indicado, limpar registros de eventos de rede internos e redefinir objetos de evento (opcional). |
| [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa) | Recupera informações sobre protocolos de transporte disponíveis. |
| [**WSAEventSelect**](/windows/win32/api/Winsock2/nf-winsock2-wsaeventselect) | Especifica um objeto de evento a ser associado ao conjunto especificado de \_ eventos de rede FD xxx. |
| [**\_\_WSAFDIsSet**](/windows/win32/api/winsock/nf-winsock-__wsafdisset) | Especifica se um soquete está incluído em um conjunto de descritores de soquete. |
| [**WSAGetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror) | Consulta o estado da opção de soquete [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) . |
| [**WSAGetIcmpErrorInfo**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo) | Consulta o endereço de origem de um erro ICMP recebido em um soquete TCP durante a instalação da conexão. |
| [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) | Recupera a MTU da camada de IP definida pelo usuário para um soquete. |
| [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) | Retorna o status de erro para a última operação que falhou. |
| [**WSAGetOverlappedResult**](/windows/win32/api/Winsock2/nf-winsock2-wsagetoverlappedresult) | Recupera os resultados de uma operação sobreposta no soquete especificado. |
| [**WSAGetQOSByName**](/windows/win32/api/Winsock2/nf-winsock2-wsagetqosbyname) | Inicializa uma estrutura de [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) baseada em um modelo nomeado ou fornece um buffer para recuperar uma enumeração dos nomes de modelo disponíveis. |
| [**WSAGetServiceClassInfo**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa) | Recupera as informações de classe (esquema) pertencentes a uma classe de serviço especificada de um provedor de namespace especificado. |
| [**WSAGetServiceClassNameByClassId**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) | Recupera o nome do serviço associado ao tipo especificado. |
| [**WSAGetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) | Recupera o tamanho máximo de uma mensagem recebida e agrupada para um soquete UDP. |
| [**WSAGetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) | Recupera o tamanho da mensagem de segmentação para um soquete UDP. |
| [**WSAHtonl**](/windows/win32/api/Winsock2/nf-winsock2-wsahtonl) | Converte um u \_ longo de ordem de byte de host em ordem de bytes de rede. |
| [**WSAHtons**](/windows/win32/api/Winsock2/nf-winsock2-wsahtons) | Converte um u \_ curto de ordem de byte de host em ordem de bytes de rede. |
| [**WSAImpersonateSocketPeer**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) | Usado para representar a entidade de segurança correspondente a um par de soquetes para executar a autorização em nível de aplicativo. |
| [**WSAInstallServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsainstallserviceclassa) | Registra um esquema de classe de serviço em um namespace. |
| [**WSAIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsaioctl) | Controla o modo de um soquete. |
| [**WSAJoinLeaf**](/windows/win32/api/Winsock2/nf-winsock2-wsajoinleaf) | Une um nó folha em uma sessão do MultiPoint, troca dados de conexão e especifica a qualidade de serviço necessária com base nas estruturas especificadas. |
| [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) | Inicia uma consulta de cliente restrita pelas informações contidas em uma estrutura [**WSAQUERYSET**](/windows/win32/api/Winsock2/ns-winsock2-wsaquerysetw) . |
| [**WSALookupServiceEnd**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupserviceend) | Libera o identificador usado pelas chamadas anteriores para [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) e [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta). |
| [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta) | Recupere as informações de serviço solicitadas. |
| [**WSANSPIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsanspioctl) | Desenvolvedores para fazer chamadas de controle de e/s para um namespace registrado. |
| [**WSANtohl**](/windows/win32/api/Winsock2/nf-winsock2-wsantohl) | Converte um u \_ longo da ordem de bytes da rede para a ordem de bytes do host. |
| [**WSANtohs**](/windows/win32/api/Winsock2/nf-winsock2-wsantohs) | Converte um u \_ curto da ordem de bytes da rede em ordem de bytes do host. |
| [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) | Determina o status de um ou mais soquetes. |
| [**WSAProviderConfigChange**](/windows/win32/api/Winsock2/nf-winsock2-wsaproviderconfigchange) | Notifica o aplicativo quando a configuração do provedor é alterada. |
| [**WSAQuerySocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) | Consulta informações sobre a segurança aplicada a uma conexão em um soquete. |
| [**WSARecv**](/windows/win32/api/Winsock2/nf-winsock2-wsarecv) | Recebe os dados de um soquete conectado. |
| [**WSARecvDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvdisconnect) | Encerra a recepção em um soquete e recupera os dados de desconexão se o soquete for orientado a conexão. |
| [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) | Recebe os dados de um soquete conectado. |
| [**WSARecvFrom**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvfrom) | Recebe um datagrama e armazena o endereço de origem. |
| [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) | Recebe dados e informações de controle opcionais de soquetes conectados e desconectados. |
| [**WSARemoveServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsaremoveserviceclass) | Remove permanentemente o esquema de classe de serviço do registro. |
| [**WSAResetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsaresetevent) | Redefine o estado do objeto de evento especificado para não sinalizado. |
| [**WSARevertImpersonation**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) | Encerra a representação de um par de soquete. |
| [**WSASend**](/windows/win32/api/Winsock2/nf-winsock2-wsasend) | Envia dados em um Soquete conectado. |
| [**WSASendDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsasenddisconnect) | Inicia o encerramento da conexão para o soquete e envia dados de desconexão. |
| [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) | Envia dados e informações de controle opcional de soquetes conectados e desconectados. |
| [**WSASendTo**](/windows/win32/api/Winsock2/nf-winsock2-wsasendto) | Envia dados para um destino específico, usando e/s sobreposta, quando aplicável. |
| [**WSASetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsasetevent) | Define o estado do objeto de evento especificado a ser sinalizado. |
| [**WSASetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror) | Define o estado da opção de soquete [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) . |
| [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) | Define a MTU da camada de IP definida pelo usuário em um soquete. |
| [**WSASetLastError**](/windows/win32/api/winsock/nf-winsock-wsasetlasterror) | Define o código de erro. |
| [**WSASetService**](/windows/win32/api/Winsock2/nf-winsock2-wsasetservicea) | Registra ou remove do registro uma instância de serviço em um ou mais namespaces. |
| [**WSASetSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) | Usado para especificar o nome de destino par (SPN) que corresponde a um endereço IP par. Esse nome de destino deve ser especificado por aplicativos cliente para identificar com segurança o par que deve ser autenticado. |
| [**WSASetSocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) | Habilita e aplica a segurança de um soquete. |
| [**WSASetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) | Define o tamanho máximo de uma mensagem agrupada definida em um soquete UDP. |
| [**WSASetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) | Define o tamanho da mensagem de segmentação em um soquete UDP. |
| [**WSASocket**](/windows/win32/api/Winsock2/nf-winsock2-wsasocketa) | Cria um soquete que está associado a um provedor de serviço de transporte específico. |
| [**WSAStartup**](/windows/win32/api/winsock/nf-winsock-wsastartup) | Inicia o uso de WS2 \_32.DLL por um processo. |
| [**WSAStringToAddress**](/windows/win32/api/Winsock2/nf-winsock2-wsastringtoaddressa) | Converte uma cadeia de caracteres numérica em uma estrutura [**SOCKADDR**](sockaddr-2.md) . |
| [**WSAWaitForMultipleEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsawaitformultipleevents) | Retorna quando um ou todos os objetos de evento especificados estão no estado sinalizado ou quando o intervalo de tempo limite expira. |
