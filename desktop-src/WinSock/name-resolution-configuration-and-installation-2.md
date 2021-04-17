---
description: Para que um provedor de namespace possa ser acessado por meio do Windows Sockets, ele deve ser instalado corretamente no sistema e registrado com o Windows Sockets.
ms.assetid: c73baf62-b862-476c-b381-be00699e78ca
title: Configuração e instalação da resolução de nomes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 423e0ca7c9c5290a040a17e0f1ded2a97a1aed15
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789929"
---
# <a name="name-resolution-configuration-and-installation"></a>Configuração e instalação da resolução de nomes

Para que um provedor de namespace possa ser acessado por meio do Windows Sockets, ele deve ser instalado corretamente no sistema e registrado com o Windows Sockets. Quando um provedor de namespace é instalado invocando o programa de instalação de um fornecedor, as informações de configuração devem ser adicionadas a um banco de dados de configuração para fornecer ao Ws2 \_32.dll informações necessárias sobre o provedor de serviços. O ws2 \_32.dll exporta [**WSCInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace) para o programa de instalação do fornecedor usar. Essa função é usada para fornecer informações relevantes sobre o provedor de serviços a ser instalado. Essas informações incluem:

-   Nome do provedor — uma cadeia de caracteres que representa o provedor para exibição no painel de controle.
-   Versão do provedor — a versão deste provedor.
-   Caminho do provedor — um nome de caminho para a DLL do provedor.
-   Namespace — o namespace com suporte no provedor.
-   GUID do provedor — um número exclusivo fornecido pelo fornecedor que representa essa combinação de provedor/namespace. Isso é usado como uma chave para todas as referências subsequentes para esse provedor e para a desinstalação. Esses valores são criados usando o utilitário Uuidgen.exe.
-   Armazena todos os sinalizadores — um sinalizador que indica se este provedor de namespace será responsável por reter todas as informações de esquema de classe de serviço para todas as classes de serviço. Se esse provedor existir, o32.dll Ws2 \_ não precisará consultar cada provedor de namespace individual para obter essas informações.

No Windows Vista e posterior, é fornecida uma função [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) avançada que permite que o provedor de namespace transmita um blob adicional de dados específicos para o namespace.

Em plataformas de 64 bits, as funções [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) e [**WSCInstallNameSpaceEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespaceex32) semelhantes são fornecidas para instalar um namespace no catálogo de 32 bits.

O \_32.dll Ws2 também fornece uma função, [**WSCUnInstallNameSpace**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscuninstallnamespace), para o programa de desinstalação de um fornecedor para remover todas as informações relevantes do banco de dados de configuração. O local exato e o formato dessas informações de configuração são privados para o \_32.dll Ws2 e só podem ser manipulados pelas funções mencionadas acima.

Em plataformas de 64 bits, uma função [**WSCInstallNameSpace32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscinstallnamespace32) semelhante é fornecida para desinstalar um namespace no catálogo de 32 bits.

A qualquer momento, um provedor de namespace é considerado ativo ou inativo, com essa configuração controlada por meio das funções [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) e [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) . Provedores de namespace que estão inativos continuam a aparecer quando enumerados (usando as funções [**WSAEnumNameSpaceProviders**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa), [**WSAEnumNameSpaceProvidersEx**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa), [**WSCEnumNameSpaceProviders32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceproviders32)e [**WSCEnumNameSpaceProvidersEx32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumnamespaceprovidersex32) ), mas o ws2 \_32.dll não roteará nenhuma consulta ou operações de registro de serviço para esses provedores. Esse recurso pode ser útil em situações em que mais de um dos provedores de namespaces instalados pode dar suporte a um namespace específico.

Quando vários provedores de namespace são referenciados em uma única função de API, a ordem na qual as operações de consultas e de registro são roteadas para provedores de namespace não é especificada. A ordem não está relacionada à ordem na qual os provedores de namespace são instalados. Há duas maneiras de controlar quais provedores de namespace são usados para resolver uma consulta de nome. Primeiro, as funções [**WSCEnableNSProvider**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider) e [**WSCEnableNSProvider32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenablensprovider32) podem ser usadas para habilitar e desabilitar namespaces de forma persistente em todo o computador. Em segundo lugar, os aplicativos podem direcionar uma consulta individual para um provedor específico especificando o GUID de identificação do provedor como parte da consulta.

 

 



