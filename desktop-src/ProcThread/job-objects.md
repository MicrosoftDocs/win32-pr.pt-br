---
description: Um objeto de trabalho permite que grupos de processos sejam gerenciados como uma unidade. Os objetos de trabalho são objetos namable, protegíveis e compartilháveis que controlam os atributos dos processos associados a eles.
ms.assetid: 59296384-5e78-44dd-8019-f1df6668928b
title: Objetos de trabalho
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e6d9758faf2b66f047ca60dbba91601b202b4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296743"
---
# <a name="job-objects"></a>Objetos de trabalho

Um *objeto de trabalho* permite que grupos de processos sejam gerenciados como uma unidade. Os objetos de trabalho são objetos namable, protegíveis e compartilháveis que controlam os atributos dos processos associados a eles. As operações realizadas em um objeto de trabalho afetam todos os processos associados ao objeto de trabalho. Os exemplos incluem a imposição de limites, como o tamanho do conjunto de trabalho e a prioridade do processo ou o encerramento de todos os processos associados a um trabalho.

-   [Criando trabalhos](#creating-jobs)
-   [Gerenciando processos em trabalhos](#managing-processes-in-jobs)
-   [Notificações e limites de trabalho](#job-limits-and-notifications)
-   [Contabilidade de recursos para trabalhos](#resource-accounting-for-jobs)
-   [Gerenciando objetos de trabalho](#managing-job-objects)
-   [Gerenciando uma árvore de processos que usa objetos de trabalho](#managing-a-process-tree-that-uses-job-objects)

## <a name="creating-jobs"></a>Criando trabalhos

Para criar um objeto de trabalho, use a função [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) . Quando o trabalho é criado, nenhum processo é associado ao trabalho.

Para associar um processo a um trabalho, use a função [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) . Depois que um processo é associado a um trabalho, a associação não pode ser quebrada. Um processo pode ser associado a mais de um trabalho em uma hierarquia de trabalhos aninhados. Para obter mais informações, consulte [tarefas aninhadas](nested-jobs.md).

**Windows 7, Windows server 2008 R2, Windows XP com SP3, Windows server 2008, Windows Vista e Windows Server 2003:** Um processo pode ser associado a apenas um trabalho. Os trabalhos não podem ser aninhados. A capacidade de aninhar trabalhos foi adicionada no Windows 8 e no Windows Server 2012.

Você pode especificar um descritor de segurança para um objeto de trabalho ao chamar a função [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta) . Para obter mais informações, consulte [segurança do objeto de trabalho e direitos de acesso](job-object-security-and-access-rights.md).

## <a name="managing-processes-in-jobs"></a>Gerenciando processos em trabalhos

Depois que um processo é associado a um trabalho, por padrão, todos os processos filho que ele cria usando [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) também são associados ao trabalho. (Processos filho criados usando [**o \_ processo Win32. Create**](../cimwin32prov/create-method-in-class-win32-process.md) não estão associados ao trabalho.) Esse comportamento padrão pode ser alterado configurando o limite estendido do objeto de trabalho limite \_ \_ \_ BREAKAWAY \_ OK ou o \_ limite de objeto de trabalho \_ \_ silencioso \_ BREAKAWAY \_ OK para o trabalho.

-   Se o trabalho tiver o limite de objeto de trabalho limite estendido \_ \_ \_ BREAKAWAY \_ OK e o processo pai tiver sido criado com o \_ sinalizador criar BREAKAWAY \_ do \_ trabalho, os processos filho do processo pai não serão associados ao trabalho.
-   Se o trabalho tiver o limite de objeto de trabalho limite estendido \_ \_ \_ \_ BREAKAWAY \_ OK, os processos filho de qualquer processo pai associado ao trabalho não serão associados ao trabalho. Não é necessário que os processos pai sejam criados com o sinalizador criar \_ BREAKAWAY \_ do \_ trabalho.

Se o trabalho estiver aninhado, as configurações de Breakaway dos trabalhos pai na hierarquia afetarão se os processos filho estão associados a outro trabalho na hierarquia. Para obter mais informações, consulte [tarefas aninhadas](nested-jobs.md).

Para determinar se um processo está sendo executado em um trabalho, use a função [**IsProcessInJob**](/windows/win32/api/jobapi/nf-jobapi-isprocessinjob) .

Para encerrar todos os processos atualmente associados a um objeto de trabalho, use a função [**TerminateJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-terminatejobobject) .

## <a name="job-limits-and-notifications"></a>Notificações e limites de trabalho

Um trabalho pode impor limites como o tamanho do conjunto de trabalho, a prioridade do processo e o limite de tempo de término do trabalho em cada processo associado ao trabalho. Se um processo associado a um trabalho tentar aumentar seu tamanho de conjunto de trabalho ou prioridade de processo do limite estabelecido pelo trabalho, a função chamará com sucesso, mas será silenciosamente ignorada. Um trabalho também pode definir limites que disparam uma notificação quando são excedidos, mas permitem que o trabalho continue a ser executado.

Para definir limites para um trabalho, use a função [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) . Para obter uma lista dos possíveis limites que podem ser definidos para um trabalho, consulte os seguintes tópicos:

-   [**\_informações de \_ limite \_ básico do JOBOBJECT**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_limit_information)
-   [**\_restrições básicas de \_ interface do usuário do JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_ui_restrictions)
-   [**\_informações de \_ controle de taxa de CPU JOBOBJECT \_ \_**](/windows/desktop/api/Winnt/ns-winnt-jobobject_cpu_rate_control_information)
-   [**\_informações de \_ limite ESTENDIdo JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_extended_limit_information)
-   [**\_informações de \_ limite de notificação do JOBOBJECT \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_notification_limit_information)

Os limites de segurança devem ser definidos individualmente para cada processo associado a um objeto de trabalho. Para obter mais informações, consulte [segurança do processo e direitos de acesso](process-security-and-access-rights.md).

**Windows XP com SP3 e Windows Server 2003:** A função [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) pode ser usada para definir limitações de segurança para todos os processos associados a um objeto de trabalho. A partir do Windows Vista, os limites de segurança devem ser definidos individualmente para cada processo associado a um objeto de trabalho.

Se o trabalho estiver aninhado, os trabalhos pai na hierarquia influenciarão o limite que é imposto para o trabalho. Para obter mais informações, consulte [tarefas aninhadas](nested-jobs.md).

Se o trabalho tiver uma porta de conclusão de e/s associada, ele poderá receber notificações quando determinados limites de trabalho forem excedidos. O sistema envia mensagens para a porta de conclusão quando um limite é excedido ou determinados outros eventos ocorrem. Para associar uma porta de conclusão a um trabalho, use a função [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) com a classe de informações do objeto de trabalho **JobObjectAssociateCompletionPortInformation** e um ponteiro para uma estrutura de [**porta de conclusão do JOBOBJECT \_ associado \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port) . É melhor fazer isso quando o trabalho está inativo, para reduzir a chance de notificações ausentes para processos cujos Estados são alterados durante a associação da porta de conclusão.

Todas as mensagens são enviadas diretamente do trabalho como se o trabalho tivesse chamado a função [**PostQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-postqueuedcompletionstatus) . Um thread deve monitorar a porta de conclusão usando a função [**GetQueuedCompletionStatus**](/windows/win32/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) para pegar as mensagens. Observe que, com a exceção de limites definidos com a classe de informações **JobObjectNotificationLimitInformation** , a entrega de mensagens para a porta de conclusão não é garantida; a falha de uma mensagem a chegar não significa necessariamente que o evento não ocorra. As notificações para os limites definidos com **JobObjectNotificationLimitInformation** têm garantia de chegar à porta de conclusão. Para obter uma lista de possíveis mensagens, consulte [**JOBOBJECT \_ associar a \_ \_ porta de conclusão**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-jobs"></a>Contabilidade de recursos para trabalhos

O objeto de trabalho registra informações de estatísticas básicas para todos os seus processos associados, incluindo os que foram encerrados. Para recuperar essas informações de contabilidade, use a função [**QueryInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-queryinformationjobobject) . Para obter uma lista das informações de estatísticas mantidas para um trabalho, consulte os seguintes tópicos:

-   [**informações de contabilidade do JOBOBJECT \_ Basic \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_accounting_information)
-   [**\_ \_ informações de contabilidade do JOBOBJECT Basic e \_ Io \_ \_**](/windows/desktop/api/WinNT/ns-winnt-jobobject_basic_and_io_accounting_information)

Se o objeto de trabalho estiver aninhado, as informações de contabilização de cada trabalho filho serão agregadas em seu trabalho pai. Para obter mais informações, consulte [tarefas aninhadas](nested-jobs.md).

## <a name="managing-job-objects"></a>Gerenciando objetos de trabalho

O estado de um objeto de trabalho é definido como sinalizado quando todos os seus processos são encerrados porque o limite de tempo final do trabalho especificado foi excedido. Use [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) ou [**WaitForSingleObjectEx**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobjectex) para monitorar o objeto de trabalho para este evento.

Para obter um identificador para um objeto de trabalho existente, use a função [**OpenJobObject**](/windows/desktop/api/WinBase/nf-winbase-openjobobjecta) e especifique o nome fornecido para o objeto quando ele foi criado. Somente objetos de trabalho nomeados podem ser abertos.

Para fechar um identificador de objeto de trabalho, use a função [**CloseHandle**](/windows/win32/api/handleapi/nf-handleapi-closehandle) . O trabalho é destruído quando seu último identificador foi fechado e todos os processos associados foram encerrados. No entanto, se o trabalho tiver o limite de objetos de trabalho \_ \_ \_ Kill \_ no \_ sinalizador de fechamento de trabalho \_ especificado, fechar o último identificador de objeto de trabalho finalizará todos os processos associados e, em seguida, destruirá o próprio objeto de trabalho. Se um trabalho aninhado tiver o \_ limite de objetos de trabalho \_ \_ Kill \_ no \_ sinalizador de fechamento de trabalho \_ especificado, fechar o último identificador de objeto de trabalho finalizará todos os processos associados ao trabalho e seus trabalhos filho na hierarquia.

## <a name="managing-a-process-tree-that-uses-job-objects"></a>Gerenciando uma árvore de processos que usa objetos de trabalho

A partir do Windows 8 e do Windows Server 2012, um aplicativo pode usar [trabalhos aninhados](nested-jobs.md) para gerenciar uma árvore de processos que usa mais de um objeto de trabalho. No entanto, um aplicativo que deve ser executado no Windows 7, no Windows Server 2008 R2 ou em versões anteriores do Windows que não dão suporte a trabalhos aninhados deve gerenciar a árvore de processo de outras maneiras.

Se uma ferramenta precisar gerenciar uma árvore de processos que usa objetos de trabalho e não for possível usar trabalhos aninhados, a ferramenta e os membros da árvore de processos deverão cooperar. Use uma das seguintes opções:

-   Use o \_ limite de \_ BREAKAWAY silencioso de limite de objeto de trabalho \_ \_ \_ . Se a ferramenta usar esse limite, ele não poderá monitorar uma árvore de processo inteira. A ferramenta pode monitorar apenas os processos que ele adiciona ao trabalho. Se esses processos criarem processos filho, eles não serão associados ao trabalho. Nessa opção, os processos filho podem ser associados a outros objetos de trabalho.
-   Use o limite de BREAKAWAY do objeto de trabalho limite \_ \_ \_ \_ OK. Se a ferramenta usar esse limite, ela poderá monitorar toda a árvore de processo, exceto pelos processos que qualquer membro da árvore separa explicitamente da árvore. Um membro da árvore pode criar um processo filho em um novo objeto de trabalho chamando a função [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) com o sinalizador criar \_ BREAKAWAY \_ do \_ trabalho e, em seguida, chamando a função [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) . Caso contrário, o membro deve manipular casos em que **AssignProcessToJobObject** falhará.

    O \_ sinalizador criar BREAKAWAY \_ do \_ trabalho não terá efeito se a árvore não estiver sendo monitorada pela ferramenta. Portanto, essa é a opção preferida, mas requer conhecimento avançado dos processos que estão sendo monitorados.

-   Evite Breakaways de qualquer tipo Configurando nem o \_ limite do objeto de trabalho \_ \_ BREAKAWAY \_ OK nem o limite do objeto de trabalho \_ BREAKAWAY o \_ \_ \_ limite silencioso \_ OK. Nessa opção, a ferramenta pode monitorar toda a árvore de processo. No entanto, se um processo filho tentar se associar a si mesmo ou a outro processo filho com um trabalho chamando [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject), a chamada falhará. Se o processo foi projetado para ser associado a um trabalho específico, essa falha poderá impedir que o processo funcione corretamente.

 

 
