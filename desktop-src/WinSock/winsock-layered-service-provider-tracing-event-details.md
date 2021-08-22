---
description: Detalhes de rastreamento de alterações do catálogo winsock
ms.assetid: 4C86618D-4E79-486E-997F-9E2509FBF6B6
title: Detalhes de rastreamento de alterações do catálogo winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae8d949caf94d3b7bbbef32945c97cb3f1db258f798b84280570712ef5299cd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051334"
---
# <a name="winsock-catalog-change-tracing-details"></a>Detalhes de rastreamento de alterações do catálogo winsock

> [!Note]  
> Provedores de serviços em camadas foram preterido. Começando com Windows 8 e Windows Server 2012, use [Windows De filtragem.](../fwp/windows-filtering-platform-start-page.md)

 

O rastreamento de eventos de Alteração do Catálogo winsock para LSPs (provedores de serviços em camadas) está relacionado à instalação do LSP, remoção de LSP, desabilitação de LSP e operações de redefinição de catálogo winsock. Todos os eventos a seguir são gravados no canal *Microsoft-Windows-Winsock-WS2HELP/Operational,* que é diferente do outro rastreamento de eventos de rede Winsock registrado no Windows Vista e posterior.

Os detalhes a seguir detalham cada um dos eventos do Winsock LSP que podem ser rastreados e descreve quais parâmetros e informações são registrados.

## <a name="lsp-install"></a>Instalação do LSP

ID do evento = 1

Nível = 4 (Informações)

Os seguintes eventos do Winsock LSP são rastreados para uma operação de instalação do LSP:

-   Uma entrada de protocolo é instalada no catálogo winsock.

Os seguintes parâmetros são registrados em um evento de instalação do LSP:



| Parâmetro                                                                                                | Descrição                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome LSP<br/>     | O nome do LSP conforme obtido do membro **szProtocol** da estrutura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo instalado.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo<br/>         | O catálogo winsock (32 bits ou 64 bits) em que o LSP está sendo instalado. Esse é um valor inteiro que é 32 ou 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador<br/> | O nome do arquivo do módulo do aplicativo que está fazendo a chamada de instalação do LSP.<br/>                                                                                          |
| <span id="GUID"></span><span id="guid"></span>Guid<br/>                                            | O valor de GUID do provedor de transporte Winsock no que o LSP está sendo instalado.<br/>                                                                      |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria<br/>     | O **membro dwCatalogEntryId** da estrutura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo instalado.<br/>                                |



 

## <a name="lsp-uninstall"></a>Desinstalação do LSP

ID do evento = 2

Nível = 4 (Informações)

Os seguintes eventos winsock LSP são rastreados para uma operação de desinstalação do LSP:

-   Uma entrada de protocolo é removida do catálogo Winsock.

Os seguintes parâmetros são registrados para um evento de desinstalação do LSP:



| Parâmetro                                                                                                | Descrição                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome LSP<br/>     | O nome do LSP conforme obtido do membro **szProtocol** da estrutura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo removido.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo<br/>         | O catálogo winsock (32 bits ou 64 bits) em que o LSP está sendo removido. Esse é um valor inteiro que é 32 ou 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador<br/> | O nome do arquivo do módulo do aplicativo que está fazendo a chamada de remoção do LSP.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>Guid<br/>                                            | O valor guid do provedor de transporte Winsock do que o LSP é removido.<br/>                                                                             |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria<br/>     | O **membro dwCatalogEntryId** da estrutura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo removido.<br/>                                |



 

## <a name="lsp-disable"></a>Desabilitar LSP

ID do evento = 3

Nível = 4 (Informações)

Os seguintes eventos winsock LSP são rastreados para uma operação de desabilitação de LSP:

-   Uma entrada de protocolo está desabilitada no catálogo winsock.

Os seguintes parâmetros são registrados para um evento de desabilitação do LSP:



| Parâmetro                                                                                                | Descrição                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LSP_Name"></span><span id="lsp_name"></span><span id="LSP_NAME"></span>Nome LSP<br/>     | O nome do LSP conforme obtido do membro **szProtocol** da estrutura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo desabilitado.<br/> |
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo<br/>         | O catálogo winsock (32 bits ou 64 bits) em que o LSP está sendo desabilitado. Esse é um valor inteiro que é 32 ou 64.<br/>                                   |
| <span id="Installer"></span><span id="installer"></span><span id="INSTALLER"></span>Instalador<br/> | O nome do arquivo do módulo do aplicativo que está fazendo com que o LSP desabilite a chamada.<br/>                                                                                         |
| <span id="GUID"></span><span id="guid"></span>Guid<br/>                                            | O valor guid do provedor de transporte Winsock em que o LSP está sendo desabilitado.<br/>                                                                           |
| <span id="Category"></span><span id="category"></span><span id="CATEGORY"></span>Categoria<br/>     | O **membro dwCatalogEntryId** da estrutura [**WSAPROTOCOL \_ INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) para o LSP que está sendo desabilitado.<br/>                                |



 

## <a name="winsock-catalog-reset"></a>Redefinição do catálogo winsock

ID do evento = 4

Nível = 4 (Informações)

Os seguintes eventos winsock LSP são rastreados para uma operação de redefinição de catálogo winsock:

-   O catálogo winsock é redefinido.

Os seguintes parâmetros são registrados em um evento de redefinição de catálogo winsock:



| Parâmetro                                                                                        | Descrição                                                                                                              |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span id="Catalog"></span><span id="catalog"></span><span id="CATALOG"></span>Catálogo<br/> | O catálogo winsock (32 bits ou 64 bits) que está sendo redefinido. Esse é um valor inteiro que é 32 ou 64.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controle do rastreamento winsock](control-of-winsock-tracing.md)
</dt> <dt>

[Rastreamento winsock](winsock-tracing.md)
</dt> <dt>

[Níveis de rastreamento winsock](winsock-tracing-levels.md)
</dt> <dt>

[Detalhes do rastreamento de eventos do Winsock Network](winsock-tracing-event-details.md)
</dt> </dl>

 

 
