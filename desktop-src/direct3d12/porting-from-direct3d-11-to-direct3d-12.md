---
title: Fazendo a portabilidade do Direct3D 11 para o Direct3D 12
description: Esta seção fornece algumas diretrizes sobre a portação de um mecanismo gráfico personalizado do Direct3D 11 para o Direct3D 12.
ms.assetid: 9EB4AC6B-AFDD-4673-8EB3-54272C151784
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ccf4a0bd10032d94ecaf4a88cc442f3a7ad516
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812553"
---
# <a name="porting-from-direct3d-11-to-direct3d-12"></a>Fazendo a portabilidade do Direct3D 11 para o Direct3D 12

Esta seção fornece algumas diretrizes sobre a portação de um mecanismo gráfico personalizado do Direct3D 11 para o Direct3D 12.

-   [Criação de dispositivo](#device-creation)
-   [Recursos comprometidos](#committed-resources)
-   [Recursos reservados](#reserved-resources)
-   [Carregando dados](#uploading-data)
-   [Sombreadores e objetos de sombreador](#shaders-and-shader-objects)
-   [Enviando trabalho para a GPU](#submitting-work-to-the-gpu)
-   [Sincronização de CPU/GPU](#cpugpu-synchronization)
-   [Associação de recursos](#resource-binding)
-   [Estado do recurso](#resource-state)
-   [Swapchains](#swapchains)
-   [Renderização de função fixa](#fixed-function-rendering)
-   [Probabilidades e termina](#odds-and-ends)
-   [Tópicos relacionados](#related-topics)

## <a name="device-creation"></a>Criação de dispositivo

O Direct3D 11 e o Direct3D 12 compartilham um padrão de criação de dispositivo semelhante. Os drivers Direct3D 12  existentes são D3D_FEATURE_LEVEL_11_0 ou melhores, portanto, você pode ignorar os níveis de recursos mais antigos e as limitações associadas.

Lembre-se também de que, com o Direct3D 12, você deve enumerar explicitamente as informações do dispositivo usando interfaces DXGI. No Direct3D 11,  você pode encadear de volta ao dispositivo DXGI do dispositivo Direct3D e isso não tem suporte para o Direct3D 12.

A criação de um dispositivo de software WARP no Direct3D 12 é feita fornecendo um adaptador explícito obtido de **IDXGIFactory4::EnumWarpAdapter**. O dispositivo WARP para Direct3D 12 está disponível somente em sistemas com o recurso opcional **Ferramentas gráficas** habilitado.

> [!NOTE]
> Não há equivalente a **D3D11CreateDeviceAndSwapChain.** Mesmo com o Direct3D 11, não é possível usar essa função, pois geralmente é melhor criar o dispositivo e trocar de lugar em etapas distintas.

## <a name="committed-resources"></a>Recursos comprometidos

Objetos criados com as interfaces a seguir no Direct3D 11 são traduzidos para o que são chamados de "recursos confirmados" no Direct3D 12. Um recurso confirmado é um recurso que tem espaço de endereço virtual e páginas físicas associadas a ele. Esse é um conceito do Modelo de Memória do Microsoft Windows Device Driver 2 (WDD2), no qual o Direct3D 12 se baseia.

Recursos do Direct3D 11:

-   [**ID3D11Resource**](/windows/win32/api/d3d11/nn-d3d11-id3d11resource)
-   [**ID3D11Buffer**](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) [ **e ID3D11Device::CreateBuffer**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createbuffer)
-   [**ID3D11Texture1D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture1d) [ **e ID3D11Device:CreateTexture1D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture1d)
-   [**ID3D11Texture2D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture2d) [ **e ID3D11Device::CreateTexture2D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture2d)
-   [**ID3D11Texture3D**](/windows/win32/api/d3d11/nn-d3d11-id3d11texture3d) [ **e ID3D11Device::CreateTexture3D**](/windows/win32/api/d3d11/nf-d3d11-id3d11device-createtexture3d)

No Direct3D 12, todos eles são representados por [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) e [**ID3D12Device::CreateCommittedResource**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommittedresource).

## <a name="reserved-resources"></a>Recursos reservados

Recursos reservados são recursos em que apenas o espaço de endereço virtual foi alocado, a memória física não é alocada até que haja uma chamada para [**ID3D12Device::CreateHeap**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createheap). Esse é essencialmente o mesmo conceito que os recursos lado a lado no Direct3D 11.

Os sinalizadores ([**SINALIZADOR \_ \_ MISC \_ de RECURSO D3D11**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)) usados no Direct3D 11 para configurar recursos lado a lado e, em seguida, mapeiá-los para a memória física.

-   D3D11 \_ RESOURCE \_ MISC LADO A \_ LADO
-   POOL DE \_ \_ \_ TILES DO MISC DO RECURSO D3D11 \_

## <a name="uploading-data"></a>Carregando dados

No Direct3D 11, há a aparência de uma única linha do tempo (chamadas após uma sequência, como dados inicializados com dados [**D3D11 \_ SUBRESOURCE \_ DATA,**](/windows/win32/api/d3d11/ns-d3d11-d3d11_subresource_data)em seguida, é feita uma chamada para [**ID3D11DeviceContext::UpdateSubresource**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-updatesubresource)e, em seguida, uma chamada para [**ID3D11DeviceContext::Map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map)). O número de cópias criadas dos dados não é óbvio para um desenvolvedor do Direct3D 11.

No Direct3D 12, há duas linhas do tempo, a linha do tempo da GPU (configurada por chamadas para [**CopyTextureRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copytextureregion)e [**CopyBufferRegion**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copybufferregion) da memória mappable) e a linha do tempo da CPU (determinada por chamadas para Mapear [**).**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map) As funções auxiliares são fornecidas (no arquivo d3dx12.h) chamadas [**Updatesubresources**](updatesubresources1.md) que usam uma linha do tempo compartilhada. Há várias variações dessa função auxiliar, uma que usa [**ID3D12Device::GetCopyablePrints**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints), outra que usa um mecanismo alocador de heap e outra que usa um mecanismo alocador de pilha. Essas funções auxiliares copiam recursos para a GPU e a CPU, por meio de uma área intermediária de preparação da memória.

Normalmente, a GPU e a CPU têm sua própria cópia de um recurso vinculado à própria linha do tempo. A abordagem de linha do tempo compartilhada mantém duas cópias da mesma forma.

## <a name="shaders-and-shader-objects"></a>Sombreadores e objetos de sombreador

No Direct3D 11, há muita criação de objetos de estado e sombreador e definição do estado desses objetos, usando os métodos de criação [**ID3D11Device**](/windows/win32/api/d3d11/nn-d3d11-id3d11device) e os métodos de conjunto [**ID3D11DeviceContext.**](/windows/win32/api/d3d11/nn-d3d11-id3d11devicecontext) Normalmente, um grande número de chamadas é feito para esses métodos, que são combinados em tempo de desenho pelo driver para definir o estado correto do pipeline.

No Direct3D 12, essa configuração de estado de pipeline foi combinada em um único objeto ([**CreateComputePipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcomputepipelinestate) para um mecanismo de computação e [**CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) para um mecanismo gráfico), que é anexado a uma lista de comandos antes da chamada de desenho com uma chamada para [**SetPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

Essas chamadas substituem todas as chamadas individuais para definir sombreadores, layout de entrada, estado de mesclagem, estado do rasterizador, estado de estêncil de profundidade e assim por diante, no Direct3D 11

- Métodos do dispositivo 11: ``CreateInputLayout`` , ``CreateXShader`` , ``CreateDepthStencilState`` eD ``CreateRasterizerState`` .
- Métodos de Contexto do Dispositivo 11:  ``IASetInputLayout`` , , , e ``xxSetShader`` ``OMSetBlendState`` ``OMSetDepthStencilState`` ``RSSetState`` .

Embora o Direct3D 12 possa dar suporte a blobs de sombreador compilados mais antigos, os sombreadores devem ser compilados usando o Modelo de Sombreador 5.1 com as APIs FXC/D3DCompile ou usando o Modelo de Sombreador 6 usando o compilador DXIL DXC. Você deve validar o suporte ao Modelo de Sombreador 6 [**com CheckFeatureSupport**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) e **D3D12_FEATURE_SHADER_MODEL**.

## <a name="submitting-work-to-the-gpu"></a>Enviando trabalho para a GPU

no Direct3D 11, há pouco controle sobre realmente como o trabalho é enviado, ele é tratado em grande parte pelo driver, embora algum controle seja habilitado por meio das chamadas [**ID3D11DeviceContext::Flush**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-flush) e [**IDXGISwapChain1::P resent1.**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)

No Direct3D 12, o envio de trabalho é muito explícito e controlado pelo aplicativo. O constructo principal para enviar trabalho é [**o ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist), que é usado para registrar todos os comandos de aplicativos (e é bastante semelhante no conceito ao contexto adiado de ID3D11). O armazenamento de backing para uma lista de comandos é fornecido pelo [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator), que permite que o aplicativo gerencie a utilização de memória da lista de comandos, expondo realmente a memória que o driver Direct3D 12 usará para armazenar a lista de comandos.

Por fim, [**o ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) é uma fila de primeiro a entrar, que armazena a ordem correta das listas de comandos para envio para a GPU. Somente quando uma lista de comandos tiver concluído a execução na GPU, a próxima lista de comandos da fila será enviada pelo driver.

No Direct3D 11, não há nenhum conceito explícito de uma fila de comandos. Na configuração comum do Direct3D 12, a lista de comandos D3D12_COMMAND_LIST_TYPE_DIRECT aberta **no** momento para o quadro atual pode ser considerada análoga ao contexto imediato do Direct3D 11. Isso fornece muitas das mesmas funções.


| D3D11DeviceContext                  | ID3D12GraphicsCommand List     |
|-------------------------------------|--------------------------------|
| ClearDepthStencilView               | ClearDepthStencilView          |
| ClearRenderTargetView               | ClearRenderTargetView          |
| ClearUnorderedAccess*               | ClearUnorderedAccess*          |
| Draw, DrawInstanced                 | DrawInstanced                  |
| DrawIndexed, DrawIndexedInstanced   | DrawIndexedInstanced           |
| Dispatch                            | Dispatch                       |
| IASetInputLayout, xxSetShader, etc. | SetPipelineState               |
| OMSetBlendState                     | OMSetBlendFactor               |
| OMSetDepthStencilState              | OMSetStencilRef                |
| OMSetRenderTargets                  | OMSetRenderTargets             |
| RSSetViewports                      | RSSetViewports                 |
| RSSetScissorRects                   | RSSetScissorRects              |
| IASetPrimitiveTopology              | IASetPrimitiveTopology         |
| IASetVertexBuffers                  | IASetVertexBuffers             |
| IASetIndexBuffer                    | IASetIndexBuffer               |
| ResolveSubresource                  | ResolveSubresource             |
| CopySubresourceRegion               | CopyBufferRegion               |
| UpdateSubresource                   | CopyTextureRegion              |
| CopyResource                        | CopyResource                   |

> [!NOTE]
> Uma lista de comandos criada com **D3D12_COMMAND_LIST_TYPE_BUNDLE** é similar a um contexto adiado. O Direct3D 12 também dá suporte ao abiilty para acessar alguns recursos de um *contexto imediato* , simultaneamente à renderização por meio de **D3D12_COMMAND_LIST_TYPE_COPY** e **D3D12_COMMAND_LIST_TYPE_COMPUTE** tipos de lista de comandos.

## <a name="cpugpu-synchronization"></a>Sincronização de CPU/GPU

Na sincronização de CPU/GPU do Direct3D 11 era amplamente automática, e não havia necessidade de o aplicativo manter o status da memória física.

no Direct3D 12, o aplicativo deve gerenciar as duas linhas do tempo (CPU e GPU) explicitamente. Isso exige que as informações precisem ser mantidas, pelo aplicativo, em quais recursos são exigidos pela GPU e por quanto tempo. Isso também significa que o aplicativo é responsável por garantir que o conteúdo dos recursos (recursos confirmados, heaps, alocadores de comando, por exemplo) não mude até que a GPU termine de usá-los.

O objeto principal para sincronizar as linhas do tempo é o objeto [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) . A operação de limites é bem simples, pois eles permitem que a GPU seja sinalizada quando tiver concluído uma tarefa. A GPU e a CPU podem sinalizar e podem esperar por limites.

Normalmente, a abordagem é que, ao enviar uma lista de comandos para execução, um sinal de cerca é transmitido pela GPU na conclusão (quando terminar de ler os dados), permitindo que a CPU reutilize ou destrua os recursos.

No Direct3D 11, o sinalizador [**ID3D11DeviceContext:: map**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-map) D3D11 \_ \_ o descarte de gravação de mapa \_ , essencialmente, tratava de cada recurso como uma quantidade infinita de memória que o aplicativo poderia gravar (um processo conhecido como "renomeando"). No Direct3D 12, o processo é explícito: a memória adicional precisa ser alocada e os limites devem ser usados para sincronizar as operações. Os buffers de anéis (consistindo em grandes buffers) podem ser uma boa técnica para isso, consulte o cenário de buffer de anéis no [Gerenciamento de recursos baseado em isolamento](fence-based-resource-management.md).

![usando um buffer de anéis](images/ring-buffer-1.png)

## <a name="resource-binding"></a>Associação de recursos

As exibições no Direct3D 11 (exibições de recursos do sombreador, exibições de destino de renderização e assim por diante) foram substituídas em grande parte no Direct3D 12 pelo conceito de um descritor. Os métodos de criação ainda existem no Direct3D 12 (como [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview) e [**CreateRenderTargetView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createrendertargetview)), que são chamados após a criação do heap de descritor, para gravar os dados no heap. A associação no Direct3D 12 agora é manipulada por identificadores de descritor descritos em uma assinatura raiz e enviada usando os métodos [**SetGraphicsRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setgraphicsrootdescriptortable) ou [**SetComputeRootDescriptorTable**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setcomputerootdescriptortable) .

As assinaturas raiz detalham os mapeamentos entre o número do slot de assinatura raiz e as tabelas de descritores, em que a tabela de descritores pode conter referências a recursos disponíveis para sombreadores de vértice, sombreadores de pixel e outros sombreadores, como buffers de constantes, exibições de recursos de sombreador e amostras. Essa flexibilidade desconecta o espaço de registro HLSL do espaço de associação de API no Direct3D 12, ao contrário do Direct3D 11, em que há um mapeamento de um para um entre eles.

Uma das implicações desse sistema é que o aplicativo é responsável por renomear tabelas de descritores, o que permite aos desenvolvedores entender o custo de desempenho da alteração até mesmo de um único descritor por chamada de desenho.

Um novo recurso do Direct3D 12 é que um aplicativo pode controlar quais descritores são compartilhados entre quais estágios do sombreador. No Direct3D 11, os recursos como UAVs são compartilhados entre todos os estágios do sombreador. Ao habilitar os descritores para serem desabilitados em determinados estágios de sombreador, os registros usados pelos descritores que foram desabilitados estão disponíveis para serem usados por descritores que estão habilitados para um determinado estágio do sombreador.

A tabela a seguir mostra um exemplo de assinatura de raiz.



| Slot de parâmetro raiz | Entrada da tabela de descritores         |
|---------------------|--------------------------------|
| 0                   | Intervalo de descritor do VS B0-B13     |
| 1                   | Intervalo do descritor do VS T0-T127    |
| 2                   | Intervalo do descritor VS S0-S16     |
| 3                   | Intervalo de descritores do PS B0-B13     |
| ...                 |                                |
| 14                  | Intervalo de descritor de DS S0-16      |
| 15                  | Intervalo de descritor compartilhado U0-u63 |



 

## <a name="resource-state"></a>Estado do recurso

No estado do recurso do Direct3D 11 não é mantido pelo aplicativo, mas pelo driver.

No Direct3D 12, a manutenção do estado do recurso se torna a responsabilidade do aplicativo, para habilitar o paralelismo total na gravação de listas de comandos: o aplicativo deve lidar com as linhas do tempo de gravação das listas de comandos (o que pode ser feito em paralelo) e as linhas do tempo de execução que devem ser sequenciais.

Uma transição de estado de recurso é tratada pelo método [**ResourceBarrier**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resourcebarrier) . Principalmente, o aplicativo deve informar o driver quando o uso de recursos estiver sendo alterado. Por exemplo, se um recurso estiver sendo usado como um destino de renderização e, em seguida, for usado como entrada para um sombreador de vértice na próxima chamada de desenho, isso poderá exigir uma pequena parada na operação de GPU para concluir a operação de destino de renderização antes de manipular o sombreador de vértice.

Esse sistema permite a sincronização refinada (as vagas de GPU) do pipeline de gráficos, bem como liberações de cache e, possivelmente, algumas alterações de layout de memória (como exibição de destino de renderização para descompactação de exibição de estêncil de profundidade).

Isso é conhecido como uma barreira de transição. Há outros tipos de barreiras, no Direct3D 11, o [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) habilitou a mesma memória física a ser usada por dois recursos diferentes do lado do ladrilho. No Direct3D 12, isso é chamado de "barreira de alias". As barreiras de alias podem ser usadas tanto para os recursos lado e inseridos no Direct3D 12. Além disso, há a barreira UAV. No Direct3D 11, todas as operações de expedição e de envio de UAV devem ser serializadas, mesmo que essas operações possam ser canalizadas ou trabalhar em paralelo. Para o Direct3D 12, essa restrição é removida pela adição de uma barreira UAV. Uma barreira UAV garante que as operações UAV sejam sequenciais, portanto, se uma segunda operação exigir que a primeira seja concluída, a segunda será forçada a aguardar pela adição da barreira. A operação padrão para UAVs é simplesmente que as operações continuarão o mais rápido possível.

Claramente, há ganhos de desempenho se uma carga de trabalho pode ser paralelizada.

## <a name="swapchains"></a>Permuta

A cadeia de permuta DXGI é a base para cadeias de permuta no Direct3D 11 e 12. Há algumas pequenas diferenças, no Direct3D 11, os três tipos de cadeia de permuta são SEQUENCIAis, descartar e inverter \_ sequenciais. Para o Direct3D 12, há apenas dois tipos: inverter \_ sequencial e \_ descartar flip. Conforme observado acima, você deve criar explicitamente seu SwapChain por meio do **IDXGIFactory4**, ou posterior, e usar a mesma interface para qualquer enumeração de adaptador.

No Direct3D 11, há uma rotação de BackBuffer automática: somente uma exibição de destino de renderização é necessária para o buffer de fundo 0. Na rotação do buffer do Direct3D 12 é explícita, é necessário haver uma exibição de destino de renderização para cada buffer de fundo. Use o método [**IDXGISwapChain3:: GetCurrentBackBufferIndex**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) para selecionar em qual deles renderizar. Novamente, essa flexibilidade adicional permite maior paralelização.

> [!NOTE]
> Embora haja várias maneiras de configurar seu aplicativo, geralmente os aplicativos têm um **ID3D12CommandAllocator** por buffer de cadeia de permuta. Isso permite que o aplicativo prossiga com a criação de um conjunto de comandos para o próximo quadro enquanto a GPU renderiza o anterior.

## <a name="fixed-function-rendering"></a>Renderização de função fixa

No Direct3D 11, havia alguns métodos que simplificaram várias operações de nível superior, como [**GenerateMips**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-generatemips) (criando cadeias de MIP completas) e [**DrawAuto**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-drawauto) (usando a saída de fluxo como entrada de sombreador sem a entrada adicional do aplicativo). Esses métodos não estão disponíveis no Direct3D 12, o aplicativo precisa lidar com essas operações criando sombreadores para realizá-las.

## <a name="odds-and-ends"></a>Chances e terminações

A tabela a seguir mostra uma série de recursos semelhantes entre o Direct3D 11 e o 12, mas não são idênticos.



| Direct3D 11                                                                            | Direct3D 12                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ID3D11Query**](/windows/win32/api/d3d11/nn-d3d11-id3d11query)                                              | O [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) permite que as consultas sejam agrupadas, reduzindo o custo.                                                                                                                                                                                                                                                                                                                                     |
| [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate)                                      | O predicação agora está habilitado por ter dados em um buffer totalmente transparente. O objeto Direct3D 11 [**ID3D11Predicate**](/windows/win32/api/d3d11/nn-d3d11-id3d11predicate) é substituído por [**ID3D12Resource:: map**](/windows/win32/api/d3d12/nf-d3d12-id3d12resource-map), que deve seguir uma chamada para [**ResolveQueryData**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-resolvequerydata) e uma operação de sincronização de GPU usando uma cerca para aguardar que os dados estejam prontos. Consulte [predicação](predication.md). |
| UAV/SO contador oculto                                                                  | O aplicativo é responsável pela alocação e pelo gerenciamento dos contadores de SO/UAV. Consulte [contadores de saída de fluxo](stream-output-counters.md) e contadores de [UAV](uav-counters.md).                                                                                                                                                                                                                                                             |
| MinLOD dinâmico de recursos (nível de detalhe)                                       | Isso foi movido para o MinLOD estático do descritor SRV.                                                                                                                                                                                                                                                                                                                                                                                 |
| Desenhar \* indireto/[**DispatchIndirect**](/windows/win32/api/d3d11/nf-d3d11-id3d11devicecontext-dispatchindirect) | Os métodos indiretos de desenho são todos mesclados em um método [**ExecuteIndirect**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executeindirect) .                                                                                                                                                                                                                                                                                                        |
| Os formatos DepthStencil são intercalados                                                   | Os formatos DepthStencil são planar. Por exemplo, um formato de 24 bits de profundidade, 8 bits de estêncil seriam armazenados no formato 24/8/24/8... etc., no Direct3D 11, mas como 24/24/24... seguido por 8/8/8... no Direct3D 12. Observe que cada plano é seu próprio subrecurso em D3D12 (consulte [subrecursos](subresources.md)).                                                                                                                    |
| [**ResizeTilePool**](/windows/win32/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)                   | Os recursos reservados podem ser mapeados para vários heaps. Quando um pool de blocos fosse aumentado no D3D11, um heap adicional pode ser alocado em D3D12 em vez disso.                                                                                                                                                                                                                                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tutoriais de vídeo do DirectX Advanced Learning: guia de portabilidade do DirectX 11 para DirectX 12](https://www.youtube.com/watch?v=BV64mdOCgZo)
</dt> <dt>

[Introdução ao Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Como trabalhar com o Direct2D, o Direct3D 10 e o Direct3D 11](direct3d-12-interop.md)
</dt> </dl>
