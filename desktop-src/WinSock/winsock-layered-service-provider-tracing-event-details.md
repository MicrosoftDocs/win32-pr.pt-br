---
description: Detalhes de rastreamento de alteração do catálogo Winsock
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Detalhes de rastreamento de alteração do catálogo Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6258ca87d5d1fba2de9364e5524110bb43c76513
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090998"
---
# <a name="winsock-catalog-change-tracing-details"></a>Detalhes de rastreamento de alteração do catálogo Winsock

> [!Note]  
> Os provedores de serviço em camadas são preteridos. A partir do Windows 8 e do Windows Server 2012, use a [plataforma de filtragem do Windows](../fwp/windows-filtering-platform-start-page.md).

 

O rastreamento de eventos de alteração do catálogo Winsock para provedores de serviço em camadas (LSPs) está relacionado à instalação de LSP, remoção de LSP, desabilitação de LSP e operações de redefinição de catálogo Winsock. Todos os eventos a seguir são gravados no canal *Microsoft-Windows-Winsock-WS2HELP/Operational* que é diferente do outro rastreamento de eventos de rede do Winsock registrado no Windows Vista e posterior.

Os detalhes a seguir são cada um dos eventos LSP Winsock que podem ser rastreados e descreve quais parâmetros e informações são registrados.

## <a name="lsp-install"></a>Instalação de LSP

ID do evento = 1

Nível = 4 (informações)

Os seguintes eventos de LSP do Winsock são rastreados para uma operação de instalação de LSP:

-   Uma entrada de protocolo é instalada no catálogo do Winsock.

Os seguintes parâmetros são registrados em log para um evento de instalação de LSP:



| Parâmetro                                                                                                | Descrição                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome do LSP<br/>     | O nome do LSP obtido do membro **szProtocol** da estrutura de informações do [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo instalado.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog<br/>         | O catálogo do Winsock (32 bits ou 64 bits) em que o LSP está sendo instalado. Este é um valor inteiro que é 32 ou 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador<br/> | O nome de arquivo do módulo do aplicativo que faz a chamada de instalação de LSP.<br/>                                                                                          |
| <span id="GUID"></span><span id="guid"></span>VOLUME<br/>                                            | O valor de GUID do provedor de transporte do Winsock no qual o LSP está sendo instalado.<br/>                                                                      |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categorias<br/>     | O membro **dwCatalogEntryId** da estrutura [**de \_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo instalado.<br/>                                |



 

## <a name="lsp-uninstall"></a>Desinstalação de LSP

ID do evento = 2

Nível = 4 (informações)

Os seguintes eventos de LSP do Winsock são rastreados para uma operação de desinstalação de LSP:

-   Uma entrada de protocolo é removida do catálogo Winsock.

Os seguintes parâmetros são registrados em log para um evento de desinstalação de LSP:



| Parâmetro                                                                                                | Descrição                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome do LSP<br/>     | O nome do LSP obtido do membro **szProtocol** da estrutura de informações do [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo removido.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog<br/>         | O catálogo Winsock (32 bits ou 64 bits) em que o LSP está sendo removido. Este é um valor inteiro que é 32 ou 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador<br/> | O nome de arquivo do módulo do aplicativo que faz a chamada de remoção de LSP.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>VOLUME<br/>                                            | O valor de GUID do provedor de transporte do Winsock do qual o LSP foi removido.<br/>                                                                             |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categorias<br/>     | O membro **dwCatalogEntryId** da estrutura [**de \_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo removido.<br/>                                |



 

## <a name="lsp-disable"></a>Desabilitação de LSP

ID do evento = 3

Nível = 4 (informações)

Os seguintes eventos de LSP do Winsock são rastreados para uma operação de desabilitação de LSP:

-   Uma entrada de protocolo está desabilitada no catálogo do Winsock.

Os seguintes parâmetros são registrados em log para um evento de desabilitação de LSP:



| Parâmetro                                                                                                | Descrição                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome do LSP<br/>     | O nome do LSP obtido do membro **szProtocol** da estrutura de informações do [**WSAPROTOCOL \_**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo desabilitado.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog<br/>         | O catálogo Winsock (32 bits ou 64 bits) em que o LSP está sendo desabilitado. Este é um valor inteiro que é 32 ou 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador<br/> | O nome de arquivo do módulo do aplicativo que faz a chamada de desabilitação de LSP.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>VOLUME<br/>                                            | O valor de GUID do provedor de transporte do Winsock em que o LSP está sendo desabilitado.<br/>                                                                           |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categorias<br/>     | O membro **dwCatalogEntryId** da estrutura [**de \_ informações do WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo desabilitado.<br/>                                |



 

## <a name="winsock-catalog-reset"></a>Redefinição de catálogo do Winsock

ID do evento = 4

Nível = 4 (informações)

Os seguintes eventos de LSP do Winsock são rastreados para uma operação de redefinição de catálogo do Winsock:

-   O catálogo do Winsock é redefinido.

Os seguintes parâmetros são registrados em log para um evento de redefinição de catálogo do Winsock:



| Parâmetro                                                                                        | Descrição                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catalog<br/> | O catálogo do Winsock (32 bits ou 64 bits) que está sendo redefinido. Este é um valor inteiro que é 32 ou 64.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controle do rastreamento do Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Rastreamento de Winsock](winsock-tracing.md)
</dt> <dt>

[Níveis de rastreamento do Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalhes de rastreamento de eventos de rede do Winsock](winsock-tracing-event-details.md)
</dt> </dl>

 

 
