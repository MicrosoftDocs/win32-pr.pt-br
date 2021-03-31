---
title: Extensão do agente de sessão dos serviços de terminal
description: Você pode estender TS \ 160; Agente de sessão usando a interface COM do IWTSSBPlugin.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b84471bcf2125017b8eef273cdb78e61a9bc620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641597"
---
# <a name="extending-terminal-services-session-broker"></a>Extensão do agente de sessão dos serviços de terminal

O agente de sessão dos serviços de terminal (agente de Sessão TS) determina se um usuário que inicia uma conexão já tem uma sessão aberta. Nesse caso, o agente de Sessão TS roteia a conexão de entrada para o servidor de Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) com a sessão existente. Caso contrário, o agente de Sessão TS roteia a conexão de entrada para o servidor de Host da Sessão RD com o menor número de sessões.

Você pode estender o agente de Sessão TS usando a interface com do [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) . Você pode usar essa interface para gerenciar conexões com servidores Host da Sessão RD, bem como qualquer tipo de conexão de protocolo RDP (RDP), por exemplo, conexões com máquinas virtuais convidadas que estejam executando o VECD (Desktop central do Windows Vista Enterprise) em um host de máquina virtual do Windows Server 2008 Hyper-V.

A interface [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) oferece vários benefícios:

-   Não é necessário instalar um agente no cliente ou no servidor de Host da Sessão RD.
-   O plug-in pode interagir diretamente com outros serviços de Serviços de Área de Trabalho Remota função, como o gateway de Área de Trabalho Remota (gateway de área de trabalho remota) e contar com informações do agente de Sessão TS sobre Estados de sessão e de computador.
-   Você pode usar o plug-in para gerenciar conexões com dispositivos cliente ou de servidor que dão suporte a RDP 5,2 ou posterior.
-   Você pode usar o plug-in para habilitar as soluções de área de trabalho do Windows Vista Enterprise central.

Ao implementar os métodos dessa interface, tenha em mente os seguintes pontos:

-   O agente de Sessão TS pode chamar os métodos desse objeto COM de vários threads.
-   Se qualquer um dos métodos chamados não retornar imediatamente e com êxito, o agente de Sessão TS não fará mais chamadas para o plug-in e será revertido para sua lógica de balanceamento de carga nativa. Para retomar as chamadas para o plug-in, você deve reiniciar o serviço de agente de sessão dos serviços de terminal.
-   Você deve registrar o plug-in como um objeto COM em todo o sistema usando Regsvr32.exe. Como o serviço de agente de sessão dos serviços de terminal é executado na conta "NetworkService", você deve conceder à conta "NetworkService" as permissões de inicialização, ativação e acesso necessárias usando Dcomcnfg.exe. O serviço de agente de sessão dos serviços de terminal procura o CLSID do objeto COM que representa o plug-in na seguinte subchave do registro:

    **HKEY \_ \_Computador local** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Tssdis** \\ **Parameters** \\ **ExtensibilityPluginCLSID**

Para obter mais informações sobre Dcomcnfg.exe, consulte [habilitando a segurança com usando DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 