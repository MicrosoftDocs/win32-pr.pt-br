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
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a>Códigos de erro-errno, h \_ errno e WSAGetLastError

Em aplicativos Winsock, os códigos de erro são recuperados usando a função [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) , o Windows Sockets substituto para a função [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) do Windows. Os códigos de erro retornados pelo Windows Sockets são semelhantes às constantes de código de erro de soquete do UNIX, mas as constantes são todos prefixadas com o WSA. Assim, em aplicativos Winsock, o código de erro WSAEWOULDBLOCK seria retornado, enquanto em aplicativos UNIX o código de erro EWOULDBLOCK seria retornado.

Os códigos de erro definidos pelo Windows Sockets não são disponibilizados por meio da variável *errno* . Além disso, para a classe **getXbyY** de funções, os códigos de erro não são disponibilizados por meio da variável de *\_ errno h* . A função [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) destina-se a fornecer uma maneira confiável para um thread em um processo multithread para obter informações de erro por thread.

Para compatibilidade com o Berkeley UNIX (BSD), versões anteriores do Windows (Windows 95 com a atualização do Windows Socket 2 e Windows 98, por exemplo) constantes de erro do Berkeley regulares redefinidas normalmente encontradas em *errno. h* no BSD como os erros de WSA equivalentes do Windows Sockets. Por exemplo, ECONNREFUSED foi definido como **WSAECONNREFUSED** no arquivo de cabeçalho *Winsock. h* . Nas versões subsequentes do Windows (Windows NT 3,1 e posterior), esses definidos foram comentados para evitar conflitos com *errno. h* usados com o Microsoft C/C++ e o Visual Studio.

O arquivo de cabeçalho *Winsock2. h* incluído com o SDK (Software Development Kit) do Microsoft Windows, o SDK (Kit de desenvolvimento de software de plataforma) e o Visual Studio ainda contém um bloco comentado de define dentro de um \# bloco ifdef 0 e \# endif que definem os códigos de erro de soquete BSD como iguais às constantes de erro de WSA. Eles podem ser usados para fornecer alguma compatibilidade com a programação de soquetes UNIX, BSD e Linux. Para compatibilidade com o BSD, um aplicativo pode optar por alterar o *Winsock2. h* e remover o comentário deste bloco. No entanto, os desenvolvedores de aplicativos são fortemente desencorajados de remover os comentários desse bloco devido a conflitos inevitáveis com *errno. h* na maioria dos aplicativos. Além disso, os erros de soquete BSD são definidos com valores muito diferentes dos usados em programas UNIX, BSD e Linux. Os desenvolvedores de aplicativos são altamente incentivados a usar as constantes de erro de WSA em aplicativos de soquete.

Esses definidos permanecem comentados no cabeçalho *Winsock2. h* dentro de um \# bloco ifdef 0 e \# endif. Se um desenvolvedor de aplicativos insistir em usar os códigos de erro do BSD para compatibilidade, um aplicativo poderá optar por incluir uma linha do formulário:


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



Isso permite que o código de rede que foi escrito para usar o *errno* global funcione corretamente em um ambiente de thread único. Há algumas desvantagens muito sérias. Se um arquivo de origem incluir um código que Inspecione *errno* para funções de soquete e sem soquete, esse mecanismo não poderá ser usado. Além disso, não é possível que um aplicativo atribua um novo valor a *errno*. (No Windows Sockets, a função [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) pode ser usada para essa finalidade.)

Estilo BSD típico


```C++
r = recv(...);
if (r == -1
    && errno == EWOULDBLOCK)
    {...}
```



Estilo preferencial


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == EWOULDBLOCK)
    {...}
```



Embora as constantes de erro consistentes com Berkeley Sockets 4,3 sejam fornecidas para fins de compatibilidade, os aplicativos são altamente incentivados a usar as definições de código de erro de WSA. Isso ocorre porque os códigos de erro retornados por certas funções do Windows Sockets se enquadram no intervalo padrão de códigos de erro, conforme definido pelo Microsoft C ©. Portanto, uma versão melhor do fragmento de código-fonte anterior é:


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



A especificação original do Winsock 1,1 definida em 1995 recomenda um conjunto de códigos de erro e listava os possíveis erros que podem ser retornados como resultado de cada função. O Windows Sockets 2 adicionou funções e recursos com outros códigos de erro do Windows Sockets retornados além daqueles listados na especificação original do Winsock. Funções adicionais foram adicionadas ao longo do tempo para aprimorar o Winsock para uso pelos desenvolvedores. Por exemplo, novas funções de serviço de nome ([**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), por exemplo) foram adicionadas que dão suporte a IPv6 e IPv4 no Windows XP e versões posteriores. Algumas das funções de serviço de nome somente IPv4 mais antigas (a classe **getXbyY** de funções, por exemplo) foram preteridas.

Uma lista completa de códigos de erro possíveis retornados pelas funções do Windows Sockets é fornecida na seção sobre [códigos de erro do Windows Sockets](windows-sockets-error-codes-2.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulando erros do Winsock](handling-winsock-errors.md)
</dt> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Códigos de erro do Windows Sockets](windows-sockets-error-codes-2.md)
</dt> <dt>

[Considerações sobre programação do Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
