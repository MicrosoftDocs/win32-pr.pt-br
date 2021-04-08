---
description: Usando os controles do mixer de vídeo
ms.assetid: 475996c6-a205-4133-8882-f55beaf9f8fd
title: Usando os controles do mixer de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a8a062c6f984e0eac0128bd67c72bf691c95af6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010799"
---
# <a name="using-the-video-mixer-controls"></a>Usando os controles do mixer de vídeo

O mixer EVR fornece várias interfaces que um aplicativo pode usar para controlar como o mixer processa o vídeo. Essas interfaces podem ser usadas tanto no DirectShow quanto no Media Foundation.



| Interface                                                      | Descrição                                                                                                                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Interface [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap)   | Alfa-combina uma imagem de bitmap estática no vídeo.                                                                                                                                                                                          |
| Interface [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) | Controla como o EVR combina subfluxos de vídeo.                                                                                                                                                                                                |
| Interface [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor)       | Controla o ajuste de cores, os filtros de imagem e outros recursos de processamento de vídeo. Essa interface fornece acesso à funcionalidade implementada pelo driver de gráficos, de modo que os recursos exatos dependerão do driver de gráficos do usuário. |



 

A maneira correta de obter ponteiros para essas interfaces depende se você está usando a versão do DirectShow do EVR ou a versão Media Foundation. Para o Media Foundation EVR, também depende se você está usando o EVR diretamente ou usando-o por meio da [sessão de mídia](media-session.md). (Normalmente, um aplicativo usará o EVR por meio da sessão de mídia, não diretamente).

Para obter um ponteiro para qualquer uma dessas interfaces, faça o seguinte:

1.  Obtenha um ponteiro para a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) no EVR.

    -   Se você estiver usando o filtro EVR do DirectShow, chame **QueryInterface** no filtro.

    -   Se você estiver usando o coletor de mídia do EVR diretamente, chame **QueryInterface** no coletor de mídia.

    -   Se você estiver usando a sessão de mídia, chame **QueryInterface** na sessão de mídia.

2.  Se você estiver usando a sessão de mídia, aguarde até que a sessão de mídia envie o evento [MESessionTopologyStatus](mesessiontopologystatus.md) com um valor de status de MF \_ TOPOSTATUS \_ Ready. (Ignore esta etapa se você não estiver usando a sessão de mídia.)

3.  Chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter a interface do mixer. Use o serviço de mixer de vídeo MR do identificador de serviço \_ \_ \_ .

## <a name="alpha-blending-a-bitmap-onto-the-video"></a>Alfa combinando um bitmap no vídeo

Você pode usar a interface [**IMFVideoMixerBitmap**](/windows/desktop/api/evr9/nn-evr9-imfvideomixerbitmap) para alfa misturar um bitmap estático no vídeo durante a reprodução. Você pode armazenar o bitmap em uma superfície do Direct3D, especificada como um ponteiro **IDirect3DSurface9** , ou usar um bitmap GDI.

Se você usar uma superfície do Direct3D para o bitmap, a superfície poderá conter dados alfa por pixel, que serão usados quando o mixer alfa misturar a imagem. Como alternativa, você pode definir uma chave de cor, ou seja, uma única cor que será transparente onde quer que apareça no bitmap. Além disso, você pode especificar um valor alfa que será aplicado a toda a imagem. Você também pode definir um retângulo de origem para cortar o bitmap e um retângulo de destino para posicionar o bitmap dentro do quadro de vídeo.

Para definir o bitmap, chame [**IMFVideoMixerBitmap:: SetAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-setalphabitmap). Esse método usa um ponteiro para uma estrutura [**MFVideoAlphaBitmap**](/windows/desktop/api/evr9/ns-evr9-mfvideoalphabitmap) que especifica o bitmap e os parâmetros de mesclagem alfa. Para obter um exemplo de código, consulte o tópico de referência para o método **SetAlphaBitmap** .

Depois de definir o bitmap, você pode atualizar os parâmetros de mesclagem, incluindo a origem e o destino recangles, chamando [**IMFVideoMixerBitmap:: UpdateAlphaBitmapParameters**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-updatealphabitmapparameters). A atualização entra em vigor no próximo quadro de vídeo. O vídeo deve estar sendo reproduzido para que a atualização ocorra. Você pode usar esse método para executar animações simples no bitmap. (Se você precisar de efeitos mais sofisticados, considere escrever um mixer EVR personalizado.)

Para limpar o bitmap, chame [**IMFVideoMixerBitmap:: ClearAlphaBitmap**](/windows/desktop/api/evr9/nf-evr9-imfvideomixerbitmap-clearalphabitmap).

## <a name="controlling-substreams"></a>Controlando subfluxos

O EVR pode misturar um ou mais subfluxos de vídeo no fluxo de vídeo primário. Para controlar a combinação de Subfluxo, use a interface [**IMFVideoMixerControl**](/windows/desktop/api/evr/nn-evr-imfvideomixercontrol) .

-   Chame [**IMFVideoMixerControl:: SetStreamOutputRect**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamoutputrect) para definir a posição de um subfluxo dentro do quadro de vídeo composto.

-   Chame [**IMFVideoMixerControl:: SetStreamZOrder**](/windows/desktop/api/evr/nf-evr-imfvideomixercontrol-setstreamzorder) para definir a ordem z para os subfluxos. O EVR desenha os fluxos de vídeo na ordem dos valores de ordem z, começando com zero. O fluxo de vídeo primário sempre é o primeiro na ordem z.

## <a name="video-processor-settings"></a>Configurações do processador de vídeo

O mixer EVR usa a DXVA (aceleração de vídeo do DirectX) para executar o processamento de vídeo nos fluxos de entrada. Os recursos de processamento exatos dependem do driver de gráficos. Os recursos de processamento de vídeo são descritos usando a estrutura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) . Um conjunto específico de recursos é chamado de *modo de processamento de vídeo*, cada modo que está sendo identificado por um GUID. Para obter uma lista de GUIDs predefinidos, consulte [**IDirectXVideoProcessorService:: GetVideoProcessorDeviceGuids**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessordeviceguids). O driver pode definir GUIDs adicionais específicos do fornecedor, representando diferentes combinações de recursos.

Para localizar os modos com suporte e os recursos de cada modo, faça o seguinte:

1.  Chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter um ponteiro para a interface [**IMFVideoProcessor**](/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor) do mixer.

2.  Chame [**IMFVideoProcessor:: GetAvailableVideoProcessorModes**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getavailablevideoprocessormodes). Esse método retorna uma matriz de GUIDs, que identifica os modos de processador de vídeo disponíveis. A lista é retornada em ordem de qualidade decrescente, o modo com a qualidade mais alta aparecendo primeiro na lista. A lista pode ser alterada dependendo do formato do vídeo.

3.  Para cada GUID na lista, chame [**IMFVideoProcessor:: GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) para localizar os recursos do modo de processador de vídeo correspondente. O método preenche uma estrutura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) com uma descrição dos recursos.

4.  Para selecionar um modo, chame [**IMFVideoProcessor:: SetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode). Caso contrário, o EVR selecionará automaticamente um modo quando o streaming começar. Nesse caso, você pode chamar [**IMFVideoProcessor:: GetVideoProcessorMode**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessormode) para descobrir qual modo foi selecionado.

A maioria dos campos na estrutura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) descreve o comportamento de driver de nível baixo e não é de interesse em um aplicativo típico. Os campos a seguir têm maior probabilidade de serem interessantes:

-   **DeviceCaps**. Esse campo indica se o processamento de vídeo é executado em hardware ou software e se o driver de gráficos é um driver de DXVA 1,0 mais antigo.

-   **DeinterlaceTechnology**. Este campo fornece alguma indicação de qual nível de qualidade de desentrelaçamento você pode esperar se o vídeo de origem estiver entrelaçado.

-   **ProcAmpControlCaps**. Este campo especifica quais controles de ajuste de cor estão disponíveis. Para obter uma lista de possíveis ajustes de cor, consulte [configurações do Procamp](procamp-settings.md). Se o driver não puder executar o ajuste de cor, esse campo será zero.

-   **VideoProcessorOperations**. Este campo contém sinalizadores que descrevem diversos recursos de processamento de vídeo. Dois sinalizadores de importância específica são o \_ sinalizador de \_ subfluxos do DXVA2 VideoProcess e \_ o \_ sinalizador de subfluxos do DXVA2 VideoProcess. Pelo menos um desses sinalizadores deve estar presente para que o EVR misture subfluxos para o fluxo de vídeo de referência. Se nenhum sinalizador estiver presente, o EVR será limitado a um fluxo de vídeo.

-   **NoiseFilterTechnology**. Este campo indica quais filtros de ruído são suportados pelo driver de gráficos. Se o driver não oferecer suporte à filtragem de ruído, o valor será DXVA2 \_ NoiseFilterTech \_ sem suporte.

-   **DetailFilterTechnology**. Este campo indica quais filtros de detalhes têm suporte no driver de gráficos. Se o driver não oferecer suporte à filtragem de ruído, o valor será DXVA2 \_ DetailFilterTech \_ sem suporte.

## <a name="color-adjustment-and-image-filtering"></a>Ajuste de cores e filtragem de imagem

O driver de gráficos pode dar suporte ao ajuste de cores (também chamado de *amplificação de processo* ou simples de *Procamp*) e filtragem de imagem. Quando executado pela GPU, o ajuste de cor e a filtragem de imagem podem ser feitos em tempo real sem sobrecarga de CPU.

Para usar esses recursos, execute as seguintes etapas:

1.  Selecione um modo de processamento de vídeo conforme descrito na seção anterior.

2.  Chame [**IMFVideoProcessor:: GetVideoProcessorCaps**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps) para localizar os recursos de processamento de vídeo, conforme descrito na seção anterior. O método preenche uma estrutura [**DXVA2 \_ VideoProcessorCaps**](/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps) que descreve os recursos, incluindo se o driver dá suporte ao ajuste de cores e ao filtro de imagem.

3.  Para cada ajuste de cor com suporte no driver, chame [**IMFVideoProcessor:: GetProcAmpRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocamprange) para localizar o intervalo de valor possível para essa configuração. Esse método também retorna o valor padrão para a configuração. Chame [**IMFVideoProcessor:: GetProcAmpValues**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocampvalues) para localizar o valor atual das configurações. Os valores não têm unidades especificadas. Cabe ao driver definir o intervalo de valores.

4.  Chame [**IMFVideoProcessor:: Setfiltervalue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue) para definir um valor de ajuste de cor.

5.  Se o driver oferecer suporte à filtragem de imagem, cada tipo de filtro (ruído e detalhes) dará suporte a três configurações — nível, raio e limite — em croma e Luma. (Consulte [configurações de filtro de imagem de DXVA](dxva-image-filter-settings.md).) Para cada configuração, chame [**IMFVideoProcessor:: GetFilteringRange**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringrange) para obter o intervalo de valores possíveis e chame [**IMFVideoProcessor:: getfiltervalue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringvalue) para obter o valor atual.

6.  Para alterar uma configuração de filtro de imagem, chame [**IMFVideoProcessor:: Setfiltervalue**](/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Processador de vídeo aprimorado](enhanced-video-renderer.md)
</dt> </dl>

 

 



