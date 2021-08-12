---
title: Como executar e sincronizar listas de comandos
description: No Microsoft Direct3D 12, o modo imediato de versões anteriores não está mais presente.
ms.assetid: D5013102-2302-4D66-8F59-079C03BA65FD
keywords:
- lista de comandos
- sincronização
- execução
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41677ee1bc17fb2a935f157d969352617c0d5c3c15eb38a76225b3a8c71e7f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118529136"
---
# <a name="executing-and-synchronizing-command-lists"></a>Como executar e sincronizar listas de comandos

No Microsoft Direct3D 12, o modo imediato de versões anteriores não está mais presente. Em vez disso, os aplicativos criam listas de comandos e pacotes e, em seguida, registram conjuntos de comandos de GPU. As filas de comando são usadas para enviar listas de comandos a serem executadas. Esse modelo permite que os desenvolvedores tenham mais controle sobre o uso eficiente da GPU (unidade de processamento gráfico) e da CPU.

-   [Visão geral da fila de comandos](#command-queue-overview)
-   [Inicializando uma fila de comandos](#initializing-a-command-queue)
-   [Executando listas de comandos](#executing-command-lists)
-   [Acessando recursos de várias filas de comandos](#accessing-resources-from-multiple-command-queues)
-   [Sincronizando a execução da lista de comandos usando limites de fila de comandos](#synchronizing-command-list-execution-using-command-queue-fences)
-   [Sincronizando recursos acessados por filas de comando](#synchronizing-resources-accessed-by-command-queues)
-   [Suporte de fila de comando para recursos de lado](#command-queue-support-for-tiled-resources)
-   [Tópicos relacionados](#related-topics)

## <a name="command-queue-overview"></a>Visão geral da fila de comandos

As filas de comando do Direct3D 12 substituem o tempo de execução e a sincronização de driver do envio de trabalho no modo imediato, anteriormente não expostas ao desenvolvedor, com APIs para gerenciar explicitamente a simultaneidade, o paralelismo e a sincronização. As filas de comando fornecem os seguintes aprimoramentos para os desenvolvedores:

-   Permite que os desenvolvedores evitem ineficiências acidentais causadas pela sincronização inesperada.
-   Permite que os desenvolvedores introduzam a sincronização em um nível mais alto, em que a sincronização necessária pode ser determinada de forma mais eficiente e precisa. Isso significa que o tempo de execução e o driver de gráficos gastarão menos tempo em paralelismo de engenharia reativa.
-   Torna as operações caras mais explícitas.

Esses aprimoramentos habilitam ou aprimoram os seguintes cenários:

-   Maior paralelismo-os aplicativos podem usar filas mais profundas para cargas de trabalho em segundo plano, como decodificação de vídeo, quando têm filas separadas para trabalhos em primeiro plano.
-   Trabalho de GPU de baixa prioridade e assíncrona-o modelo de fila de comandos permite a execução simultânea de trabalho de GPU de baixa prioridade e operações atômicas que permitem que um thread de GPU consuma os resultados de outro thread não sincronizado sem bloqueio.
-   Trabalho de computação de alta prioridade – esse design permite cenários que exigem a interrupção da renderização 3D para fazer uma pequena quantidade de trabalho de computação de alta prioridade para que o resultado possa ser obtido antecipadamente para processamento adicional na CPU.

## <a name="initializing-a-command-queue"></a>Inicializando uma fila de comandos

As filas de comando podem ser criadas chamando [**ID3D12Device:: CreateCommandQueue**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandqueue). Esse método usa um [**\_ tipo de \_ lista \_ de comandos D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type) indicando que tipo de fila deve ser criado e, portanto, que tipo de comandos pode ser enviado para essa fila. Lembre-se de que os pacotes só podem ser chamados de listas de comandos diretos e não podem ser enviados diretamente para uma fila. Os tipos de fila com suporte são:

-   [**\_Tipo de lista de comandos D3D12 \_ \_ \_ direto**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**\_Tipo de lista de comandos D3D12 \_ \_ \_ computação**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**\_Cópia do \_ tipo de lista de comandos D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)

Em geral, filas DIRETAs e listas de comandos aceitam qualquer comando, filas de computação e listas de comandos aceitam comandos de computação e cópia relacionados, e filas de cópia e listas de comandos aceitam apenas comandos de cópia.

## <a name="executing-command-lists"></a>Executando listas de comandos

Depois de gravar uma lista de comandos e recuperar a fila de comandos padrão ou criar uma nova, execute as listas de comandos chamando [**ID3D12CommandQueue:: ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

Os aplicativos podem enviar listas de comandos para qualquer fila de comandos de vários threads. O tempo de execução executará o trabalho de serialização dessas solicitações na ordem de envio.

O tempo de execução validará a lista de comandos enviados e descartará a chamada para [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) se qualquer uma das restrições for violada. As chamadas serão descartadas pelos seguintes motivos:

-   A lista de comandos fornecida é um pacote, não uma lista de comandos diretos.
-   [**ID3D12GraphicsCommandList:: Close**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close) não foi chamado na lista de comandos fornecida para concluir a gravação.
-   [**ID3D12CommandAllocator:: Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandallocator-reset) foi chamado no alocador de comando associado à lista de comandos, pois ele foi gravado. Para obter mais informações sobre os alocadores de comando, consulte [criando e gravando listas de comandos e pacotes](recording-command-lists-and-bundles.md).
-   O limite de fila de comando indica que uma execução anterior da lista de comandos ainda não foi concluída. Os limites de fila de comando são discutidos em detalhes abaixo.
-   Os Estados de consultas before e After, definidos com chamadas para [**ID3D12GraphicsCommandList:: BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) e [**ID3D12GraphicsCommandList:: endquery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery), não são correspondidos corretamente.
-   Os Estados de antes e depois de barreiras de transição de recursos não são correspondidos corretamente. Para obter mais informações, consulte [usando barreiras de recursos para sincronizar Estados de recursos](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="accessing-resources-from-multiple-command-queues"></a>Acessando recursos de várias filas de comandos

Há algumas regras impostas pelo tempo de execução que restringem o acesso de recursos de várias filas de comandos. Essas regras são as seguintes:

1. Um recurso não pode ser gravado a partir de várias filas de comandos simultaneamente. Quando um recurso é transferido para um estado gravável em uma fila, ele é considerado exclusivamente de propriedade da fila e deve fazer a transição para um estado de leitura ou comum (consulte [**D3D12_RESOURCE_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)) antes que ele possa ser acessado por outra fila.

2. Quando em um estado de leitura, um recurso pode ser lido de várias filas de comando simultaneamente, incluindo entre processos, com base em seu estado de leitura.

Para obter mais informações sobre as restrições de acesso de recursos e o uso de barreiras de recursos para sincronizar o acesso aos recursos, consulte [usando barreiras de recursos para sincronizar Estados de recursos](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="synchronizing-command-list-execution-using-command-queue-fences"></a>Sincronizando a execução da lista de comandos usando limites de fila de comandos

O suporte para várias filas de comandos paralelos no Direct3D 12 oferece mais flexibilidade e controle sobre a priorização do trabalho assíncrono na GPU. Esse design também significa que os aplicativos precisam gerenciar explicitamente a sincronização do trabalho, especialmente quando as listas de comandos em uma fila dependem dos recursos que estão sendo operados por outra fila de comandos. Alguns exemplos disso incluem aguardar a conclusão de uma operação em uma fila de computação para que o resultado possa ser usado para uma operação de renderização na fila 3D e aguardar a conclusão de uma operação 3D para que uma operação na fila de computação possa acessar um recurso para gravação. Para habilitar a sincronização de trabalho entre as filas, o Direct3D 12 usa o conceito de limites, que são representados na API pela interface [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) .

Uma cerca é um inteiro que representa a unidade de trabalho atual que está sendo processada. Quando o aplicativo avança a cerca, chamando [**ID3D12CommandQueue:: Signal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal), o inteiro é atualizado. Os aplicativos podem verificar o valor de uma cerca e determinar se uma unidade de trabalho foi concluída para decidir se uma operação subsequente pode ser iniciada.

## <a name="synchronizing-resources-accessed-by-command-queues"></a>Sincronizando recursos acessados por filas de comando

No Direct3D 12, a sincronização do estado de alguns recursos é implementada com barreiras de recursos. Em cada barreira de recurso, um aplicativo declara os Estados de antes e depois de um recurso. Um exemplo comum é para um recurso para fazer a transição entre uma exibição de recurso do sombreador para uma exibição de destino de renderização. Para a maior parte, essas barreiras de recursos são gerenciadas nas listas de comandos. Quando as camadas de depuração são habilitadas, o sistema impõe que os Estados de antes e depois de todos os recursos correspondam, garantindo que o recurso esteja no estado correto para uma operação específica em uma transição de barreira.

Para obter mais informações sobre a sincronização do estado do recurso, consulte [usando barreiras de recursos para sincronizar Estados de recursos](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="command-queue-support-for-tiled-resources"></a>Suporte de fila de comando para recursos de lado

Os métodos para gerenciar os recursos de ladrilhos, que foram expostos por meio da interface [**ID3D11DeviceContext2**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) no Direct3D 11, são fornecidos pela interface [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) no Direct3D 12. Esses métodos incluem:



| Método                                                              | Descrição                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings)     | Copia mapeamentos de um recurso de origem para o lado a lado em um recurso de destino.<br/>                 |
| [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) | Atualiza os mapeamentos de locais de bloco em recursos de blocos gráficos para locais de memória em um heap de recursos.<br/> |



 

Para obter mais informações sobre como usar os recursos de lado do xadrez nos aplicativos do Direct3D 12, consulte [Direct3D11s em ladrilhos](/windows/desktop/direct3d11/tiled-resources).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Envio de trabalho no Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

