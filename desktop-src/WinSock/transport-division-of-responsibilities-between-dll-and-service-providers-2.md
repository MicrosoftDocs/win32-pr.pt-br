---
description: Esta seção fornece uma visão geral da divisão de responsabilidade entre os \_ provedores de serviço de transporte e32.dll de Ws2.
ms.assetid: e1ea1e99-a2bc-4e76-91f6-e388c39dfbbb
title: Divisão de responsabilidades de transporte entre DLL e provedores de serviços
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33c256cb03bcc9e3f8746db5196c21fc2de0a8b157304a205587b275acc0bbb3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733216"
---
# <a name="transport-division-of-responsibilities-between-dll-and-service-providers"></a>Divisão de responsabilidades de transporte entre DLL e provedores de serviços

Esta seção fornece uma visão geral da divisão de responsabilidade entre os \_ provedores de serviço de transporte e32.dll de Ws2.

## <a name="ws2_32dll-functionality-for-transport"></a>Ws2 \_32.dll funcionalidade para transporte

A principal tarefa da parte de transporte de dados do \_32.dll Ws2 é servir como Gerenciador de tráfego entre provedores de serviço e aplicativos. Com vários provedores de serviços diferentes interagindo com o mesmo aplicativo, cada provedor de serviços interage estritamente com o \_32.dll Ws2. A DLL cuida de:

-   Selecionando um provedor de serviços apropriado para criar soquetes com base em uma descrição de protocolo.
-   Encaminhamento de chamadas de procedimento de aplicativo envolvendo um soquete para o provedor de serviços apropriado que criou ou controla esse soquete. Os provedores de serviços não sabem que isso está ocorrendo.

Eles não precisam se preocupar com os detalhes da cooperação entre si ou até mesmo a existência de outros provedores de serviços. Ao abstrair os provedores de serviço em uma interface de DLL consistente e executar essa função de roteamento de tráfego automático, o ws2 \_32.dll permite que os aplicativos interajam com uma variedade de provedores sem exigir que os aplicativos estejam cientes das divisões entre os provedores, onde provedores diferentes são instalados.

O \_32.dll Ws2 se baseia nos parâmetros das funções de criação de soquete de API ( [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) e [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa)) para determinar qual provedor de serviços utilizar. O provedor de serviço de transporte selecionado será invocado por meio da função [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) . No caso da função **Socket** , o ws2 \_32.dll localiza a primeira entrada no conjunto de estruturas de informações de [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) instaladas que corresponde aos valores fornecidos na tupla formada pelos parâmetros (*família de endereços*, tipo de *soquete*, *protocolo*). Para preservar a compatibilidade com versões anteriores, o \_32.dll Ws2 trata o valor de zero para a *família de endereços* ou *tipo de soquete* como um valor curinga. O valor de zero para protocolo não é considerado um valor de curinga pelo \_32.dll Ws2, a menos que esse comportamento seja indicado para um protocolo específico, fazendo com que a PFL \_ corresponda o \_ sinalizador zero de protocolo \_ definido na estrutura de **\_ informações de WSAPROTOCOL** .

Para a função [**WSASocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) , se NULL for fornecido para *lpProtocolInfo*, o comportamento será exatamente o mesmo descrito para [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket). No entanto, se uma estrutura de [**\_ informações WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) for referenciada, o32.dll de ws2 \_ não executará nenhuma função correspondente, mas retransmitirá imediatamente a solicitação de criação de soquete para o provedor de serviços de transporte associado à estrutura de **\_ informações WSAPROTOCOL** indicada. Os valores da tupla (*família de endereços,* *tipo de soquete*) são fornecidos intactos para o provedor de serviços na função [**WSPSocket**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspsocket) . Os provedores de serviço são livres para ignorar ou prestar atenção aos valores dos parâmetros (*família de endereços,* *tipo de soquete),* conforme apropriado, mas não devem indicar uma condição de erro quando o valor da *família de endereços* ou tipo de *soquete* for zero. Além disso, os provedores de serviço não devem indicar uma condição de erro quando a constante de manifesto das \_ informações de protocolo \_ estiver contida em qualquer um dos parâmetros (*família de endereços,* *tipo de soquete*). Esse valor simplesmente indica que o aplicativo deseja usar os valores encontrados nos parâmetros correspondentes da estrutura de **\_ informações de WSAPROTOCOL** : (**iAddressFamily**, **iSocketType**, **iProtocol**).

Como parte da criação de soquetes, um provedor de serviços informa o ws2 \_32.dll sobre a associação entre si mesmo e o novo soquete por meio de parâmetros passados para [**WPUCreateSocketHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpucreatesockethandle) ou [**WPUModifyIFSHandle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpumodifyifshandle). O \_32.dll Ws2 controla essa associação entre identificadores de soquete e provedores de serviço específicos. Sempre que uma função de interface de aplicativo que se refere a um identificador de soquete é chamada, o ws2 \_32.dll pesquisa a associação e chama a função de interface de provedor de serviço correspondente do provedor de serviços apropriado.

Além de seu principal serviço de roteamento de tráfego, o ws2 \_32.dll fornece vários outros serviços, como enumeração de protocolo, gerenciamento de descritor de soquete (alocação, desalocação e Associação de valor de contexto) para provedores de serviço de sistema de arquivos, bloqueando o gerenciamento de gancho por thread, utilitários de troca de bytes, Enfileiramento de chamadas de procedimento assíncronos (APCs) para facilitar a invocação de rotinas de conclusão de e/s e a negociação de versão entre aplicativos e o32.dll de ws2 \_ , bem como entre o ws2 \_32.dll e

## <a name="transport-service-provider-functionality"></a>Funcionalidade do provedor de serviço de transporte

Os provedores de serviço implementam o protocolo de transporte real que inclui funções como configurar conexões, transferir dados, exercer controle de fluxo e controle de erro, etc. O \_32.dll Ws2 não tem conhecimento sobre como as solicitações para provedores de serviço são realizadas; essa é a implementação do provedor de serviços. A implementação dessas funções pode diferir muito de um provedor para outro. Os provedores de serviço ocultam os detalhes específicos da implementação de como as operações de rede são realizadas.

Os provedores de serviço de transporte podem ser amplamente divididos em duas categorias: aqueles cujos descritores de soquete são identificadores de sistema de arquivos reais (e estão daqui em diante como provedores de IFS (sistema de arquivos instaláveis); o restante é conhecido como provedores não IFS. o Ws2 \_32.dll sempre passa o descritor de soquete do provedor de serviço de transporte até o aplicativo Windows sockets, para que os aplicativos sejam livres para aproveitar os descritores de soquete que são identificadores do sistema de arquivos, se escolherem.

Para resumir: os provedores de serviço implementam os protocolos específicos de rede de nível baixo. O \_32.dll Ws2 fornece o gerenciamento de tráfego de nível médio que interconecta esses protocolos de transporte com aplicativos. Os aplicativos, por sua vez, fornecem a política de como esses fluxos de tráfego e operações específicas de rede são usados para realizar as funções desejadas pelo usuário.

 

 
