---
title: Pontos de entrada do plug-in de operações
description: Pontos de entrada do plug-in de operações
ms.assetid: 9a3ddc2b-9fde-4915-b0e8-0a5e79e73c00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5941746e8e6b952f2f1cd6f21c697398cb4cbb60b024daa557e65151a0a1cfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119412766"
---
# <a name="operations-plug-in-entry-points"></a>Pontos de entrada do plug-in de operações

Um plug-in de operações precisa implementar determinados pontos de entrada, dependendo dos recursos que ele deseja dar suporte.

Um plug-in deve ser registrado com o Windows WinRM (Gerenciamento Remoto), que contém os nomes dos pontos de entrada de DLL do plug-in. Todas as operações têm pontos de entrada de DLL predefinidos que devem ser expostos se há suporte para essa operação.

A tabela a seguir fornece uma visão geral dos pontos de entrada de plug-in de operações na API de plug-in do WinRM.



| Função                                                                                 | Descrição                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**COMANDO \_ PLUG-IN do \_ WSMAN**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)                                   | Define o retorno de chamada de comando para um plug-in.<br/> Todos os plug-ins winRM que suportam recursos de shell precisam implementar esse retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginCommand.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)<br/> |
| [**PLUG-IN DO WSMAN \_ \_ CONNECT**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)                                   | Define o retorno de chamada de conexão para um plug-in.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginConnect.**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)<br/>                                                                                                |
| [**RECEBIMENTO DE \_ PLUG-IN DO \_ WSMAN**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)                                   | Define o retorno de chamada de recebimento para um plug-in.<br/> Todos os plug-ins winRM que suportam recursos de shell precisam implementar esse retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginReceive.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)<br/> |
| [**CONTEXTO DE COMANDO DE VERSÃO DO \_ \_ \_ PLUG-IN DO WSMAN \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context) | Define o retorno de chamada do comando de versão para o plug-in.<br/> O nome do ponto de entrada da DLL deve ser [**WSManPluginReleaseCommandContext.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context)<br/>                                                                        |
| [**CONTEXTO DO SHELL DE VERSÃO \_ \_ DO \_ PLUG-IN DO \_ WSMAN**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_shell_context)     | Define o retorno de chamada do shell de versão para o plug-in.<br/> O nome do ponto de entrada da DLL deve ser [**WSManPluginReleaseCommandContext.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context)<br/>                                                                          |
| [**ENVIO DE \_ PLUG-IN WSMAN \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)                                         | Define o retorno de chamada de envio para um plug-in.<br/> Todos os plug-ins winRM que suportam recursos de shell precisam implementar esse retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginSend.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)<br/>          |
| [**SHELL DE \_ PLUG-IN do WSMAN \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)                                       | Define o retorno de chamada do shell para um plug-in.<br/> Todos os plug-ins winRM que suportam recursos de shell precisam implementar esse retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginShell.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)<br/>       |
| [**DESLIGAMENTO DO \_ PLUG-IN do WSMAN \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)                                 | Define o retorno de chamada de desligamento para o plug-in.<br/> Todos os plug-ins do WinRM devem implementar essa função de retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginShutdown.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)<br/>                      |
| [**SINAL DE \_ PLUG-IN do WSMAN \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)                                     | Define o retorno de chamada de sinal para um plug-in.<br/> Todos os plug-ins winRM que suportam recursos de shell precisam implementar esse retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginSignal.**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)<br/>    |
| [**INICIALIZAÇÃO DO \_ PLUG-IN DO WSMAN \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)                                   | Define o retorno de chamada de inicialização para o plug-in.<br/> Todos os plug-ins do WinRM devem implementar essa função de retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginStartup.**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)<br/>                         |



 

 

