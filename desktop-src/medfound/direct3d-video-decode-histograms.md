---
description: Este artigo contém diretrizes para gerar histogramas ao decodificar vídeo usando as APIs de vídeo do Direct3D 11 ou 12.
ms.assetid: ''
title: Histogramas de decodificação de vídeo Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 6e25abd39ba95b669c2d76ced5f825ea80c4e3c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812134"
---
# <a name="direct3d-video-decode-histograms"></a>Histogramas de decodificação de vídeo Direct3D

Este artigo contém diretrizes para gerar histogramas ao decodificar vídeo usando as APIs de vídeo do Direct3D 11 ou 12.

## <a name="checking-the-video-device-for-histogram-capabilities"></a>Verificando o dispositivo de vídeo para recursos de histograma

Antes de tentar gerar histogramas, você deve verificar se o dispositivo de vídeo atual dá suporte ao recurso de histograma de decodificação de vídeo.

### <a name="direct3d-12"></a>Direct3D 12

Chame [ID3D12VideoDevice:: CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) para verificar os detalhes de suporte para operações de decodificação de vídeo do Direct3D 12. Passe o valor **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** da enumeração [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) para especificar que você está solicitando suporte para histogramas de decodificação de vídeo.

### <a name="direct3d-11"></a>Direct3D 11

Chame [ID3D11VideoDevice2:: CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) e transmita o valor **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** da [D3D11_FEATURE_VIDEO](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) para determinar se há suporte para histogramas para o dispositivo atual.

## <a name="enabling-histogram-during-decode"></a>Habilitando o histograma durante a decodificação

A coleção de dados de histograma é habilitada pelo chamador fornecendo os buffers nos quais os dados de histograma são armazenados.  Um buffer de saída de histograma nulo para um determinado componente indica que a coleção de histograma está desabilitada.

### <a name="direct3d-12"></a>Direct3D 12

Para fornecer buffers de saída para receber dados de histograma usando o Direct3D 12, você deve criar sua lista de comandos de decodificação usando o método [ID3D12VideoDecodeCommandList1::D ecodeframe1](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) . Esse método usa uma estrutura [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) como um argumento. **D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** tem um campo do tipo [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), que permite especificar um [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) no qual os dados do histograma são gerados.

### <a name="direct3d-11"></a>Direct3D 11

A interface [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) fornece o método [DecoderBeginFrame1](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) , que permite que você forneça uma ou mais interfaces [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) nas quais os dados de histograma serão gerados. O [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) para especificar os componentes para os quais você deseja que os dados de histograma sejam gerados.


## <a name="buffer-format"></a>Formato de buffer

A saída do histograma de decodificação é gravada em um buffer como um contador inteiro por componente.  O formato do buffer é um valor de 32 bits por compartimento.  Um dispositivo pode usar uma profundidade de bit de contador de inteiros menor que 32 bits, mas deve ser 16, 24 ou 32 bits.  Nesse caso, o valor do contador é armazenado nos bits inferiores e os bits não usados superiores são zero.  Quando a contagem de um compartimento exceder o valor máximo, o dispositivo definirá o valor máximo em vez disso. Dispositivos relatam o número de compartimentos com suporte, que deve ser um valor que seja uma potência de 2.  O número mínimo de compartimentos necessário para dispositivos que dão suporte a esse recurso é 64. 

Você deve fornecer um buffer com um deslocamento alinhado de 256 bytes e um tamanho que seja o número de compartimentos com suporte multiplicado pelo tamanho do compartimento (4 bytes) para cada componente solicitado.  O posicionamento do compartimento é determinado por:

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


Quando um formato define os bits úteis de um componente menor que o número de bits de armazenamento (por exemplo, P010 usa os 10 principais bits de 16 bits de armazenamento de componentes), somente os bits úteis são considerados (P010 é tratado como um valor de 10 bits). 

O dispositivo de vídeo relata quais componentes têm suporte.  Se o chamador não quiser um histograma para um determinado componente, ele especificará nullptr.  Se o driver não oferecer suporte a um histograma para um determinado componente, o buffer de histograma do componente deverá ser nullptr.

Quando há suporte para vários componentes, o aplicativo pode solicitar qualquer combinação de componentes por decodificação de quadro.  Por exemplo, se o hardware fornece suporte para os componentes Y, U e V, o aplicativo pode solicitar o histograma Y somente para o quadro um, o histograma de U somente para o quadro dois e o histograma V somente para o quadro 3.  Eles também podem solicitar qualquer combinação de dois componentes ou de todos os três componentes.

Os aplicativos fornecem um deslocamento/ponteiro de buffer/identificador separado para cada componente solicitado.  Esse ponteiro pode apontar para o mesmo recurso que outro componente ou um recurso separado.  O deslocamento permite colocar vários componentes no mesmo buffer, mas a região de saída especificada pelo deslocamento e o tamanho do histograma não devem sobrepor outra saída do componente de histograma.  O histograma também pode ser gravado no mesmo buffer que outro conteúdo não relacionado, como quando usado em uma estratégia de subalocação de recursos.


O tempo de execução do D3D valida se os chamadores só habilitam o histograma para componentes com suporte, se o deslocamento do buffer está alinhado e se o tamanho do buffer é suficiente para o número relatado de compartimentos.


## <a name="protected-content"></a>Conteúdo protegido

Os buffers de histograma precisam ter a mesma proteção de superfície que a superfície de saída de decodificação. Se a superfície de saída de decodificação não for um recurso protegido, o buffer de histograma não deverá ser um recurso protegido. Se a superfície de saída de decodificação for um recurso protegido, o histograma deverá ser um recurso protegido.








## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>APIs de vídeo do 
[Direct3D 12](direct3d-12-video-apis.md) 
 [Guia de programação Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 




