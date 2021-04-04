---
title: Diretrizes para serviços
description: Os serviços devem aderir a essas diretrizes para garantir que o Gerenciador de reinicialização possa desligar e reiniciar os serviços, se necessário, para instalar atualizações. Os aplicativos podem usar as diretrizes descritas em diretrizes para aplicativos.
ms.assetid: 69a98f82-71bb-4780-8a3f-294cc5629900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51374c0a4c6fc561b8259aadf15e3d5487e12483
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007889"
---
# <a name="guidelines-for-services"></a>Diretrizes para serviços

Os serviços devem aderir a essas diretrizes para garantir que o Gerenciador de reinicialização possa desligar e reiniciar os serviços, se necessário, para instalar atualizações. Os aplicativos podem usar as diretrizes descritas em [diretrizes para aplicativos](guidelines-for-applications.md).

-   Os serviços devem ser capazes de serem desligados e reiniciados usando o [Gerenciador de controle de serviço](/windows/desktop/Services/service-control-manager) sem a necessidade de uma reinicialização do sistema. As exceções a essa diretriz são processos críticos do sistema que são executados no contexto de lsass.exe ou services.exe.
-   O Gerenciador de reinicialização honra as dependências de serviço. Quando um serviço é desligado e reiniciado, seus serviços dependentes são desligados e reiniciados.
-   Os serviços devem especificar o intervalo de recuperação e o período de redefinição no [Gerenciador de controle de serviço (SCM)](/windows/desktop/Services/service-control-manager). O intervalo de recuperação é o tempo, em MS, após a última falha que o SCM aguarda antes de realizar a ação de recuperação. O período de redefinição é o tempo, em segundos, após a última falha que o Gerenciador de controle de serviço espera antes de redefinir a contagem de falhas para 0. Os serviços podem usar a função [**ChangeServiceConfig2**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a) para alterar as definições de configuração.

    Os [serviços críticos](critical-system-services.md) devem usar as seguintes configurações de recuperação para especificar que o serviço seja reiniciado um minuto após a primeira falha para reiniciar o serviço, reiniciado dois minutos após a segunda falha e que o computador seja reiniciado um minuto após a terceira falha. A contagem de falhas é redefinida para 0 após 300 segundos.

    <dl> Ações de recuperação: Restart/60000/Restart/120000/reboot/60000 & Reset = 300  
    </dl>

    [Serviços críticos](critical-system-services.md) devem ser iniciados antes de serviços não críticos. Os serviços que não são críticos devem usar as seguintes configurações de recuperação para especificar que o serviço seja reiniciado dois minutos após a primeira falha ao reiniciar o serviço. O serviço não é reiniciado após a segunda falha, e um administrador precisaria intervir nesse caso. A contagem de falhas é redefinida para 0 após 900 segundos.

    <dl> Ações de recuperação: Restart/120000/Restart/300000/None/0 & Reset = 900  
    </dl>

 

 