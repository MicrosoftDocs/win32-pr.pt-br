---
title: Categorizando aplicativos e provedores de serviços em camadas
description: O Winsock 2 acomoda protocolos em camadas.
ms.assetid: 1c5efd2e-1b42-4c20-a4da-b81a5fc4243c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0993b7a4003b87cf902b9daccbea4742a0bcd0760642429db79b1f1bb0a22600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322387"
---
# <a name="categorizing-layered-service-providers-and-apps"></a>Categorizando aplicativos e provedores de serviços em camadas

> [!Note]  
> Provedores de serviços em camadas foram preterido. Começando com Windows 8 e Windows Server 2012, use [Windows De filtragem.](../fwp/windows-filtering-platform-start-page.md)

 

O Winsock 2 acomoda protocolos em camadas. Um protocolo em camadas é aquele que implementa apenas funções de comunicação de nível superior, enquanto depende de uma pilha de transporte subjacente para a troca real de dados com um ponto de extremidade remoto. Um exemplo de um protocolo em camadas ou provedor de serviços em camadas seria uma camada de segurança que adiciona protocolo ao processo de estabelecimento de conexão para executar a autenticação e estabelecer um esquema de criptografia mutuamente estabelecido. Esse protocolo de segurança geralmente exigiria os serviços de um protocolo de transporte confiável subjacente, como TCP ou SPX. O termo protocolo base implementado pelo provedor base refere-se a um provedor Winsock que implementa um protocolo como TCP ou SPX que é capaz de executar comunicações de dados com um ponto de extremidade remoto. O termo protocolo em camadas é usado para descrever um protocolo que não pode ficar sozinho. Esses protocolos em camadas são instalados como LSPs (Provedores de Serviços em Camadas) winsock.

Um exemplo de um LSP é o provedor de serviços Cliente de Firewall da Microsoft instalado como parte do ISA (Servidor de Autenticação e Secutidade da Internet) em clientes. O Cliente de Firewall da Microsoft de Serviços do Winsock é instalado nos provedores base winsock para TCP e UDP. Uma DLL (biblioteca de vínculo dinâmico) no software cliente do Firewall isa torna-se um provedor de serviços winsock em camadas que todos os aplicativos Winsock usam de forma transparente. Dessa forma, o LSP do cliente do Firewall isa pode interceptar chamadas de função Winsock de aplicativos cliente e, em seguida, rotear uma solicitação para o provedor de serviços base subjacente original se o destino for local ou para o serviço firewall em um computador servidor ISA se o destino for remoto. Um LSP semelhante é instalado como parte do Serviço de Firewall do Microsoft Forefront e do cliente TMG (Gateway de Gerenciamento de Ameaças) em clientes.

Durante a inicialização do LSP, o LSP deve fornecer ponteiros para várias funções spi (Interface do Provedor de Serviços) winsock. Essas funções serão chamadas durante o processamento normal pela camada diretamente acima do LSP (outro LSP ou Ws2 \_32.DLL).

É possível definir categorias LSP com base no subconjunto de funções SPI que um LSP implementa e a natureza do processamento extra executado para cada uma dessas funções. Ao classificar LSPs, bem como classificar aplicativos que usam soquetes Winsock, torna-se possível determinar seletivamente se um LSP deve estar envolvido em um determinado processo em runtime.

No Windows Vista e posterior, um novo método é fornecido para categorizar provedores de serviços em camadas winsock e aplicativos para que apenas determinados LSPs sejam carregados. Há vários motivos para adicionar esses recursos.

Um dos principais motivos é que determinados processos críticos do sistema, como winlogon e lsass, criam soquetes, mas esses processos não usam esses soquetes para enviar tráfego na rede. Portanto, a maioria dos LSPs não deve ser carregada nesses processos. Vários casos também foram documentados em que LSPs com bug podem causar *lsass.exe* falha. Se lsass falhar, o sistema força um desligamento. Um efeito colateral desses processos do sistema que carregaM LSPs é que esses processos nunca saem, portanto, quando um LSP é instalado ou removido, uma reinicialização é necessária.

Um motivo secundário é que há alguns casos em que os aplicativos podem não querer carregar determinados LSPs. Por exemplo, alguns aplicativos podem não querer carregar LSPs criptográficos, o que pode impedir que o aplicativo se comunique com outros sistemas que não têm o LSP ciptográfico instalado.

Por fim, as categorias LSP podem ser usadas por outros LSPs para determinar onde na cadeia de protocolo Winsock eles devem se instalar. Por anos, vários desenvolvedores de LSP quiseram uma maneira de saber como um LSP se comportará. Por exemplo, um LSP que inspeciona o fluxo de dados gostaria de estar acima de um LSP que criptografa os dados. É claro que esse método de categorização LSP não é uma prova de engano, pois se baseia em LSPs de terceiros para categorizar-se adequadamente.

A categorização do LSP e outras melhorias de segurança no Windows Vista e posteriores são projetadas para ajudar a impedir que os usuários instalem LSPs mal-intencionados involuções.

## <a name="lsp-categories"></a>Categorias LSP

No Windows Vista e posterior, um LSP pode ser classificado com base em como ele interage com Windows soquetes e dados. Uma categoria de LSP é um grupo identificável de comportamentos em um subconjunto de funções spi winsock. Por exemplo, um filtro de conteúdo HTTP seria categorizado como um inspetor de dados (a categoria LSP \_ INSPECTOR). A categoria LSP \_ INSPECTOR inspecionará (mas não alterará) parâmetros para funções SPI de transferência de dados. Um aplicativo pode consultar a categoria de um LSP e optar por não carregar o LSP com base na categoria LSP e no conjunto de categorias LSP permitidas do aplicativo.

A tabela a seguir lista as categorias em que um LSP pode ser classificado.

| Categoria LSP              | Descrição                                                     |
|---------------------------|-----------------------------------------------------------------|
| **COMPACTAÇÃO DE \_ CRIPTOGRAFIA \_ LSP** | O LSP é um provedor de criptografia ou compactação de dados.         |
| **FIREWALL do LSP \_**         | O LSP é um provedor de firewall.                                 |
| **CACHE \_ LOCAL do LSP \_**     | O LSP é um provedor de cache local.                              |
| **LSP \_ INBOUND \_ MODIFY**  | O LSP modifica os dados de entrada.                                  |
| **INSPETOR do \_ LSP**        | O LSP inspeciona ou filtra dados.                               |
| **LSP \_ OUTBOUND \_ MODIFY** | O LSP modifica os dados de saída.                                 |
| **LSP \_ PROXY**            | O LSP atua como um proxy e redireciona pacotes.                  |
| **REDIRECIONADOR \_ LSP**       | O LSP é um redirecionador de rede.                                |
| **LSP \_ SYSTEM**           | O LSP é aceitável para uso em serviços e processos do sistema. |



 

Um LSP pode pertencer a mais de uma categoria. Por exemplo, um LSP de firewall/segurança pode pertencer às categorias inspetor (**LSP \_ INSPECTOR**) e firewall (**\_ FIREWALL do LSP**).

Se um LSP não tiver uma categoria definida, ele será considerado na categoria Todos os Outros. Essa categoria LSP não será carregada em serviços ou processos do sistema (por exemplo, lsass, winlogon e muitos processos svchost).

## <a name="categorizing-lsps"></a>Categorizando LSPs

Várias novas funções estão disponíveis no Windows Vista e posterior para categorizar um LSP:

-   [**WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo)
-   [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32)
-   [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo)
-   [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32)

Para categorizar um LSP, a função [**WSCSetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo) ou [**WSCSetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetproviderinfo32) é chamada com um GUID para identificar a entrada oculta do LSP, a classe de informações a ser definida para essa entrada de protocolo LSP e um conjunto de sinalizadores usados para modificar o comportamento da função.

A [**função WSCGetProviderInfo**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo) ou [**WSCGetProviderInfo32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetproviderinfo32) é usada da mesma forma para recuperar os dados associados a uma classe de informações para um LSP.

## <a name="categorizing-applications"></a>Categorizando aplicativos

Várias novas funções estão disponíveis no Windows Vista e posterior para categorizar um aplicativo:

-   [**WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory)
-   [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory)

Para categorizar um aplicativo, a função [**WSCSetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscsetapplicationcategory) é chamada com o caminho de carregamento para a imagem executável para identificar o aplicativo, os argumentos de linha de comando usados ao iniciar o aplicativo e as categorias LSP que são permitidas para todas as instâncias desse aplicativo.

A [**função WSCGetApplicationCategory**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscgetapplicationcategory) é usada da mesma forma para recuperar as categorias de LSP (provedor de serviços em camadas) associadas a um aplicativo.

## <a name="determining-which-lsps-get-loaded"></a>Determinando quais LSPs são carregados

A parte final da categorização LSP é determinar quais LSPs serão carregados em quais processos. Quando um processo carrega o Winsock, as seguintes comparações são feitas da categoria de aplicativo e das categorias LSP para todos os LSPs instalados:

-   Se o aplicativo não for categorizado, permita que todos os LSPs sejam carregados no processo.
-   Se o aplicativo e o LSP têm categorias atribuídas, todas as seguintes condições devem ser verdadeiras: <dl> Pelo menos uma das categorias LSP está presente nas categorias especificadas do aplicativo.  
    Somente as categorias especificadas nas categorias especificadas do aplicativo são especificadas nas categorias LSPs. Por exemplo, se o aplicativo especificar uma categoria, ele deverá estar na categoria do LSP.  
    Se a categoria SISTEMA LSP estiver presente na categoria do aplicativo, ela deverá estar presente nas \_ categorias do LSP.  
    </dl>

> [!Note]  
> Se um LSP não for categorizado, sua categoria será efetivamente zero. Para que uma combinação ocorra, todas as categorias especificadas do LSP devem estar presentes nas categorias do aplicativo (as categorias do aplicativo devem ser um superconjunto das categorias do LSP) com a advertência de que, se o LSP SYSTEM estiver presente na categoria do aplicativo, ele também deverá estar presente na categoria do \_ LSP.

 

Considere o seguinte exemplo:

O *Foo.exe* aplicativo é categorizado como LSP \_ SYSTEM + LSP FIREWALL + \_ LSP CRYPTO \_ \_ COMPRESS. O aplicativo *Bar.exe* é categorizado como FIREWALL LSP \_ + LSP CRYPTO \_ \_ COMPRESS. Há quatro LSPs instalados no sistema:

-   O LSP1 definiu uma categoria de LSP \_ SYSTEM.
-   LSP2 não é categorias definidas, portanto, sua categoria é zero.
-   O LSP3 definiu uma categoria de FIREWALL do \_ LSP.
-   O LSP4 definiu categorias de \_ LSP SYSTEM + FIREWALL LSP \_ + LSP \_ CRYPTO \_ COMPRESS + \_ LSP INSPECTOR

Neste exemplo, o *Foo.exe* único carregaria LSP1, enquanto oBar.exe *aplicativo* carregaria OSP3.

## <a name="determining-winsock-providers-installed"></a>Determinando provedores Winsock instalados

O SDK (Software Development Kit) do Microsoft Windows inclui um programa Winsock de exemplo que pode ser usado para determinar os provedores de transporte Winsock instalados em um computador local. Por padrão, o código-fonte deste exemplo winsock é instalado no seguinte diretório do SDK do Windows para Windows 7:

*C: \\ Arquivos de Programas SDKs da Microsoft Windows \\ \\ \\ exemplos v7.0 \\ \\ NetDs \\ winsock \\ LSP*

Este exemplo é um utilitário para instalar e testar provedores de serviços em camadas. Mas também pode ser usado para coletar programaticamente informações detalhadas do catálogo winsock em um computador local. Para listar todos os provedores Winsock atuais, incluindo provedores base e provedores de serviços de camada, crie este exemplo winsock e execute o seguinte comando de console:

**instlsp -p**

A saída será uma lista de provedores Winsock instalados no computador local, incluindo provedores de serviços em camadas. A saída lista a ID do catálogo e o nome da cadeia de caracteres para o provedor Winsock

Para coletar informações mais detalhadas sobre todos os provedores Winsock, execute o seguinte comando de console:

**instlsp -p -v**

A saída será uma lista de [**estruturas de INFORMAÇÕES WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) com suporte no computador local.

Para uma lista de apenas provedores de serviços em camadas instalados no computador local, execute o seguinte comando de console:

**instlsp -l**

Para mapear a estrutura LSP, execute o seguinte comando de console:

**instlsp -m**

> [!Note]  
> O recurso TDI foi preterido e será removido em versões futuras do Microsoft Windows. Dependendo de como você usa o TDI, use o WSK (Winsock Kernel) ou o WFP (Windows Filtering Platform). Para obter mais informações sobre WFP e WSK, [consulte Windows Filtering Platform e](../fwp/windows-filtering-platform-start-page.md) [Winsock Kernel](/windows-hardware/drivers/ddi/_netvista/). Para uma Windows blog do Windows Core Networking sobre WSK e TDI, consulte [Introdução ao WSK (Kernel winsock).](/archive/blogs/wndp/)

 

 

 
