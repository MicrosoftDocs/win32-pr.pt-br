---
description: Um objeto que encapsula vários DSPs relacionados à captura de voz.
ms.assetid: 6c77c8f6-289e-4130-b56a-e1f0bcc40f3e
title: DSP de Captura de Voz (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d05eb6d3f97f748d5c82d8fa566ee25a3a01ce225ab76e84d73f0a86b132afb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972545"
---
# <a name="voice-capture-dsp"></a>DSP de Captura de Voz

Um objeto que encapsula vários DSPs relacionados à captura de voz.

## <a name="clsid"></a>CLSID

CLSID \_ CWMAudioAEC

## <a name="interfaces"></a>Interfaces

-   [**Imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   **Ipropertystore**

## <a name="properties"></a>Propriedades



| Propriedade                                                                                     | Descrição                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [ÍNDICES DE \_ DISPOSITIVO WMAAECMA MFPKEY \_ \_](mfpkey-wmaaecma-device-indexesproperty.md)              | Especifica quais dispositivos de áudio o DMO usa para capturar e renderizar áudio.                     |
| [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md)            | Identifica a combinação de dispositivos de áudio que o aplicativo está usando no momento.              |
| [MFPKEY \_ WMAAECMA \_ DMO \_ SOURCE \_ MODE](mfpkey-wmaaecma-dmo-source-modeproperty.md)           | Especifica se o DMO usa o modo de origem ou o modo de filtro.                                        |
| [MFPKEY \_ WMAAECMACALR \_ \_ AES](mfpkey-wmaaecma-featr-aesproperty.md)                        | Especifica quantas vezes o DMO executa a supressão de eco acústico (AES) no sinal residual. |
| [MFPKEY \_ WMAAECMAGCR \_ \_ AGC](mfpkey-wmaaecma-featr-agcproperty.md)                        | Especifica se o DMO executa o controle de ganho automático.                                        |
| [MFPKEY \_ WMAAECMA \_ ROTEADOR \_ CENTER \_ CLIP](mfpkey-wmaaecma-featr-center-clipproperty.md)       | Especifica se o DMO executa o recorte central.                                               |
| [COMPRIMENTO DE ECO \_ MFPKEY WMAAECMA \_ FOCALR \_ \_](mfpkey-wmaaecma-featr-echo-lengthproperty.md)       | Especifica a duração do eco que o algoritmo AEC (cancelamento de eco acústico) pode manipular.    |
| [TAMANHO DO QUADRO \_ MFPKEY WMAAECMA \_ FRAMER \_ \_](mfpkey-wmaaecma-featr-frame-sizeproperty.md)         | Especifica o tamanho do quadro de áudio.                                                                   |
| [MFPKEY \_ WMAAECMACALR \_ \_ MICARR \_](mfpkey-wmaaecma-featr-micarr-beamproperty.md)       | Especifica qual conjunto de DMO usa para processamento de matriz de microfone.                                |
| [MODO \_ MICARR MFPKEY WMAAECMA \_ \_ MICARR \_](mfpkey-wmaaecma-featr-micarr-modeproperty.md)       | Especifica como o DMO executa o processamento da matriz de microfone.                                       |
| [MFPKEY \_ WMAAECMA \_ FEATR \_ MICARR \_ PREPROC](mfpkey-wmaaecma-featr-micarr-preprocproperty.md) | Especifica se o DMO executa o pré-processamento da matriz de microfone.                                |
| [PREENCHIMENTO DE RUÍDO \_ MFPKEY WMAAECMACALR \_ \_ \_](mfpkey-wmaaecma-featr-noise-fillproperty.md)         | Especifica se o DMO executa o preenchimento de ruído.                                                 |
| [MFPKEY \_ WMAAECMACALR \_ \_ NS](mfpkey-wmaaecma-featr-nsproperty.md)                          | Especifica se o DMO executa a supressão de ruído.                                             |
| [MFPKEY \_ WMAAECMACALR \_ \_ VAD](mfpkey-wmaaecma-featr-vadproperty.md)                        | Especifica o tipo de detecção de atividade de voz que o DMO executa.                             |
| [MODO DE RECURSO \_ MFPKEY WMAAECMA \_ \_](mfpkey-wmaaecma-feature-modeproperty.md)                  | Permite que o aplicativo substitua as configurações padrão em várias propriedades.                   |
| [MFPKEY \_ WMAAECMA \_ MIC \_ GAIN \_ BOUNDER](mfpkey-wmaaecma-mic-gain-bounderproperty.md)         | Especifica se o DMO aplica a delimitação de ganho de microfone.                                       |
| [MFPKEY \_ WMAAECMA \_ MICARRAY \_ DESCPTR](mfpkey-wmaaecma-micarray-descptrproperty.md)          | Especifica a geometria da matriz de microfone.                                                          |
| [\_MÉTRICAS DE QUALIDADE WMAAECMA MFPKEY \_ \_](mfpkey-wmaaecma-quality-metricsproperty.md)            | Recupera métricas de qualidade para a AEC.                                                                |
| [MFPKEY \_ WMAAECMA \_ RETRIEVE \_ TS \_ STATS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md)       | Especifica se o DMO armazena estatísticas de carimbo de data/hora no Registro.                           |
| [MODO DE SISTEMA \_ MFPKEY WMAAECMA \_ \_](mfpkey-wmaaecma-system-modeproperty.md)                    | Define o modo de processamento.                                                                         |



 

## <a name="remarks"></a>Comentários

Ao contrário dos outros DSPs, o objeto de captura de voz encapsula vários DSPs em um único objeto e o objeto é apenas um objeto DMO (ele não implementa [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)). A captura de DMO inclui os seguintes componentes do DSP:

-   Cancelamento de eco acústico (AEC)
-   Processamento de matriz de microfone
-   Supressão de ruído
-   Controle de ganho automático
-   Detecção de atividade de voz

Os aplicativos podem ativar e desativar cada componente individualmente.

A captura de DMO dá suporte a dois modos de operação, *modo de filtro* e modo de *origem.* No modo de filtro, o aplicativo envia amostras de áudio do microfone e da linha do locutor para o DMO, e o DMO produz a saída.

No modo de origem, o aplicativo não precisa fornecer exemplos para o DMO. Em vez disso, o DMO gerencia todas as operações nos dispositivos de áudio, incluindo inicializar os dispositivos, capturar e sincronizar os fluxos de áudio, calcular carimbos de data/hora e recuperar a geometria da matriz do microfone. Usando o modo de origem, o aplicativo simplesmente configura o DMO e a saída do DMO é um sinal de microfone limpo e processado. O modo de origem é significativamente mais fácil de usar do que o modo de filtro e é recomendado para a maioria dos aplicativos.

Atualmente, a captura de voz DMO dá suporte apenas ao AEC (cancelamento de eco acústico de canal único), portanto, a saída da linha do locutor deve ser de canal único. Se o processamento da matriz de microfone estiver desabilitado, a entrada de vários canais será dobrada para um canal para processamento do AEC. Se o processamento da matriz de microfone e o processamento do AEC estão habilitados, o AEC é executado em cada elemento de microfone antes do processamento da matriz do microfone.

### <a name="microphone-array-processing"></a>Processamento de matriz de microfone

Uma matriz de microfone é um conjunto de microfones posicionados de perto. As matrizes de microfone atingem melhor direcionalidade do que um único microfone, porque as ondas acústicas chegam a cada microfone em um momento ligeiramente diferente. Para obter mais informações sobre matrizes de microfone, consulte os artigos da Web Suporte à Matriz de Microfone no [Windows Vista](/windows-hardware/design/component-guidelines/audio) e Como criar e usar matrizes de microfone para [Windows Vista](/windows-hardware/drivers/audio/microphone-array-geometry-descriptor-format).

### <a name="using-the-voice-capture-dsp"></a>Usando o DSP de Captura de Voz

Para usar o DSP de Captura de Voz, execute as etapas a seguir.

### <a name="1-initialize-the-dmo"></a>1. Inicializar o DMO

Crie a captura de DMO chamando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) com **CLSID CLSID \_ CWMAudioAEC**. O DSDP de captura de voz expõe apenas as interfaces [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) e [**IPropertyStore,**](/windows/win32/api/propsys/nn-propsys-ipropertystore) portanto, ele só pode ser usado como um DMO.

O DMO padrão é o modo de origem. Para selecionar o modo de filtro, de definir [a propriedade \_ MFPKEY WMAAECMA \_ DMO SOURCE \_ \_ MODE](mfpkey-wmaaecma-dmo-source-modeproperty.md) como **VARIANT \_ FALSE.**

Em seguida, configure as propriedades internas do DMO usando a interface [**IPropertyStore.**](/windows/win32/api/propsys/nn-propsys-ipropertystore) A única propriedade que um aplicativo deve definir é a [propriedade MFPKEY \_ WMAAECMA \_ SYSTEM \_ MODE.](mfpkey-wmaaecma-system-modeproperty.md) Essa propriedade configura o pipeline de processamento dentro do DMO. As outras propriedades são opcionais.

### <a name="2-set-the-input-and-output-formats"></a>2. Definir os formatos de entrada e saída

Se você estiver usando o DMO no modo de filtro, de definido o formato de entrada chamando [**IMediaObject::SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype). O formato de entrada pode ser quase qualquer tipo de áudio de ponto flutuante PCM ou IEEE descompactado válido. Se o formato de entrada não corresponder ao formato de saída, o DMO executará automaticamente a conversão de taxa de amostra.

Se você estiver usando o DMO no modo de origem, não de definido o formato de entrada. O DMO configura automaticamente o formato de entrada com base nos dispositivos de áudio.

Em ambos os modos, de definido o formato de saída chamando [**IMediaObject::SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype). O DMO pode aceitar os seguintes formatos de saída:

-   Subtipo: **MEDIASUBTYPE \_ PCM** ou **MEDIASUBTYPE \_ IEEE \_ FLOAT**
-   Bloco de formato: [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) ou [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85))
-   Exemplos por segundo: 8.000; 11,025; 16,000; ou 22.050
-   Canais: 1 para o modo somente AEC, 2 ou 4 para processamento de matriz de microfone
-   Bits por exemplo: 16

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



### <a name="3-process-data"></a>3. Processar dados

Antes de processar quaisquer dados, é recomendável chamar [**IMediaObject:: AllocateStreamingResources**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-allocatestreamingresources). Esse método aloca os recursos usados internamente pelo DMO. Chame **AllocateStreamingResources** após as etapas listadas anteriormente, não antes. se você não chamar esse método, a DMO alocará automaticamente os recursos quando o processamento de dados for iniciado.

se você estiver usando o DMO no modo de filtro, deverá passar dados de entrada para o DMO chamando [**IMediaObject::P rocessinput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput). Os dados de áudio do microfone vão para o fluxo 0 e os dados de áudio da linha do orador vão para o fluxo 1. se você estiver usando o DMO no modo de origem, não será necessário chamar **ProcessInput**.

Para obter dados de saída do DSP, execute as seguintes etapas:

1.  Crie um objeto de buffer para armazenar os dados de saída. O objeto de buffer deve implementar a interface [**IMediaBuffer**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediabuffer) . O tamanho do buffer depende dos requisitos do seu aplicativo. Alocar um buffer maior pode reduzir as chances de falhas ocorrendo.
2.  Declare uma [**DMO estrutura de BUFFER de \_ \_ dados \_ de saída**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) e defina o membro **pBuffer** para apontar para o objeto BUFFER.
3.  passe o DMO a estrutura de [**\_ BUFFER de \_ dados \_ de saída**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) para o método [**IMediaObject::P rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) .
4.  Continue a chamar esse método por enquanto o DMO tiver dados de saída. o DSP sinaliza que ele tem mais saída definindo o sinalizador **DMO \_ output \_ data \_ BUFFERF \_ incompleto** no membro **dwStatus** da estrutura de [**\_ BUFFER de \_ dados \_ de saída DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_output_data_buffer) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfwmaaec.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Processadores de sinais digitais](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
