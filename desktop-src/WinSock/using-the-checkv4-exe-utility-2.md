---
description: Usando o utilitário Checkv4.exe para modificar seu aplicativo IPv4 para dar suporte a IPv6.
ms.assetid: 36b72e4f-133d-4d96-a3c9-86a852d3a479
title: Usando o utilitário Checkv4.exe aplicativo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3377e62e5a874910f91857b6c5dc64df3c3cccddbe405ab6ca199241038a4ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121056"
---
# <a name="using-the-checkv4exe-utility"></a>Usando o utilitário Checkv4.exe aplicativo

> [!IMPORTANT]
> O *utilitárioCheckv4.exe* não é o SDK do Windows para Windows 8, nem em versões posteriores do SDK do Windows.

O *Checkv4.exe* utilitário foi projetado para fornecer um parceiro de porta de código; um utilitário que realiza etapas em sua base de código com você, identifica possíveis problemas ou realça o código que pode se beneficiar de funções ou estruturas com capacidade para IPv6 e faz recomendações. Com o Checkv4.exe, a tarefa de modificar um aplicativo IPv4 existente para dar suporte a IPv6 se torna muito mais fácil.

O *utilitárioCheckv4.exe* é instalado como parte do SDK (Software Development Kit) do Microsoft Windows lançado para o Windows Vista e SDKs posteriores (até, mas não incluindo, o SDK (Software Development Kit) do Windows para Windows 8).

Uma versão anterior do *utilitárioCheckv4.exe* com recursos mais limitados também foi disponibilizada como parte do Microsoft IPv6 Technology Preview anterior para Windows 2000.

As seções a seguir descrevem como usar o *utilitárioCheckv4.exe* e explicar a abordagem recomendada para modificar um aplicativo IPv4 existente para dar suporte a IPv6.

## <a name="recommendations-for-running-checkv4exe"></a>Recomendações para execução de Checkv4.exe

-   O *Checkv4.exe* utilitário é simples. Basta executar *Checkv4.exe* na linha de comando com o nome do arquivo que você deseja verificar como o parâmetro . *Checkv4.exe* o arquivo e fornece comentários sobre onde existem problemas de portação IPv6 nesse arquivo. Colocar o *Checkv4.exe* no caminho do computador facilita muito a execução do utilitário *Checkv4.exe* de qualquer lugar na estrutura do diretório do código-fonte. Por exemplo, colocar *Checkv4.exe* em %windir% permite que  vocêCheckv4.exede qualquer diretório em seu computador sem incluir seu caminho.

-   Em seguida, emie o seguinte comando no prompt de comando para analisar o arquivo Simplec.c:

    **Checkv4 simplec.c**

    Observe que algumas das recomendações feitas pelo utilitárioCheckv4.exeexigem estruturas disponíveis somente em versões recentes do arquivo de título *Ws2tcpip.h,* como *a* estrutura **SOCKADDR \_ IN6.** Esses arquivos de header estão incluídos no SDK Windows lançado para Windows Vista e posterior. Esses arquivos de header também estão incluídos no SDK (Software Development Kit) da Plataforma anterior lançado para Windows Server 2003. Esses arquivos de header também são incluídos como parte de uma assinatura do MSDN ou por download.

    A captura de tela a seguir exibe os resultados do uso *do utilitárioCheckv4.exe* no arquivo Simplec.c incluído no Apêndice A:

    ![checkv4.exe relata incompatibilidades ipv6 no arquivo simplec.c](images/portingguide002.jpg)

    A captura de tela a seguir exibe os resultados do uso *do utilitárioCheckv4.exe* no arquivo Simples.c, que também está incluído no Apêndice A:

    ![checkv4.exe relata incompatibilidades ipv6 no arquivo simples.c](images/portingguide003.jpg)

## <a name="the-application-modification-process-where-to-start"></a>O processo de modificação do aplicativo: por onde começar

Há um procedimento recomendado associado à adição da funcionalidade IPv6 aos aplicativos. Seguir essa sequência é benéfico, pois permite aos desenvolvedores garantir que todas as etapas necessárias para modificar um aplicativo IPv4 existente para dar suporte ao IPv6 sejam realizadas. Determinados aplicativos podem exigir atenção mais ampla a uma dessas sequências; por exemplo, um serviço de sistema provavelmente teria menos problemas de interface do usuário do que um FTP (programa de transferência de arquivo gráfico).

**Para modificar aplicativos IPv4 para dar suporte a IPv6**

1.  Corrige estruturas e declarações para habilitar a compatibilidade IPv6 e IPv4.
2.  Modifique chamadas de função para aproveitar as funções habilitadas para IPv6, como as [**funções getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) e [**getnameinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
3.  Revise o código-fonte para o uso de endereços IPv4 codificados, como o endereço de loopback ou o uso de outras cadeias de caracteres literais.
4.  Execute uma revisão completa da interface do usuário, incluindo caixas de diálogo informativas. Dê uma ideia de se é apropriado que aplicativos habilitados para IPv6 especifiquem ou forneçam informações baseadas em endereço IP.
5.  Determine se seu aplicativo depende de protocolos subjacentes, como RPC, e faça alterações programáticas apropriadas para lidar com endereços IPv6.
6.  Use o sinalizador de tempo de compilação IPV6STRICT ao compilar aplicativos no Windows XP e posterior. Esse sinalizador resulta na falha na compilação do código incompatível, da seguinte forma:

    Windows Os aplicativos sockets 1.x com código incompatível falham ao compilar e retornam a mensagem de erro "WINSOCK2 Required".

    Windows Os aplicativos sockets 2.x com código incompatível causam um erro de tempo de compilação para cada instância de código incompatível. Uma mensagem de erro é gerada no seguinte formato:

    `[file name] ([line number]) : [error message] '[symbol]_IPV6INCOMPATIBLE'`

    Por exemplo:

    `sample.c(8) : error C2065: 'gethostbyaddr_IPV6INCOMPATIBLE' : undeclared identifier`

 

 



