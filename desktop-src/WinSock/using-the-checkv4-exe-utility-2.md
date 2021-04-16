---
description: Usando o utilitário Checkv4.exe para modificar seu aplicativo IPv4 para dar suporte ao IPv6.
ms.assetid: 36b72e4f-133d-4d96-a3c9-86a852d3a479
title: Usando o utilitário Checkv4.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc9eca96b2138f9950b157a4b7690dc382f273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558370"
---
# <a name="using-the-checkv4exe-utility"></a>Usando o utilitário Checkv4.exe

> [!IMPORTANT]
> O utilitário *Checkv4.exe* não é fornecido no SDK (Kit de desenvolvimento de software) do Windows para Windows 8, nem em versões posteriores do SDK do Windows.

O utilitário *Checkv4.exe* foi projetado para fornecer um parceiro de porta de código; um utilitário que percorre sua base de código com você, identifica possíveis problemas ou realça código que pode se beneficiar de funções ou estruturas compatíveis com IPv6 e faz recomendações. Com o utilitário Checkv4.exe, a tarefa de modificar um aplicativo IPv4 existente para dar suporte ao IPv6 torna-se muito mais fácil.

O utilitário *Checkv4.exe* é instalado como parte do SDK (Software Development Kit) do Microsoft Windows lançado para o Windows Vista e SDKs posteriores (até, mas não incluindo, o SDK (Software Development Kit) do Windows para Windows 8).

Uma versão anterior do utilitário de *Checkv4.exe* com recursos mais limitados também foi disponibilizada como parte do Microsoft IPv6 Technology Preview anterior para Windows 2000.

As seções a seguir descrevem como usar o utilitário *Checkv4.exe* e, em seguida, explicam a abordagem recomendada para modificar um aplicativo IPv4 existente para dar suporte ao IPv6.

## <a name="recommendations-for-running-checkv4exe"></a>Recomendações para execução de Checkv4.exe

-   O utilitário *Checkv4.exe* é simples. Basta executar *Checkv4.exe* na linha de comando com o nome do arquivo que você deseja verificar como o parâmetro. *Checkv4.exe* analisa o arquivo e fornece comentários sobre onde existem problemas de porta IPv6 nesse arquivo. Colocar o *Checkv4.exe* no caminho do computador torna a execução do utilitário de *Checkv4.exe* de qualquer lugar em sua estrutura de diretórios de código-fonte muito mais fácil. Por exemplo, colocar *Checkv4.exe* em% windir% permite que você inicie o *Checkv4.exe* de qualquer diretório no computador sem incluir seu caminho.

-   Emita o seguinte comando no prompt de comando para analisar o arquivo Simplec. c:

    **Checkv4 simplec. c**

    Observe que algumas das recomendações feitas pelo utilitário de *Checkv4.exe* exigem estruturas disponíveis somente em versões recentes do arquivo de cabeçalho *Ws2tcpip. h* , como a estrutura **SOCKADDR \_ In6** . Esses arquivos de cabeçalho estão incluídos no SDK do Windows lançado para Windows Vista e posterior. Esses arquivos de cabeçalho também estão incluídos no SDK (Kit de desenvolvimento de software) da plataforma anterior lançado para o Windows Server 2003. Esses arquivos de cabeçalho também são incluídos como parte de uma assinatura do MSDN ou por download.

    A captura de tela a seguir exibe os resultados do uso do utilitário *Checkv4.exe* no arquivo Simplec. c incluído no apêndice A:

    ![checkv4.exe relata incompatibilidades de IPv6 no arquivo simplec. c](images/portingguide002.jpg)

    A captura de tela a seguir exibe os resultados do uso do utilitário *Checkv4.exe* no arquivo simples. c, que também está incluído no apêndice A:

    ![checkv4.exe relata incompatibilidades de IPv6 no arquivo simples. c](images/portingguide003.jpg)

## <a name="the-application-modification-process-where-to-start"></a>O processo de modificação do aplicativo: onde começar

Há um procedimento recomendado associado à adição do recurso IPv6 aos aplicativos. Seguir essa sequência é benéfico, pois permite aos desenvolvedores garantir que todas as etapas necessárias para modificar um aplicativo IPv4 existente para dar suporte ao IPv6 sejam tiradas. Determinados aplicativos podem exigir uma atenção mais abrangente para uma dessas sequências; por exemplo, um serviço do sistema provavelmente terá menos problemas de interface do usuário do que um FTP (programa de transferência de arquivos) gráfico.

**Para modificar aplicativos IPv4 para dar suporte a IPv6**

1.  Corrija estruturas e declarações para habilitar a compatibilidade com IPv6 e IPv4.
2.  Modifique as chamadas de função para tirar proveito das funções habilitadas para IPv6, como as funções [**Getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .
3.  Revise o código-fonte para o uso de endereços IPv4 embutidos em código, como o endereço de loopback ou o uso de outras cadeias de caracteres literais.
4.  Execute uma revisão completa da interface do usuário, incluindo caixas de diálogo informativas. Pense se é apropriado para os aplicativos habilitados para IPv6 especificar ou fornecer informações baseadas em endereço IP.
5.  Determine se seu aplicativo depende de protocolos subjacentes, como RPC, e faça as alterações programáticas apropriadas para lidar com endereços IPv6.
6.  Use o sinalizador de tempo de compilação IPV6STRICT ao compilar aplicativos no Windows XP e versões posteriores. Esse sinalizador resulta na falha da compilação de um código incompatível, da seguinte maneira:

    Aplicativos do Windows Sockets 1. x com código incompatível falha ao compilar e retornar a mensagem de erro "WINSOCK2 necessário".

    Os aplicativos do Windows Sockets 2. x com código incompatível causam um erro de tempo de compilação para cada instância de código incompatível. Uma mensagem de erro é gerada no seguinte formato:

    `[file name] ([line number]) : [error message] '[symbol]_IPV6INCOMPATIBLE'`

    Por exemplo:

    `sample.c(8) : error C2065: 'gethostbyaddr_IPV6INCOMPATIBLE' : undeclared identifier`

 

 



