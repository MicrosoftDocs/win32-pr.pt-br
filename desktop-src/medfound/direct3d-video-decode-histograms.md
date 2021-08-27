---
description: Este artigo contém diretrizes para gerar histogramas durante a decodificação de vídeo usando APIs de vídeo do Direct3D 11 ou 12.
ms.assetid: ''
title: Histogramas de decodificar vídeo do Direct3D
ms.topic: article
ms.date: 08/19/2019
ms.openlocfilehash: 94371fd68c981a98c4ba629822f928e148c230565b5103dfaa2350543bbe9a57
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061626"
---
# <a name="direct3d-video-decode-histograms"></a>Histogramas de decodificar vídeo do Direct3D

Este artigo contém diretrizes para gerar histogramas durante a decodificação de vídeo usando APIs de vídeo do Direct3D 11 ou 12.

## <a name="checking-the-video-device-for-histogram-capabilities"></a>Verificando os recursos de histograma do dispositivo de vídeo

Antes de tentar gerar histogramas, você deve verificar se o dispositivo de vídeo atual dá suporte ao recurso de histograma de decodificar vídeo.

### <a name="direct3d-12"></a>Direct3D 12

Chame [ID3D12VideoDevice::CheckFeatureSupport](/windows/desktop/api/d3d12video/nf-d3d12video-id3d12videodevice-checkfeaturesupport) para verificar os detalhes de suporte para operações de decodificação de vídeo do Direct3D 12. Passe o **D3D12_FEATURE_VIDEO_DECODE_HISTOGRAM** da enumeração [D3D12_FEATURE_VIDEO](/windows/desktop/api/d3d12video/ne-d3d12video-d3d12_feature_video) para especificar que você está solicitando suporte para histogramas de decodificar vídeo.

### <a name="direct3d-11"></a>Direct3D 11

Chame [ID3D11VideoDevice2::CheckFeatureSupport](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videodevice2-checkfeaturesupport) e passe o valor **D3D11_FEATURE_VIDEO_DECODER_HISTOGRAM** do [D3D11_FEATURE_VIDEO para](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_feature_video) determinar se há suporte para histogramas para o dispositivo atual.

## <a name="enabling-histogram-during-decode"></a>Habilitando o histograma durante a decodificar

A coleção de dados de histograma é habilitada pelo chamador que fornece os buffers nos quais os dados de histograma são armazenados.  Um buffer de saída de histograma nulo para um determinado componente indica que a coleção de histogramas está desabilitada.

### <a name="direct3d-12"></a>Direct3D 12

Para fornecer buffers de saída para receber dados de histograma usando o Direct3D 12, você deve criar sua lista de comandos de decodificar usando o método [ID3D12VideoDecodeCommandList1::D ecodeFrame1.](/windows/win32/api/d3d12video/nf-d3d12video-id3d12videodecodecommandlist1-decodeframe1) Esse método assume uma [D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_stream_arguments1) como um argumento. **D3D12_VIDEO_DECODE_OUTPUT_STREAM_ARGUMENTS1** tem um campo do tipo [D3D12_VIDEO_DECODE_OUTPUT_HISTOGRAM](/windows/win32/api/d3d12video/ns-d3d12video-d3d12_video_decode_output_histogram), que permite especificar um [ID3D12Resource](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) no qual os dados de histograma são produzidos.

### <a name="direct3d-11"></a>Direct3D 11

A interface [ID3D11VideoContext3](/windows/win32/api/d3d11_4/nn-d3d11_4-id3d11videocontext3) fornece o método [DecoderBeginFrame1,](/windows/win32/api/d3d11_4/nf-d3d11_4-id3d11videocontext3-decoderbeginframe1) que permite que você forneça uma ou mais interfaces [ID3D11Buffer](/windows/win32/api/d3d11/nn-d3d11-id3d11buffer) nas quais os dados de histograma serão produzidos. O [D3D11_VIDEO_DECODER_HISTOGRAM_COMPONENT](/windows/win32/api/d3d11_4/ne-d3d11_4-d3d11_video_decoder_histogram_component) especificar os componentes para os quais você deseja que os dados de histograma sejam gerados.


## <a name="buffer-format"></a>Formato do buffer

A saída de histograma de decodificar é escrita em um buffer como um contador inteiro por componente.  O formato de buffer é um valor de 32 bits por compartimento.  Um dispositivo pode usar uma profundidade de bit de contador inteiro menor que 32 bits, mas deve ter 16, 24 ou 32 bits.  Nesse caso, o valor do contador é armazenado nos bits inferiores e os bits superiores nãoutilados são zero.  Quando a contagem de um compartimento exceder o valor máximo, o dispositivo define o valor máximo em vez disso. Os dispositivos relatam o número de compartimentos com suporte, que deve ser um valor que seja uma potência de 2.  O número mínimo de compartimentos necessário para dispositivos que suportam esse recurso é 64. 

Você deve fornecer um buffer com um deslocamento alinhado de 256 bytes e um tamanho que seja o número de compartimentos com suporte multiplicado pelo tamanho do compartimento (4 bytes) para cada componente solicitado.  O posicionamento do compartimento é determinado por:

`binIndex = floor(value / [max value of channel + 1] * (countBins))`


Quando um formato define os bits úteis de um componente como menor que o número de bits de armazenamento (por exemplo, P010 usa os 10 bits principais de 16 bits de armazenamento de componentes), somente os bits úteis são considerados (P010 é tratado como um valor de 10 bits). 

O dispositivo de vídeo relata quais componentes têm suporte.  Se o chamador não quiser um histograma para um determinado componente, ele especificará nullptr.  Se o driver não dá suporte a um histograma para um determinado componente, o buffer de histograma desse componente deve ser nullptr.

Quando há suporte para vários componentes, o aplicativo pode solicitar qualquer combinação de componentes por decodificar quadro.  Por exemplo, se o hardware relata suporte para componentes Y, U e V, o aplicativo pode solicitar o histograma Y apenas para o quadro um, o histograma U apenas para o quadro dois e o histograma V apenas para o quadro 3.  Eles também podem solicitar qualquer combinação de dois componentes ou todos os três componentes.

Os aplicativos fornecem um deslocamento separado e um ponteiro/alça de buffer para cada componente solicitado.  Esse ponteiro pode apontar para o mesmo recurso que outro componente ou um recurso separado.  O deslocamento permite colocar vários componentes no mesmo buffer, mas a região de saída especificada pelo deslocamento e o tamanho do histograma não devem sobrepor outra saída de componente histograma.  O histograma também pode ser gravado no mesmo buffer que outro conteúdo não relacionado, como ao ser usado em uma estratégia de subatribuição de recursos.


O runtime D3D valida que os chamadores só habilitam o histograma para componentes com suporte, se o deslocamento do buffer está alinhado e que o tamanho do buffer é suficiente para o número relatado de compartimentos.


## <a name="protected-content"></a>Conteúdo protegido

Os buffers de Histograma são necessários para ter a mesma proteção de superfície que a superfície de saída de decodificar. Se a superfície de saída de decodificar não for um recurso protegido, o buffer de histograma não deverá ser um recurso protegido. Se a superfície de saída de decodificar for um recurso protegido, o histograma deverá ser um recurso protegido.








## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>APIs de vídeo do 
[Direct3D 12](direct3d-12-video-apis.md) 
 [Guia Media Foundation programação do Media Foundation](media-foundation-programming-guide.md)
</dt> </dl>

 

 




