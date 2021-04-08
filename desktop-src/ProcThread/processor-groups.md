---
description: As versões de 64 bits do Windows 7 e do Windows Server 2008 R2 e versões posteriores do Windows dão suporte a mais de 64 processadores lógicos em um único computador. Essa funcionalidade não está disponível nas versões de 32 bits do Windows.
ms.assetid: c627ac0f-96e8-48b5-9103-4316f487e173
title: Grupos de processadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cebc5b9ab1b386847b6561a9f6322c2fca0e2ae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104011018"
---
# <a name="processor-groups"></a>Grupos de processadores

As versões de 64 bits do Windows 7 e do Windows Server 2008 R2 e versões posteriores do Windows dão suporte a mais de 64 processadores lógicos em um único computador. Essa funcionalidade não está disponível nas versões de 32 bits do Windows.

Sistemas com mais de um processador físico ou sistemas com processadores físicos com vários núcleos fornecem o sistema operacional com vários processadores lógicos. Um *processador lógico* é um mecanismo de computação lógico da perspectiva do sistema operacional, aplicativo ou driver. Um *núcleo* é uma unidade de processador, que pode consistir em um ou mais processadores lógicos. Um *processador físico* pode consistir em um ou mais núcleos. Um processador físico é o mesmo que um pacote de processador, um soquete ou uma CPU.

O suporte para sistemas com mais de 64 processadores lógicos é baseado no conceito de um *grupo de processadores*, que é um conjunto estático de até 64 processadores lógicos que são tratados como uma única entidade de agendamento. Os grupos de processador são numerados a partir de 0. Sistemas com menos de 64 processadores lógicos sempre têm um único grupo, grupo 0.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para grupos de processador.

Quando o sistema é iniciado, o sistema operacional cria grupos de processadores e atribui processadores lógicos aos grupos. Se o sistema for capaz de adicionar processadores de forma automática, o sistema operacional permite o espaço em grupos para processadores que podem chegar enquanto o sistema está em execução. O sistema operacional minimiza o número de grupos em um sistema. Por exemplo, um sistema com processadores lógicos 128 teria dois grupos de processadores com processadores 64 em cada grupo, e não quatro grupos com processadores lógicos de 32 em cada grupo.

Para obter um melhor desempenho, o sistema operacional leva à localidade física em conta ao atribuir processadores lógicos a grupos. Todos os processadores lógicos em um núcleo e todos os núcleos em um processador físico são atribuídos ao mesmo grupo, se possível. Os processadores físicos que estão fisicamente próximos um do outro são atribuídos ao mesmo grupo. Um nó NUMA é atribuído a um único grupo, a menos que a capacidade do nó exceda o tamanho máximo do grupo. Para obter mais informações, consulte [suporte a numa](numa-support.md).

Em sistemas com 64 ou menos processadores, os aplicativos existentes funcionarão corretamente sem modificação. Os aplicativos que não chamam nenhuma função que use máscaras de afinidade de processador ou números de processador funcionarão corretamente em todos os sistemas, independentemente do número de processadores. Para operar corretamente em sistemas com mais de 64 processadores lógicos, os seguintes tipos de aplicativos podem exigir modificação:

-   Os aplicativos que gerenciam, mantêm ou exibem informações por processador para todo o sistema devem ser modificados para dar suporte a mais de 64 processadores lógicos. Um exemplo desse tipo de aplicativo é o Gerenciador de tarefas do Windows, que exibe a carga de trabalho de cada processador no sistema.
-   Aplicativos para os quais o desempenho é crítico e que podem ser dimensionados com eficiência além de 64 processadores lógicos devem ser modificados para serem executados em tais sistemas. Por exemplo, os aplicativos de banco de dados podem se beneficiar de modificações.
-   Se um aplicativo usa uma DLL que tem estruturas de dados por processador e a DLL não foi modificada para dar suporte a mais de 64 processadores lógicos, todos os threads no aplicativo que chamam funções exportadas pela DLL devem ser atribuídos ao mesmo grupo.

Por padrão, um aplicativo é restrito a um único grupo, o que deve fornecer um amplo recurso de processamento para o aplicativo típico. Inicialmente, o sistema operacional atribui cada processo a um único grupo de uma maneira Round Robin entre os grupos no sistema. Um processo começa sua execução atribuída a um grupo. Inicialmente, o primeiro thread de um processo é executado no grupo ao qual o processo é atribuído. Cada thread recém-criado é atribuído ao mesmo grupo do thread que o criou.

Um aplicativo que exige o uso de vários grupos para que ele possa ser executado em mais de 64 processadores deve determinar explicitamente onde executar seus threads e é responsável por definir as afinidades de processador de threads para os grupos desejados. O sinalizador de [ \_ \_ afinidade de pai herdado](process-creation-flags.md) pode ser usado para especificar um processo pai (que pode ser diferente do processo atual) do qual gerar a afinidade para um novo processo. Se o processo estiver sendo executado em um único grupo, ele poderá ler e modificar sua afinidade usando [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) e [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) enquanto estiver restante no mesmo grupo; se a afinidade de processo for modificada, a nova afinidade será aplicada a seus threads.

A afinidade de um thread pode ser especificada na criação usando o atributo de afinidade de grupo de atributos de thread do proc com a função [**CreateRemoteThreadEx**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) . [**\_ \_ \_ \_**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) Depois que o thread é criado, sua afinidade pode ser alterada chamando [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) ou [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity). Se um thread for atribuído a um grupo diferente do processo, a afinidade do processo será atualizada para incluir a afinidade do thread e o processo se tornará um processo de vários grupos. Outras alterações de afinidade devem ser feitas para threads individuais; a afinidade de um processo de vários grupos não pode ser modificada usando [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask). A função [**GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity) recupera o conjunto de grupos aos quais um processo e seus threads são atribuídos.

Para especificar a afinidade de todos os processos associados a um objeto de trabalho, use a função [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) com a classe de informações **JobObjectGroupInformation** ou **JobObjectGroupInformationEx** .

Um processador lógico é identificado por seu número de grupo e seu número de processador relativo ao grupo. Isso é representado por uma estrutura de [**\_ número de processador**](/windows/desktop/api/WinNT/ns-winnt-processor_number) . Números numéricos de processador usados por funções herdadas são relativos a grupos.

Para uma discussão sobre as alterações da arquitetura do sistema operacional para dar suporte a mais de 64 processadores, consulte a white paper [sistemas de suporte que têm mais de 64 processadores](https://www.microsoft.com/whdc/system/Sysinternals/MoreThan64proc.mspx).

Para obter uma lista de novas funções e estruturas que dão suporte a grupos de processadores, consulte [novidades em processos e threads](what-s-new-in-processes-and-threads.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vários processadores](multiple-processors.md)
</dt> <dt>

[Suporte a NUMA](numa-support.md)
</dt> </dl>

 

 
