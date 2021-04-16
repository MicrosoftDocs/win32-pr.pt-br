---
description: A estrutura sockaddr varia dependendo do protocolo selecionado.
ms.assetid: d1392e1c-2b20-425a-8adf-38e665fb6275
title: SOCKADDR
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- sockaddr
api_type:
- NA
api_location: ''
ms.openlocfilehash: ccd4b98efc987630ab625e5c9788f0be16018e88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764973"
---
# <a name="sockaddr"></a>SOCKADDR

A estrutura sockaddr varia dependendo do protocolo selecionado. Exceto para o *parâmetro \* \_ da família Sin* , o conteúdo do sockaddr é expresso em ordem de bytes de rede.

As funções do Winsock usando SOCKADDR não são estritamente interpretadas para serem ponteiros para uma estrutura sockaddr. A estrutura é interpretada de forma diferente no contexto de famílias de endereços diferentes. Os únicos requisitos são que o primeiro **u \_ curto** é a família de endereços e o tamanho total do buffer de memória em bytes é *namelen*.

A estrutura de [**\_ armazenamento SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) também armazena informações de endereço de soquete e a estrutura é suficientemente grande para armazenar informações de endereço IPv4 ou IPv6. O uso da estrutura **de \_ armazenamento SOCKADDR** promove a independência de versão do protocolo e da família de protocolos e simplifica o desenvolvimento. É recomendável que a estrutura de **\_ armazenamento SOCKADDR** seja usada no lugar da estrutura sockaddr. A estrutura de **\_ armazenamento SOCKADDR** tem suporte no Windows Server 2003 e posterior.

A estrutura sockaddr e SOCKADDR \_ nas estruturas abaixo são usadas com IPv4. Outros protocolos usam estruturas semelhantes.

``` syntax
struct sockaddr {
        ushort  sa_family;
        char    sa_data[14];
};

struct sockaddr_in {
        short   sin_family;
        u_short sin_port;
        struct  in_addr sin_addr;
        char    sin_zero[8];
};
```

As \_ estruturas antigas SOCKADDR In6 e SOCKADDR \_ In6 \_ abaixo são usadas com o IPv6.

``` syntax
struct sockaddr_in6 {
        short   sin6_family;
        u_short sin6_port;
        u_long  sin6_flowinfo;
        struct  in6_addr sin6_addr;
        u_long  sin6_scope_id;
};

typedef struct sockaddr_in6 SOCKADDR_IN6;
typedef struct sockaddr_in6 *PSOCKADDR_IN6;
typedef struct sockaddr_in6 FAR *LPSOCKADDR_IN6;


struct sockaddr_in6_old {
        short   sin6_family;        
        u_short sin6_port;          
        u_long  sin6_flowinfo;      
        struct  in6_addr sin6_addr;  
};
```

No SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior, **SOCKADDR** e **SOCKADDR \_ em** marcas typedef são definidos para SOCKADDR e SOCKADDR \_ em estruturas da seguinte maneira:

``` syntax
typedef struct sockaddr {
#if (_WIN32_WINNT < 0x0600)
    u_short sa_family;
#else 
    ADDRESS_FAMILY sa_family;
#endif //(_WIN32_WINNT < 0x0600)
    CHAR sa_data[14];
} SOCKADDR, *PSOCKADDR, FAR *LPSOCKADDR;


typedef struct sockaddr_in {
#if(_WIN32_WINNT < 0x0600)
    short   sin_family;    
#else //(_WIN32_WINNT < 0x0600)
    ADDRESS_FAMILY sin_family;
#endif //(_WIN32_WINNT < 0x0600)
    USHORT sin_port;
    IN_ADDR sin_addr;
    CHAR sin_zero[8];
} SOCKADDR_IN, *PSOCKADDR_IN;
```

No SDK do Windows lançado para o Windows Vista e posterior, a organização dos arquivos de cabeçalho foi alterada e as SOCKADDR e SOCKADDR \_ nas estruturas são definidas no arquivo de cabeçalho *Ws2def. h* , não no arquivo de cabeçalho *Winsock2. h* . O arquivo de cabeçalho *Ws2def. h* é incluído automaticamente pelo arquivo de cabeçalho *Winsock2. h* . A \_ estrutura sockaddr In6 é definida no arquivo de cabeçalho *Ws2ipdef. h* , não no arquivo de cabeçalho *Ws2tcpip. h* . O arquivo de cabeçalho *Ws2ipdef. h* é incluído automaticamente pelo arquivo de cabeçalho *Ws2tcpip. h* . Os arquivos de cabeçalho *Ws2def. h* e *Ws2ipdef. h* nunca devem ser usados diretamente.

## <a name="example-code"></a>Código de exemplo

O exemplo a seguir demonstra o uso da estrutura **SOCKADDR** .


```C++

// Declare variables
SOCKET ListenSocket;
struct sockaddr_in saServer;
hostent* localHost;
char* localIP;

// Create a listening socket
ListenSocket = socket(AF_INET, SOCK_STREAM, IPPROTO_TCP);

// Get the local host information
localHost = gethostbyname("");
localIP = inet_ntoa (*(struct in_addr *)*localHost->h_addr_list);

// Set up the sockaddr structure
saServer.sin_family = AF_INET;
saServer.sin_addr.s_addr = inet_addr(localIP);
saServer.sin_port = htons(5150);

// Bind the listening socket using the
// information in the sockaddr structure
bind( ListenSocket,(SOCKADDR*) &saServer, sizeof(saServer) );


```



## <a name="see-also"></a>Consulte Também

[**\_armazenamento SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))


 

 
