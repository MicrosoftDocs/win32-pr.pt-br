---
title: API de Serviços de Área de Trabalho Remota
description: A API Serviços de Área de Trabalho Remota é principalmente útil para aplicativos cliente/servidor e aplicativos para administração de Serviços de Área de Trabalho Remota.
ms.assetid: 4bd10a15-78d6-4754-9e17-f2576ee8b9d0
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5aa187378625242463ea91151a6961b08d2a77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822510"
---
# <a name="remote-desktop-services-api"></a>API de Serviços de Área de Trabalho Remota

A maioria dos aplicativos é executada sem modificação em um ambiente Serviços de Área de Trabalho Remota (anteriormente conhecido como serviços de terminal) e não precisa usar a API Serviços de Área de Trabalho Remota. A API Serviços de Área de Trabalho Remota é principalmente útil para aplicativos cliente/servidor e aplicativos para administração de Serviços de Área de Trabalho Remota.

A API Serviços de Área de Trabalho Remota é um conjunto de chamadas de função em Wtsapi32.dll. Para criar seu aplicativo para ser executado em ambientes Serviços de Área de Trabalho Remota e não Serviços de Área de Trabalho Remota, use a vinculação dinâmica em tempo de execução para verificar a presença de Wtsapi32.dll. Para obter mais informações, consulte [vinculação de tempo de execução para Wtsapi32.dll](run-time-linking-to-wtsapi32-dll.md).

A API Serviços de Área de Trabalho Remota permite que os aplicativos executem as seguintes tarefas em um ambiente de Serviços de Área de Trabalho Remota:

-   A [Administração de serviços de área de trabalho remota](terminal-services-administration.md), como a enumeração e o gerenciamento de servidores Host da Sessão da Área de Trabalho Remota (host da Sessão RD) (anteriormente conhecidos como servidores de terminal) em um domínio ou a enumeração e o gerenciamento de sessões e processos em um servidor host da Sessão RD.
-   Aprimorando aplicativos cliente/servidor em um ambiente Serviços de Área de Trabalho Remota.
-   Usar [serviços de área de trabalho remota canais virtuais](terminal-services-virtual-channels.md) para se comunicar entre módulos de cliente e de servidor de um aplicativo.
-   [Definir e recuperar serviços de área de trabalho remota informações específicas de configuração do usuário](terminal-services-user-configuration.md).

 

 




