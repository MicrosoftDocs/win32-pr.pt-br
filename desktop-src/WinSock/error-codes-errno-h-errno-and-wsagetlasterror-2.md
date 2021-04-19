---
description: Em aplicativos Winsock, os códigos de erro são recuperados usando a função WSAGetLastError, o Windows Sockets substituto para a função GetLastError do Windows.
ms.assetid: cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1
title: Códigos de erro-errno, h_errno e WSAGetLastError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b547e0b580599aaec27a0b77bfad0ffaa8966e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782722"
---
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a><span data-ttu-id="70c3e-103">Códigos de erro-errno, h \_ errno e WSAGetLastError</span><span class="sxs-lookup"><span data-stu-id="70c3e-103">Error Codes - errno, h\_errno and WSAGetLastError</span></span>

<span data-ttu-id="70c3e-104">Em aplicativos Winsock, os códigos de erro são recuperados usando a função [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) , o Windows Sockets substituto para a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) do Windows.</span><span class="sxs-lookup"><span data-stu-id="70c3e-104">In Winsock applications, error codes are retrieved using the [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function, the Windows Sockets substitute for the Windows [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function.</span></span> <span data-ttu-id="70c3e-105">Os códigos de erro retornados pelo Windows Sockets são semelhantes às constantes de código de erro de soquete do UNIX, mas as constantes são todos prefixadas com o WSA.</span><span class="sxs-lookup"><span data-stu-id="70c3e-105">The error codes returned by Windows Sockets are similar to UNIX socket error code constants, but the constants are all prefixed with WSA.</span></span> <span data-ttu-id="70c3e-106">Assim, em aplicativos Winsock, o código de erro WSAEWOULDBLOCK seria retornado, enquanto em aplicativos UNIX o código de erro EWOULDBLOCK seria retornado.</span><span class="sxs-lookup"><span data-stu-id="70c3e-106">So in Winsock applications the WSAEWOULDBLOCK error code would be returned, while in UNIX applications the EWOULDBLOCK error code would be returned.</span></span>

<span data-ttu-id="70c3e-107">Os códigos de erro definidos pelo Windows Sockets não são disponibilizados por meio da variável *errno* .</span><span class="sxs-lookup"><span data-stu-id="70c3e-107">Error codes set by Windows Sockets are not made available through the *errno* variable.</span></span> <span data-ttu-id="70c3e-108">Além disso, para a classe **getXbyY** de funções, os códigos de erro não são disponibilizados por meio da variável de *\_ errno h* .</span><span class="sxs-lookup"><span data-stu-id="70c3e-108">Additionally, for the **getXbyY** class of functions, error codes are not made available through the *h\_errno* variable.</span></span> <span data-ttu-id="70c3e-109">A função [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) destina-se a fornecer uma maneira confiável para um thread em um processo multithread para obter informações de erro por thread.</span><span class="sxs-lookup"><span data-stu-id="70c3e-109">The [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) function is intended to provide a reliable way for a thread in a multithreaded process to obtain per-thread error information.</span></span>

<span data-ttu-id="70c3e-110">Para compatibilidade com o Berkeley UNIX (BSD), versões anteriores do Windows (Windows 95 com a atualização do Windows Socket 2 e Windows 98, por exemplo) constantes de erro do Berkeley regulares redefinidas normalmente encontradas em *errno. h* no BSD como os erros de WSA equivalentes do Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="70c3e-110">For compatibility with Berkeley UNIX (BSD), early versions of Windows (Windows 95 with the Windows Socket 2 Update and Windows 98, for example) redefined regular Berkeley error constants typically found in *errno.h* on BSD as the equivalent Windows Sockets WSA errors.</span></span> <span data-ttu-id="70c3e-111">Por exemplo, ECONNREFUSED foi definido como **WSAECONNREFUSED** no arquivo de cabeçalho *Winsock. h* .</span><span class="sxs-lookup"><span data-stu-id="70c3e-111">So for example, ECONNREFUSED was defined as **WSAECONNREFUSED** in the *Winsock.h* header file.</span></span> <span data-ttu-id="70c3e-112">Nas versões subsequentes do Windows (Windows NT 3,1 e posterior), esses definidos foram comentados para evitar conflitos com *errno. h* usados com o Microsoft C/C++ e o Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="70c3e-112">In subsequent versions of Windows (Windows NT 3.1 and later) these defines were commented out to avoid conflicts with *errno.h* used with Microsoft C/C++ and Visual Studio.</span></span>

<span data-ttu-id="70c3e-113">O arquivo de cabeçalho *Winsock2. h* incluído com o SDK (Software Development Kit) do Microsoft Windows, o SDK (Kit de desenvolvimento de software de plataforma) e o Visual Studio ainda contém um bloco comentado de define dentro de um \# bloco ifdef 0 e \# endif que definem os códigos de erro de soquete BSD como iguais às constantes de erro de WSA.</span><span class="sxs-lookup"><span data-stu-id="70c3e-113">The *Winsock2.h* header file included with the Microsoft Windows Software Development Kit (SDK), Platform Software Development Kit (SDK), and Visual Studio still contains a commented out block of defines within an \#ifdef 0 and \#endif block that define the BSD socket error codes to be the same as the WSA error constants.</span></span> <span data-ttu-id="70c3e-114">Eles podem ser usados para fornecer alguma compatibilidade com a programação de soquetes UNIX, BSD e Linux.</span><span class="sxs-lookup"><span data-stu-id="70c3e-114">These can be used to provide some compatibility with UNIX, BSD, and Linux socket programming.</span></span> <span data-ttu-id="70c3e-115">Para compatibilidade com o BSD, um aplicativo pode optar por alterar o *Winsock2. h* e remover o comentário deste bloco.</span><span class="sxs-lookup"><span data-stu-id="70c3e-115">For compatibility with BSD, an application may choose to change the *Winsock2.h* and uncomment this block.</span></span> <span data-ttu-id="70c3e-116">No entanto, os desenvolvedores de aplicativos são fortemente desencorajados de remover os comentários desse bloco devido a conflitos inevitáveis com *errno. h* na maioria dos aplicativos.</span><span class="sxs-lookup"><span data-stu-id="70c3e-116">However, application developers are strongly discouraged from uncommenting this block because of inevitable conflicts with *errno.h* in most applications.</span></span> <span data-ttu-id="70c3e-117">Além disso, os erros de soquete BSD são definidos com valores muito diferentes dos usados em programas UNIX, BSD e Linux.</span><span class="sxs-lookup"><span data-stu-id="70c3e-117">Also, the BSD socket errors are defined to very different values than are used in UNIX, BSD, and Linux programs.</span></span> <span data-ttu-id="70c3e-118">Os desenvolvedores de aplicativos são altamente incentivados a usar as constantes de erro de WSA em aplicativos de soquete.</span><span class="sxs-lookup"><span data-stu-id="70c3e-118">Application developers are very strongly encouraged to use the WSA error constants in socket applications.</span></span>

<span data-ttu-id="70c3e-119">Esses definidos permanecem comentados no cabeçalho *Winsock2. h* dentro de um \# bloco ifdef 0 e \# endif.</span><span class="sxs-lookup"><span data-stu-id="70c3e-119">These defines remain commented out in the *Winsock2.h* header within an \#ifdef 0 and \#endif block.</span></span> <span data-ttu-id="70c3e-120">Se um desenvolvedor de aplicativos insistir em usar os códigos de erro do BSD para compatibilidade, um aplicativo poderá optar por incluir uma linha do formulário:</span><span class="sxs-lookup"><span data-stu-id="70c3e-120">If an application developer insists on using the BSD error codes for compatibility, then an application may choose to include a line of the form:</span></span>


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



<span data-ttu-id="70c3e-121">Isso permite que o código de rede que foi escrito para usar o *errno* global funcione corretamente em um ambiente de thread único.</span><span class="sxs-lookup"><span data-stu-id="70c3e-121">This allows networking code which was written to use the global *errno* to work correctly in a single-threaded environment.</span></span> <span data-ttu-id="70c3e-122">Há algumas desvantagens muito sérias.</span><span class="sxs-lookup"><span data-stu-id="70c3e-122">There are some very serious drawbacks.</span></span> <span data-ttu-id="70c3e-123">Se um arquivo de origem incluir um código que Inspecione *errno* para funções de soquete e sem soquete, esse mecanismo não poderá ser usado.</span><span class="sxs-lookup"><span data-stu-id="70c3e-123">If a source file includes code which inspects *errno* for both socket and non-socket functions, this mechanism cannot be used.</span></span> <span data-ttu-id="70c3e-124">Além disso, não é possível que um aplicativo atribua um novo valor a *errno*.</span><span class="sxs-lookup"><span data-stu-id="70c3e-124">Furthermore, it is not possible for an application to assign a new value to *errno*.</span></span> <span data-ttu-id="70c3e-125">(No Windows Sockets, a função [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) pode ser usada para essa finalidade.)</span><span class="sxs-lookup"><span data-stu-id="70c3e-125">(In Windows Sockets, the function [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) may be used for this purpose.)</span></span>

<span data-ttu-id="70c3e-126">Estilo BSD típico</span><span class="sxs-lookup"><span data-stu-id="70c3e-126">Typical BSD Style</span></span>


```C++
r = recv(...);
if (r == -1
    && errno == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="70c3e-127">Estilo preferencial</span><span class="sxs-lookup"><span data-stu-id="70c3e-127">Preferred Style</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == EWOULDBLOCK)
    {...}
```



<span data-ttu-id="70c3e-128">Embora as constantes de erro consistentes com Berkeley Sockets 4,3 sejam fornecidas para fins de compatibilidade, os aplicativos são altamente incentivados a usar as definições de código de erro de WSA.</span><span class="sxs-lookup"><span data-stu-id="70c3e-128">Although error constants consistent with Berkeley Sockets 4.3 are provided for compatibility purposes, applications are strongly encouraged to use the WSA error code definitions.</span></span> <span data-ttu-id="70c3e-129">Isso ocorre porque os códigos de erro retornados por certas funções do Windows Sockets se enquadram no intervalo padrão de códigos de erro, conforme definido pelo Microsoft C ©.</span><span class="sxs-lookup"><span data-stu-id="70c3e-129">This is because error codes returned by certain Windows Sockets functions fall into the standard range of error codes as defined by Microsoft C©.</span></span> <span data-ttu-id="70c3e-130">Portanto, uma versão melhor do fragmento de código-fonte anterior é:</span><span class="sxs-lookup"><span data-stu-id="70c3e-130">Thus, a better version of the preceding source code fragment is:</span></span>


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



<span data-ttu-id="70c3e-131">A especificação original do Winsock 1,1 definida em 1995 recomenda um conjunto de códigos de erro e listava os possíveis erros que podem ser retornados como resultado de cada função.</span><span class="sxs-lookup"><span data-stu-id="70c3e-131">The original Winsock 1.1 specification defined in 1995 recommended a set of error codes, and listed the possible errors that can be returned as a result of each function.</span></span> <span data-ttu-id="70c3e-132">O Windows Sockets 2 adicionou funções e recursos com outros códigos de erro do Windows Sockets retornados além daqueles listados na especificação original do Winsock.</span><span class="sxs-lookup"><span data-stu-id="70c3e-132">Windows Sockets 2 added functions and features with other Windows Sockets error codes returned in addition to those listed in the original Winsock specification.</span></span> <span data-ttu-id="70c3e-133">Funções adicionais foram adicionadas ao longo do tempo para aprimorar o Winsock para uso pelos desenvolvedores.</span><span class="sxs-lookup"><span data-stu-id="70c3e-133">Additional functions have been added over time to enhance Winsock for use by developers.</span></span> <span data-ttu-id="70c3e-134">Por exemplo, novas funções de serviço de nome ([**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), por exemplo) foram adicionadas que dão suporte a IPv6 e IPv4 no Windows XP e versões posteriores.</span><span class="sxs-lookup"><span data-stu-id="70c3e-134">For example, new name service functions ([**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), for example) were added that support both IPv6 and IPv4 on Windows XP and later.</span></span> <span data-ttu-id="70c3e-135">Algumas das funções de serviço de nome somente IPv4 mais antigas (a classe **getXbyY** de funções, por exemplo) foram preteridas.</span><span class="sxs-lookup"><span data-stu-id="70c3e-135">Some of the older IPv4-only name service functions (the **getXbyY** class of functions, for example) have been deprecated.</span></span>

<span data-ttu-id="70c3e-136">Uma lista completa de códigos de erro possíveis retornados pelas funções do Windows Sockets é fornecida na seção sobre [códigos de erro do Windows Sockets](windows-sockets-error-codes-2.md).</span><span class="sxs-lookup"><span data-stu-id="70c3e-136">A complete list of possible error codes returned by Windows Sockets functions is given in the section on [Windows Sockets Error Codes](windows-sockets-error-codes-2.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="70c3e-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70c3e-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70c3e-138">Manipulando erros do Winsock</span><span class="sxs-lookup"><span data-stu-id="70c3e-138">Handling Winsock Errors</span></span>](handling-winsock-errors.md)
</dt> <dt>

[<span data-ttu-id="70c3e-139">Portando aplicativos de soquete para Winsock</span><span class="sxs-lookup"><span data-stu-id="70c3e-139">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="70c3e-140">Códigos de erro do Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="70c3e-140">Windows Sockets Error Codes</span></span>](windows-sockets-error-codes-2.md)
</dt> <dt>

[<span data-ttu-id="70c3e-141">Considerações sobre programação do Winsock</span><span class="sxs-lookup"><span data-stu-id="70c3e-141">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
