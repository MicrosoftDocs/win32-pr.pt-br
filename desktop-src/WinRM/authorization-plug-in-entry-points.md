---
title: Pontos de entrada de plug-in de autorização
description: Pontos de entrada de plug-in de autorização
ms.assetid: 6cbfa79a-b57b-44b8-a421-d5e79c1b3757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16ca861df6b6546920aaf3f778c61117776ff3861556377b280c990c03711fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118324074"
---
# <a name="authorization-plug-in-entry-points"></a>Pontos de entrada de plug-in de autorização

Os plug-ins de autorização são configurados somente para um processo Serviços de Informações da Internet host (IIS). Somente um plug-in de autorização pode ser configurado por diretório virtual.

Todos os plug-ins de autorização devem dar suporte aos seguintes pontos de entrada:

-   [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)
-   [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)
-   [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)
-   [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)

O seguinte ponto de entrada é opcional:

-   [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)

A tabela a seguir fornece uma visão geral dos pontos de entrada de plug-in de autorização na API de plug-in Windows WinRM (Gerenciamento Remoto).



| Função                                                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OPERAÇÃO DE AUTORIZAÇÃO DO \_ \_ PLUG-IN DO \_ WSMAN**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)              | Chamado para autorizar uma operação específica. <br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginAuthzOperation.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)<br/>                                                                                                                                                                                                       |
| [**COTA DE CONSULTA DE \_ \_ \_ AUTORIZAÇÃO DO PLUG-IN DO WSMAN \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)           | Chamado depois que uma conexão foi autorizada a recuperar informações de cota para o usuário. <br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginAuthzQueryQuota.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)<br/>                                                                                                                                                    |
| [**CONTEXTO DE VERSÃO DE AUTORIZAÇÃO DO \_ \_ \_ PLUG-IN DO \_ WSMAN**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context) | Chamado para liberar o contexto que um plug-in relata dos métodos [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete) ou [**WSManPluginAuthzOperationComplete.**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete) <br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginAuthzReleaseContext**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context).<br/> |
| [**AUTORIZAR USUÁRIO DO \_ \_ PLUG-IN do WSMAN \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)                         | Chamado para determinar se o usuário tem permissão para realizar uma solicitação. <br/> O nome do ponto de entrada da DLL (biblioteca de vínculo dinâmico) para esse método deve ser [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user).<br/>                                                                                                                                                            |



 

 

