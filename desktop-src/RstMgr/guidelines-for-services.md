---
title: Diretrizes para serviços
description: Os serviços devem seguir essas diretrizes para garantir que o Gerenciador de Reinicialização possa desligar e reiniciar os serviços, se necessário, para instalar atualizações. Os aplicativos podem usar as diretrizes descritas em Diretrizes para aplicativos.
ms.assetid: 69a98f82-71bb-4780-8a3f-294cc5629900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6198da0d4f6f7887aaf37c858d98f3eb48e72c0d7722a1b5785a1cb280c96fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010134"
---
# <a name="guidelines-for-services"></a>Diretrizes para serviços

Os serviços devem seguir essas diretrizes para garantir que o Gerenciador de Reinicialização possa desligar e reiniciar os serviços, se necessário, para instalar atualizações. Os aplicativos podem usar as diretrizes descritas em [Diretrizes para aplicativos.](guidelines-for-applications.md)

-   Os serviços devem ser capazes de ser desligados e reiniciados usando o [Gerenciador de Controle de Serviço](/windows/desktop/Services/service-control-manager) sem exigir uma reinicialização do sistema. As exceções a essa diretriz são processos críticos do sistema que são executados no contexto de lsass.exe ou services.exe.
-   O Gerenciador de Reinicialização do reconhece as dependências de serviço. Quando um serviço é desligado e reiniciado, seus serviços dependentes são desligados e reiniciados.
-   Os serviços devem especificar o intervalo de recuperação e o período de redefinição no [SCM (Service Control Manager).](/windows/desktop/Services/service-control-manager) O intervalo de recuperação é o tempo, em msecs, após a última falha que o SCM aguarda antes de tomar a ação de recuperação. O período de redefinição é o tempo, em segundos, após a última falha que o Gerenciador de Controle de Serviço aguarda antes de redefinir a contagem de falhas para 0. Os serviços podem usar [**a função ChangeServiceConfig2**](/windows/desktop/api/winsvc/nf-winsvc-changeserviceconfig2a) para alterar as definições de configuração.

    [Os](critical-system-services.md) serviços críticos devem usar as seguintes configurações de recuperação para especificar que o serviço seja reiniciado um minuto após a primeira falha ao reiniciar o serviço, reiniciado dois minutos após a segunda falha e que o computador seja reiniciado um minuto após a terceira falha. A contagem de falhas é redefinida para 0 após 300 segundos.

    <dl> Ações de recuperação: Reinicialização/60000/Restart/120000/Reboot/60000 & Reset =300  
    </dl>

    [Os serviços críticos](critical-system-services.md) devem ser iniciados antes dos serviços não críticos. Os serviços que não são serviços críticos devem usar as seguintes configurações de recuperação para especificar que o serviço seja reiniciado dois minutos após a primeira falha ao reiniciar o serviço. O serviço não é reiniciado após a segunda falha e um administrador precisaria intervir nesse caso. A contagem de falhas é redefinida para 0 após 900 segundos.

    <dl> Ações de recuperação: Reinicialização/120000/Restart/300000/None/0 & Reset = 900  
    </dl>

 

 