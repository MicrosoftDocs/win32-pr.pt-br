---
description: O aplicativo é dividido em dois programas. Um dos programas é executado como usuário padrão e o outro é executado com o privilégio de administrador.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Modelo de agente do administrador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299d35c995fb56f969fc5983864cfc93b25b6c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828829"
---
# <a name="administrator-broker-model"></a>Modelo de agente do administrador

No modelo de agente do administrador, o aplicativo é dividido em dois programas. Um dos programas é executado como usuário padrão e o outro é executado com o privilégio de administrador.

Usando um manifesto de aplicativo, marque o programa de usuário padrão com um **requestedExecutionLevel** de **asInvoker** e marque o programa administrativo com um **requestedExecutionLevel** de **requireAdministrator**. Um usuário inicia o programa de usuário padrão primeiro. Quando o usuário tenta executar uma operação que requer um token de acesso de administrador completo, o programa de usuário padrão chama a função [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) para iniciar o programa administrativo. A função **ShellExecute** solicita aprovação do usuário antes de executar o aplicativo com o token de acesso de administrador completo do usuário. O programa administrativo pode executar tarefas que exigem privilégios de administrador.

O programa administrativo não está completamente isolado do programa de usuário padrão. O programa administrativo pode habilitar a comunicação entre processos com o programa de usuário padrão. No entanto, essa comunicação é limitada pela política de integridade obrigatória padrão. Para obter informações sobre considerações de integridade obrigatórias, consulte [projetando aplicativos para serem executados em um nível de baixa integridade](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).

Os seguintes usos são possíveis para o modelo de agente do administrador:

-   Desenvolvendo assistentes. Quando um assistente de hardware determina que um driver necessário não está instalado no computador ou localizado no local aprovado da empresa, ele chama um aplicativo elevado com a capacidade de mover um driver para o repositório do computador.
-   Autorun.exe chamando Setup.exe. Quando um usuário executa software de um CD, Autorun.exe, que é executado como usuário padrão, inicia Setup.exe, que é executado como administrador, para instalar o software no computador.

A seguir estão as desvantagens de usar o modelo de agente do administrador:

-   As transições do aplicativo para o aplicativo podem ser confusas para o usuário. Pode ser difícil informar ao usuário por que um novo aplicativo aparece no monitor.
-   Pode ser difícil passar informações de estado entre os dois aplicativos. Por exemplo, você não usaria esse modelo para passar informações de estado entre um CPL (painel de controle de usuário) padrão e sua contraparte de administrador simplesmente para permitir que o mesmo CPL tenha funcionalidade de usuário administrativa e padrão. O CPL de usuário padrão teria que armazenar seu estado em algum lugar.
-   Pode haver muitos códigos replicados ao dividir a funcionalidade entre dois programas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desenvolvendo aplicativos que exigem privilégios de administrador](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Modelo de objeto COM do administrador](administrator-com-object-model.md)
</dt> <dt>

[Modelo de serviço do sistema operacional](operating-system-service-model.md)
</dt> <dt>

[Modelo de tarefa elevada](elevated-task-model.md)
</dt> </dl>

 

 
