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
# <a name="sockaddr"></a><span data-ttu-id="0035d-103">SOCKADDR</span><span class="sxs-lookup"><span data-stu-id="0035d-103">sockaddr</span></span>

<span data-ttu-id="0035d-104">A estrutura sockaddr varia dependendo do protocolo selecionado.</span><span class="sxs-lookup"><span data-stu-id="0035d-104">The sockaddr structure varies depending on the protocol selected.</span></span> <span data-ttu-id="0035d-105">Exceto para o *parâmetro \* \_ da família Sin* , o conteúdo do sockaddr é expresso em ordem de bytes de rede.</span><span class="sxs-lookup"><span data-stu-id="0035d-105">Except for the *sin\*\_family* parameter, sockaddr contents are expressed in network byte order.</span></span>

<span data-ttu-id="0035d-106">As funções do Winsock usando SOCKADDR não são estritamente interpretadas para serem ponteiros para uma estrutura sockaddr.</span><span class="sxs-lookup"><span data-stu-id="0035d-106">Winsock functions using sockaddr are not strictly interpreted to be pointers to a sockaddr structure.</span></span> <span data-ttu-id="0035d-107">A estrutura é interpretada de forma diferente no contexto de famílias de endereços diferentes.</span><span class="sxs-lookup"><span data-stu-id="0035d-107">The structure is interpreted differently in the context of different address families.</span></span> <span data-ttu-id="0035d-108">Os únicos requisitos são que o primeiro **u \_ curto** é a família de endereços e o tamanho total do buffer de memória em bytes é *namelen*.</span><span class="sxs-lookup"><span data-stu-id="0035d-108">The only requirements are that the first **u\_short** is the address family and the total size of the memory buffer in bytes is *namelen*.</span></span>

<span data-ttu-id="0035d-109">A estrutura de [**\_ armazenamento SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) também armazena informações de endereço de soquete e a estrutura é suficientemente grande para armazenar informações de endereço IPv4 ou IPv6.</span><span class="sxs-lookup"><span data-stu-id="0035d-109">The [**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85)) structure also stores socket address information and the structure is sufficiently large to store IPv4 or IPv6 address information.</span></span> <span data-ttu-id="0035d-110">O uso da estrutura **de \_ armazenamento SOCKADDR** promove a independência de versão do protocolo e da família de protocolos e simplifica o desenvolvimento.</span><span class="sxs-lookup"><span data-stu-id="0035d-110">The use of the **SOCKADDR\_STORAGE** structure promotes protocol-family and protocol-version independence, and simplifies development.</span></span> <span data-ttu-id="0035d-111">É recomendável que a estrutura de **\_ armazenamento SOCKADDR** seja usada no lugar da estrutura sockaddr.</span><span class="sxs-lookup"><span data-stu-id="0035d-111">It is recommended that the **SOCKADDR\_STORAGE** structure be used in place of the sockaddr structure.</span></span> <span data-ttu-id="0035d-112">A estrutura de **\_ armazenamento SOCKADDR** tem suporte no Windows Server 2003 e posterior.</span><span class="sxs-lookup"><span data-stu-id="0035d-112">The **SOCKADDR\_STORAGE** structure is supported on Windows Server 2003 and later.</span></span>

<span data-ttu-id="0035d-113">A estrutura sockaddr e SOCKADDR \_ nas estruturas abaixo são usadas com IPv4.</span><span class="sxs-lookup"><span data-stu-id="0035d-113">The sockaddr structure and sockaddr\_in structures below are used with IPv4.</span></span> <span data-ttu-id="0035d-114">Outros protocolos usam estruturas semelhantes.</span><span class="sxs-lookup"><span data-stu-id="0035d-114">Other protocols use similar structures.</span></span>

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

<span data-ttu-id="0035d-115">As \_ estruturas antigas SOCKADDR In6 e SOCKADDR \_ In6 \_ abaixo são usadas com o IPv6.</span><span class="sxs-lookup"><span data-stu-id="0035d-115">The sockaddr\_in6 and sockaddr\_in6\_old structures below are used with IPv6.</span></span>

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

<span data-ttu-id="0035d-116">No SDK (Software Development Kit) do Microsoft Windows lançado para Windows Vista e posterior, **SOCKADDR** e **SOCKADDR \_ em** marcas typedef são definidos para SOCKADDR e SOCKADDR \_ em estruturas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0035d-116">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, **SOCKADDR** and **SOCKADDR\_IN** typedef tags are defined for sockaddr and sockaddr\_in structures as follows:</span></span>

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

<span data-ttu-id="0035d-117">No SDK do Windows lançado para o Windows Vista e posterior, a organização dos arquivos de cabeçalho foi alterada e as SOCKADDR e SOCKADDR \_ nas estruturas são definidas no arquivo de cabeçalho *Ws2def. h* , não no arquivo de cabeçalho *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="0035d-117">On the Windows SDK released for Windows Vista and later, the organization of header files has changed and the sockaddr and sockaddr\_in structures are defined in the *Ws2def.h* header file, not the *Winsock2.h* header file.</span></span> <span data-ttu-id="0035d-118">O arquivo de cabeçalho *Ws2def. h* é incluído automaticamente pelo arquivo de cabeçalho *Winsock2. h* .</span><span class="sxs-lookup"><span data-stu-id="0035d-118">The *Ws2def.h* header file is automatically included by the *Winsock2.h* header file.</span></span> <span data-ttu-id="0035d-119">A \_ estrutura sockaddr In6 é definida no arquivo de cabeçalho *Ws2ipdef. h* , não no arquivo de cabeçalho *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="0035d-119">The sockaddr\_in6 structure is defined in the *Ws2ipdef.h* header file, not the *Ws2tcpip.h* header file.</span></span> <span data-ttu-id="0035d-120">O arquivo de cabeçalho *Ws2ipdef. h* é incluído automaticamente pelo arquivo de cabeçalho *Ws2tcpip. h* .</span><span class="sxs-lookup"><span data-stu-id="0035d-120">The *Ws2ipdef.h* header file is automatically included by the *Ws2tcpip.h* header file.</span></span> <span data-ttu-id="0035d-121">Os arquivos de cabeçalho *Ws2def. h* e *Ws2ipdef. h* nunca devem ser usados diretamente.</span><span class="sxs-lookup"><span data-stu-id="0035d-121">The *Ws2def.h* and *Ws2ipdef.h* header files should never be used directly.</span></span>

## <a name="example-code"></a><span data-ttu-id="0035d-122">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="0035d-122">Example Code</span></span>

<span data-ttu-id="0035d-123">O exemplo a seguir demonstra o uso da estrutura **SOCKADDR** .</span><span class="sxs-lookup"><span data-stu-id="0035d-123">The following example demonstrates the use of the **sockaddr** structure.</span></span>


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



## <a name="see-also"></a><span data-ttu-id="0035d-124">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0035d-124">See Also</span></span>

<span data-ttu-id="0035d-125">[**\_armazenamento SOCKADDR**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="0035d-125">[**SOCKADDR\_STORAGE**](/previous-versions/windows/desktop/legacy/ms740504(v=vs.85))</span></span>


 

 
