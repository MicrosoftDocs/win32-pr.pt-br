---
description: O SCM (gerenciador de controle de serviço) é iniciado na inicialização do sistema. É um servidor RPC (chamada de procedimento remoto), para que os programas de configuração de serviço e controle de serviço possam manipular serviços em máquinas remotas.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Gerenciador de Controle de Serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d37d651a96f9685fa82b5ea92ebb3a0b72d80bfc62cd0db80729ec1cb95acc45
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889029"
---
# <a name="service-control-manager"></a>Gerenciador de Controle de Serviço

O SCM (gerenciador de controle de serviço) é iniciado na inicialização do sistema. É um servidor RPC (chamada de procedimento remoto), para que os programas de configuração de serviço e controle de serviço possam manipular serviços em máquinas remotas.

As funções de serviço fornecem uma interface para as seguintes tarefas executadas pelo SCM:

-   Manutenção do banco de dados de serviços instalados.
-   Iniciando serviços e serviços de driver na inicialização do sistema ou sob demanda.
-   Enumerando serviços instalados e serviços de driver.
-   Manter informações de status para executar serviços e serviços de driver.
-   Transmissão de solicitações de controle para serviços em execução.
-   Bloqueio e desbloqueio do banco de dados de serviço.

As seções a seguir descrevem o SCM mais detalhadamente:

-   [Banco de dados de serviços instalados](database-of-installed-services.md)
-   [Iniciando automaticamente os serviços](automatically-starting-services.md)
-   [Iniciando serviços sob demanda](starting-services-on-demand.md)
-   [Lista de registros de serviço](service-record-list.md)
-   [Alças SCM](scm-handles.md)

 

 



