---
description: O SCM (Gerenciador de controle de serviço) é iniciado na inicialização do sistema. É um servidor RPC (chamada de procedimento remoto), para que os programas de configuração de serviço e de controle de serviço possam manipular serviços em máquinas remotas.
ms.assetid: 56ad011d-17c4-4410-b598-6ef47fb3638f
title: Gerenciador de Controle de Serviço
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8a35fd34bd2714d22d40ccf618c89a8b66a6c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771810"
---
# <a name="service-control-manager"></a>Gerenciador de Controle de Serviço

O SCM (Gerenciador de controle de serviço) é iniciado na inicialização do sistema. É um servidor RPC (chamada de procedimento remoto), para que os programas de configuração de serviço e de controle de serviço possam manipular serviços em máquinas remotas.

As funções de serviço fornecem uma interface para as seguintes tarefas executadas pelo SCM:

-   Manutenção do banco de dados dos serviços instalados.
-   Inicialização de serviços e serviços de driver na inicialização do sistema ou sob demanda.
-   Enumerando serviços instalados e serviços de driver.
-   Manutenção de informações de status para a execução de serviços e serviços de driver.
-   Transmissão de solicitações de controle para a execução de serviços.
-   Bloqueando e desbloqueando o banco de dados de serviço.

As seções a seguir descrevem o SCM mais detalhadamente:

-   [Banco de dados dos serviços instalados](database-of-installed-services.md)
-   [Iniciando serviços automaticamente](automatically-starting-services.md)
-   [Iniciando serviços sob demanda](starting-services-on-demand.md)
-   [Lista de registros de serviço](service-record-list.md)
-   [Identificadores SCM](scm-handles.md)

 

 



