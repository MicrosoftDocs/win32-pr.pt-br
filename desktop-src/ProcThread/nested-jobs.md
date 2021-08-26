---
description: Um aplicativo pode usar trabalhos aninhados para gerenciar subconjuntos de processos. Os trabalhos aninhados também habilitam um aplicativo que usa trabalhos para hospedar outros aplicativos que também usam trabalhos.
ms.assetid: FA22493B-CD29-49A7-BDAC-349FA96B8C9E
title: Trabalhos aninhados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fba0a517b71cdc01ec701a4a8f6a4f272f039797c140333e64ecad5532aca23f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032197"
---
# <a name="nested-jobs"></a>Trabalhos aninhados

Um aplicativo pode usar trabalhos aninhados para gerenciar subconjuntos de processos. Os trabalhos aninhados também habilitam um aplicativo que usa trabalhos para hospedar outros aplicativos que também usam trabalhos.

**Windows 7, Windows server 2008 R2, Windows XP com SP3, Windows server 2008, Windows Vista e Windows server 2003:** Um processo pode ser associado a apenas um único trabalho. os trabalhos aninhados foram introduzidos em Windows 8 e Windows Server 2012.

Este tópico fornece uma visão geral do comportamento de aninhamento de trabalho e de trabalhos aninhados:

-   [Hierarquias de trabalho aninhadas](#nested-job-hierarchies)
-   [Criando uma hierarquia de trabalho aninhada](#creating-a-nested-job-hierarchy)
-   [Limites de trabalho e notificações para trabalhos aninhados](#job-limits-and-notifications-for-nested-jobs)
-   [Contabilidade de recursos para trabalhos aninhados](#resource-accounting-for-nested-jobs)
-   [Término de trabalhos aninhados](#termination-of-nested-jobs)

Para obter informações gerais sobre trabalhos e objetos de trabalho, consulte [objetos de trabalho](job-objects.md).

## <a name="nested-job-hierarchies"></a>Hierarquias de trabalho aninhadas

Os trabalhos aninhados têm uma relação pai-filho na qual cada trabalho filho contém um subconjunto dos processos em seu trabalho pai. Se um processo que já está em um trabalho for adicionado a outro trabalho, os trabalhos serão aninhados por padrão se o sistema puder formar uma hierarquia de trabalhos válida e nenhum dos limites de interface do usuário definirá os restrições ([**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) com **JobObjectBasicUIRestrictions**).

A Figura 1 mostra uma hierarquia de trabalhos que contém uma árvore de processos rotulados como P0 até P7. O trabalho 1 é o *trabalho pai* do trabalho 2 e do trabalho 4, e é um *ancestral* do trabalho 3. O trabalho 2 é o *pai imediato* do trabalho 3; O trabalho 3 é o *filho imediato* do trabalho 2. Os trabalhos 1, 2 e 3 formam uma *cadeia de trabalhos* em que os trabalhos 1 e 2 são a cadeia de trabalhos *pai* 3. O trabalho final em uma cadeia de trabalhos é o *trabalho imediato* dos processos nesse trabalho. Na Figura 1, o trabalho 3 é o trabalho imediato de Processes P2, P3 e P4.

![Figura 1. uma hierarquia de trabalho aninhada que contém uma árvore de processo](images/nested-jobs-a.png)

Os trabalhos aninhados também podem ser usados para gerenciar grupos de processos de pares. Na hierarquia de trabalhos mostrada na Figura 2, o trabalho 1 é o trabalho pai do trabalho 2. Observe que uma hierarquia de trabalho pode conter apenas parte de uma árvore de processo. Na Figura 2, P0 não está na hierarquia, mas seus processos filho P1 a P5 são.

![Figura 2. uma hierarquia de trabalho aninhada que contém processos de pares](images/nested-jobs-b.png)

## <a name="creating-a-nested-job-hierarchy"></a>Criando uma hierarquia de trabalho aninhada

Os processos em uma hierarquia de trabalho são explicitamente associados a um objeto de trabalho usando a função [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) ou implicitamente associados durante a criação do processo, o mesmo que para trabalhos autônomos. A ordem na qual os trabalhos são criados e os processos são atribuídos determina se uma hierarquia pode ser criada.

Para criar uma hierarquia de trabalho usando Associação explícita, todos os objetos de trabalho devem ser criados usando [**CreateJobObject**](/windows/desktop/api/WinBase/nf-winbase-createjobobjecta), então, [**AssignProcessToJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-assignprocesstojobobject) deve ser chamado várias vezes para cada processo para associar o processo a cada trabalho ao qual deve pertencer. Para garantir que a hierarquia de trabalhos seja válida, primeiro atribua todos os processos ao trabalho na raiz da hierarquia, em seguida, atribua um subconjunto de processos ao objeto de trabalho filho imediato e assim por diante. Se os processos forem atribuídos aos trabalhos nesta ordem, um trabalho filho sempre terá um subconjunto de processos em seu trabalho pai enquanto a hierarquia estiver sendo criada, o que é necessário para o aninhamento. Se os processos forem atribuídos a trabalhos em ordem aleatória, em algum momento um trabalho filho terá processos que não estão em seu trabalho pai. Isso não é permitido pelo aninhamento e causará falha de **AssignProcessToJobObject** .

Quando os processos são implicitamente associados a um trabalho durante a criação do processo, um processo filho é associado a cada trabalho na cadeia de trabalhos de seu processo pai. Se o objeto de trabalho imediato permitir Breakaway, o processo filho desaparecerá do objeto de trabalho imediato e de cada trabalho na cadeia de trabalhos pai, movendo a hierarquia até atingir um trabalho que não permita Breakaway. Se o objeto de trabalho imediato não permitir Breakaway, o processo filho não se interromperá mesmo se os trabalhos em sua cadeia de trabalhos pai permitirem.

## <a name="job-limits-and-notifications-for-nested-jobs"></a>Limites de trabalho e notificações para trabalhos aninhados

Para determinados limites de recursos, o limite definido para trabalhos em uma cadeia de trabalhos pai determinam o *limite efetivo* que é imposto para um trabalho filho. O limite efetivo para o trabalho filho pode ser mais restritivo do que o limite de seu pai, mas não pode ser menos restritivo. Por exemplo, se a classe de prioridade de um trabalho filho estiver acima da \_ \_ classe de prioridade normal \_ e a classe de prioridade do trabalho pai for a classe de prioridade normal \_ \_ , o limite efetivo para processos no trabalho filho será a \_ classe de prioridade normal \_ . No entanto, se a classe de prioridade do trabalho filho estiver abaixo da \_ \_ classe de prioridade normal \_ , o limite efetivo para processos no trabalho filho estará abaixo da \_ classe de prioridade normal \_ \_ . Os limites efetivos são impostos para classe de prioridade, afinidade, encargo de confirmação, limite de tempo de execução por processo, limite de classe de agendamento e mínimo e máximo de conjunto de trabalho. Para obter mais informações sobre limites de recursos específicos, consulte [ **SetInformationJobObject.**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject)

Quando determinados eventos ocorrem, como nova criação de processo ou violação de limite de recursos, uma mensagem é enviada para a porta de conclusão de e/s associada a um trabalho. Um trabalho também pode se registrar para receber notificações quando determinados limites forem excedidos. Para um trabalho não aninhado, a mensagem é enviada para a porta de conclusão de e/s associada ao trabalho. Para um trabalho aninhado, a mensagem é enviada a cada porta de conclusão de e/s associada a qualquer trabalho na cadeia de trabalhos pai do trabalho que disparou a mensagem. Um trabalho filho não precisa ter uma porta de conclusão de e/s associada para as mensagens que ele dispara para serem enviadas para as portas de conclusão de e/s de trabalhos pai acima na cadeia de trabalhos. Para obter mais informações sobre mensagens específicas, consulte [**JOBOBJECT \_ associar a \_ \_ porta de conclusão**](/windows/desktop/api/WinNT/ns-winnt-jobobject_associate_completion_port).

## <a name="resource-accounting-for-nested-jobs"></a>Contabilidade de recursos para trabalhos aninhados

As informações de contabilização de recursos para um trabalho aninhado descrevem o uso de todos os processos associados a esse trabalho, incluindo processos em trabalhos filho. Cada trabalho em uma cadeia de trabalhos, portanto, representa os recursos agregados usados por seus próprios processos e os processos de cada trabalho filho abaixo dele na cadeia de trabalhos.

## <a name="termination-of-nested-jobs"></a>Término de trabalhos aninhados

Quando um trabalho em uma hierarquia de trabalhos é encerrado, o sistema encerra os processos nesse trabalho e todos os seus trabalhos filho, começando com o trabalho filho na parte inferior da hierarquia. Os recursos pendentes usados por cada processo encerrado são cobrados no trabalho pai.

O identificador de trabalho deve ter o \_ objeto de trabalho \_ encerrar acesso direito, o mesmo que para trabalhos autônomos.

 

 
