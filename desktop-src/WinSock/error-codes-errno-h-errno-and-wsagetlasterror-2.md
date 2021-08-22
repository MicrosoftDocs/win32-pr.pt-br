---
description: em aplicativos Winsock, os códigos de erro são recuperados usando a função WSAGetLastError, os soquetes de Windows substituem para a função Windows getlasterror.
ms.assetid: cb73fc92-74bd-4c8b-a1c0-6daf4d298aa1
title: Códigos de erro-errno, h_errno e WSAGetLastError
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2e9c4372bd479ee4b94bd3226128737dae3d5637be94046eb013716590ac285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132629"
---
# <a name="error-codes---errno-h_errno-and-wsagetlasterror"></a>Códigos de erro-errno, h \_ errno e WSAGetLastError

em aplicativos Winsock, os códigos de erro são recuperados usando a função [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) , os soquetes de Windows substituem para a função Windows [**getlasterror**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) . os códigos de erro retornados por Windows soquetes são semelhantes às constantes de código de erro de soquete UNIX, mas as constantes são todas prefixadas com o WSA. assim, em aplicativos Winsock, o código de erro WSAEWOULDBLOCK seria retornado, enquanto em aplicativos UNIX o código de erro EWOULDBLOCK seria retornado.

os códigos de erro definidos por Windows soquetes não são disponibilizados por meio da variável *errno* . Além disso, para a classe **getXbyY** de funções, os códigos de erro não são disponibilizados por meio da variável de *\_ errno h* . A função [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) destina-se a fornecer uma maneira confiável para um thread em um processo multithread para obter informações de erro por thread.

para compatibilidade com Berkeley UNIX (BSD), versões anteriores do Windows (Windows 95 com a atualização Windows soquete 2 e Windows 98, por exemplo) constantes de erro do Berkeley regulares redefinidas normalmente encontradas em *errno. h* no BSD como os erros de WSA do Windows sockets equivalentes. Por exemplo, ECONNREFUSED foi definido como **WSAECONNREFUSED** no arquivo de cabeçalho *Winsock. h* . nas versões subsequentes do Windows (Windows NT 3,1 e posteriores), esses definidos foram comentados para evitar conflitos com *errno. h* usados com o Microsoft C/C++ e o Visual Studio.

o arquivo de cabeçalho *Winsock2. h* incluído no Microsoft Windows Software development kit (sdk), plataforma sdk (kit de desenvolvimento de software) e Visual Studio ainda contém um bloco comentado de define em um \# bloco ifdef 0 e \# endif que definem os códigos de erro de soquete BSD como iguais às constantes de erro de WSA. eles podem ser usados para fornecer alguma compatibilidade com a programação de soquetes UNIX, BSD e Linux. Para compatibilidade com o BSD, um aplicativo pode optar por alterar o *Winsock2. h* e remover o comentário deste bloco. No entanto, os desenvolvedores de aplicativos são fortemente desencorajados de remover os comentários desse bloco devido a conflitos inevitáveis com *errno. h* na maioria dos aplicativos. além disso, os erros de soquete BSD são definidos com valores muito diferentes dos usados nos programas UNIX, BSD e Linux. Os desenvolvedores de aplicativos são altamente incentivados a usar as constantes de erro de WSA em aplicativos de soquete.

Esses definidos permanecem comentados no cabeçalho *Winsock2. h* dentro de um \# bloco ifdef 0 e \# endif. Se um desenvolvedor de aplicativos insistir em usar os códigos de erro do BSD para compatibilidade, um aplicativo poderá optar por incluir uma linha do formulário:


```C++
#include <windows.h>

#define errno WSAGetLastError()
```



Isso permite que o código de rede que foi escrito para usar o *errno* global funcione corretamente em um ambiente de thread único. Há algumas desvantagens muito sérias. Se um arquivo de origem incluir um código que Inspecione *errno* para funções de soquete e sem soquete, esse mecanismo não poderá ser usado. Além disso, não é possível que um aplicativo atribua um novo valor a *errno*. (em soquetes Windows, a função [**WSASetLastError**](/windows/desktop/api/winsock/nf-winsock-wsasetlasterror) pode ser usada para essa finalidade.)

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



Embora as constantes de erro consistentes com Berkeley Sockets 4,3 sejam fornecidas para fins de compatibilidade, os aplicativos são altamente incentivados a usar as definições de código de erro de WSA. isso ocorre porque os códigos de erro retornados por determinadas funções de soquetes de Windows se encaixam no intervalo padrão de códigos de erro, conforme definido pelo Microsoft C ©. Portanto, uma versão melhor do fragmento de código-fonte anterior é:


```C++
r = recv(...);
if (r == -1       /* (but see below) */
    && WSAGetLastError() == WSAEWOULDBLOCK)
    {...}
```



A especificação original do Winsock 1,1 definida em 1995 recomenda um conjunto de códigos de erro e listava os possíveis erros que podem ser retornados como resultado de cada função. Windows os soquetes 2 adicionaram funções e recursos com outros códigos de erro de soquetes de Windows retornados além daqueles listados na especificação original do Winsock. Funções adicionais foram adicionadas ao longo do tempo para aprimorar o Winsock para uso pelos desenvolvedores. por exemplo, novas funções de serviço de nome ([**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo), por exemplo) foram adicionadas que dão suporte a IPv6 e IPv4 no Windows XP e posterior. Algumas das funções de serviço de nome somente IPv4 mais antigas (a classe **getXbyY** de funções, por exemplo) foram preteridas.

uma lista completa de códigos de erro possíveis retornados pelas funções de soquetes de Windows é fornecida na seção sobre [códigos de erro de soquetes de Windows](windows-sockets-error-codes-2.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Manipulando erros do Winsock](handling-winsock-errors.md)
</dt> <dt>

[Portando aplicativos de soquete para Winsock](porting-socket-applications-to-winsock.md)
</dt> <dt>

[Windows Códigos de erro de soquetes](windows-sockets-error-codes-2.md)
</dt> <dt>

[Considerações sobre programação do Winsock](winsock-programming-considerations.md)
</dt> </dl>

 

 
