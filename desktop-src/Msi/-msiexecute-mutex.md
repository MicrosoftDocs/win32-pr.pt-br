---
description: O \_ mutex MSIExecute é definido somente durante o processamento da tabela InstallExecuteSequence, tabela AdminExecuteSequence ou tabela AdvtExecuteSequence.
ms.assetid: 2186422d-ccb2-4f7e-8c6d-326c00e0d9a9
title: _MSIExecute mutex
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c22a9ca79e83e8593c2ee99884965acfd414ff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828107"
---
# <a name="_msiexecute-mutex"></a>\_Mutex MSIExecute

O \_ mutex MSIExecute é definido somente durante o processamento da tabela [InstallExecuteSequence](installexecutesequence-table.md), [tabela AdminExecuteSequence](adminexecutesequence-table.md)ou [tabela AdvtExecuteSequence](advtexecutesequence-table.md).

Como duas instalações não podem ser executadas no mesmo processo, uma tentativa de chamar a API (interface de programação de aplicativo) do instalador retorna um erro \_ \_ de instalação já \_ em execução (1618) em dois casos:

-   Enquanto o \_ mutex MSIExecute é definido.
-   Enquanto o processo atual está processando a tabela [InstallUISequence](installuisequence-table.md) ou a [tabela AdminUISequence](adminuisequence-table.md).

Consulte as mensagens de [log de eventos](event-logging.md) para obter informações sobre qual aplicativo está sendo instalado.

Nos casos em que é impraticável retornar um erro de \_ instalação \_ já \_ em execução, você pode recuperar o status atual do serviço de Windows Installer antes de tentar iniciar a instalação usando a função [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) . O serviço de Windows Installer está em execução no momento se o valor do membro **dwControlsAccepted** da estrutura de [**processo de \_ status \_ do serviço**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) retornado for **serviço de \_ \_ desligamento de aceitação**.

**Windows Installer 2,0:** Sem suporte. O uso da função [**QueryServiceStatusEx**](/windows/desktop/api/winsvc/nf-winsvc-queryservicestatusex) para recuperar o status atual do serviço de Windows Installer requer Windows Installer versão 3,0 ou superior.

 

 
