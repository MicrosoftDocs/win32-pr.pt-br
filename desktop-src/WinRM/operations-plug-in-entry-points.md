---
title: Pontos de entrada de plug-in de operações
description: Pontos de entrada de plug-in de operações
ms.assetid: 9a3ddc2b-9fde-4915-b0e8-0a5e79e73c00
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0834363c7447bc50269da09d361e630d9bc0615a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454072"
---
# <a name="operations-plug-in-entry-points"></a>Pontos de entrada de plug-in de operações

Um plug-in de operações precisa implementar determinados pontos de entrada dependendo dos recursos aos quais deseja dar suporte.

Um plug-in deve se registrar no Serviço Gerenciamento Remoto do Windows (WinRM), que contém os nomes dos pontos de entrada da DLL de plug-in. Todas as operações têm pontos de entrada DLL predefinidos que devem ser expostos se houver suporte para essa operação.

A tabela a seguir fornece uma visão geral dos pontos de entrada de plug-in de operações na API de plug-in do WinRM.



| Função                                                                                 | Descrição                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_comando de plug-in do WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command)                                   | Define o retorno de chamada do comando para um plug-in.<br/> Todos os plug-ins do WinRM que dão suporte a recursos do Shell precisam implementar esse retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginCommand**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_command).<br/> |
| [**\_conexão de plug-in WSMan \_**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect)                                   | Define o retorno de chamada de conexão para um plug-in.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginConnect**](/windows/desktop/api/WsMan/nc-wsman-wsman_plugin_connect).<br/>                                                                                                |
| [**\_recebimento de plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive)                                   | Define o retorno de chamada de recebimento para um plug-in.<br/> Todos os plug-ins do WinRM que dão suporte a recursos do Shell precisam implementar esse retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginReceive**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_receive).<br/> |
| [**\_contexto do \_ comando de liberação do plug-in WSMan \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context) | Define o retorno de chamada do comando de liberação para o plug-in.<br/> O nome do ponto de entrada da DLL deve ser [**WSManPluginReleaseCommandContext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context).<br/>                                                                        |
| [**\_contexto do \_ Shell de liberação do plugin do WSMan \_ \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_shell_context)     | Define o retorno de chamada do Shell de liberação para o plug-in.<br/> O nome do ponto de entrada da DLL deve ser [**WSManPluginReleaseCommandContext**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_release_command_context).<br/>                                                                          |
| [**\_envio de plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send)                                         | Define o retorno de chamada de envio para um plug-in.<br/> Todos os plug-ins do WinRM que dão suporte a recursos do Shell precisam implementar esse retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginSend**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_send).<br/>          |
| [**\_Shell de plug-in do WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell)                                       | Define o retorno de chamada do Shell para um plug-in.<br/> Todos os plug-ins do WinRM que dão suporte a recursos do Shell precisam implementar esse retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginShell**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shell).<br/>       |
| [**\_desligamento de plug-in WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown)                                 | Define o retorno de chamada de desligamento para o plug-in.<br/> Todos os plug-ins do WinRM devem implementar essa função de retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginShutdown**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_shutdown).<br/>                      |
| [**\_sinal de plug-in do WSMan \_**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal)                                     | Define o retorno de chamada de sinal para um plug-in.<br/> Todos os plug-ins do WinRM que dão suporte a recursos do Shell precisam implementar esse retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginSignal**](/windows/win32/api/wsman/nc-wsman-wsman_plugin_signal).<br/>    |
| [**\_inicialização do plug-in do WSMan \_**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup)                                   | Define o retorno de chamada de inicialização para o plug-in.<br/> Todos os plug-ins do WinRM devem implementar essa função de retorno de chamada.<br/> O nome do ponto de entrada da DLL para esse método deve ser [**WSManPluginStartup**](/windows/desktop/api/Wsman/nc-wsman-wsman_plugin_startup).<br/>                         |



 

 

