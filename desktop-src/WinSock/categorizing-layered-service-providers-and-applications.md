---
title: Categorizando provedores de serviços em camadas e aplicativos
description: O Winsock 2 acomoda protocolos em camadas.
ms.assetid: 1c5efd2e-1b42-4c20-a4da-b81a5fc4243c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a966d54da0be26f75a074de18abe1b9e080c0c9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105813584"
---
# <a name="categorizing-layered-service-providers-and-apps"></a>Categorizando provedores de serviços em camadas e aplicativos

> [!Note]  
> Os provedores de serviço em camadas são preteridos. A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).

 

O Winsock 2 acomoda protocolos em camadas. Um protocolo em camadas é aquele que implementa apenas funções de comunicação de nível mais alto, enquanto dependem de uma pilha de transporte subjacente para a troca real de dados com um ponto de extremidade remoto. Um exemplo de um protocolo em camadas ou de um provedor de serviços em camadas seria uma camada de segurança que adiciona o protocolo ao processo de estabelecimento da conexão para executar a autenticação e estabelecer um esquema de criptografia acordado mutuamente. Esse protocolo de segurança, em geral, exigiria os serviços de um protocolo de transporte confiável subjacente, como TCP ou SPX. O termo protocolo base implementado pelo provedor base refere-se a um provedor de Winsock que implementa um protocolo como TCP ou SPX que é capaz de executar comunicações de dados com um ponto de extremidade remoto. O termo protocolo em camadas é usado para descrever um protocolo que não pode ser autônomo. Esses protocolos em camadas são instalados como LSPs (provedores de serviços em camadas) do Winsock.

Um exemplo de LSP é o provedor de serviços de firewall da Microsoft instalado como parte do servidor de autenticação e secutity da Internet (ISA) em clientes. O provedor de serviços do Microsoft Firewall Client é instalado nos provedores de base do Winsock para TCP e UDP. Uma DLL (biblioteca de vínculo dinâmico) no software cliente do ISA firewall se torna um provedor de serviços em camadas do Winsock que todos os aplicativos Winsock usam de forma transparente. Dessa forma, o LSP do cliente ISA firewall pode interceptar chamadas de função Winsock de aplicativos cliente e, em seguida, rotear uma solicitação para o provedor de serviço base subjacente original se o destino for local ou para o serviço de firewall em um computador do ISA Server se o destino for remoto. Um LSP semelhante é instalado como parte do serviço Microsoft Forefront firewall e do cliente TMG (Threat Management Gateway) em clientes.

Durante a inicialização de LSP, o LSP deve fornecer ponteiros para uma série de funções de SPI (interface do provedor de serviço) do Winsock. Essas funções serão chamadas durante o processamento normal pela camada diretamente acima do LSP (outro LSP ou Ws2 \_32.DLL).

É possível definir categorias de LSP com base no subconjunto de funções SPI que um LSP implementa e a natureza do processamento extra realizado para cada uma dessas funções. Ao classificar LSPs, além de classificar os aplicativos que usam soquetes Winsock, é possível determinar seletivamente se um LSP deve estar envolvido em um determinado processo no tempo de execução.

No Windows Vista e posterior, um novo método é fornecido para categorizar os provedores de serviços em camadas do Winsock e os aplicativos para que apenas determinados LSPs sejam carregados. Há vários motivos para adicionar esses recursos.

Um dos principais motivos é que determinados processos críticos do sistema, como Winlogon e LSASS, criam soquetes, mas esses processos não usam esses soquetes para enviar qualquer tráfego na rede. Portanto, a maioria dos LSPs não deve ser carregada nesses processos. Vários casos também foram documentados em que LSPs de bugs podem causar *lsass.exe* a falhar. Se o LSASS falhar, o sistema forçará um desligamento. Um efeito colateral desses processos do sistema de carregamento de LSPs é que esses processos nunca são encerrados, assim quando um LSP é instalado ou removido, uma reinicialização é necessária.

Um motivo secundário é que há alguns casos em que os aplicativos podem não querer carregar determinados LSPs. Por exemplo, alguns aplicativos podem não querer carregar LSPs criptográficos que poderiam impedir que o aplicativo se comunique com outros sistemas que não têm o LSP cyptographic instalado.

Por fim, as categorias de LSP podem ser usadas por outros LSPs para determinar onde na cadeia de protocolo Winsock eles devem se instalar. Há anos, vários desenvolvedores de LSP queriam uma maneira de saber como um LSP se comportará. Por exemplo, um LSP que inspeciona o fluxo de dados deve estar acima de um LSP que criptografa os dados. É claro que esse método de categorização de LSP não é uma prova de obsolescência, pois se baseia em LSPs de terceiros para se categorizar adequadamente.

A categorização de LSP e outros aprimoramentos de segurança no Windows Vista e versões posteriores foram criados para ajudar a impedir que os usuários instalem os LSPs mal-intencionados de forma não intencional.

## <a name="lsp-categories"></a>Categorias de LSP

No Windows Vista e posterior, um LSP pode ser classificado com base em como ele interage com os dados e as chamadas do Windows Sockets. Uma categoria LSP é um grupo de comportamentos identificável em um subconjunto de funções SPI do Winsock. Por exemplo, um filtro de conteúdo HTTP seria Categorizado como um inspetor de dados (a \_ categoria do Inspetor LSP). A categoria do Inspetor de LSP \_ inspecionará (mas não alterar) os parâmetros para as funções SPI de transferência de dados. Um aplicativo pode consultar a categoria de um LSP e optar por não carregar o LSP com base na categoria de LSP e no conjunto de categorias LSP permitidas do aplicativo.

A tabela a seguir lista as categorias nas quais um LSP pode ser classificado.

| Categoria de LSP              | Descrição                                                     |
|---------------------------|-----------------------------------------------------------------|
| **\_compactação de criptografia LSP \_** | O LSP é um provedor de criptografia ou de compactação de dados.         |
| **\_Firewall LSP**         | O LSP é um provedor de firewall.                                 |
| **\_cache local \_ LSP**     | O LSP é um provedor de cache local.                              |
| **modificação de entrada de LSP \_ \_**  | O LSP modifica os dados de entrada.                                  |
| **Inspetor de LSP \_**        | O LSP inspeciona ou filtra os dados.                               |
| **\_modificação de saída de LSP \_** | O LSP modifica os dados de saída.                                 |
| **\_proxy LSP**            | O LSP atua como um proxy e redireciona os pacotes.                  |
| **Redirecionador de LSP \_**       | O LSP é um redirecionador de rede.                                |
| **\_sistema LSP**           | O LSP é aceitável para uso em serviços e processos do sistema. |



 

Um LSP pode pertencer a mais de uma categoria. Por exemplo, um LSP de firewall/segurança poderia pertencer às categorias Inspetor (**LSP \_ Inspector**) e firewall **( \_ Firewall LSP**).

Se um LSP não tiver uma categoria definida, ele será considerado na categoria todos. Essa categoria de LSP não será carregada em serviços ou processos do sistema (por exemplo, LSASS, Winlogon e muitos processos do svchost).

## <a name="categorizing-lsps"></a>Categorizando LSPs

Várias novas funções estão disponíveis no Windows Vista e posterior para categorizar um LSP:

-   [**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo)
-   [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32)
-   [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo)
-   [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32)

Para categorizar um LSP, a função [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo) ou [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32) é chamada com um GUID para identificar a entrada oculta de LSP, a classe Information a ser definida para essa entrada de protocolo LSP e um conjunto de sinalizadores usado para modificar o comportamento da função.

A função [**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo) ou [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32) é usada da mesma forma para recuperar os dados associados a uma classe de informações para um LSP.

## <a name="categorizing-applications"></a>Categorizando aplicativos

Várias novas funções estão disponíveis no Windows Vista e posterior para categorizar um aplicativo:

-   [**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory)
-   [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory)

Para categorizar um aplicativo, a função [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory) é chamada com o caminho de carga para a imagem executável para identificar o aplicativo, os argumentos de linha de comando usados ao iniciar o aplicativo e as categorias de LSP que são permitidas para todas as instâncias desse aplicativo.

A função [**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory) é usada da mesma forma para recuperar as categorias de LSP (provedor de serviço em camadas) associadas a um aplicativo.

## <a name="determining-which-lsps-get-loaded"></a>Determinando quais LSPs são carregados

A parte final da categorização de LSP é determinar quais LSPs serão carregados em quais processos. Quando um processo carrega o Winsock, as seguintes comparações são feitas na categoria do aplicativo e nas categorias de LSP para todos os LSPs instalados:

-   Se o aplicativo não for Categorizado, permita que todos os LSPs sejam carregados no processo.
-   Se o aplicativo e o LSP tiverem categorias atribuídas, todos os itens a seguir deverão ser verdadeiros: <dl> Pelo menos uma das categorias LSP está presente nas categorias especificadas do aplicativo.  
    Somente as categorias especificadas nas categorias especificadas do aplicativo são especificadas nas categorias LSPs. Por exemplo, se o aplicativo especificar uma categoria, ele deverá estar na categoria do LSP.  
    Se a \_ categoria do sistema LSP estiver presente na categoria do aplicativo, ela deverá estar presente nas categorias do LSP.  
    </dl>

> [!Note]  
> Se um LSP não for Categorizado, sua categoria será efetivamente zero. Para que ocorra uma correspondência, todas as categorias especificadas do LSP devem estar presentes nas categorias do aplicativo (as categorias do aplicativo devem ser um superconjunto das categorias do LSP) com a limitação de que, se o \_ sistema LSP estiver presente na categoria do aplicativo, ele também deverá estar presente na categoria do LSP.

 

Considere o seguinte exemplo:

O aplicativo *Foo.exe* é Categorizado como sistema de LSP \_ + \_ Firewall LSP + \_ compactação de criptografia LSP \_ . O *Bar.exe* do aplicativo é Categorizado como \_ Firewall LSP + \_ compactação de criptografia LSP \_ . Há quatro LSPs instalados no sistema:

-   LSP1 definiu uma categoria de \_ sistema LSP.
-   LSP2 não é categorias definidas, portanto, sua categoria é zero.
-   LSP3 definiu uma categoria de \_ Firewall LSP.
-   LSP4 tem categorias definidas de um \_ sistema de LSP + firewall LSP + \_ \_ criptografia LSP \_ compress + Inspetor de LSP \_

Neste exemplo, o aplicativo *Foo.exe* só carregaria LSP1, enquanto o aplicativo *Bar.exe* carregaria LSP3.

## <a name="determining-winsock-providers-installed"></a>Determinando provedores Winsock instalados

O SDK (Software Development Kit) do Microsoft Windows inclui um programa de exemplo de Winsock que pode ser usado para determinar os provedores de transporte do Winsock instalados em um computador local. Por padrão, o código-fonte para este exemplo de Winsock é instalado no seguinte diretório do SDK do Windows para o Windows 7:

*C: \\ arquivos de programas \\ Microsoft SDKs \\ Windows \\ v 7.0 \\ amostras \\ NetDs \\ Winsock \\ LSP*

Este exemplo é um utilitário para instalar e testar provedores de serviço em camadas. Mas ele também pode ser usado para coletar programaticamente informações detalhadas do catálogo do Winsock em um computador local. Para listar todos os provedores de Winsock atuais, incluindo provedores de base e provedores de serviço de camada, compile este exemplo de Winsock e execute o seguinte comando de console:

**instlsp-p**

A saída será uma lista de provedores de Winsock instalados no computador local, incluindo provedores de serviço em camadas. A saída lista a ID do catálogo e o nome da cadeia de caracteres para o provedor de Winsock

Para coletar informações mais detalhadas sobre todos os provedores de Winsock, execute o seguinte comando de console:

**instlsp-p-v**

A saída será uma lista de estruturas de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) com suporte no computador local.

Para obter uma lista de somente provedores de serviço em camadas instalados no computador local, execute o seguinte comando de console:

**instlsp-l**

Para mapear a estrutura LSP, execute o seguinte comando de console:

**instlsp-m**

> [!Note]  
> O recurso TDI foi preterido e será removido em versões futuras do Microsoft Windows. Dependendo de como você usa o TDI, use o kernel do Winsock (WSK) ou a WFP (plataforma de filtragem do Windows). Para obter mais informações sobre WFP e WSK, consulte [Windows Filtering Platform](../fwp/windows-filtering-platform-start-page.md) e [Winsock Kernel](/windows-hardware/drivers/ddi/_netvista/). Para obter uma entrada de blog de sistema de rede do Windows Core sobre WSK e TDI, consulte [Introduction to Winsock kernel (WSK)](/archive/blogs/wndp/).

 

 

 
