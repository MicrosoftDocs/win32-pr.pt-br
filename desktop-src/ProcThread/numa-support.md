---
description: O modelo tradicional para suporte multiprocessador é o SMP (multiprocessador simétrico). Nesse modelo, cada processador tem acesso igual à memória e e/s. À medida que mais processadores são adicionados, o barramento do processador torna-se uma limitação para o desempenho do sistema.
ms.assetid: a1263968-2b26-45cc-bdd7-6aa354821a5a
title: Suporte a NUMA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 559df7d4e13571953f2826188bd80ccbc472b2ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759608"
---
# <a name="numa-support"></a>Suporte a NUMA

O modelo tradicional para suporte multiprocessador é o SMP (multiprocessador simétrico). Nesse modelo, cada processador tem acesso igual à memória e e/s. À medida que mais processadores são adicionados, o barramento do processador torna-se uma limitação para o desempenho do sistema.

Os designers do sistema usam o NUMA (acesso não uniforme à memória) para aumentar a velocidade do processador sem aumentar a carga no barramento do processador. A arquitetura não é uniforme porque cada processador está perto de algumas partes da memória e mais distante de outras partes da memória. O processador rapidamente obtém acesso à memória em que está perto, enquanto pode levar mais tempo para obter acesso à memória que está mais distante.

Em um sistema NUMA, as CPUs são organizadas em sistemas menores chamados *nós*. Cada nó tem seus próprios processadores e memória e está conectado ao sistema maior por meio de um barramento de interconexão coerente com o cache.

O sistema tenta melhorar o desempenho agendando threads em processadores que estão no mesmo nó que a memória que está sendo usada. Ele tenta satisfazer as solicitações de alocação de memória de dentro do nó, mas alocará memória de outros nós, se necessário. Ele também fornece uma API para tornar a topologia do sistema disponível para os aplicativos. Você pode melhorar o desempenho de seus aplicativos usando as funções de NUMA para otimizar o uso de memória e agendamento.

Em primeiro lugar, será necessário determinar o layout dos nós no sistema. Para recuperar o nó numerado mais alto no sistema, use a função [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber) . Observe que esse número não é garantido como igual ao número total de nós no sistema. Além disso, não há garantia de que os nós com números sequenciais estejam próximos juntos. Para recuperar a lista de processadores no sistema, use a função [**GetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-getprocessaffinitymask) . Você pode determinar o nó para cada processador na lista usando a função [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode) . Como alternativa, para recuperar uma lista de todos os processadores em um nó, use a função [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask) .

Depois de determinar quais processadores pertencem a quais nós, você pode otimizar o desempenho do aplicativo. Para garantir que todos os threads do processo sejam executados no mesmo nó, use a função [**SetProcessAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setprocessaffinitymask) com uma máscara de afinidade de processo que especifique os processadores no mesmo nó. Isso aumenta a eficiência dos aplicativos cujos threads precisam acessar a mesma memória. Como alternativa, para limitar o número de threads em cada nó, use a função [**SetThreadAffinityMask**](/windows/desktop/api/WinBase/nf-winbase-setthreadaffinitymask) .

Aplicativos com uso intensivo de memória precisarão otimizar seu uso de memória. Para recuperar a quantidade de memória livre disponível para um nó, use a função [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode) . A função [**VirtualAllocExNuma**](/windows/win32/api/memoryapi/nf-memoryapi-virtualallocexnuma) permite que o aplicativo especifique um nó preferencial para a alocação de memória. O **VirtualAllocExNuma** não aloca nenhuma página física, portanto, será bem sucedido se as páginas estão disponíveis ou não nesse nó ou em outro lugar no sistema. As páginas físicas são alocadas sob demanda. Se o nó preferencial for executado fora de páginas, o Gerenciador de memória usará páginas de outros nós. Se a memória for paginada, o mesmo processo será usado quando for retornado.

### <a name="numa-support-on-systems-with-more-than-64-logical-processors"></a>Suporte a NUMA em sistemas com mais de 64 processadores lógicos

Em sistemas com mais de 64 processadores lógicos, os nós são atribuídos a [grupos de processadores](processor-groups.md) de acordo com a capacidade dos nós. A capacidade de um nó é o número de processadores que estão presentes quando o sistema é iniciado junto com quaisquer processadores lógicos adicionais que podem ser adicionados enquanto o sistema está em execução.

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Não há suporte para grupos de processador.

Cada nó deve estar totalmente contido em um grupo. Se as capacidades dos nós forem relativamente pequenas, o sistema atribuirá mais de um nó ao mesmo grupo, escolhendo os nós que estão fisicamente próximos um do outro para melhorar o desempenho. Se a capacidade de um nó exceder o número máximo de processadores em um grupo, o sistema dividirá o nó em vários nós menores, cada um pequeno o suficiente para caber em um grupo.

Um nó NUMA ideal para um novo processo pode ser solicitado usando o atributo estendido do [**atributo de thread proc de \_ \_ \_ \_ nó de preferência**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-updateprocthreadattribute) quando o processo é criado. Como um processador ideal para thread, o nó ideal é uma dica para o Agendador, que atribui o novo processo ao grupo que contém o nó solicitado, se possível.

As funções NUMA estendidas [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex), [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex), [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)e [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex) diferem de suas contrapartes não estendidas, pois o número do nó é um valor **UShort** em vez de um **UCHAR**, para acomodar o número potencialmente maior de nós em um sistema com mais de 64 processadores lógicos. Além disso, o processador especificado com ou recuperado pelas funções estendidas inclui o grupo de processadores; o processador especificado com ou recuperado pelas funções não estendidas é relativo ao grupo. Para obter detalhes, consulte os tópicos de referência de função individuais.

Um aplicativo com reconhecimento de grupo pode atribuir todos os seus threads a um nó específico de maneira semelhante à descrita anteriormente neste tópico, usando as funções NUMA estendidas correspondentes. O aplicativo usa [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) para obter a lista de todos os processadores no sistema. Observe que o aplicativo não pode definir a máscara de afinidade de processo, a menos que o processo seja atribuído a um único grupo e o nó pretendido esteja localizado nesse grupo. Normalmente, o aplicativo deve chamar [**SetThreadGroupAffinity**](/windows/win32/api/processtopologyapi/nf-processtopologyapi-setthreadgroupaffinity) para limitar seus threads ao nó desejado.

## <a name="numa-api"></a>API NUMA

A tabela a seguir descreve a API NUMA.



| Função                                                                     | Descrição                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllocateUserPhysicalPagesNuma**](/windows/win32/api/memoryapi/nf-memoryapi-allocateuserphysicalpagesnuma)      | Aloca páginas de memória física a serem mapeadas e não mapeadas em qualquer região de AWE ( [Address Windowing Extensions](../memory/address-windowing-extensions.md) ) de um processo especificado e especifica o nó numa para a memória física. |
| [**CreateFileMappingNuma**](/windows/win32/api/memoryapi/nf-memoryapi-createfilemappingnumaw)                      | Cria ou abre um objeto de mapeamento de arquivo nomeado ou sem nome para um arquivo especificado e especifica o nó NUMA para a memória física.                                                                                              |
| [**GetLogicalProcessorInformation**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformation)     | Recupera informações sobre processadores lógicos e hardwares relacionados.                                                                                                                                                            |
| [**GetLogicalProcessorInformationEx**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getlogicalprocessorinformationex) | Recupera informações sobre as relações de processadores lógicos e hardwares relacionados.                                                                                                                                       |
| [**GetNumaAvailableMemoryNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynode)             | Recupera a quantidade de memória disponível no nó especificado.                                                                                                                                                                 |
| [**GetNumaAvailableMemoryNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaavailablememorynodeex)         | Recupera a quantidade de memória disponível em um nó especificado como um valor **UShort** .                                                                                                                                             |
| [**GetNumaHighestNodeNumber**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumahighestnodenumber)                 | Recupera o nó que atualmente tem o número mais alto.                                                                                                                                                                       |
| [**GetNumaNodeProcessorMask**](/windows/desktop/api/WinBase/nf-winbase-getnumanodeprocessormask)                 | Recupera a máscara do processador para o nó especificado.                                                                                                                                                                            |
| [**GetNumaNodeProcessorMaskEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumanodeprocessormaskex)             | Recupera a máscara do processador para um nó especificado como um valor **UShort** .                                                                                                                                                        |
| [**GetNumaProcessorNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornode)                         | Recupera o número do nó do processador especificado.                                                                                                                                                                          |
| [**GetNumaProcessorNodeEx**](/windows/desktop/api/WinBase/nf-winbase-getnumaprocessornodeex)                     | Recupera o número do nó como um valor **UShort** para o processador especificado.                                                                                                                                                    |
| [**GetNumaProximityNode**](/windows/desktop/api/WinBase/nf-winbase-getnumaproximitynode)                         | Recupera o número do nó para o identificador de proximidade especificado.                                                                                                                                                               |
| [**GetNumaProximityNodeEx**](/windows/win32/api/systemtopologyapi/nf-systemtopologyapi-getnumaproximitynodeex)                     | Recupera o número do nó como um valor **UShort** para o identificador de proximidade especificado.                                                                                                                                         |
| [**MapViewOfFileExNuma**](/windows/win32/api/winbase/nf-winbase-mapviewoffileexnuma)                          | Mapeia uma exibição de um mapeamento de arquivo para o espaço de endereço de um processo de chamada e especifica o nó NUMA para a memória física.                                                                                                 |
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

 

 
