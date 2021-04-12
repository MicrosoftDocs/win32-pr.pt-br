---
description: O processamento de vídeo de DXVA encapsula as funções do hardware de gráficos que são dedicadas ao processamento de imagens de vídeo descompactadas. Os serviços de processamento de vídeo incluem desentrelaçamento e mixagem de vídeo.
ms.assetid: bd688f81-4b7c-4016-b0bd-e40782131f8e
title: Processamento de vídeo de DXVA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf5058d93ddd7c506a501eb6ca07c4661755fc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501173"
---
# <a name="dxva-video-processing"></a>Processamento de vídeo de DXVA

O processamento de vídeo de DXVA encapsula as funções do hardware de gráficos que são dedicadas ao processamento de imagens de vídeo descompactadas. Os serviços de processamento de vídeo incluem desentrelaçamento e mixagem de vídeo.

Este tópico contém as seguintes seções:

-   [Visão geral](#overview)
-   [Criando um dispositivo de processamento de vídeo](#creating-a-video-processing-device)
    -   [Obter o ponteiro IDirectXVideoProcessorService](#get-the-idirectxvideoprocessorservice-pointer)
    -   [Enumerar os dispositivos de processamento de vídeo](#enumerate-the-video-processing-devices)
    -   [Enumerar formatos de Render-Target](#enumerate-render-target-formats)
    -   [Consultar os recursos do dispositivo](#query-the-device-capabilities)
    -   [Criar o dispositivo](#create-the-device)
-   [Blit de processo de vídeo](#video-process-blit)
    -   [Parâmetros de blit](#blit-parameters)
    -   [Exemplos de entrada](#input-samples)
-   [Composição de imagem](#image-composition)
    -   [Exemplo 1: formato Letterbox](#example-1-letterboxing)
    -   [Exemplo 2: alongar imagens de Subfluxo](#example-2-stretching-substream-images)
    -   [Exemplo 3: alturas de fluxo incompatíveis](#example-3-mismatched-stream-heights)
    -   [Exemplo 4: retângulo de destino menor que superfície de destino](#example-4-target-rectangle-smaller-than-destination-surface)
    -   [Exemplo 5: retângulos de origem](#example-5-source-rectangles)
    -   [Exemplo 6: retângulos de destino com interseção](#example-6-intersecting-destination-rectangles)
    -   [Exemplo 7: alongando e cortando vídeo](#example-7-stretching-and-cropping-video)
-   [Ordem de amostra de entrada](#input-sample-order)
    -   [Exemplo 1](#example-1-letterboxing)
    -   [Exemplo 2](#example-2-stretching-substream-images)
    -   [Exemplo 3](#example-3-mismatched-stream-heights)
    -   [Exemplo 4](#example-4-target-rectangle-smaller-than-destination-surface)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

O hardware de gráficos pode usar a GPU (unidade de processamento gráfico) para processar imagens de vídeo descompactadas. Um dispositivo de *processamento de vídeo* é um componente de software que encapsula essas funções. Os aplicativos podem usar um dispositivo de processamento de vídeo para executar funções como:

-   Desentrelaçamento e telecineon inverso
-   Misturando subfluxos de vídeo na imagem de vídeo principal
-   Ajuste de cores (Procamp) e filtragem de imagem
-   Dimensionamento de imagem
-   Conversão de espaço de cor
-   Mesclagem alfa

O diagrama a seguir mostra os estágios no pipeline de processamento de vídeo. O diagrama não deve mostrar uma implementação real. Por exemplo, o driver de gráficos pode combinar vários estágios em uma única operação. Todas essas operações podem ser executadas em uma única chamada para o dispositivo de processamento de vídeo. Alguns estágios mostrados aqui, como filtragem de ruído e de detalhes, podem não ser suportados pelo driver.

![diagrama mostrando os estágios do processamento de vídeo DXVA.](images/8581554e-a1bc-4cab-9ae1-99a6537e2a84.gif)

A entrada para o pipeline de processamento de vídeo sempre inclui um fluxo de vídeo *primário* , que contém os dados da imagem principal. O fluxo de vídeo primário determina a taxa de quadros para o vídeo de saída. Cada quadro do vídeo de saída é calculado em relação aos dados de entrada do fluxo de vídeo primário. Os pixels no fluxo primário são sempre opacos, sem dados alfa por pixel. O fluxo de vídeo primário pode ser progressivo ou entrelaçado.

Opcionalmente, o pipeline de processamento de vídeo pode receber até 15 subfluxos de vídeo. Um subfluxo contém dados de imagem auxiliares, como legendas codificadas ou subfiguras de DVD. Essas imagens são exibidas sobre o fluxo de vídeo primário e, em geral, não devem ser mostradas por si mesmas. As imagens de substream podem conter dados alfa por pixel e são sempre quadros progressivos. O dispositivo de processamento de vídeo Alpha-combina as imagens de subfluxo com o quadro desentrelaçado atual do fluxo de vídeo primário.

No restante deste tópico, o termo *imagem* é usado para os dados de entrada para um dispositivo de processamento de vídeo. Uma imagem pode consistir em um quadro progressivo, um único campo ou dois campos intercalados. A saída é sempre um quadro desentrelaçado.

Um driver de vídeo pode implementar mais de um dispositivo de processamento de vídeo, para fornecer diferentes conjuntos de recursos de processamento de vídeo. Os dispositivos são identificados por GUID. Os GUIDs a seguir são predefinidos:

-   **DXVA2 \_ VideoProcBobDevice**. Este dispositivo executa Bob deentrelaçando.
-   **DXVA2 \_ VideoProcProgressiveDevice**. Este dispositivo será usado se o vídeo contiver apenas quadros progressivos, sem quadros entrelaçados. (Alguns conteúdos de vídeo contêm uma mistura de quadros progressivos e entrelaçados. O dispositivo progressivo não pode ser usado para esse tipo de conteúdo de vídeo "misto", pois uma etapa de desentrelaçamento é necessária para os quadros entrelaçados.)

Cada driver de gráficos que dá suporte ao processamento de vídeo de DXVA deve implementar pelo menos esses dois dispositivos. O driver de gráficos também pode fornecer outros dispositivos, que são identificados por GUIDs específicos de driver. Por exemplo, um driver pode implementar um algoritmo de desentrelaçamento proprietário que produz uma saída de qualidade melhor do que Bob desentrelaçar. Alguns algoritmos de desentrelaçamento podem exigir imagens de referência diretas ou regressivas do fluxo principal. Nesse caso, o chamador deve fornecer essas imagens para o driver na sequência correta, conforme descrito posteriormente nesta seção.

Também é fornecido um dispositivo de software de referência. O dispositivo de software é otimizado para qualidade em vez de velocidade e pode não ser adequado para processamento de vídeo em tempo real. O dispositivo de software de referência usa o valor de GUID DXVA2 \_ VideoProcSoftwareDevice.

## <a name="creating-a-video-processing-device"></a>Criando um dispositivo de processamento de vídeo

Antes de usar o processamento de vídeo de DXVA, o aplicativo deve criar um dispositivo de processamento de vídeo. Aqui está uma breve descrição das etapas, que são explicadas com mais detalhes no restante desta seção:

1.  Obtenha um ponteiro para a interface [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) .
2.  Crie uma descrição do formato de vídeo para o fluxo de vídeo primário. Use esta descrição para obter uma lista dos dispositivos de processamento de vídeo que dão suporte ao formato de vídeo. Os dispositivos são identificados por GUID.
3.  Para um dispositivo específico, obtenha uma lista de formatos de destino de renderização com suporte no dispositivo. Os formatos são retornados como uma lista de valores de **D3DFORMAT** . Se você planeja misturar subfluxos, obtenha também uma lista dos formatos de subfluxo com suporte.
4.  Consulte os recursos de cada dispositivo.
5.  Crie o dispositivo de processamento de vídeo.

Às vezes, você pode omitir algumas dessas etapas. Por exemplo, em vez de obter a lista de formatos de destino de renderização, você poderia simplesmente tentar criar o dispositivo de processamento de vídeo com seu formato preferido e ver se ele foi bem sucedido. Um formato comum, como D3DFMT \_ X8R8G8B8, provavelmente será bem sucedido.

O restante desta seção descreve essas etapas em detalhes.

### <a name="get-the-idirectxvideoprocessorservice-pointer"></a>Obter o ponteiro IDirectXVideoProcessorService

A interface [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) é obtida do dispositivo Direct3D. Há duas maneiras de obter um ponteiro para essa interface:

-   De um dispositivo Direct3D.
-   Do [Direct3D gerenciador de dispositivos](direct3d-device-manager.md).

Se você tiver um ponteiro para um dispositivo Direct3D, poderá obter um ponteiro [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) chamando a função [**DXVA2CreateVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createvideoservice) . Passe um ponteiro para a interface **IDirect3DDevice9** do dispositivo e especifique IDirectXVideoProcessorService de **IID \_** para o parâmetro *riid* , conforme mostrado no código a seguir:


```C++
    // Create the DXVA-2 Video Processor service.
    hr = DXVA2CreateVideoService(g_pD3DD9, IID_PPV_ARGS(&g_pDXVAVPS));
```



n alguns casos, um objeto cria o dispositivo Direct3D e, em seguida, compartilha-o com outros objetos por meio do [Direct3D gerenciador de dispositivos](direct3d-device-manager.md). Nessa situação, você pode chamar [**IDirect3DDeviceManager9:: GetVideoService**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-getvideoservice) no Gerenciador de dispositivos para obter o ponteiro [**IDirectXVideoProcessorService**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice) , conforme mostrado no código a seguir:


```C++
HRESULT GetVideoProcessorService(
    IDirect3DDeviceManager9 *pDeviceManager,
    IDirectXVideoProcessorService **ppVPService
    )
{
    *ppVPService = NULL;

    HANDLE hDevice;

    HRESULT hr = pDeviceManager->OpenDeviceHandle(&hDevice);
    if (SUCCEEDED(hr))
    {
        // Get the video processor service 
        HRESULT hr2 = pDeviceManager->GetVideoService(
            hDevice, 
            IID_PPV_ARGS(ppVPService)
            );

        // Close the device handle.
        hr = pDeviceManager->CloseDeviceHandle(hDevice);

        if (FAILED(hr2))
        {
            hr = hr2;
        }
    }

    if (FAILED(hr))
    {
        SafeRelease(ppVPService);
    }

    return hr;
}
```



### <a name="enumerate-the-video-processing-devices"></a>Enumerar os dispositivos de processamento de vídeo

Para obter uma lista de dispositivos de processamento de vídeo, preencha uma estrutura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) com o formato do fluxo de vídeo primário e passe essa estrutura para o método [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) . O método retorna uma matriz de GUIDs, uma para cada dispositivo de processamento de vídeo que pode ser usado com este formato de vídeo.

Considere um aplicativo que renderiza um fluxo de vídeo no formato YUY2, usando a definição BT. 709 da cor YUV, com uma taxa de quadros de 29,97 quadros por segundo. Suponha que o conteúdo do vídeo consiste inteiramente em quadros progressivos. O fragmento de código a seguir mostra como preencher a descrição do formato e obter os GUIDs do dispositivo:


```C++
    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);
```



O código para este exemplo é obtido do exemplo de SDK do [DXVA2 \_ VideoProc](dxva2-videoproc-sample.md) .

A matriz *pGuids* neste exemplo é alocada pelo método [**GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids) , de modo que o aplicativo deve liberar a matriz chamando [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree). As etapas restantes podem ser executadas usando qualquer um dos GUIDs de dispositivo retornados por esse método.

### <a name="enumerate-render-target-formats"></a>Enumerar formatos de Render-Target

Para obter a lista de formatos de destino de renderização com suporte pelo dispositivo, passe o GUID do dispositivo e a estrutura [**DXVA2 \_ VideoDesc**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc) para o método [**IDirectXVideoProcessorService:: GetVideoProcessorRenderTargets**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorrendertargets) , conforme mostrado no código a seguir:


```C++
    // Query the supported render-target formats.

    UINT i, count;
    D3DFORMAT* formats = NULL;

    HRESULT hr = g_pDXVAVPS->GetVideoProcessorRenderTargets(
        guid, &g_VideoDesc, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorRenderTargets failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_RENDER_TARGET_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the render-target format.\n"));
        return FALSE;
    }
```



O método retorna uma matriz de valores **D3DFORMAT** . Neste exemplo, onde o tipo de entrada é YUY2, uma lista típica de formatos pode ser D3DFMT \_ X8R8G8B8 (32-bit RGB) e D3DMFT \_ YUY2 (o formato de entrada). No entanto, a lista exata dependerá do driver.

A lista de formatos disponíveis para os subfluxos pode variar dependendo do formato de destino de renderização e do formato de entrada. Para obter a lista de formatos de Subfluxo, passe o GUID do dispositivo, a estrutura de formato e o formato de destino de renderização para o método [**IDirectXVideoProcessorService:: GetVideoProcessorSubStreamFormats**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorsubstreamformats) , conforme mostrado no código a seguir:


```C++
    // Query the supported substream formats.

    formats = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorSubStreamFormats(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &count, &formats);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorSubStreamFormats failed: 0x%x.\n", hr));
        return FALSE;
    }

    for (i = 0; i < count; i++)
    {
        if (formats[i] == VIDEO_SUB_FORMAT)
        {
            break;
        }
    }

    CoTaskMemFree(formats);

    if (i >= count)
    {
        DBGMSG((L"The device does not support the substream format.\n"));
        return FALSE;
    }
```



Esse método retorna outra matriz de valores **D3DFORMAT** . Os formatos de Subfluxo típicos são AYUV e AI44.

### <a name="query-the-device-capabilities"></a>Consultar os recursos do dispositivo

Para obter os recursos de um dispositivo específico, passe o GUID do dispositivo, a estrutura de formato e um formato de destino de renderização para o método [**IDirectXVideoProcessorService:: GetVideoProcessorCaps**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps) . O método preenche uma estrutura de estrutura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) com os recursos do dispositivo.


```C++
    // Query video processor capabilities.

    hr = g_pDXVAVPS->GetVideoProcessorCaps(
        guid, &g_VideoDesc, VIDEO_RENDER_TARGET_FORMAT, &g_VPCaps);

    if (FAILED(hr))
    {
        DBGMSG((L"GetVideoProcessorCaps failed: 0x%x.\n", hr));
        return FALSE;
    }
```



### <a name="create-the-device"></a>Criar o dispositivo

Para criar o dispositivo de processamento de vídeo, chame [**IDirectXVideoProcessorService:: CreateVideoProcessor**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-createvideoprocessor). A entrada para esse método é o GUID do dispositivo, a descrição do formato, o formato de destino de renderização e o número máximo de subfluxos que você planeja misturar. O método retorna um ponteiro para a interface [**IDirectXVideoProcessor**](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor) , que representa o dispositivo de processamento de vídeo.


```C++
    // Finally create a video processor device.

    hr = g_pDXVAVPS->CreateVideoProcessor(
        guid,
        &g_VideoDesc,
        VIDEO_RENDER_TARGET_FORMAT,
        SUB_STREAM_COUNT,
        &g_pDXVAVPD
        );
```



## <a name="video-process-blit"></a>Blit de processo de vídeo

A principal operação de processamento de vídeo é o *blit de processamento de vídeo*. (Um *blit* é qualquer operação que combina dois ou mais bitmaps em um único bitmap. Um blit de processamento de vídeo combina imagens de entrada para criar um quadro de saída.) Para executar um blit de processamento de vídeo, chame [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt). Esse método passa um conjunto de amostras de vídeo para o dispositivo de processamento de vídeo. Em resposta, o dispositivo de processamento de vídeo processa as imagens de entrada e gera um quadro de saída. O processamento pode incluir desentrelaçamento, conversão de espaço em cores e mistura de Subfluxo. A saída é gravada em uma superfície de destino fornecida pelo chamador.

O método [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) usa os seguintes parâmetros:

-   o *pRT* aponta para uma superfície de destino de renderização **IDirect3DSurface9** que receberá o quadro de vídeo processado.
-   *pBltParams* aponta para uma [**estrutura \_ VideoProcessBltParams DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) que especifica os parâmetros para o blit.
-   *pSamples* é o endereço de uma matriz de [**estruturas \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) . Essas estruturas contêm os exemplos de entrada para o blit.
-   *NumSamples* fornece o tamanho da matriz *pSamples* .
-   O parâmetro *reservado* é reservado e deve ser definido como **nulo**.

Na matriz *pSamples* , o chamador deve fornecer os seguintes exemplos de entrada:

-   A imagem atual do fluxo de vídeo primário.
-   Imagens de referência para frente e para trás, se exigido pelo algoritmo de desentrelaçamento.
-   Zero ou mais imagens de Subfluxo, até um máximo de 15 subfluxos.

O driver espera que essa matriz esteja em uma ordem específica, conforme descrito em [ordem de amostra de entrada](#input-sample-order).

### <a name="blit-parameters"></a>Parâmetros de blit

A estrutura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) contém parâmetros gerais para o blit. Os parâmetros mais importantes são armazenados nos seguintes membros da estrutura:

-   **TargetFrame** é a hora da apresentação do quadro de saída. Para conteúdo progressivo, essa hora deve ser igual à hora de início do quadro atual do fluxo de vídeo primário. Esse tempo é especificado no membro **inicial** da estrutura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) para esse exemplo de entrada.

    Para conteúdo entrelaçado, um quadro com dois campos intercalados produz dois quadros de saída desentrelaçados. No primeiro quadro de saída, a hora da apresentação deve ser igual à hora de início da imagem atual no fluxo de vídeo primário, assim como o conteúdo progressivo. No segundo quadro de saída, a hora de início deve ser igual ao ponto médio entre a hora de início da imagem atual no fluxo de vídeo primário e a hora de início da próxima imagem no fluxo. Por exemplo, se o vídeo de entrada for de 25 quadros por segundo (50 campos por segundo), os quadros de saída terão os carimbos de data/hora mostrados na tabela a seguir. Os carimbos de data/hora são mostrados em unidades de 100 nanossegundos.

    

    | Imagem de entrada | **TargetFrame** (1) | **TargetFrame** (2) |
    |---------------|---------------------|---------------------|
    | 0             | 0                   | 200000              |
    | 400000        | 0                   | 600000              |
    | 800000        | 800000              | 1.000.000             |
    | 1,2 milhões       | 1,2 milhões             | 1,4 milhões             |

    

     

    Se o conteúdo entrelaçado consistir em campos únicos em vez de campos intercalados, os tempos de saída sempre corresponderão aos tempos de entrada, como com conteúdo progressivo.

-   **TargetRect** define uma região retangular dentro da superfície de destino. O blit gravará a saída nessa região. Especificamente, todos os pixels dentro de **TargetRect** serão modificados e nenhum pixel fora do **TargetRect** será modificado. O retângulo de destino define o retângulo delimitador para todos os fluxos de vídeo de entrada. O posicionamento de fluxos individuais dentro desse retângulo é controlado por meio do parâmetro *pSamples* de [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt).
-   **BackgroundColor** fornece a cor do plano de fundo sempre que nenhuma imagem de vídeo é exibida. Por exemplo, quando uma imagem de vídeo de 16 x 9 é exibida dentro de uma área 4 x 3 (formato Letterbox), as regiões letterboxed são exibidas com a cor do plano de fundo. A cor do plano de fundo só se aplica dentro do retângulo de destino (**TargetRect**). Quaisquer pixels fora de **TargetRect** não são modificados.
-   **DestFormat** descreve o espaço de cores para o vídeo de saída — por exemplo, se a cor ITU-R BT. 709 ou BT. 601 é usada. Essas informações podem afetar a forma como a imagem é exibida. Para obter mais informações, consulte [informações de cores estendidas](extended-color-information.md).

Outros parâmetros são descritos na página de referência da estrutura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .

### <a name="input-samples"></a>Exemplos de entrada

O parâmetro *pSamples* de [**IDirectXVideoProcessor:: VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) aponta para uma matriz de [**estruturas \_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) . Cada uma dessas estruturas contém informações sobre um exemplo de entrada e um ponteiro para a superfície do Direct3D que contém o exemplo. Cada exemplo é um dos seguintes:

-   A imagem atual do fluxo primário.
-   Uma imagem de referência para frente ou para trás do fluxo principal, usada para desentrelaçar.
-   Uma imagem de Subfluxo.

A ordem exata na qual os exemplos devem aparecer na matriz é descrita posteriormente, na seção ordem de [exemplo de entrada](#input-sample-order).

Até 15 imagens de Subfluxo podem ser fornecidas, embora a maioria dos aplicativos de vídeo precise apenas de um subfluxo, no máximo. O número de subfluxos pode ser alterado com cada chamada para [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt). As imagens de substream são indicadas pela configuração do membro **SampleFormat. SampleFormat** da estrutura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) igual a DXVA2 \_ SampleSubStream. Para o fluxo de vídeo primário, esse membro descreve o entrelaçamento do vídeo de entrada. Para obter mais informações, consulte Enumeração do [**DXVA2 \_ SampleFormat**](/windows/desktop/api/dxva2api/ne-dxva2api-dxva2_sampleformat) .

Para o fluxo de vídeo primário, os membros de **início** e **término** da estrutura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) fornecem os horários de início e término do exemplo de entrada. Para imagens de Subfluxo, defina esses valores como zero, porque a hora da apresentação é sempre calculada a partir do fluxo primário. O aplicativo é responsável por controlar quando cada imagem de Subfluxo deve ser apresentada e enviá-la para [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) no momento adequado.

Dois retângulos definem como o vídeo de origem é posicionado para cada fluxo:

-   O membro **SrcRect** da estrutura [**\_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) especifica o *retângulo de origem*, uma região retangular da imagem de origem que será exibida no quadro de saída composto. Para cortar a imagem, defina-a com um valor menor que o tamanho do quadro. Caso contrário, defina-o como igual ao tamanho do quadro.
-   O membro **DstRect** da mesma estrutura especifica o *retângulo de destino*, uma região retangular da superfície de destino onde o quadro de vídeo será exibido.

O driver blits pixels do retângulo de origem para o retângulo de destino. Os dois retângulos podem ter diferentes tamanhos ou proporções; o driver dimensionará a imagem conforme necessário. Além disso, cada fluxo de entrada pode usar um fator de dimensionamento diferente. Na verdade, o dimensionamento pode ser necessário para produzir a taxa de proporção correta no quadro de saída. O driver não pega a taxa de proporção de pixel da origem em conta, portanto, se a imagem de origem usar pixels não quadrados, cabe ao aplicativo calcular o retângulo de destino correto.

Os formatos de Subfluxo preferenciais são AYUV e AI44. O último é um formato de palete com 16 cores. As entradas da paleta são especificadas no membro **PAL** da estrutura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) . (Se o formato de vídeo de origem for expresso originalmente como um tipo de mídia Media Foundation, as entradas da paleta serão armazenadas no atributo de [**\_ \_ paleta MF MT**](mf-mt-palette-attribute.md) .) Para formatos não paletes, limpe essa matriz para zero.

## <a name="image-composition"></a>Composição de imagem

Cada operação blit é definida pelos três retângulos a seguir:

-   O retângulo de *destino* (**TargetRect**) define a região dentro da superfície de destino onde a saída será exibida. A imagem de saída é recortada para este retângulo.
-   O retângulo de *destino* de cada fluxo (**DstRect**) define onde o fluxo de entrada aparece na imagem compostada.
-   O retângulo de *origem* de cada fluxo (**SrcRect**) define qual parte da imagem de origem é exibida.

Os retângulos de destino e destino são especificados em relação à superfície de destino. O retângulo de origem é especificado em relação à imagem de origem. Todos os retângulos são especificados em pixels.

![diagrama mostrando os retângulos de origem, destino e destino](images/dxva-vp-rects.gif)

O dispositivo de processamento de vídeo Alpha combina as imagens de entrada, usando qualquer uma das seguintes fontes de dados alfa:

-   Dados alfa por pixel de subfluxos.
-   Um valor alfa planar para cada fluxo de vídeo, especificado no membro **PlanarAlpha** da estrutura [**\_ VideoSample DXVA2**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) .
-   O valor alfa planar da imagem compostada, especificado no membro **alfa** da estrutura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) . Esse valor é usado para misturar toda a imagem composta com a cor do plano de fundo.

Esta seção fornece uma série de exemplos que mostram como o dispositivo de processamento de vídeo cria a imagem de saída.

### <a name="example-1-letterboxing"></a>Exemplo 1: formato Letterbox

Este exemplo mostra como Letterbox a imagem de origem, definindo o retângulo de destino como menor do que o retângulo de destino. O fluxo de vídeo primário neste exemplo é uma imagem 720 × 480 e deve ser exibido com uma taxa de proporção de 16:9. A superfície de destino é de 640 × 480 pixels (taxa de proporção de 4:3). Para obter a taxa de proporção correta, o retângulo de destino deve ser 640 × 360. Para simplificar, este exemplo não inclui um subfluxo. O diagrama a seguir mostra os retângulos de origem e de destino.

![diagrama mostrando formato letterbox.](images/428105fa-a26b-48a6-991d-44d24ab786b1.gif)

O diagrama anterior mostra os seguintes retângulos:

-   Retângulo de destino: {0, 0, 640, 480}
-   Vídeo primário:

    -   Retângulo de origem: {0, 0, 720, 480}
    -   Retângulo de destino: {0, 60, 640, 420}

O driver desentrelaçará o vídeo, reduzirá o quadro desentrelaçado para 640 × 360 e blit o quadro no retângulo de destino. O retângulo de destino é maior que o retângulo de destino, portanto, o driver usará a cor da tela de fundo para preencher as barras horizontais acima e abaixo do quadro. A cor do plano de fundo é especificada na estrutura [**DXVA2 \_ VideoProcessBltParams**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessbltparams) .

### <a name="example-2-stretching-substream-images"></a>Exemplo 2: alongar imagens de Subfluxo

As imagens de Subfluxo podem se estender além da imagem de vídeo principal. No vídeo em DVD, por exemplo, o fluxo de vídeo primário pode ter uma taxa de proporção de 4:3, enquanto o Subfluxo é 16:9. Neste exemplo, ambos os fluxos de vídeo têm as mesmas dimensões de origem (720 × 480), mas o Subfluxo destina-se a ser mostrado com uma taxa de proporção de 16:9. Para obter essa taxa de proporção, a imagem de Subfluxo é esticada horizontalmente. Os retângulos de origem e de destino são mostrados no diagrama a seguir.

![diagrama mostrando o alongamento da imagem de Subfluxo.](images/7ab31c65-06b9-4843-90b8-2f9fb6f6b20e.gif)

O diagrama anterior mostra os seguintes retângulos:

-   Retângulo de destino: {0, 0, 854, 480}
-   Vídeo primário:

    -   Retângulo de origem: {0, 0, 720, 480}
    -   Retângulo de destino: {0, 107, 474, 480}

-   Subfluxo
    -   Retângulo de origem: {0, 0, 720, 480}
    -   Retângulo de destino: {0, 0, 854, 480}

Esses valores preservam a altura da imagem e dimensionam as imagens horizontalmente. Nas regiões em que as duas imagens aparecem, elas são alfa misturadas. Onde a imagem de Subfluxo ultrapassa o vídeo primária, o Subfluxo é alfa misturado com a cor do plano de fundo. Essas contas de mesclagem alfa para as cores alteradas no lado direito do diagrama.

### <a name="example-3-mismatched-stream-heights"></a>Exemplo 3: alturas de fluxo incompatíveis

No exemplo anterior, o Subfluxo e o fluxo principal têm a mesma altura. Os fluxos também podem ter alturas incompatíveis, conforme mostrado neste exemplo. As áreas dentro do retângulo de destino onde nenhum vídeo é exibido são desenhadas usando a cor do plano de fundo — preto neste exemplo. Os retângulos de origem e de destino são mostrados no diagrama a seguir.

![diagrama mostrando alturas de fluxo incompatíveis,](images/0190a15a-d971-450f-90ed-ce5633e1069c.gif)

O diagrama anterior mostra os seguintes retângulos:

-   Retângulo de destino: {0, 0, 150, 85}
-   Vídeo primário:
    -   Retângulo de origem: {0, 0, 150, 50}
    -   Retângulo de destino: {0, 17, 150, 67}
-   Subfluxo
    -   Retângulo de origem: {0, 0, 100, 85}
    -   Retângulo de destino: {25, 0, 125, 85}

### <a name="example-4-target-rectangle-smaller-than-destination-surface"></a>Exemplo 4: retângulo de destino menor que superfície de destino

Este exemplo mostra um caso em que o retângulo de destino é menor do que a superfície de destino.

![diagrama mostrando um blit para um retângulo de destino.](images/360a85a3-333c-4b32-b8f7-1beb1e805921.gif)

O diagrama anterior mostra os seguintes retângulos:

-   Superfície de destino: {0, 0, 300, 200}
-   Retângulo de destino: {0, 0, 150, 85}
-   Vídeo primário:
    -   Retângulo de origem: {0, 0, 150, 50}
    -   Retângulo de destino: {0, 17, 150, 67}
-   Subfluxo
    -   Retângulo de origem: {0, 0, 100, 85}
    -   Retângulo de destino: {25, 0, 125, 85}

Os pixels fora do retângulo de destino não são modificados, portanto, a cor do plano de fundo aparece apenas dentro do retângulo de destino. A área pontilhada indica partes da superfície de destino que não são afetadas pelo blit.

### <a name="example-5-source-rectangles"></a>Exemplo 5: retângulos de origem

Se você especificar um retângulo de origem menor do que a imagem de origem, o driver blitrá apenas essa parte da imagem. Neste exemplo, os retângulos de origem especificam o quadrante inferior direito do fluxo de vídeo primário e o quadrante inferior esquerdo do Subfluxo (indicado pelas marcas de hash no diagrama). Os retângulos de destino são os mesmos tamanhos que os retângulos de origem, portanto, o vídeo não é ampliado. Os retângulos de origem e de destino são mostrados no diagrama a seguir.

![diagrama mostrando um blit de dois retângulos de origem.](images/b1de4cc3-0155-40be-acac-b486e2af8c0d.gif)

O diagrama anterior mostra os seguintes retângulos:

-   Retângulo de destino: {0, 0, 720, 576}
-   Vídeo primário:
    -   Tamanho da superfície de origem: {0, 0, 720, 480}
    -   Retângulo de origem: {360, 240, 720, 480}
    -   Retângulo de destino: {0, 0, 360, 240}
-   Subfluxo
    -   Tamanho da superfície de origem: {0, 0, 640, 576}
    -   Retângulo de origem: {0, 288, 320, 576}
    -   Retângulo de destino: {400, 0, 720, 288}

### <a name="example-6-intersecting-destination-rectangles"></a>Exemplo 6: retângulos de destino com interseção

Este exemplo é semelhante ao anterior, mas os retângulos de destino se cruzam. As dimensões da superfície são as mesmas do exemplo anterior, mas os retângulos de origem e de destino não são. Novamente, o vídeo é cortado, mas não ampliado. Os retângulos de origem e de destino são mostrados no diagrama a seguir.

![diagrama mostrando retângulos de destino de interseção.](images/fbe450cb-c84d-4110-9515-00f27601528e.gif)

O diagrama anterior mostra os seguintes retângulos:

-   Retângulo de destino: {0, 0, 720, 576}
-   Vídeo primário:
    -   Tamanho da superfície de origem: {0, 0, 720, 480}
    -   Retângulo de origem: {260, 92, 720, 480}
    -   Retângulo de destino: {0, 0, 460, 388}
-   Subfluxo
    -   Tamanho da superfície de origem: {0, 0, 640, 576}
    -   Retângulo de origem: {0, 0, 460, 388}
    -   Retângulo de destino: {260, 188, 720, 576}

### <a name="example-7-stretching-and-cropping-video"></a>Exemplo 7: alongando e cortando vídeo

Neste exemplo, o vídeo é alongado, bem como cortado. Uma região 180 × 120 de cada fluxo é ampliada para cobrir uma área 360 × 240 no retângulo de destino.

![diagrama mostrando alongamento e corte.](images/ce83529c-8545-492c-9d3e-ef221c30e326.gif)

O diagrama anterior mostra os seguintes retângulos:

-   Retângulo de destino: {0, 0, 720, 480}
-   Vídeo primário:
    -   Tamanho da superfície de origem: {0, 0, 360, 240}
    -   Retângulo de origem: {180, 120, 360, 240}
    -   Retângulo de destino: {0, 0, 360, 240}
-   Subfluxo
    -   Tamanho da superfície de origem: {0, 0, 360, 240}
    -   Retângulo de origem: {0, 0, 180, 120}
    -   Retângulo de destino: {360, 240, 720, 480}

## <a name="input-sample-order"></a>Ordem de amostra de entrada

O parâmetro *pSamples* do método [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) é um ponteiro para uma matriz de exemplos de entrada. Os exemplos do fluxo de vídeo primário aparecem primeiro, seguidos pelas imagens de Subfluxo na ordem Z. Os exemplos devem ser colocados na matriz na seguinte ordem:

-   Os exemplos do fluxo de vídeo primário aparecem primeiro na matriz, em ordem temporal. Dependendo do modo de desentrelaçamento, o driver pode exigir um ou mais exemplos de referência do fluxo de vídeo primário. Os membros **NumForwardRefSamples** e **NumBackwardRefSamples** da estrutura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) especificam quantas amostras de referência para frente e para trás são necessárias. O chamador deve fornecer esses exemplos de referência, mesmo se o conteúdo do vídeo for progressivo e não exigir desentrelaçamento. (Isso pode ocorrer quando os quadros progressivos são fornecidos a um dispositivo de desentrelaçamento, por exemplo, quando a origem contém uma mistura de quadros entrelaçados e progressivos.)
-   Após os exemplos do fluxo de vídeo primário, a matriz pode conter até 15 amostras de Subfluxo, organizadas em ordem Z, de baixo para cima. Os subfluxos são sempre progressivos e não exigem imagens de referência.

A qualquer momento, o fluxo de vídeo primário pode alternar entre conteúdo entrelaçado e progressivo, e o número de subfluxos pode ser alterado.

O membro **SampleFormat. SampleFormat** da estrutura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) indica o tipo de imagem. Para imagens de Subfluxo, defina esse valor como DXVA2 \_ SampleSubStream. Para imagens progressivas, o valor é DXVA2 \_ SampleProgressiveFrame. Para imagens entrelaçadas, o valor depende do layout do campo.

Se o driver exigir amostras de referência para frente e para trás, o número completo de amostras poderá não estar disponível no início da sequência de vídeo. Nesse caso, inclua entradas para elas na matriz *pSamples* , mas marque os exemplos ausentes como tendo o tipo DXVA2 \_ SampleUnknown.

Os membros **inicial** e **final** da estrutura [**DXVA2 \_ VideoSample**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videosample) fornecem o local temporal de cada amostra. Esses valores são usados apenas para exemplos do fluxo de vídeo primário. Para imagens de Subfluxo, defina ambos os membros como zero.

Os exemplos a seguir podem ajudar a esclarecer esses requisitos.

### <a name="example-1"></a>Exemplo 1

O caso mais simples ocorre quando não há subfluxos e o algoritmo de desentrelaçamento não requer exemplos de referência (**NumForwardRefSamples** e **NumBackwardRefSamples** são ambos zero). Bob desentrelaçado é um exemplo desse algoritmo. Nesse caso, a matriz *pSamples* deve conter uma única superfície de entrada, conforme mostrado na tabela a seguir.



| Índice           | Tipo de superfície        | Local temporal |
|-----------------|---------------------|-------------------|
| *pSamples* \[ 0\] | Imagem entrelaçada. | *T*               |



 

O valor de hora *T* é considerado como a hora de início do quadro de vídeo atual.

### <a name="example-2"></a>Exemplo 2

Neste exemplo, o aplicativo combina dois subfluxos com o fluxo principal. O algoritmo de desentrelaçamento não requer exemplos de referência. A tabela a seguir mostra como esses exemplos são organizados na matriz *pSamples* .



| Índice           | Tipo de superfície       | Local temporal | Ordem z |
|-----------------|--------------------|-------------------|---------|
| *pSamples* \[ 0\] | Imagem entrelaçada | *T*               | 0       |
| *pSamples* \[ uma\] | Subfluxo          | 0                 | 1       |
| *pSamples* \[ 2\] | Subfluxo          | 0                 | 2       |



 

### <a name="example-3"></a>Exemplo 3

Agora suponha que o algoritmo de desentrelaçamento exija um exemplo de referência retroativa e um exemplo de referência de encaminhamento. Além disso, duas imagens de Subfluxo são fornecidas, para um total de cinco superfícies. A ordenação correta é mostrada na tabela a seguir.



| Índice           | Tipo de superfície                   | Local temporal | Ordem z        |
|-----------------|--------------------------------|-------------------|----------------|
| *pSamples* \[ 0\] | Imagem entrelaçada (referência) | *T* − 1            | Não aplicável |
| *pSamples* \[ uma\] | Imagem entrelaçada             | *T*               | 0              |
| *pSamples* \[ 2\] | Imagem entrelaçada (referência) | *T* + 1            | Não aplicável |
| *pSamples* \[ Beta\] | Subfluxo                      | 0                 | 1              |
| *pSamples* \[ quatro\] | Subfluxo                      | 0                 | 2              |



 

A hora *T* − 1 é a hora de início do quadro antes do quadro atual e *T* + 1 é a hora de início do quadro a seguir.

Se o fluxo de vídeo mudar para o conteúdo progressivo, usando o mesmo modo de desentrelaçamento, o aplicativo deverá fornecer o mesmo número de amostras, conforme mostrado na tabela a seguir.



| Índice           | Tipo de superfície                    | Local temporal | Ordem z        |
|-----------------|---------------------------------|-------------------|----------------|
| *pSamples* \[ 0\] | Imagem progressiva (referência) | *T* − 1            | Não aplicável |
| *pSamples* \[ uma\] | Imagem progressiva             | *T*               | 0              |
| *pSamples* \[ 2\] | Imagem progressiva (referência) | *T* + 1            | Não aplicável |
| *pSamples* \[ Beta\] | Subfluxo                       | 0                 | 1              |
| *pSamples* \[ quatro\] | Subfluxo                       | 0                 | 2              |



 

### <a name="example-4"></a>Exemplo 4

No início de uma sequência de vídeo, amostras de referência para frente e para trás podem não estar disponíveis. Quando isso acontece, as entradas para os exemplos ausentes são incluídas na matriz *pSamples* , com o tipo de exemplo DXVA2 \_ SampleUnknown.

Supondo que o modo de desentrelaçamento precise de um exemplo de referência posterior e de um retrocesso, as três primeiras chamadas para [**VideoProcessBlt**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) teriam as sequências de entradas mostradas nas três tabelas a seguir.



| Índice           | Tipo de superfície                   | Local temporal |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ 0\] | Unknown                        | 0                 |
| *pSamples* \[ uma\] | Unknown                        | 0                 |
| *pSamples* \[ 2\] | Imagem entrelaçada (referência) | *T* + 1            |



 



| Índice           | Tipo de superfície                   | Local temporal |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ 0\] | Unknown                        | 0                 |
| *pSamples* \[ uma\] | Imagem entrelaçada             | *T*               |
| *pSamples* \[ 2\] | Imagem entrelaçada (referência) | *T* + 1            |



 



| Índice           | Tipo de superfície                   | Local temporal |
|-----------------|--------------------------------|-------------------|
| *pSamples* \[ 0\] | Imagem entrelaçada             | *T* − 1            |
| *pSamples* \[ uma\] | Imagem entrelaçada             | *T*               |
| *pSamples* \[ 2\] | Imagem entrelaçada (referência) | *T* + 1            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Aceleração de vídeo do DirectX 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[Exemplo de VideoProc de DXVA2 \_](dxva2-videoproc-sample.md)
</dt> </dl>

 

 
