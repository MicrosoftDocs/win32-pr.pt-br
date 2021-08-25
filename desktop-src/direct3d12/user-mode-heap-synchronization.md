---
title: Sincronização de vários mecanismos
description: Este tópico aborda a sincronização do acesso aos vários mecanismos independentes encontrados nas GPUs mais modernas.
ms.assetid: 93903F50-A6CA-41C2-863D-68D645586B4C
ms.localizationpriority: high
ms.topic: article
ms.date: 09/25/2019
ms.openlocfilehash: 2d250133d8cacb26d933d3774f397de4c949c72b7b58114759791c103d374c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987538"
---
# <a name="multi-engine-synchronization"></a>Sincronização de vários mecanismos

A maioria das GPUs modernas contém vários mecanismos independentes que fornecem funcionalidade especializada. Muitos têm um ou mais mecanismos de cópia dedicados e um mecanismo de computação, geralmente distintos do mecanismo 3D. Cada um desses mecanismos pode executar comandos em paralelo entre si. O Direct3D 12 fornece acesso fino aos mecanismos 3D, computação e cópia, usando filas e listas de comandos.

## <a name="gpu-engines"></a>Mecanismos de GPU

O diagrama a seguir mostra os threads de CPU de um título, cada um preenchendo uma ou mais das filas de cópia, computação e 3D. A fila 3D pode conduzir todos os três mecanismos de GPU; a fila de computação pode impulsionar os mecanismos de computação e cópia; e a fila de cópia simplesmente o mecanismo de cópia.

À medida que os diferentes threads preenchem as filas, não pode haver nenhuma garantia simples da ordem de execução, portanto, a necessidade de mecanismos de sincronização quando o &mdash; título as exigir.

![quatro threads enviando comandos para três filas](images/gpu-engines.png)

A imagem a seguir ilustra como um título pode agendar o trabalho em vários mecanismos de GPU, incluindo a sincronização entre mecanismos quando necessário: mostra as cargas de trabalho por mecanismo com dependências entre mecanismos. Neste exemplo, o mecanismo de cópia primeiro copia alguma geometria necessária para renderização. O mecanismo 3D aguarda a conclusão dessas cópias e renderiza uma passagem prévia da geometria. Em seguida, isso é consumido pelo mecanismo de computação. Os resultados da Expedição do mecanismo de [**computação,**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)juntamente com várias operações de cópia de textura no mecanismo de cópia, são consumidos pelo mecanismo 3D para a chamada final de [**Desenho.**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-drawinstanced)

![copiar, gráficos e mecanismos de computação se comunicando](images/gpu-sync.png)

O pseudocódigo a seguir ilustra como um título pode enviar tal carga de trabalho.

``` syntax
// Get per-engine contexts. Note that multiple queues may be exposed
// per engine, however that design is not reflected here.
copyEngine = device->GetCopyEngineContext();
renderEngine = device->GetRenderEngineContext();
computeEngine = device->GetComputeEngineContext();
copyEngine->CopyResource(geometry, ...); // copy geometry
copyEngine->Signal(copyFence, 101);
copyEngine->CopyResource(tex1, ...); // copy textures
copyEngine->CopyResource(tex2, ...); // copy more textures
copyEngine->CopyResource(tex3, ...); // copy more textures
copyEngine->CopyResource(tex4, ...); // copy more textures
copyEngine->Signal(copyFence, 102);
renderEngine->Wait(copyFence, 101); // geometry copied
renderEngine->Draw(); // pre-pass using geometry only into rt1
renderEngine->Signal(renderFence, 201);
computeEngine->Wait(renderFence, 201); // prepass completed
computeEngine->Dispatch(); // lighting calculations on pre-pass (using rt1 as SRV)
computeEngine->Signal(computeFence, 301);
renderEngine->Wait(computeFence, 301); // lighting calculated into buf1
renderEngine->Wait(copyFence, 102); // textures copied
renderEngine->Draw(); // final render using buf1 as SRV, and tex[1-4] SRVs
```

O pseudocódigo a seguir ilustra a sincronização entre a cópia e os mecanismos 3D para realizar a alocação de memória em forma de heap por meio de um buffer de anéis. Os títulos têm a flexibilidade de escolher o equilíbrio certo entre maximizar o paralelismo (por meio de um buffer grande) e reduzir o consumo e a latência de memória (por meio de um buffer pequeno).

``` syntax
device->CreateBuffer(&ringCB);
for(int i=1;i++){
  if(i > length) copyEngine->Wait(fence1, i - length);
  copyEngine->Map(ringCB, value%length, WRITE, pData); // copy new data
  copyEngine->Signal(fence2, i);
  renderEngine->Wait(fence2, i);
  renderEngine->Draw(); // draw using copied data
  renderEngine->Signal(fence1, i);
}

// example for length = 3:
// copyEngine->Map();
// copyEngine->Signal(fence2, 1); // fence2 = 1  
// copyEngine->Map();
// copyEngine->Signal(fence2, 2); // fence2 = 2
// copyEngine->Map();
// copyEngine->Signal(fence2, 3); // fence2 = 3
// copy engine has exhausted the ring buffer, so must wait for render to consume it
// copyEngine->Wait(fence1, 1); // fence1 == 0, wait
// renderEngine->Wait(fence2, 1); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 1); // fence1 = 1, copy engine now unblocked
// renderEngine->Wait(fence2, 2); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 2); // fence1 = 2
// renderEngine->Wait(fence2, 3); // fence2 == 3, pass
// renderEngine->Draw();
// renderEngine->Signal(fence1, 3); // fence1 = 3
// now render engine is starved, and so must wait for the copy engine
// renderEngine->Wait(fence2, 4); // fence2 == 3, wait
```

## <a name="multi-engine-scenarios"></a>Cenários de vários mecanismos

O Direct3D 12 permite que você evite acidentalmente ter ineficiências causadas por atrasos de sincronização inesperados. Ele também permite que você introduza a sincronização em um nível mais alto em que a sincronização necessária pode ser determinada com maior certeza. Um segundo problema que os vários mecanismos resolvem é tornar as operações caras mais explícitas, o que inclui transições entre 3D e vídeo que eram tradicionalmente dispendiosas devido à sincronização entre vários contextos de kernel.

Em particular, os cenários a seguir podem ser abordados com o Direct3D 12.

-   Trabalho de GPU assíncrona e de baixa prioridade. Isso permite a execução simultânea de operações atômicas e de trabalho de GPU de baixa prioridade que permitem que um thread de GPU consuma os resultados de outro thread não sincronizado sem bloqueio.
-   Trabalho de computação de alta prioridade. Com a computação em segundo plano, é possível interromper a renderização 3D para fazer uma pequena quantidade de trabalho de computação de alta prioridade. Os resultados desse trabalho podem ser obtidos no início para processamento adicional na CPU.
-   Trabalho de computação em segundo plano. Uma fila de baixa prioridade separada para cargas de trabalho de computação permite que um aplicativo utilize ciclos de GPU sobressalente para executar a computação em segundo plano sem impacto negativo nas tarefas de renderização primária (ou outras). As tarefas em segundo plano podem incluir a descompactação de recursos ou a atualização de simulações ou estruturas de aceleração. As tarefas em segundo plano devem ser sincronizadas na CPU raramente (aproximadamente uma vez por quadro) para evitar a parada ou a lentidão do trabalho em primeiro plano.
-   Streaming e carregamento de dados. Uma fila de cópia separada substitui os conceitos D3D11 de dados iniciais e recursos de atualização. Embora o aplicativo seja responsável por mais detalhes no modelo direct3D 12, essa responsabilidade vem com potência. O aplicativo pode controlar a memória do sistema dedicada ao armazenamento em buffer de dados de upload. O aplicativo pode escolher quando e como (CPU vs GPU, bloqueando versus sem bloqueio) para sincronizar e pode acompanhar o progresso e controlar a quantidade de trabalho na fila.
-   Maior paralelismo. Os aplicativos podem usar filas mais profundas para cargas de trabalho em segundo plano (por exemplo, decodificar vídeo) quando têm filas separadas para trabalho em primeiro plano.

No Direct3D 12, o conceito de uma fila de comandos é a representação de API de uma sequência de trabalho aproximadamente serial enviada pelo aplicativo. Barreiras e outras técnicas permitem que esse trabalho seja executado em um pipeline ou fora de ordem, mas o aplicativo vê apenas uma única linha do tempo de conclusão. Isso corresponde ao contexto imediato em D3D11.

## <a name="synchronization-apis"></a>APIs de sincronização

### <a name="devices-and-queues"></a>Dispositivos e filas

O dispositivo Direct3D 12 tem métodos para criar e recuperar filas de comandos de diferentes tipos e prioridades. A maioria dos aplicativos deve usar as filas de comandos padrão porque elas permitem o uso compartilhado por outros componentes. Aplicativos com requisitos de competência adicionais podem criar filas adicionais. As filas são especificadas pelo tipo de lista de comandos que consomem.

Consulte os seguintes métodos de criação de [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device).

-   [**CreateCommandQueue:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandqueue) cria uma fila de comandos com base nas informações em uma estrutura [**\_ \_ \_ DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_command_queue_desc) da FILA de COMANDOS do Direct3D 12.
-   [**CreateCommandList:**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist) cria uma lista de comandos do tipo [**DIRECT3D 12 \_ COMMAND LIST \_ \_ TYPE**](/windows/win32/api/d3d12/ne-d3d12-d3d12_command_list_type).
-   [**CreateFence**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createfence) : cria uma cerca, notando os sinalizadores em [**SINALIZADORES \_ DE \_ CERCA do Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_fence_flags). As cercas são usadas para sincronizar filas.

As filas de todos os tipos (3D, computação e cópia) compartilham a mesma interface e são baseadas em lista de comandos.

Consulte os seguintes métodos de [**ID3D12CommandQueue.**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue)

-   [**ExecuteCommandLists:**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) envia uma matriz de listas de comandos para execução. Cada lista de comandos que está sendo [**definida por ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist).
-   [**Sinal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) : define um valor de cerca quando a fila (em execução na GPU) atinge um determinado ponto.
-   [**Wait**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-wait) : a fila aguarda até que o cerca especificado atinja o valor especificado.

Observe que os pacotes não são consumidos por nenhuma fila e, portanto, esse tipo não pode ser usado para criar uma fila.

### <a name="fences"></a>Limites

A API de vários mecanismos fornece APIs explícitas para criar e sincronizar usando cercas. Um fence é um constructo de sincronização controlado por um valor UINT64. Os valores de cerca são definidos pelo aplicativo. Uma operação de sinal modifica o valor de cerca e uma operação de espera bloqueia até que o bloqueio tenha atingido o valor solicitado ou superior. Um evento pode ser acionado quando uma cerca atinge um determinado valor.

Consulte os métodos da interface [**ID3D12Fence.**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)

-   [**GetCompletedValue**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-getcompletedvalue) : retorna o valor atual da cerca.
-   [**SetEventOnCompletion:**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-seteventoncompletion) faz com que um evento seja a incêndio quando o cerca atinge um determinado valor.
-   [**Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) : define o cerca para o valor determinado.

As cercas permitem o acesso da CPU ao valor de cerca atual e as esperas e sinais da CPU.

O [**método Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12fence-signal) na interface [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) atualiza uma cerca do lado da CPU. Essa atualização ocorre imediatamente. O [**método Signal**](/windows/win32/api/d3d12/nf-d3d12-id3d12commandqueue-signal) em [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) atualiza uma cerca do lado da GPU. Essa atualização ocorre depois que todas as outras operações na fila de comandos são concluídas.

Todos os nós em uma configuração de vários mecanismos podem ler e reagir a qualquer cerca que alcance o valor correto.

Os aplicativos configuram seus próprios valores de cerca, um bom ponto de partida pode estar aumentando uma cerca uma vez por quadro.

Um cerca *pode* ser *remado.* Isso significa que o valor de cerca não precisa incrementar exclusivamente. Se  uma operação signal for enfilfilada em duas filas de comandos diferentes ou se dois threads de CPU estão chamando **Signal** em uma cerca, pode haver uma corrida para determinar qual **Signal** é concluído por último e, portanto, qual valor de cerca será aquele que permanecerá. Se uma cerca for refeita, quaisquer novas esperas (incluindo solicitações **SetEventOnCompletion)** serão comparadas com o novo valor de cerca inferior e, portanto, poderão não ser atendidas, mesmo que o valor de cerca tenha sido anteriormente alto o suficiente para satisfazê-los. Se ocorrer uma corrida, entre um valor que atenderá a uma espera  pendente e um valor menor que não, a espera será atendida, independentemente de qual valor permanecerá posteriormente.

As APIs de cerca fornecem uma funcionalidade de sincronização avançada, mas podem criar problemas potencialmente difíceis de depurar. É recomendável que cada cerca seja usada apenas para indicar o progresso em uma linha do tempo para evitar problemas entre os sinalistas.

### <a name="copy-and-compute-command-lists"></a>Copiar e computar listas de comandos

Todos os três tipos de lista de comandos usam a interface [**ID3D12GraphicsCommandList,**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) no entanto, somente um subconjunto dos métodos tem suporte para cópia e computação.

As listas de comandos copiar e computar podem usar os métodos a seguir.

-   [**Perto**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close)
-   [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion)
-   [**CopyResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)
-   [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)
-   [**CopyTiles**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytiles)
-   [**Redefinir**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-reset)
-   [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier)

As listas de comandos de computação também podem usar os métodos a seguir.

-   [**ClearState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate)
-   [**ClearUnorderedAccessViewFloat**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewfloat)
-   [**ClearUnorderedAccessViewUint**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearunorderedaccessviewuint)
-   [**DiscardResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-discardresource)
-   [**Dispatch**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-dispatch)
-   [**ExecuteIndirect**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect)
-   [**SetComputeRoot32BitConstant**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstant)
-   [**SetComputeRoot32BitConstants**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputeroot32bitconstants)
-   [**SetComputeRootConstantBufferView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootconstantbufferview)
-   [**SetComputeRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable)
-   [**SetComputeRootShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootshaderresourceview)
-   [**SetComputeRootSignature**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootsignature)
-   [**SetComputeRootUnorderedAccessView**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootunorderedaccessview)
-   [**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)
-   [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate)
-   [**SetPredication**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpredication)

As listas de comandos de computação devem definir um PSO de computação ao chamar [**Setpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

Os grupos não podem ser usados com listas de comandos ou filas de computação ou cópia.

## <a name="pipelined-compute-and-graphics-example"></a>Exemplo de computação e gráficos em pipeline

Este exemplo mostra como a sincronização de isolamento pode ser usada para criar um pipeline de trabalho de computação em uma fila (referenciada por `pComputeQueue` ) que é consumida por gráficos funcionam na fila `pGraphicsQueue` . O trabalho de computação e gráficos é canalizado com a fila de gráficos que consome o resultado do trabalho de computação de vários quadros de volta e um evento de CPU é usado para limitar o total de trabalhos na fila geral.

```cpp
void PipelinedComputeGraphics()
{
    const UINT CpuLatency = 3;
    const UINT ComputeGraphicsLatency = 2;

    HANDLE handle = CreateEvent(nullptr, FALSE, FALSE, nullptr);

    UINT64 FrameNumber = 0;

    while (1)
    {
        if (FrameNumber > ComputeGraphicsLatency)
        {
            pComputeQueue->Wait(pGraphicsFence,
                FrameNumber - ComputeGraphicsLatency);
        }

        if (FrameNumber > CpuLatency)
        {
            pComputeFence->SetEventOnFenceCompletion(
                FrameNumber - CpuLatency,
                handle);
            WaitForSingleObject(handle, INFINITE);
        }

        ++FrameNumber;

        pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
        pComputeQueue->Signal(pComputeFence, FrameNumber);
        if (FrameNumber > ComputeGraphicsLatency)
        {
            UINT GraphicsFrameNumber = FrameNumber - ComputeGraphicsLatency;
            pGraphicsQueue->Wait(pComputeFence, GraphicsFrameNumber);
            pGraphicsQueue->ExecuteCommandLists(1, &pGraphicsCommandList);
            pGraphicsQueue->Signal(pGraphicsFence, GraphicsFrameNumber);
        }
    }
}
```

Para dar suporte a esse pipeline, deve haver um buffer de `ComputeGraphicsLatency+1` cópias diferentes dos dados que passam da fila de computação para a fila de gráficos. As listas de comandos devem usar UAVs e indireção para ler e gravar a partir da "versão" apropriada dos dados no buffer. A fila de computação deve aguardar até que a fila de gráficos termine de ler os dados do quadro N antes que ele possa gravar o quadro `N+ComputeGraphicsLatency` .

Observe que a quantidade de filas de computação trabalhadas em relação à CPU não depende diretamente da quantidade de buffer necessária, no entanto, o trabalho da GPU de enfileiramento além da quantidade de espaço disponível no buffer é menos valioso.

Um mecanismo alternativo para evitar o indireção seria criar várias listas de comandos correspondentes a cada uma das versões "renomeadas" dos dados. O exemplo a seguir usa essa técnica enquanto estende o exemplo anterior para permitir que as filas de computação e gráficos sejam executadas de forma assíncrona.

## <a name="asynchronous-compute-and-graphics-example"></a>Exemplo de computação assíncrona e gráficos

Este exemplo a seguir permite que os gráficos sejam renderizados de forma assíncrona da fila de computação. Ainda há uma quantidade fixa de dados armazenados em buffer entre os dois estágios; no entanto, agora o trabalho gráfico funciona de forma independente e usa o resultado mais atualizado do estágio de computação como conhecido na CPU quando o trabalho de gráficos é colocado na fila. Isso seria útil se o trabalho de gráficos estivesse sendo atualizado por outra fonte, por exemplo, entrada do usuário. Deve haver várias listas de comandos para permitir que os `ComputeGraphicsLatency` quadros de trabalho de gráficos estejam em trânsito por vez e a função `UpdateGraphicsCommandList` represente a atualização da lista de comandos para incluir os dados de entrada mais recentes e ler os dados de computação do buffer apropriado.

A fila de computação ainda deve aguardar a conclusão da fila de gráficos com os buffers de pipe, mas uma terceira cerca ( `pGraphicsComputeFence` ) é introduzida para que o progresso dos gráficos de leitura do trabalho de computação versus o progresso de gráficos em geral possa ser acompanhado. Isso reflete o fato de que agora quadros gráficos consecutivos podiam ler do mesmo resultado de computação ou podem ignorar um resultado de computação. Um design mais eficiente, mas ligeiramente mais complicado, usaria apenas a única cerca de gráficos e armazenaria um mapeamento para os quadros de computação usados por cada quadro de gráficos.

```cpp
void AsyncPipelinedComputeGraphics()
{
    const UINT CpuLatency{ 3 };
    const UINT ComputeGraphicsLatency{ 2 };

    // The compute fence is at index 0; the graphics fence is at index 1.
    ID3D12Fence* rgpFences[]{ pComputeFence, pGraphicsFence };
    HANDLE handles[2];
    handles[0] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    handles[1] = CreateEvent(nullptr, FALSE, TRUE, nullptr);
    UINT FrameNumbers[]{ 0, 0 };

    ID3D12GraphicsCommandList* rgpGraphicsCommandLists[CpuLatency];
    CreateGraphicsCommandLists(ARRAYSIZE(rgpGraphicsCommandLists),
        rgpGraphicsCommandLists);

    // Graphics needs to wait for the first compute frame to complete; this is the
    // only wait that the graphics queue will perform.
    pGraphicsQueue->Wait(pComputeFence, 1);

    while (true)
    {
        for (auto i = 0; i < 2; ++i)
        {
            if (FrameNumbers[i] > CpuLatency)
            {
                rgpFences[i]->SetEventOnCompletion(
                    FrameNumbers[i] - CpuLatency,
                    handles[i]);
            }
            else
            {
                ::SetEvent(handles[i]);
            }
        }


        auto WaitResult = ::WaitForMultipleObjects(2, handles, FALSE, INFINITE);
        if (WaitResult > WAIT_OBJECT_0 + 1) continue;
        auto Stage = WaitResult - WAIT_OBJECT_0;
        ++FrameNumbers[Stage];

        switch (Stage)
        {
        case 0:
        {
            if (FrameNumbers[Stage] > ComputeGraphicsLatency)
            {
                pComputeQueue->Wait(pGraphicsComputeFence,
                    FrameNumbers[Stage] - ComputeGraphicsLatency);
            }
            pComputeQueue->ExecuteCommandLists(1, &pComputeCommandList);
            pComputeQueue->Signal(pComputeFence, FrameNumbers[Stage]);
            break;
        }
        case 1:
        {
            // Recall that the GPU queue started with a wait for pComputeFence, 1
            UINT64 CompletedComputeFrames = min(1,
                pComputeFence->GetCompletedValue());
            UINT64 PipeBufferIndex =
                (CompletedComputeFrames - 1) % ComputeGraphicsLatency;
            UINT64 CommandListIndex = (FrameNumbers[Stage] - 1) % CpuLatency;
            // Update graphics command list based on CPU input and using the appropriate
            // buffer index for data produced by compute.
            UpdateGraphicsCommandList(PipeBufferIndex,
                rgpGraphicsCommandLists[CommandListIndex]);

            // Signal *before* new rendering to indicate what compute work
            // the graphics queue is DONE with
            pGraphicsQueue->Signal(pGraphicsComputeFence, CompletedComputeFrames - 1);
            pGraphicsQueue->ExecuteCommandLists(1,
                rgpGraphicsCommandLists + PipeBufferIndex);
            pGraphicsQueue->Signal(pGraphicsFence, FrameNumbers[Stage]);
            break;
        }
        }
    }
}
```

## <a name="multi-queue-resource-access"></a>Acesso a recursos de várias filas

Para acessar um recurso em mais de uma fila, um aplicativo deve aderir às regras a seguir.

-   O acesso aos recursos (consulte os [**\_ \_ Estados de recursos do Direct3D 12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_resource_states)) é determinado pelo objeto classe tipo fila não fila. Há duas classes de tipo de fila: a fila de computação/3D é de uma classe de tipo, a cópia é uma segunda classe de tipo. Portanto, um recurso que tem uma barreira para o \_ \_ estado do recurso de sombreador não pixel \_ em uma fila 3D pode ser usado nesse estado em qualquer fila 3D ou de computação, sujeito aos requisitos de sincronização que exigem a serialização da maioria das gravações. Os Estados de recursos que são compartilhados entre as duas classes de tipo ( \_ origem de cópia e destino de cópia \_ ) são considerados Estados diferentes para cada classe de tipo. Portanto, se um recurso fizer a transição para o dest de cópia \_ em uma fila de cópia, ele não poderá ser acessado como um destino de cópia de filas 3D ou de computação e vice-versa.

    Para resumir.

    -   Uma fila "Object" é qualquer fila única.
    -   Uma fila "tipo" é qualquer uma destas três: Compute, 3D e Copy.
    -   Uma fila "tipo classe" é qualquer uma destas duas: Compute/3D e Copy.

-   Os sinalizadores de cópia ( \_ destino de cópia e \_ origem da cópia) usados como Estados iniciais representam Estados na classe do tipo 3D/computação. Para usar um recurso inicialmente em uma fila de cópia, ele deve iniciar no estado comum. O estado comum pode ser usado para todos os usos em uma fila de cópia usando as transições de estado implícitas. 
-   Embora o estado do recurso seja compartilhado entre todas as filas de computação e 3D, não é permitido gravar no recurso simultaneamente em filas diferentes. "Simultaneamente" aqui significa não sincronizado, não é possível observar a execução não sincronizada em alguns hardwares. As regras a seguir se aplicam.

    -   Apenas uma fila pode gravar em um recurso por vez.
    -   Várias filas podem ler do recurso contanto que eles não leiam os bytes que estão sendo modificados pelo gravador (os bytes de leitura que estão sendo gravados simultaneamente produzem resultados indefinidos).
    -   Um limite deve ser usado para sincronizar após a gravação antes que outra fila possa ler os bytes gravados ou fazer qualquer acesso de gravação.

-   Os buffers de fundo que estão sendo apresentados devem estar \_ no \_ estado comum do estado do recurso do Direct3D 12 \_ . 

## <a name="related-topics"></a>Tópicos relacionados

[Guia de programação do Direct3D 12](directx-12-programming-guide.md)

[Usando barreiras de recursos para sincronizar Estados de recursos no Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md)

[Gerenciamento de memória no Direct3D 12](memory-management.md)
