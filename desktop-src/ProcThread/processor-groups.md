---
description: As versões de 64 bits do Windows 7 e Windows Server 2008 R2 e versões posteriores do Windows suportam mais de 64 processadores lógicos em um único computador. Essa funcionalidade não está disponível em versões de 32 bits do Windows.
ms.assetid: c627ac0f-96e8-48b5-9103-4316f487e173
title: Grupos de processadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc5916faf3cf90bce7f8549834fe130f299f782d6b2534969c89d74df454ae9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119418666"
---
# <a name="processor-groups"></a>Grupos de processadores

As versões de 64 bits do Windows 7 e Windows Server 2008 R2 e versões posteriores do Windows suportam mais de 64 processadores lógicos em um único computador. Essa funcionalidade não está disponível em versões de 32 bits do Windows.

Sistemas com mais de um processador físico ou sistemas com processadores físicos que têm vários núcleos fornecem ao sistema operacional vários processadores lógicos. Um *processador lógico* é um mecanismo de computação lógico da perspectiva do sistema operacional, aplicativo ou driver. Um *núcleo* é uma unidade de processador, que pode consistir em um ou mais processadores lógicos. Um *processador físico* pode consistir em um ou mais núcleos. Um processador físico é o mesmo que um pacote de processador, um soquete ou uma CPU.

O suporte para sistemas que têm mais de 64 processadores lógicos baseia-se no conceito de um grupo de processadores *,* que é um conjunto estático de até 64 processadores lógicos que é tratado como uma única entidade de agendamento. Os grupos de processadores são numerados começando com 0. Sistemas com menos de 64 processadores lógicos sempre têm um único grupo, Grupo 0.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para grupos de processadores.

Quando o sistema é iniciado, o sistema operacional cria grupos de processadores e atribui processadores lógicos aos grupos. Se o sistema for capaz de adicionar processadores a quente, o sistema operacional permitirá espaço em grupos para processadores que podem chegar enquanto o sistema estiver em execução. O sistema operacional minimiza o número de grupos em um sistema. Por exemplo, um sistema com 128 processadores lógicos teria dois grupos de processadores com 64 processadores em cada grupo, não quatro grupos com 32 processadores lógicos em cada grupo.

Para melhorar o desempenho, o sistema operacional leva em conta a localidade física ao atribuir processadores lógicos a grupos. Todos os processadores lógicos em um núcleo e todos os núcleos em um processador físico são atribuídos ao mesmo grupo, se possível. Processadores físicos fisicamente próximos um do outro são atribuídos ao mesmo grupo. Um nó NUMA é atribuído a um único grupo, a menos que a capacidade do nó exceda o tamanho máximo do grupo. Para obter mais informações, consulte [Suporte a NUMA](numa-support.md).

Em sistemas com 64 processadores ou menos, os aplicativos existentes funcionarão corretamente sem modificação. Aplicativos que não chamam nenhuma função que use máscaras de afinidade de processador ou números de processador funcionarão corretamente em todos os sistemas, independentemente do número de processadores. Para operar corretamente em sistemas com mais de 64 processadores lógicos, os seguintes tipos de aplicativos podem exigir modificação:

-   Os aplicativos que gerenciam, mantêm ou exibem informações por processador para todo o sistema devem ser modificados para dar suporte a mais de 64 processadores lógicos. Um exemplo desse aplicativo é Windows Gerenciador de Tarefas, que exibe a carga de trabalho de cada processador no sistema.
-   Aplicativos para os quais o desempenho é crítico e que podem ser dimensionado com eficiência além de 64 processadores lógicos devem ser modificados para serem executados nesses sistemas. Por exemplo, aplicativos de banco de dados podem se beneficiar de modificações.
-   Se um aplicativo usar uma DLL que tenha estruturas de dados por processador e a DLL não tiver sido modificada para dar suporte a mais de 64 processadores lógicos, todos os threads no aplicativo que chamam funções exportadas pela DLL deverão ser atribuídos ao mesmo grupo.

Por padrão, um aplicativo é restrito a um único grupo, que deve fornecer uma ampla capacidade de processamento para o aplicativo típico. Inicialmente, o sistema operacional atribui cada processo a um único grupo de maneira round robin entre os grupos no sistema. Um processo inicia sua execução atribuída a um grupo. O primeiro thread de um processo é executado inicialmente no grupo ao qual o processo é atribuído. Cada thread recém-criado é atribuído ao mesmo grupo que o thread que o criou.

Um aplicativo que exige o uso de vários grupos para que ele possa ser executado em mais de 64 processadores deve determinar explicitamente onde executar seus threads e é responsável por definir as afinidades do processador dos threads para os grupos desejados. O [sinalizador INHERIT PARENT \_ \_ AFFINITY](process-creation-flags.md) pode ser usado para especificar um processo pai (que pode ser diferente do processo atual) do qual gerar a afinidade para um novo processo. Se o processo estiver em execução em um único grupo, ele poderá ler e modificar sua afinidade usando [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) e [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) enquanto permanece no mesmo grupo; se a afinidade de processo for modificada, a nova afinidade será aplicada a seus threads.

A afinidade de um thread pode ser especificada na criação usando o atributo estendido [**PROC THREAD ATTRIBUTE GROUP \_ \_ \_ \_ AFFINITY**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) com a [**função CreateRemoteThreadEx.**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethreadex) Depois que o thread é criado, sua afinidade pode ser alterada chamando [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) ou [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity). Se um thread for atribuído a um grupo diferente do processo, a afinidade do processo será atualizada para incluir a afinidade do thread e o processo se tornará um processo de vários grupos. Outras alterações de afinidade devem ser feitas para threads individuais; A afinidade de um processo de vários grupos não pode ser modificada usando [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask). A [**função GetProcessGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-getprocessgroupaffinity) recupera o conjunto de grupos aos quais um processo e seus threads são atribuídos.

Para especificar a afinidade para todos os processos associados a um objeto de trabalho, use a função [**SetInformationJobObject**](/windows/win32/api/jobapi2/nf-jobapi2-setinformationjobobject) com a classe de informações **JobObjectGroupInformation** ou **JobObjectGroupInformationEx.**

Um processador lógico é identificado por seu número de grupo e seu número de processador relativo ao grupo. Isso é representado por uma estrutura [**PROCESSOR \_ NUMBER.**](/windows/desktop/api/WinNT/ns-winnt-processor_number) Os números numéricos do processador usados por funções herdadas são relativos ao grupo.

Para obter uma discussão sobre alterações na arquitetura do sistema operacional para dar suporte a mais de 64 processadores, consulte o white paper sistemas de suporte que têm mais de [64 processadores](https://www.microsoft.com/whdc/system/Sysinternals/MoreThan64proc.mspx).

Para ver uma lista de novas funções e estruturas que suportam grupos de processadores, consulte [Novidades em processos e threads.](what-s-new-in-processes-and-threads.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Vários processadores](multiple-processors.md)
</dt> <dt>

[Suporte ao NUMA](numa-support.md)
</dt> </dl>

 

 
