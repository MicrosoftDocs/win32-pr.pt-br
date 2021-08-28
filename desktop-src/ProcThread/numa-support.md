---
description: O modelo tradicional para suporte multiprocessador é o SMP (multiprocessador simétrico). Nesse modelo, cada processador tem acesso igual à memória e e/s. À medida que mais processadores são adicionados, o barramento do processador torna-se uma limitação para o desempenho do sistema.
ms.assetid: a1263968-2b26-45cc-bdd7-6aa354821a5a
title: Suporte ao NUMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 503b64f6f18779fb66a87fc3c45b682fcb97248c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479422"
---
# <a name="numa-support"></a>Suporte ao NUMA

O modelo tradicional para suporte multiprocessador é o SMP (multiprocessador simétrico). Nesse modelo, cada processador tem acesso igual à memória e e/s. À medida que mais processadores são adicionados, o barramento do processador torna-se uma limitação para o desempenho do sistema.

Os designers do sistema usam o NUMA (acesso não uniforme à memória) para aumentar a velocidade do processador sem aumentar a carga no barramento do processador. A arquitetura não é uniforme porque cada processador está perto de algumas partes da memória e mais distante de outras partes da memória. O processador rapidamente obtém acesso à memória em que está perto, enquanto pode levar mais tempo para obter acesso à memória que está mais distante.

Em um sistema NUMA, as CPUs são organizadas em sistemas menores chamados *nós*. Cada nó tem seus próprios processadores e memória e está conectado ao sistema maior por meio de um barramento de interconexão coerente com o cache.

O sistema tenta melhorar o desempenho agendando threads em processadores que estão no mesmo nó que a memória que está sendo usada. Ele tenta satisfazer as solicitações de alocação de memória de dentro do nó, mas alocará memória de outros nós, se necessário. Ele também fornece uma API para tornar a topologia do sistema disponível para os aplicativos. Você pode melhorar o desempenho de seus aplicativos usando as funções de NUMA para otimizar o uso de memória e agendamento.

Em primeiro lugar, será necessário determinar o layout dos nós no sistema. Para recuperar o nó numerado mais alto no sistema, use a função [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber) . Observe que esse número não é garantido como igual ao número total de nós no sistema. Além disso, não há garantia de que os nós com números sequenciais estejam próximos juntos. Para recuperar a lista de processadores no sistema, use a função [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) . Você pode determinar o nó para cada processador na lista usando a função [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode) . Como alternativa, para recuperar uma lista de todos os processadores em um nó, use a função [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask) .

Depois de determinar quais processadores pertencem a quais nós, você pode otimizar o desempenho do aplicativo. Para garantir que todos os threads do processo sejam executados no mesmo nó, use a função [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) com uma máscara de afinidade de processo que especifique os processadores no mesmo nó. Isso aumenta a eficiência dos aplicativos cujos threads precisam acessar a mesma memória. Como alternativa, para limitar o número de threads em cada nó, use a função [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) .

Aplicativos com uso intensivo de memória precisarão otimizar seu uso de memória. Para recuperar a quantidade de memória livre disponível para um nó, use a função [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode) . A função [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) permite que o aplicativo especifique um nó preferencial para a alocação de memória. O **VirtualAllocExNuma** não aloca nenhuma página física, portanto, será bem sucedido se as páginas estão disponíveis ou não nesse nó ou em outro lugar no sistema. As páginas físicas são alocadas sob demanda. Se o nó preferencial for executado fora de páginas, o Gerenciador de memória usará páginas de outros nós. Se a memória for paginada, o mesmo processo será usado quando for retornado.

### <a name="numa-support-on-systems-with-more-than-64-logical-processors"></a>Suporte a NUMA em sistemas com mais de 64 processadores lógicos

Em sistemas com mais de 64 processadores lógicos, os nós são atribuídos a [grupos de processadores](processor-groups.md) de acordo com a capacidade dos nós. A capacidade de um nó é o número de processadores que estão presentes quando o sistema é iniciado junto com quaisquer processadores lógicos adicionais que podem ser adicionados enquanto o sistema está em execução.

**Windows server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Não há suporte para grupos de processador.

Cada nó deve estar totalmente contido em um grupo. Se as capacidades dos nós forem relativamente pequenas, o sistema atribuirá mais de um nó ao mesmo grupo, escolhendo os nós que estão fisicamente próximos um do outro para melhorar o desempenho. Se a capacidade de um nó exceder o número máximo de processadores em um grupo, o sistema dividirá o nó em vários nós menores, cada um pequeno o suficiente para caber em um grupo.

Um nó NUMA ideal para um novo processo pode ser solicitado usando o atributo estendido do [**atributo de thread proc de \_ \_ \_ \_ nó de preferência**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) quando o processo é criado. Como um processador ideal para thread, o nó ideal é uma dica para o Agendador, que atribui o novo processo ao grupo que contém o nó solicitado, se possível.

As funções NUMA estendidas [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex), [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex), [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)e [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex) diferem de suas contrapartes não estendidas, pois o número do nó é um valor **UShort** em vez de um **UCHAR**, para acomodar o número potencialmente maior de nós em um sistema com mais de 64 processadores lógicos. Além disso, o processador especificado com ou recuperado pelas funções estendidas inclui o grupo de processadores; o processador especificado com ou recuperado pelas funções não estendidas é relativo ao grupo. Para obter detalhes, consulte os tópicos de referência de função individuais.

Um aplicativo com reconhecimento de grupo pode atribuir todos os seus threads a um nó específico de maneira semelhante à descrita anteriormente neste tópico, usando as funções NUMA estendidas correspondentes. O aplicativo usa [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) para obter a lista de todos os processadores no sistema. Observe que o aplicativo não pode definir a máscara de afinidade de processo, a menos que o processo seja atribuído a um único grupo e o nó pretendido esteja localizado nesse grupo. Normalmente, o aplicativo deve chamar [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity) para limitar seus threads ao nó desejado.


### <a name="behavior-starting-with-windows-10-build-20348"></a>comportamento começando com Windows 10 Build 20348 

> [!NOTE]
> a partir do Windows 10 Build 20348, o comportamento dessa e de outras funções NUMA foi modificado para oferecer melhor suporte a sistemas com nós que contenham mais de 64 processadores.

a criação de nós "falsificados" para acomodar um mapeamento 1:1 entre grupos e nós resultou em comportamentos confusos em que números inesperados de nós NUMA são relatados e, portanto, começando com Windows 10 Build 20348, o sistema operacional foi alterado para permitir que vários grupos sejam associados a um nó e, portanto, agora a topologia NUMA real do sistema pode ser relatada.  

Como parte dessas alterações no sistema operacional, várias APIs NUMA foram alteradas para dar suporte ao relatório de vários grupos que agora podem ser associados a um único nó NUMA. As APIs atualizadas e novas são rotuladas na tabela na seção da **API numa** abaixo.

Como a remoção da divisão de nó pode afetar potencialmente os aplicativos existentes, um valor de registro está disponível para permitir a permissão de volta ao comportamento de divisão de nó herdado. A divisão de nó pode ser reabilitada com a criação de um valor de **REG_DWORD** chamado "SplitLargeNodes" com o valor 1 abaixo de HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\NUMA. As alterações nessa configuração exigem que uma reinicialização entre em vigor.

```powershell
reg add "HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\NUMA" /v SplitLargeNodes /t REG_DWORD /d 1
```

> [!NOTE]
> Os aplicativos que são atualizados para usar a nova funcionalidade de API que relata a verdadeira topologia NUMA continuarão funcionando corretamente em sistemas em que a divisão de nó grande foi reabilitada com essa chave do registro.

O exemplo a seguir demonstra primeiro os possíveis problemas com os processadores de mapeamento de tabelas do para nós NUMA usando as APIs de afinidade herdadas, que não fornecem mais uma capa completa de todos os processadores no sistema, isso pode resultar em uma tabela incompleta. As implicações dessa inintegridade dependem do conteúdo da tabela. Se a tabela simplesmente armazenar o número de nó correspondente, isso provavelmente é apenas um problema de desempenho com processadores descobertos sendo deixados como parte do nó 0. No entanto, se a tabela contiver ponteiros para uma estrutura de contexto por nó, isso poderá resultar em desreferências nulas no tempo de execução.

Em seguida, o exemplo de código ilustra duas soluções alternativas para o problema. A primeira é migrar para as APIs de afinidade de nó de vários grupos (modo de usuário e modo kernel). A segunda é usar **KeQueryLogicalProcessorRelationship** para consultar diretamente o nó numa associado a um determinado número de processador.

```cpp

//
// Problematic implementation using KeQueryNodeActiveAffinity.
//

USHORT CurrentNode;
USHORT HighestNodeNumber;
GROUP_AFFINITY NodeAffinity;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    KeQueryNodeActiveAffinity(CurrentNode, &NodeAffinity, NULL);
    while (NodeAffinity.Mask != 0) {

        ProcessorNumber.Group = NodeAffinity.Group;
        BitScanForward(&ProcessorNumber.Number, NodeAffinity.Mask);

        ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

        ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode;]

        NodeAffinity.Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
    }
}

//
// Resolution using KeQueryNodeActiveAffinity2.
//

USHORT CurrentIndex;
USHORT CurrentNode;
USHORT CurrentNodeAffinityCount;
USHORT HighestNodeNumber;
ULONG MaximumGroupCount;
PGROUP_AFFINITY NodeAffinityMasks;
ULONG ProcessorIndex;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

MaximumGroupCount = KeQueryMaximumGroupCount();
NodeAffinityMasks = ExAllocatePool2(POOL_FLAG_PAGED,
                                    sizeof(GROUP_AFFINITY) * MaximumGroupCount,
                                    'tseT');

if (NodeAffinityMasks == NULL) {
    return STATUS_NO_MEMORY;
}

HighestNodeNumber = KeQueryHighestNodeNumber();
for (CurrentNode = 0; CurrentNode <= HighestNodeNumber; CurrentNode += 1) {

    Status = KeQueryNodeActiveAffinity2(CurrentNode,
                                        NodeAffinityMasks,
                                        MaximumGroupCount,
                                        &CurrentNodeAffinityCount);
    NT_ASSERT(NT_SUCCESS(Status));

    for (CurrentIndex = 0; CurrentIndex < CurrentNodeAffinityCount; CurrentIndex += 1) {

        CurrentAffinity = &NodeAffinityMasks[CurrentIndex];

        while (CurrentAffinity->Mask != 0) {

            ProcessorNumber.Group = CurrentAffinity.Group;
            BitScanForward(&ProcessorNumber.Number, CurrentAffinity->Mask);

            ProcessorIndex = KeGetProcessorIndexFromNumber(&ProcessorNumber);

            ProcessorNodeContexts[ProcessorIndex] = NodeContexts[CurrentNode];

            CurrentAffinity->Mask &= ~((KAFFINITY)1 << ProcessorNumber.Number);
        }
    }
}

//
// Resolution using KeQueryLogicalProcessorRelationship.
//

ULONG ProcessorCount;
ULONG ProcessorIndex;
SYSTEM_LOGICAL_PROCESSOR_INFORMATION_EX ProcessorInformation;
ULONG ProcessorInformationSize;
PROCESSOR_NUMBER ProcessorNumber;
NTSTATUS Status;

ProcessorCount = KeQueryActiveProcessorCountEx(ALL_PROCESSOR_GROUPS);

for (ProcessorIndex = 0; ProcessorIndex < ProcessorCount; ProcessorIndex += 1) {

    Status = KeGetProcessorNumberFromIndex(ProcessorIndex, &ProcessorNumber);
    NT_ASSERT(NT_SUCCESS(Status));

    ProcessorInformationSize = sizeof(ProcessorInformation);
    Status = KeQueryLogicalProcessorRelationship(&ProcessorNumber,
                                                    RelationNumaNode,
                                                    &ProcessorInformation,
                                                    &ProcesorInformationSize);
    NT_ASSERT(NT_SUCCESS(Status));

    NodeNumber = ProcessorInformation.NumaNode.NodeNumber;

    ProcessorNodeContexts[ProcessorIndex] = NodeContexts[NodeNumber];
}
```

## <a name="numa-api"></a>API NUMA

A tabela a seguir descreve a API NUMA.



| Função                                                                     | Descrição                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)      | Aloca páginas de memória física a serem mapeadas e não mapeadas em qualquer região de AWE ( [Address Windowing Extensions](../memory/address-windowing-extensions.md) ) de um processo especificado e especifica o nó numa para a memória física. |
| [**CreateFileMappingNuma**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingnumaw)                      | Cria ou abre um objeto de mapeamento de arquivo nomeado ou sem nome para um arquivo especificado e especifica o nó NUMA para a memória física.                                                                                              |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | atualizado em Windows 10 Build 20348. Recupera informações sobre processadores lógicos e hardwares relacionados.                                                                                                                                                            |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | atualizado em Windows 10 Build 20348. Recupera informações sobre as relações de processadores lógicos e hardwares relacionados.                                                                                                                                       |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)             | Recupera a quantidade de memória disponível no nó especificado.                                                                                                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)         | Recupera a quantidade de memória disponível em um nó especificado como um valor **UShort** .                                                                                                                                             |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)                 | Recupera o nó que atualmente tem o número mais alto.                                                                                                                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)                 | atualizado em Windows 10 Build 20348. Recupera a máscara do processador para o nó especificado.                                                                                                                                                                            |
| [**GetNumaNodeProcessorMask2**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormask2)                         | novo no Windows 10 Build 20348. Recupera a máscara do processador de vários grupos do nó especificado.                                                                                                                                                                          |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)             | atualizado em Windows 10 Build 20348. Recupera a máscara do processador para um nó especificado como um valor **UShort** .                                                                                                                                                        |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                         | Recupera o número do nó do processador especificado.                                                                                                                                                                          |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                     | Recupera o número do nó como um valor **UShort** para o processador especificado.                                                                                                                                                    |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                         | Recupera o número do nó para o identificador de proximidade especificado.                                                                                                                                                               |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                     | Recupera o número do nó como um valor **UShort** para o identificador de proximidade especificado.                                                                                                                                         |
| [**GetProcessDefaultCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocessdefaultcpusetmasks)                     | novo no Windows 10 Build 20348. Recupera a lista de conjuntos de CPU no conjunto padrão de processo que foi definido por SetProcessDefaultCpuSetMasks ou SetProcessDefaultCpuSets.                                                                                                                                         |
| [**GetThreadSelectedCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadselectedcpusetmasks)                     | novo no Windows 10 Build 20348. Define a atribuição de conjuntos de CPU selecionados para o thread especificado. Essa atribuição substitui a atribuição padrão do processo, se houver uma definida.                                                                                                                                          |
| [**MapViewOfFileExNuma**](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)                          | Mapas uma exibição de um mapeamento de arquivo no espaço de endereço de um processo de chamada e especifica o nó NUMA para a memória física.                                                                                                 |
| [**SetProcessDefaultCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessdefaultcpusetmasks)                     | novo no Windows 10 Build 20348. Define a atribuição de conjuntos de CPU padrão para threads no processo especificado.                                                                                                                                          |
| [**SetThreadSelectedCpuSetMasks**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadselectedcpusetmasks)                     | novo no Windows 10 Build 20348. Define a atribuição de conjuntos de CPU selecionados para o thread especificado. Essa atribuição substitui a atribuição padrão do processo, se houver uma definida.                                                                                                                                          |
| [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma)                            | Reserva ou confirma uma região de memória dentro do espaço de endereço virtual do processo especificado e especifica o nó NUMA para a memória física.                                                                          |



 

A função [**QueryWorkingSetEx**](/windows/win32/api/psapi/nf-psapi-queryworkingsetex) pode ser usada para recuperar o nó numa no qual uma página é alocada. Para obter um exemplo, consulte [Alocando memória de um nó numa](../memory/allocating-memory-from-a-numa-node.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Alocando memória de um nó NUMA](../memory/allocating-memory-from-a-numa-node.md)
</dt> <dt>

[Vários processadores](multiple-processors.md)
</dt> <dt>

[Grupos de processadores](processor-groups.md)
</dt> </dl>

 

 
