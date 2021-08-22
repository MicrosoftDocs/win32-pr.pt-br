---
description: Um provedor de namespace implementa um mapeamento de interface entre a SPI do namespace winsock e a interface programática nativa de um serviço de nome existente, como DNS, X.500 ou Serviços de diretório do NetWare (NDS).
ms.assetid: 9b35aa58-9011-4e0d-8c93-02714952b4a5
title: Provedores de serviços de namespace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35e6ecc9ad0dcb9667bdd3d08049b9d41c3211de422cae0530506f6103494527
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822634"
---
# <a name="namespace-service-providers"></a>Provedores de serviços de namespace

Um provedor de namespace implementa um mapeamento de interface entre a SPI do namespace winsock e a interface programática nativa de um serviço de nome existente, como DNS, X.500 ou Serviços de diretório do NetWare (NDS). Embora um provedor de namespace seja compatível com exatamente um namespace, é possível que vários provedores de um determinado namespace sejam instalados. Também é possível que uma única DLL crie uma instância de vários provedores de namespace. À medida que os provedores de namespace são instalados, um catálogo [**de estruturas WSANAMESPACE \_ INFO**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infow) é mantido. Um aplicativo pode usar [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) para descobrir quais namespaces têm suporte em um computador.

No Windows Vista e posterior, uma estrutura [**WSANAMESPACE \_ INFOEX**](/windows/desktop/api/Winsock2/ns-winsock2-wsanamespace_infoexw) aprimorada e a [**função WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) são fornecidas.

Em plataformas de 64 bits, as funções [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32) e [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) semelhantes são fornecidas para enumerar o catálogo de 32 bits.

Consulte [Requisitos do provedor de serviços de namespace winsock](winsock-namespace-service-provider-requirements.md) para obter informações detalhadas.

## <a name="legacy-getxbyy-service-providers"></a>Provedores de serviços GetXbyY herdado

Windows Os soquetes 2 são totalmente compatíveis com os recursos de resolução de nomes específicos do TCP/IP encontrados Windows Sockets versão 1.1. Ele faz isso incluindo o conjunto de **funções GetXbyY** na SPI. No entanto, o tratamento desse conjunto de funções é um pouco diferente do restante das funções spi. As **funções GetXbyY** que aparecem na SPI são pré-facedas com GETXBYYSP e são resumidas \_ na tabela a seguir.

Funções de estilo De Berkeley



| Nome da função SPI           | Descrição                                                                              |
|-----------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ gethostbyaddr    | Fornece uma [**estrutura de hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para o endereço de host especificado.        |
| GETXBYYSP \_ gethostbyname    | Fornece uma [**estrutura hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para o nome do host especificado.           |
| GETXBYYSP \_ getprotobyname   | Fornece uma [**estrutura protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) para o nome do protocolo especificado.     |
| GETXBYYSP \_ getprotobynumber | Fornece uma [**estrutura protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) para o número de protocolo especificado.   |
| GETXBYYSP \_ getservbyname    | Fornece uma [**estrutura de servent**](/windows/desktop/api/winsock/ns-winsock-servent) para o serviço especificado nam.e        |
| GETXBYYSP \_ getservbyport    | Fornece uma [**estrutura de evento**](/windows/desktop/api/winsock/ns-winsock-servent) para o serviço na porta especificada. |
| GETXBYYSP \_ gethostname      | Retorna o nome do host padrão para o computador local.                                   |



 

Funções de estilo assíncrono



| Nome da função SPI                   | Descrição                                                                              |
|-------------------------------------|------------------------------------------------------------------------------------------|
| GETXBYYSP \_ WSAAsyncGetHostByAddr    | Fornece uma [**estrutura de hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para o endereço de host especificado.        |
| GETXBYYSP \_ WSAAsyncGetHostByName    | Fornece uma [**estrutura hostent**](/windows/desktop/api/winsock/ns-winsock-hostent) para o nome do host especificado.           |
| GETXBYYSP \_ WSAAsyncGetProtoByName   | Fornece uma [**estrutura protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) para o nome do protocolo especificado.     |
| GETXBYYSP \_ WSAAsyncGetProtoByNumber | Fornece uma [**estrutura protoent**](/windows/desktop/api/winsock/ns-winsock-protoent) para o número de protocolo especificado.   |
| GETXBYYSP \_ WSAAsyncGetServByName    | Fornece uma [**estrutura de evento**](/windows/desktop/api/winsock/ns-winsock-servent) para o nome do serviço especificado.        |
| GETXBYYSP \_ WSAAsyncGetServByPort    | Fornece uma [**estrutura de evento**](/windows/desktop/api/winsock/ns-winsock-servent) para o serviço na porta especificada. |
| GETXBYYSP \_ WSACancelAsyncRequest    | Cancela uma operação **GetXbyY** assíncrona.                                           |



 

A sintaxe e a semântica dessas funções **GetXbyY** na SPI são exatamente iguais às documentadas na Especificação de API e, portanto, não são repetidas aqui.

A DLL Windows Soquetes 2 permite que exatamente um provedor de serviços ofereça esses serviços. Portanto, não é necessário incluir ponteiros para essas funções na tabela de procedimento recebida dos provedores de serviços na inicialização. Em Windows ambientes, o caminho para a DLL que implementa essas funções é recuperado do valor encontrado no caminho do Registro a seguir. Essa entrada do Registro não existe por padrão:

**HKEY \_ \_Parâmetros** \\  \\  \\  \\ GetXByYLibraryPath dos **Serviços WinSock2** \\  \\ **do sistema LOCAL** MACHINE

## <a name="built-in-default-getxbyy-service-provider"></a>Built-In provedor de serviços GetXbyy padrão

Um provedor **de serviços GetXbyY** padrão é integrado aos componentes de tempo de Windows Desoquetes 2 padrão. Esse provedor padrão implementa todas as funções acima, portanto, não é necessário que essas funções sejam implementadas por nenhum provedor de namespace. No entanto, um provedor de namespace é livre para fornecer qualquer ou todas essas funções (e, portanto, substituir os padrões) simplesmente armazenar a cadeia de caracteres que é o caminho para a DLL que implementa essas funções na chave do Registro indicada. Qualquer uma das **funções GetXbyY** não exportadas pela DLL do provedor nomeado será fornecida por meio dos padrões integrados. No entanto, observe que, se um provedor optar por fornecer qualquer uma das versões assíncronas das funções **GetXbyY,** ele deverá fornecer todas as funções assíncronas para que a operação de cancelamento funcione adequadamente.

A implementação atual do provedor de **serviços GetXbyY** padrão reside no Wsock32.dll. Dependendo de como as configurações de TCP/IP foram estabelecidas por meio Painel de Controle, a resolução de nomes ocorrerá usando arquivos DNS ou host local. Quando o DNS é usado, o provedor de serviços **GetXbyY** padrão usa chamadas padrão de API Windows Sockets 1.1 para se comunicar com o servidor DNS. Essas transações ocorrerão usando qualquer pilha TCP/IP configurada como a pilha TCP/IP padrão. Dois casos especiais, no entanto, mencionam menção especial.

A implementação padrão de GETXBYYSP \_ gethostname obtém o nome do host local do Registro. Isso corresponderá ao nome atribuído a "Meu Computador". A implementação padrão de GETXBYYSP \_ gethostbyname e GETXBYYSP WSAAsyncGetHostByName sempre compara o nome do host fornecido com o nome \_ do host local. Se eles corresponderem, a implementação padrão usará uma interface privada para investigar a pilha TCP/IP da Microsoft para descobrir seu endereço IP local. Portanto, para ser completamente independente da pilha TCP/IP da Microsoft, um provedor de namespace deve implementar GETXBYYSP \_ gethostbyname e GETXBYYSP \_ WSAAsyncGetHostByName.

 

 



