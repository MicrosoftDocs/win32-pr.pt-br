---
description: Este artigo contém diretrizes gerais para usar as APIs de vídeo do Direct3D 12.
ms.assetid: ''
title: Visão geral do vídeo do Direct3D 12
ms.topic: article
ms.date: 06/03/2019
ms.openlocfilehash: 561ceba8a3110d6aa7e9a336430c0a14ddb45bc5707c650588a08c391cd65863
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828316"
---
# <a name="direct3d-12-video-overview"></a>Visão geral do vídeo do Direct3D 12

Este artigo contém diretrizes gerais para usar as APIs de vídeo do Direct3D 12.

## <a name="about-direct3d-12-video"></a>Sobre o vídeo do Direct3D 12

A interface de vídeo do Direct3D 12 fornece uma nova maneira para os aplicativos implementarem a decodificação e o processo de vídeo. A interface direct3D 12 é diferente da interface anterior do Direct3D 11 porque foi projetada para ser consistente com os princípios e estilo do Direct3D 12, que inclui o seguinte:

- Dar aos desenvolvedores mais controle
 - Alocação de memória acessível por hardware
 - Threads de CPU usados para gerar & comandos de envio
   - Geração e envio independentes
   - Sem bloqueio
 - Agendamento de trabalho de hardware
- Aborda a funcionalidade existente, incluindo a maioria das funcionalidades de vídeo do Direct3D 11, mas, ao mesmo tempo, mantém a simplicidade e a facilidade de uso em mente
- Potência e desempenho dos principais aplicativos Direct3D 12 iguais ou melhores que o Direct3D 11
- Consistência com outras APIs do Direct3D 12
- Interoperabilidade com APIs de gráficos existentes


## <a name="video-decoding"></a>Decodificação de vídeo

As seções a seguir descrevem algumas das tarefas envolvidas na implementação da decodificação de vídeo do Direct3D 12.

### <a name="query-for-decoding-capabilities"></a>Consultar recursos de decodificação

Chame [ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) para verificar os detalhes de suporte para operações de decodificação de vídeo do Direct3D 12. Passe um valor da [enumeração D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) para especificar o recurso para o qual você está solicitando informações de suporte.

### <a name="create-the-video-decoder"></a>Criar o decodificador de vídeo

Chame [ID3D12VideoDevice::CreateVideoDecoder](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoder) para criar uma instância da interface [ID3D12VideoDecoder.](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoder) O decodificador mantém o estado de uma sessão de decodificar, incluindo dados relacionados à referência, como vetores de movimento.  No caso de uma alteração de resolução ou de [uma alteração MaxDecodePictureBufferCount,](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decoder_heap_desc) o objeto decodificador é recriado. A largura e a altura de decodificar especificam a resolução de fluxo nativo antes de qualquer escala.  A contagem máxima do DPB (Buffer de Imagem de Decodificar) especifica a maior contagem de DPB que pode ser usada sem recriar o decodificador de vídeo.

O decodificador pode ser usado para registrar comandos de várias listas de comandos, mas só pode ser associado a uma lista de comandos por vez.  O aplicativo é responsável por sincronizar o acesso ao decodificador.

### <a name="create-the-video-decoder-heap"></a>Criar o heap do decodificador de vídeo 

Chame [ID3D12VideoDevice::CreateVideoDecoderHeap](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideodecoderheap) para criar uma instância da interface [ID3D12VideoDecoderHeap.](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videodecoderheap) Esse objeto contém o estado e os recursos de driver dependentes de resolução.

### <a name="decoding-a-frame"></a>Decodificar um quadro

Todos os parâmetros de entrada e saída para as operações de processamento de vídeo são organizados em uma estrutura de parâmetro de [entrada,](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_input_stream_arguments)D3D12_VIDEO_DECODE_INPUT_STREAM_ARGUMENTS e uma estrutura de parâmetro de saída, [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments).
O aplicativo gerencia os quadros de referência e, como tal, precisa definir os quadros de referência para cada operação de decodificação.
Quando a lista de comandos for registrada corretamente, chame [ID3D12CommandQueue::ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) na fila de comandos de vídeo para enviar a decodificação de quadro para a GPU.


### <a name="enabling-decoder-output-conversions"></a>Habilitando conversões de saída do decodificador
Se o decodificador dá suporte à conversão, habilita as conversões desejadas preenchendo corretamente a [estrutura D3D12_VIDEO_DECODE_CONVERSION_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_decode_conversion_arguments) dados. O formato e as resoluções da saída desejada versus a saída nativa do decodificador são comunicados por meio da diferença no espaço de cores e nas resoluções especificadas nos parâmetros de conversão.

##  <a name="querying-decoding-status"></a>Consultar o status da decodificação 
Use os métodos [ID3D12VideoDecodeCommandList::BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery) e [ID3D12VideoDecodeCommandList::EndQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery) para consultar o status da operação de decodificação.

A [estrutura D3D12_QUERY_DATA_VIDEO_DECODE_STATISTICS](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_query_data_video_decode_statistics) é usada para descrever estatísticas de decodificar vídeo. Para obter uma instância dessa estrutura, chame [ID3D12VideoDecodeCommandList::EndQuery,](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-endquery)passando o valor do tipo de consulta heap [de D3D12_QUERY_TYPE_VIDEO_DECODE_STATISTIC](/windows/win32/api/d3d12/ne-d3d12-d3d12_query_type). Observe que essa consulta não usa [ID3D12VideoDecodeCommandList::BeginQuery](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist-beginquery).

## <a name="video-processing"></a>Processamento de vídeo

As APIs de vídeo do Direct3D 12 têm uma abordagem simplificada para o processamento de vídeo, eliminando recursos do Direct3D 11 que não foram amplamente usados e removendo verificações de funcionalidade para recursos que são obrigatórios entre dispositivos. O processo de enumeração para processamento de vídeo é eliminado. Em vez disso, chame [ID3D12VideoDevice::CheckFeatureSupport,](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) que permite que um aplicativo identifique os recursos do processador de vídeo. Os formatos de vídeo, intercalação, estéreo e taxas desejados são fornecidos como entrada para **CheckFeatureSupport.**

### <a name="removed-capabilities"></a>Recursos removidos

Não há suporte para os seguintes recursos do Direct3D 11 no processamento de vídeo do Direct3D 12:
- Taxas personalizadas.  Em vez disso, há uma taxa de entrada e saída determinada durante a gravação do comando [ID3D12VideoProcessCommandList::P rocessFrames.](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes)
- Há apenas dois modos de desintercalação disponíveis agora: [BOB](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags) e [CUSTOM.](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_deinterlace_flags) Outros modos foram eliminados. CUSTOM é um modo de desintercalação de alta qualidade fornecido pelo fornecedor de hardware.
- Todos os formatos estéreos opcionais [D3D11_VIDEO_PROCESSOR_STEREO_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_stereo_caps) não têm mais suporte. Em vez [disso, nono](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format), [horizontal,](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) [vertical](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format)e [separado](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_frame_stereo_format) são obrigatórios para todos os dispositivos de hardware se há suporte para estéreo.
- Não há equivalente para [D3D11_VIDEO_PROCESSOR_FORMAT_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_format_caps) ou [D3D11_VIDEO_PROCESSOR_AUTO_STREAM_CAPS](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_auto_stream_caps). Em vez disso, os formatos de entrada e saída são argumentos para a criação do processador de vídeo e, nesse momento, ele deve ser conhecido se o processador de vídeo pode ou não executar a operação com o formato determinado. O [D3D12_VIDEO_PROCESS_AUTO_PROCESSING_FLAGS](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_process_auto_processing_flags) é usado para indicar se os recursos de processamento automático estão disponíveis.
- Não há equivalente para [D3D11_VIDEO_PROCESSOR_CAPS_LEGACY](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps).
- Não há equivalente para [D3D11_VIDEO_PROCESSOR_CAPS_CONSTRICTION](/windows/desktop/api/d3d11/ne-d3d11-d3d11_video_processor_feature_caps).
- Ao converter de estéreo para mono, presumimos que a exibição de linha de base seja 0.
- O processamento de vídeo do Direct3D 12 não dá suporte à conversão de mono em estéreo e não há suporte para deslocamento mono. 


### <a name="creating-a-video-processor"></a>Criando um processador de vídeo

Chame [ID3D12VideoDevice::CreateVideoProcessor](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-createvideoprocessor) para criar uma instância do [ID3D12VideoProcessor](/windows/desktop/api/d3d12video/nn-d3d12video-id3d12videoprocessor). O processador de vídeo mantém o estado de uma sessão de processamento de vídeo, incluindo memória intermediária necessária, dados de processamento armazenados em cache ou outro espaço de trabalho temporário. Os argumentos de criação do processador de vídeo especificam quais operações são executadas ou estão disponíveis em [ID3D12VideoProcessCommandList1::P rocessFrames1](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist1-processframes1) time.  As alocações de driver para executar a operação de processo de vídeo (por exemplo, intermediários) são alocadas no momento da criação do processador de vídeo.  Use [D3D12_FEATURE_VIDEO_PROCESSOR_SIZE](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) para determinar o tamanho da alocação do processador de vídeo com antecedência.

O processador de vídeo só pode ser usado para registrar comandos de várias listas de comandos, mas só pode ser associado a uma lista de comandos por vez.  O aplicativo é responsável por sincronizar o acesso ao processador de vídeo.  O aplicativo também deve registrar comandos de processamento de vídeo no procoessor de vídeo na ordem em que eles são executados na GPU.

Todos os argumentos de entrada e saída para as operações de processamento de vídeo são organizados em uma estrutura de argumento de [entrada,](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_input_stream_arguments)D3D12_VIDEO_PROCESS_INPUT_STREAM_ARGUMENTS e uma estrutura de argumento de saída, [D3D12_VIDEO_PROCESS_OUTPUT_STREAM_ARGUMENTS](/windows/desktop/api/d3d12video/ns-d3d12video-d3d12_video_process_output_stream_arguments). O aplicativo deve chamar [ID3D12VideoProcessCommandList::P rocessFrames](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videoprocesscommandlist-processframes) para registrar a operação de processamento de vídeo que deseja executar. 

Quando a lista de comandos for registrada, chame [ID3D12CommandQueue::ExecuteCommandLists](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) na fila de comandos de vídeo para enviar o processamento de quadros para a GPU.


## <a name="tiers"></a>Tiers

O vídeo do Direct3D 12 define camadas que agrupam os recursos de dispositivos de hardware, para que o aplicativo possa ter menos caminhos de código para atender à variedade de hardware. As camadas são especificadas com a [enumeração D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier) dados.

Em todas as camadas, o seguinte estará disponível:

- Não há necessidade de recriação do decodificador em alterações de resolução. Somente o heap do decodificador precisa ser recriado na alteração de resolução.
- Todos os quadros de referência serão gerenciados pelo aplicativo. Isso permite que o sistema economize memória, pois não precisamos alocar o número máximo de DPBs no momento da criação do decodificador em algumas camadas e oferece aos aplicativos flexibilidade na resolução de cenários de alteração.

Observe que as camadas são superconjunto. Um aplicativo pode decidir fazer a camada 1 e não usar os recursos de nível superior, o que é permitido, mas pode não fornecer um desempenho ideal. Para obter mais informações sobre os recursos associados a diferentes níveis de camada, [consulte D3D12_VIDEO_DECODE_TIER](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_video_decode_tier).

## <a name="reference-frames"></a>Quadros de referência

Com o vídeo do Direct3D 12, os quadros de referência são passados explicitamente. Isso permite o uso claro de matrizes de texturas ou matrizes de textura quando estamos decodificando quadros. O aplicativo não é necessário para passar exatamente o mesmo handle de recurso ao usá-lo como uma referência; ele pode, por exemplo, decidir copiar um recurso para outro e, em seguida, passar a cópia em vez do original. Os índices *DXVA RefFrameList* e *CurrPic* ainda são usados pelo driver para armazenar dados relevantes para cada quadro decodificado.


## <a name="directx-12-fences"></a>Cercas do DirectX 12

No DirectX 12, o aplicativo é responsável por sincronizar o acesso aos buffers. Para o caso de decodificação, haverá a necessidade de adicionar cercas aos buffers de entrada e aos buffers de saída. Cada cerca tem um valor associado a ele e é usada para sincronização da CPU e dos mecanismos de hardware. Para obter mais informações, consulte [Using Resource Barriers to Synchronize Resource States in Direct3D 12](/windows/desktop/direct3d12/using-resource-barriers-to-synchronize-resource-states-in-direct3d-12).

Uma implementação típica terá uma cerca para cada buffer de entrada. No caso de buffers de entrada, é possível que o buffer possa estar disponível antes que todo o processo de decodificação seja feito. O sistema ignorará esse caso e assumirá que o buffer de entrada está disponível quando a decodificação for feita.
Uma implementação também geralmente terá uma cerca para cada buffer de saída. No caso de enviar a saída para o compositor, por exemplo, uma cerca é necessária que é sinalizada quando a apresentação desse quadro é finalmente feita, indicando que a saída está novamente disponível para o decodificador.


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>APIs de vídeo do 
[Direct3D 12](direct3d-12-video-apis.md) 
 [Guia Media Foundation programação do Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 
