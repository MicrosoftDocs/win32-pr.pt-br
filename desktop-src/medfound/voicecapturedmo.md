---
description: Um objeto que encapsula vários DSPs relacionados à captura de voz.
ms.assetid: 6c77c8f6-289e-4130-b56a-e1f0bcc40f3e
title: DSP de captura de voz (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e48c3b3194873008f45ef80ef3a21dad416158b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661813"
---
# <a name="voice-capture-dsp"></a>DSP de captura de voz

Um objeto que encapsula vários DSPs relacionados à captura de voz.

## <a name="clsid"></a>CLSID

\_CWMAUDIOAEC CLSID

## <a name="interfaces"></a>Interfaces

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   **IPropertyStore**

## <a name="properties"></a>Propriedades



| Propriedade                                                                                     | Descrição                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [MFPKEY \_ \_ índices de dispositivo WMAAECMA \_](mfpkey-wmaaecma-device-indexesproperty.md)              | Especifica quais dispositivos de áudio o DMO usa para capturar e renderizar áudio.                     |
| [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md)            | Identifica a combinação de dispositivos de áudio que o aplicativo está usando no momento.              |
| [\_modo de origem MFPKEY WMAAECMA \_ DMO \_ \_](mfpkey-wmaaecma-dmo-source-modeproperty.md)           | Especifica se o DMO usa o modo de origem ou o modo de filtro.                                        |
| [AES do MFPKEY \_ WMAAECMA \_ \_](mfpkey-wmaaecma-featr-aesproperty.md)                        | Especifica quantas vezes o DMO executa a supressão de eco acústico (AES) no sinal residual. |
| [\_AGC MFPKEY WMAAECMA \_ \_](mfpkey-wmaaecma-featr-agcproperty.md)                        | Especifica se o DMO executa o controle de lucro automático.                                        |
| [\_clipe do \_ \_ Centro \_ do MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-center-clipproperty.md)       | Especifica se o DMO executa recorte de centro.                                               |
| [MFPKEY \_ WMAAECMA com \_ comprimento de \_ eco \_](mfpkey-wmaaecma-featr-echo-lengthproperty.md)       | Especifica a duração do eco que o algoritmo de cancelamento de eco acústico (AEC) pode manipular.    |
| [\_tamanho do \_ \_ quadro \_ do MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-frame-sizeproperty.md)         | Especifica o tamanho do quadro de áudio.                                                                   |
| [MFPKEY \_ WMAAECMA com \_ \_ MICARR \_ feixe](mfpkey-wmaaecma-featr-micarr-beamproperty.md)       | Especifica qual transmissão o DMO usa para processamento de matriz de microfone.                                |
| [\_ \_ \_ modo MICARR do MFPKEY WMAAECMA \_](mfpkey-wmaaecma-featr-micarr-modeproperty.md)       | Especifica como o DMO executa o processamento da matriz de microfone.                                       |
| [MFPKEY \_ WMAAECMA refeito \_ \_ MICARR \_ preproc](mfpkey-wmaaecma-featr-micarr-preprocproperty.md) | Especifica se o DMO executa o pré-processamento da matriz do microfone.                                |
| [\_preenchimento de \_ \_ ruído \_ do MFPKEY WMAAECMA](mfpkey-wmaaecma-featr-noise-fillproperty.md)         | Especifica se o DMO executa o preenchimento de ruído.                                                 |
| [\_ns MFPKEY WMAAECMA \_ \_](mfpkey-wmaaecma-featr-nsproperty.md)                          | Especifica se o DMO executa a supressão de ruído.                                             |
| [MFPKEY \_ WMAAECMA para \_ \_ VAD](mfpkey-wmaaecma-featr-vadproperty.md)                        | Especifica o tipo de detecção de atividade de voz que o DMO executa.                             |
| [modo de recurso do MFPKEY \_ WMAAECMA \_ \_](mfpkey-wmaaecma-feature-modeproperty.md)                  | Permite que o aplicativo substitua as configurações padrão em várias propriedades.                   |
| [\_limitador de MFPKEY WMAAECMA \_ MIC \_ \_](mfpkey-wmaaecma-mic-gain-bounderproperty.md)         | Especifica se o DMO aplica o limite de lucro do microfone.                                       |
| [MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR](mfpkey-wmaaecma-micarray-descptrproperty.md)          | Especifica a geometria da matriz do microfone.                                                          |
| [\_ \_ métricas de qualidade MFPKEY WMAAECMA \_](mfpkey-wmaaecma-quality-metricsproperty.md)            | Recupera métricas de qualidade para AEC.                                                                |
| [MFPKEY \_ WMAAECMA \_ recuperar \_ Estatísticas de TS \_](mfpkey-wmaaecma-retrieve-ts-statsproperty.md)       | Especifica se o DMO armazena estatísticas de carimbo de data/hora no registro.                           |
| [MFPKEY \_ WMAAECMA \_ modo de sistema \_](mfpkey-wmaaecma-system-modeproperty.md)                    | Define o modo de processamento.                                                                         |



 

## <a name="remarks"></a>Comentários

Ao contrário dos outros DSPs, o objeto de captura de voz encapsula vários DSPs em um único objeto e o objeto é apenas um objeto DMO (ele não implementa [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)). O Voice Capture DMO inclui os seguintes componentes do DSP:

-   Cancelamento de eco acústico (AEC)
-   Processamento de matriz de microfone
-   Supressão de ruído
-   Controle de lucro automático
-   Detecção de atividade de voz

Os aplicativos podem ativar e desativar cada componente individualmente.

O Voice Capture DMO dá suporte a dois modos de operação, modo de *filtro* e modo de *origem* . No modo de filtro, o aplicativo envia amostras de áudio do microfone e da linha do viva-voz para o DMO, e o DMO produz a saída.

No modo de origem, o aplicativo não precisa fornecer exemplos para o DMO. Em vez disso, o DMO gerencia todas as operações nos dispositivos de áudio, inclusive inicializando os dispositivos, capturando e sincronizando os fluxos de áudio, calculando carimbos de data/hora e recuperando a geometria da matriz de microfone. Usando o modo de origem, o aplicativo simplesmente configura o DMO, e a saída do DMO é um sinal de microfone limpo e processado. O modo de origem é significativamente mais fácil de usar do que o modo de filtro e é recomendado para a maioria dos aplicativos.

Atualmente, o Voice Capture DMO dá suporte apenas a AEC (cancelamento de eco acústico) de canal único, de modo que a saída da linha do orador deve ser de canal único. Se o processamento da matriz de microfone estiver desabilitado, a entrada multicanal será dobrada para um canal para processamento de AEC. Se o processamento da matriz de microfone e o processamento de AEC estiverem habilitados, o AEC será executado em cada elemento do microfone antes do processamento da matriz do microfone.

### <a name="microphone-array-processing"></a>Processamento de matriz de microfone

Uma matriz de microfone é um conjunto de microtelefones com posicionamento próximo. As matrizes de microfone atingem uma direcionalidade melhor do que um único microfone, pois as ondas acústicas chegam em cada microfone em um momento ligeiramente diferente. Para obter mais informações sobre matrizes de microfone, consulte os artigos da Web [suporte de matriz de microfone no Windows Vista](/windows-hardware/design/component-guidelines/audio) e [como criar e usar matrizes de microfone para o Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

### <a name="using-the-voice-capture-dsp"></a>Usando o DSP de captura de voz

Para usar o DSP de captura de voz, execute as etapas a seguir.

### <a name="1-initialize-the-dmo"></a>1. Inicialize o DMO

Crie o Voice Capture DMO chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com o CLSID **CLSID \_ CWMAudioAEC**. O DSDP de captura de voz expõe apenas as interfaces [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) e [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , portanto, ela só pode ser usada como um DMO.

O padrão de DMO é o modo de origem. Para selecionar o modo de filtro, defina a propriedade [ \_ modo de origem MFPKEY WMAAECMA \_ DMO \_ \_](mfpkey-wmaaecma-dmo-source-modeproperty.md) como **variante \_ false**.

Em seguida, configure as propriedades internas do DMO usando a interface [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) . A única propriedade que um aplicativo deve definir é a propriedade do [ \_ modo do \_ sistema \_ MFPKEY WMAAECMA](mfpkey-wmaaecma-system-modeproperty.md) . Essa propriedade configura o pipeline de processamento no DMO. As outras propriedades são opcionais.

### <a name="2-set-the-input-and-output-formats"></a>2. definir os formatos de entrada e saída

Se você estiver usando o DMO no modo de filtro, defina o formato de entrada chamando [**IMediaObject:: SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype). O formato de entrada pode ser quase qualquer tipo de áudio de ponto flutuante de formato PCM ou IEEE não compactado válido. Se o formato de entrada não corresponder ao formato de saída, o DMO executará automaticamente a conversão de taxa de amostragem.

Se você estiver usando o DMO no modo de origem, não defina o formato de entrada. O DMO configura automaticamente o formato de entrada com base nos dispositivos de áudio.

Em ambos os modos, defina o formato de saída chamando [**IMediaObject:: SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). O DMO pode aceitar os seguintes formatos de saída:

-   Subtipo: **MEDIASUBTYPE \_ PCM** ou **MEDIASUBTYPE \_ IEEE \_ float**
-   Bloco de formato: [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) ou [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))
-   Exemplos por segundo: 8.000; 11.025; 16.000; ou 22.050
-   Canais: 1 para modo somente AEC, 2 ou 4 para processamento de matriz de microfone
-   Bits por amostra: 16

O código a seguir define o tipo de saída como áudio PCM de canal único de 16 bits:


```
DMO_MEDIA_TYPE mt;  // Media type.
mt.majortype = MEDIATYPE_Audio;
mt.subtype = MEDIASUBTYPE_PCM;
mt.lSampleSize = 0;
mt.bFixedSizeSamples = TRUE;
mt.bTemporalCompression = FALSE;
mt.formattype = FORMAT_WaveFormatEx;

// Allocate the format block to hold the WAVEFORMATEX structure.
hr = MoInitMediaType(&mt, sizeof(WAVEFORMATEX));
if (SUCCEEDED(hr))
{
    WAVEFORMATEX *pwav = (WAVEFORMATEX*)mt.pbFormat;
    pwav->wFormatTag = WAVE_FORMAT_PCM;
    pwav->nChannels = 1;
    pwav->nSamplesPerSec = 16000;
    pwav->nAvgBytesPerSec = 32000;
    pwav->nBlockAlign = 2;
    pwav->wBitsPerSample = 16;
    pwav->cbSize = 0;

    // Set the output type.
    if (SUCCEEDED(hr))
    {
        hr = pDMO->SetOutputType(0, &mt, 0); 
    }
    // Free the format block.
    MoFreeMediaType(&mt);
}
```



### <a name="3-process-data"></a>3. processar dados

Antes de processar quaisquer dados, é recomendável chamar [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources). Esse método aloca os recursos usados internamente pelo DMO. Chame **AllocateStreamingResources** após as etapas listadas anteriormente, não antes. Se você não chamar esse método, o DMO alocará automaticamente os recursos quando o processamento de dados for iniciado.

Se você estiver usando o DMO no modo de filtro, deverá passar os dados de entrada para o DMO chamando [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput). Os dados de áudio do microfone vão para o fluxo 0 e os dados de áudio da linha do orador vão para o fluxo 1. Se você estiver usando o DMO no modo de origem, não será necessário chamar **ProcessInput**.

Para obter dados de saída do DSP, execute as seguintes etapas:

1.  Crie um objeto de buffer para armazenar os dados de saída. O objeto de buffer deve implementar a interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) . O tamanho do buffer depende dos requisitos do seu aplicativo. Alocar um buffer maior pode reduzir as chances de falhas ocorrendo.
2.  Declare uma estrutura de [**buffer de \_ dados de saída \_ \_ DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) e defina o membro **pBuffer** para apontar para o objeto buffer.
3.  Passe a estrutura do buffer de dados de saída do DMO para o método [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) . [**\_ \_ \_**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer)
4.  Continue a chamar esse método enquanto o DMO tiver dados de saída. O DSP sinaliza que ele tem mais saída definindo o sinalizador de **dados de saída de DMO \_ \_ \_ BUFFERF \_ incompleto** no membro **dwStatus** da estrutura do buffer de [**dados de saída do DMO \_ \_ \_**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfwmaaec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Processadores de sinais digitais](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
