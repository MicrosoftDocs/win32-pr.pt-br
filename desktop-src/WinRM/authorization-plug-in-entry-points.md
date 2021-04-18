---
title: Pontos de entrada de plug-in de autorização
description: Pontos de entrada de plug-in de autorização
ms.assetid: 6cbfa79a-b57b-44b8-a421-d5e79c1b3757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ee0db76457860106e51bd6c29cead3d0f8227d7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105785197"
---
# <a name="authorization-plug-in-entry-points"></a>Pontos de entrada de plug-in de autorização

Os plug-ins de autorização são configurados apenas para um processo de host Serviços de Informações da Internet (IIS). Somente um plug-in de autorização pode ser configurado por diretório virtual.

Todos os plug-ins de autorização devem dar suporte aos seguintes pontos de entrada:

-   [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)
-   [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)
-   [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)
-   [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)

O seguinte ponto de entrada é opcional:

-   [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota)

A tabela a seguir fornece uma visão geral dos pontos de entrada de plug-in de autorização na API de plug-in do Gerenciamento Remoto do Windows (WinRM).



| Função                                                                                      | Descrição                                                                                                                                                                                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_operação de autorização de plug-in WSMan \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)              | Chamado para autorizar uma operação específica. <br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginAuthzOperation**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation).<br/>                                                                                                                                                                                                       |
| [**\_cota de \_ consulta de autorização de plug-in WSMan \_ \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_operation)           | Chamado depois que uma conexão foi autorizada para recuperar informações de cota para o usuário. <br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginAuthzQueryQuota**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_query_quota).<br/>                                                                                                                                                    |
| [**\_contexto de \_ liberação de autorizar plug-in do \_ WSMan \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context) | Chamado para liberar o contexto que um plug-in relata dos métodos [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete) ou [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete) . <br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginAuthzReleaseContext**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_release_context).<br/> |
| [**\_plug-in do WSMan \_ autorizar \_ usuário**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user)                         | Chamado para determinar se o usuário tem permissão para realizar uma solicitação. <br/> O nome do ponto de entrada da biblioteca de vínculo dinâmico (DLL) para esse método deve ser [**WSManPluginAuthzUser**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_authorize_user).<br/>                                                                                                                                                            |



 

 

