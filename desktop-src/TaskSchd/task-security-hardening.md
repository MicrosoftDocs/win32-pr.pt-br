---
title: Proteção de segurança de tarefa
description: Usar o recurso de proteção de segurança de tarefas permitirá que os proprietários da tarefa executem suas tarefas com os privilégios mínimos necessários.
ms.assetid: ba03add5-aa05-4bef-baec-684ca17363bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ab70679d605a9ad56c6d26116245ae17d41a7a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159832"
---
# <a name="task-security-hardening"></a>Proteção de segurança de tarefa

Usar o recurso de proteção de segurança de tarefas permitirá que os proprietários da tarefa executem suas tarefas com os privilégios mínimos necessários. Observe que esse recurso está habilitado por padrão e os proprietários da tarefa podem fazer ajustes adicionais usando o tipo de identificador de segurança do token de processo e a matriz de privilégios necessários da tarefa.

## <a name="task-process-token-sid-type-and-task-required-privileges-array"></a>Tipo de SID do token do processo de tarefa e matriz de privilégios necessários da tarefa

Especificar **ProcessTokenSidType** no nível de definição de tarefa permite que os proprietários da tarefa solicitem que um processo de tarefa seja executado com o tipo de Sid "nenhum" ou o tipo de Sid "irrestrito". Se o campo estiver presente na definição de tarefa, a validação garantirá que a UserId da tarefa contenha o nome ou a cadeia de caracteres SID correspondente para uma das contas de serviço internas do sistema operacional: "serviço de rede" ou "serviço LOCAL".

O tipo de SID "None" significa que a tarefa é executada em um processo que não contém um SID de token de processo (nenhuma alteração será feita na lista de grupos de tokens de processo). O SID da conta da entidade de tarefa (LocalService/NetworkService) nesse caso tem acesso completo ao token do processo.

O tipo de SID "irrestrito" significa que um SID de tarefa será derivado do caminho de tarefa completo e será adicionado à lista de grupos de tokens de processo. Por exemplo, o \\ RACTask do Microsoft \\ Windows \\ RAC \\ que é executado na conta de serviço local, o SID da tarefa é derivado do nome Microsoft-Windows-RAC-RACTask, em que um "-" é substituído por um " \\ ", já que " \\ " é um caractere de nome de usuário inválido. O nome do grupo bem conhecido para o SID da tarefa seria "NT TASK \\ <modified full task path> " (o formato de nome de usuário DomainName \\ ). A DACL (lista de controle de acesso discricionário) padrão do token de processo também será modificada para permitir o controle total somente para o SID da tarefa e o SID do sistema local e o controle de leitura para o SID da conta da entidade de tarefa. "schtasks.exe/showsid/TN <full task path> " mostrará o SID da tarefa que corresponde à tarefa.

Quando uma ação de tarefa não COM é iniciada, o mecanismo de agendamento faz o log na conta da entidade de segurança, obtém o token do processo e consulta a lista de privilégios que o token tem e, em seguida, compara isso com a lista de privilégios especificada em RequiredPrivileges. Se um privilégio não for especificado no último, isso será marcado como privilégio de SE \_ \_ removido. A ação executável será então iniciada com o identificador de token resultante usando a API CreateProcessAsUser.

Quando uma ação de tarefa COM é iniciada, ela deve ser ativada pelo processo de taskhost.exe. O mecanismo de agendamento consulta o bloco de contexto de cada taskhost.exe em execução com a mesma conta que a tarefa inicial. Se ele descobrir que um processo de host foi iniciado com um superconjunto de privilégios necessário para a tarefa inicial, essa tarefa será hospedada nesse processo. Se ele não encontrar esse processo, ele combinará as informações de proteção de todas as tarefas em execução no TaskHosts na conta de entidade de segurança com a máscara RequiredPrivileges especificada e, em seguida, iniciará uma nova instância do taskhost.exe.

Se RequiredPrivileges não estiver presente na definição de tarefa, os privilégios padrão da conta de entidade de tarefa sem o SeImpersonatePrivilege serão usados para o processo de tarefa. Se **ProcessTokenSidType** não estiver presente na definição de tarefa, "irrestrito" será usado como o padrão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Informações de registro da tarefa](task-registration-information.md)
</dt> <dt>

[Sobre o Agendador de Tarefas](about-the-task-scheduler.md)
</dt> <dt>

[Contextos de segurança para tarefas](security-contexts-for-running-tasks.md)
</dt> </dl>

 

 




