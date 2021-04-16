---
description: Um provedor de namespace implementa um mapeamento de interface entre o SPI do namespace do Winsock e a interface programática nativa de um serviço de nome existente, como DNS, X. 500 ou Serviços de diretório do NetWare (NDS).
ms.assetid: 9b35aa58-9011-4e0d-8c93-02714952b4a5
title: Provedores de serviço de namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e975c7ad0e5df29910624bb8f0b9d94fd24d9b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752384"
---
# <a name="namespace-service-providers"></a>Provedores de serviço de namespace

Um provedor de namespace implementa um mapeamento de interface entre o SPI do namespace do Winsock e a interface programática nativa de um serviço de nome existente, como DNS, X. 500 ou Serviços de diretório do NetWare (NDS). Embora um provedor de namespace dê suporte a exatamente um namespace, é possível que vários provedores de um determinado namespace sejam instalados. Também é possível que uma única DLL crie uma instância de vários provedores de namespace. Como os provedores de namespace são instalados, um catálogo das estruturas de [**\_ informações do WSANAMESPACE**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infow) é mantido. Um aplicativo pode usar o [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) para descobrir quais namespaces têm suporte em um computador.

No Windows Vista e posterior, uma estrutura [**\_ INFOEX WSANAMESPACE**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infoexw) e uma função [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) aprimoradas são fornecidas.

Em plataformas de 64 bits, as funções [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32) e [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) semelhantes são fornecidas para enumerar o catálogo de 32 bits.

Consulte [requisitos do provedor de serviço de namespace do Winsock](winsock-namespace-service-provider-requirements.md) para obter informações detalhadas.

## <a name="legacy-getxbyy-service-providers"></a>Provedores de serviço GetXbyY herdados

O Windows Sockets 2 dá suporte total a instalações de resolução de nomes específicas de TCP/IP encontradas no Windows Sockets versão 1,1. Ele faz isso incluindo o conjunto de funções **GetXbyY** no SPI. No entanto, o tratamento desse conjunto de funções é um pouco diferente do restante das funções SPI. As funções **GetXbyY** exibidas no SPI são precedidas de GETXBYYSP \_ e resumidas na tabela a seguir.

Funções de estilo Berkeley



| Nome da função SPI           | Descrição                                                                              |
|-----------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ GetHostbyaddr    | Fornece uma estrutura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para o endereço de host especificado.        |
| GETXBYYSP \_ gethostbyname    | Fornece uma estrutura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para o nome de host especificado.           |
| GETXBYYSP \_ getprotobyname   | Fornece uma estrutura [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) para o nome de protocolo especificado.     |
| GETXBYYSP \_ getprotobynumber | Fornece uma estrutura [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) para o número de protocolo especificado.   |
| GETXBYYSP \_ getservbyname    | Fornece uma estrutura [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) para o ServiceName especificado. e        |
| GETXBYYSP \_ getservbyport    | Fornece uma estrutura [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) para o serviço na porta especificada. |
| GETXBYYSP \_ GetHostName      | Retorna o nome de host padrão para o computador local.                                   |



 

Funções de estilo assíncrono



| Nome da função SPI                   | Descrição                                                                              |
|-------------------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ WSAAsyncGetHostByAddr    | Fornece uma estrutura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para o endereço de host especificado.        |
| GETXBYYSP \_ WSAAsyncGetHostByName    | Fornece uma estrutura [**hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para o nome de host especificado.           |
| GETXBYYSP \_ WSAAsyncGetProtoByName   | Fornece uma estrutura [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) para o nome de protocolo especificado.     |
| GETXBYYSP \_ WSAAsyncGetProtoByNumber | Fornece uma estrutura [**protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) para o número de protocolo especificado.   |
| GETXBYYSP \_ WSAAsyncGetServByName    | Fornece uma estrutura [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) para o nome do serviço especificado.        |
| GETXBYYSP \_ WSAAsyncGetServByPort    | Fornece uma estrutura [**servent**](/windows/desktop/api/winsock/ns-winsock-servent) para o serviço na porta especificada. |
| GETXBYYSP \_ WSACancelAsyncRequest    | Cancela uma operação assíncrona de **GetXbyY** .                                           |



 

A sintaxe e a semântica dessas funções **GetXbyY** no SPI são exatamente as mesmas que aquelas documentadas na especificação de API e são, portanto, não repetidas aqui.

A DLL do Windows Sockets 2 permite que exatamente um provedor de serviços ofereça esses serviços. Portanto, não há necessidade de incluir ponteiros para essas funções na tabela de procedimento recebida de provedores de serviço na inicialização. Em ambientes do Windows, o caminho para a DLL que implementa essas funções é recuperado do valor encontrado no seguinte caminho de registro. Essa entrada de registro não existe por padrão:

**HKEY \_ Sistemas do \_ computador local** \\  \\ **CurrentControlSet** \\ **Services** \\ **Winsock2** \\ **Parameters** \\ **GetXByYLibraryPath**

## <a name="built-in-default-getxbyy-service-provider"></a>Built-In provedor de serviço GetXbyY padrão

Um provedor de serviços **GetXbyY** padrão é integrado aos componentes de tempo de execução padrão do Windows Sockets 2. Esse provedor padrão implementa todas as funções acima, portanto, não é necessário que essas funções sejam implementadas por qualquer provedor de namespace. No entanto, um provedor de namespace é gratuito para fornecer qualquer ou todas essas funções (e, portanto, substituir os padrões) simplesmente armazenando a cadeia de caracteres que é o caminho para a DLL que implementa essas funções na chave do Registro indicada. Qualquer uma das funções **GetXbyY** não exportadas pela DLL do provedor nomeado será fornecida por meio dos padrões internos. No entanto, observe que se um provedor optar por fornecer qualquer versão assíncrona das funções **GetXbyY** , ele deverá fornecer todas as funções assíncronas para que a operação de cancelamento funcione adequadamente.

A implementação atual do provedor de serviços **GetXbyY** padrão reside dentro do Wsock32.dll. Dependendo de como as configurações de TCP/IP tiverem sido estabelecidas por meio do painel de controle, a resolução de nomes ocorrerá usando arquivos de host DNS ou locais. Quando o DNS é usado, o provedor de serviço padrão do **GetXbyY** usa chamadas à API do Windows sockets 1,1 para se comunicar com o servidor DNS. Essas transações ocorrerão usando qualquer pilha TCP/IP configurada como a pilha TCP/IP padrão. No entanto, dois casos especiais merecem menção especial.

A implementação padrão de GETXBYYSP \_ GetHostName Obtém o nome do host local do registro. Isso corresponderá ao nome atribuído a "Meu Computador". A implementação padrão de GETXBYYSP \_ GetHostByName e GETXBYYSP \_ WSAAsyncGetHostByName sempre compara o nome de host fornecido com o nome de host local. Se eles corresponderem, a implementação padrão usará uma interface privada para investigar a pilha do Microsoft TCP/IP a fim de descobrir seu endereço IP local. Portanto, para ser completamente independente da pilha do Microsoft TCP/IP, um provedor de namespace deve implementar GETXBYYSP \_ GetHostByName e GETXBYYSP \_ WSAAsyncGetHostByName.

 

 



