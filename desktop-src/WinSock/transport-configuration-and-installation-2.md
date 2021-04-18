---
description: Para que um protocolo de transporte seja acessível por meio do Windows Sockets, ele deve ser instalado corretamente no sistema e registrado com o Windows Sockets.
ms.assetid: 0f0b22e4-81b7-43a7-bc2f-7124fa32d925
title: Configuração e instalação de transporte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea980740f727e39338c7568f4cc30a961b5484df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105764501"
---
# <a name="transport-configuration-and-installation"></a>Configuração e instalação de transporte

Para que um protocolo de transporte seja acessível por meio do Windows Sockets, ele deve ser instalado corretamente no sistema e registrado com o Windows Sockets. Quando um provedor de serviço de transporte é instalado invocando o programa de instalação de um fornecedor, as informações de configuração devem ser adicionadas a um banco de dados de configuração para fornecer ao Ws2 \_32.dll informações necessárias sobre o provedor de serviços. O ws2 \_32.dll exporta várias funções de instalação, [**WSCInstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider) e [**WSCInstallProviderAndChains**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains), para o programa de instalação do fornecedor fornecer as informações relevantes sobre o provedor de serviços a ser instalado. Essas informações incluem, por exemplo, o nome e o caminho para a DLL do provedor de serviço e uma lista de estruturas de [**\_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) às quais esse provedor pode dar suporte. O \_32.dll Ws2 também fornece uma função, [**WSCDeinstallProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider), para o programa de desinstalação de um fornecedor para remover todas as informações relevantes do banco de dados de configuração mantidas pelo32.dll de ws2 \_ . O local exato e o formato dessas informações de configuração são privados para o \_32.dll Ws2 e só podem ser manipulados pelas funções mencionadas acima.

Em plataformas de 64 bits, há funções semelhantes que operam em catálogos de 32 bits e de 64 bits. Essas funções incluem [**WSCInstallProvider64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallprovider64_32), [**WSCInstallProviderAndChains64 \_ 32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallproviderandchains64_32)e [**WSCDeinstallProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscdeinstallprovider32).

A ordem na qual os provedores de serviço de transporte são instalados inicialmente controla a ordem na qual eles são enumerados por meio de [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols) e [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) na interface do provedor de serviço ou por meio de [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) na interface do aplicativo. O mais importante é que essa ordem também governa a ordem em que os protocolos e provedores de serviço são considerados quando um cliente solicita a criação de um soquete com base em sua família de endereços, tipo e identificador de protocolo. O Windows Sockets 2 inclui um applet chamado Sporder.exe que permite que o catálogo de protocolos instalados seja reordenado interativamente depois que os protocolos já tiverem sido instalados. O Windows Sockets 2 também inclui uma DLL auxiliar, Sporder.dll, que exporta uma interface de procedimento para reordenar protocolos. Essa interface de procedimento consiste em um único procedimento chamado [**WSCWriteProviderOrder**](/windows/desktop/api/Sporder/nf-sporder-wscwriteproviderorder).

## <a name="installing-layered-protocols-and-protocol-chains"></a>Instalando protocolos em camadas e cadeias de protocolos

A estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) fornecida com cada protocolo a ser instalado indica se o protocolo é um protocolo base, um protocolo em camadas ou uma cadeia de protocolos. O valor do parâmetro *ProtocolChain. ChainLen* é interpretado conforme mostrado na tabela a seguir.

| Valor | Significado                                           |
|-------|---------------------------------------------------|
| 0     | Protocolo em camadas.                                 |
| 1     | Protocolo base (ou cadeia com apenas um componente). |
| > 1 | Cadeia de protocolos.                                   |



 

A instalação de cadeias de protocolo só pode ocorrer após a instalação bem-sucedida de todos os componentes constituintes (protocolos de base e protocolos em camadas). A estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para uma cadeia de protocolos usa o parâmetro *ProtocolChain* para descrever o comprimento da cadeia e a identidade de cada componente. Os protocolos individuais que compõem uma cadeia são listados em ordem na matriz ProtocolChain. ChainEntries, com o elemento inicial da matriz correspondente ao primeiro provedor em camadas. Os protocolos são identificados por seus valores de *CatalogEntryID* , que são atribuídos pelo Ws2 \_32.dll no momento da instalação do protocolo e podem ser encontrados na estrutura de **\_ informações do WSAPROTOCOL** para cada protocolo.

Os valores para os parâmetros restantes na estrutura de [**\_ informações WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) da cadeia de protocolos devem ser escolhidos para refletir os atributos e identificadores que melhor caracterizam a cadeia de protocolos como um todo. Ao selecionar esses valores, os desenvolvedores devem ter em mente que as comunicações sobre cadeias de protocolos só podem ocorrer quando ambos os pontos de extremidade têm cadeias de protocolos compatíveis instaladas e esses aplicativos devem ser capazes de reconhecer a estrutura de **\_ informações WSAPROTOCOL** correspondente.

Quando um protocolo base é instalado, não é necessário fazer nenhuma entrada na matriz *ProtocolChain. ChainEntries* . Ele é compreendido implicitamente que o único componente dessa cadeia já está identificado no parâmetro *CatalogEntryID* da mesma estrutura de [**\_ informações de WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) . Observe também que as cadeias de protocolos podem não incluir várias instâncias do mesmo protocolo em camadas.

 

 
