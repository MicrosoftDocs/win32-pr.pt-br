---
description: Este artigo descreve como escrever um apresentador personalizado para o processador de vídeo avançado (EVR).
ms.assetid: 1135b309-b158-4b70-9f76-5c93d0ad3250
title: Como escrever um apresentador EVR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 505ba7ec225ac5f1316ad4343a4e1058ff0b6cb8
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118771"
---
# <a name="how-to-write-an-evr-presenter"></a>Como escrever um apresentador EVR

Este artigo descreve como escrever um apresentador personalizado para o processador de vídeo avançado (EVR). Um apresentador personalizado pode ser usado com o DirectShow e o Media Foundation; as interfaces e o modelo de objeto são os mesmos para ambas as tecnologias, embora a seqüência exata de operações possa variar.

O código de exemplo neste tópico é adaptado do [exemplo EVRPresenter](evrpresenter-sample.md), que é fornecido na SDK do Windows.

Este tópico contém as seguintes seções:

-   [Pré-requisitos](#prerequisites)
-   [Modelo de objeto do apresentador](#presenter-object-model)
    -   [Fluxo de dados dentro do EVR](#data-flow-inside-the-evr)
    -   [Estados do apresentador](#presenter-states)
    -   [Interfaces do apresentador](#presenter-interfaces)
    -   [Implementando IMFVideoDeviceID](#implementing-imfvideodeviceid)
    -   [Implementando IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient)
    -   [Implementando IMFVideoPresenter](#implementing-imfvideopresenter)
    -   [Implementando IMFClockStateSink](#implementing-imfclockstatesink)
    -   [Implementando IMFRateSupport](#implementing-imfratesupport)
    -   [Enviando eventos para o EVR](#sending-events-to-the-evr)
-   [Negociando formatos](#negotiating-formats)
-   [Gerenciando o dispositivo Direct3D](#managing-the-direct3d-device)
    -   [Alocando superfícies do Direct3D](#allocating-direct3d-surfaces)
    -   [Amostras de rastreamento](#tracking-samples)
-   [Processando saída](#processing-output)
    -   [Repintando quadros](#repainting-frames)
    -   [Exemplos de agendamento](#scheduling-samples)
    -   [Apresentando exemplos](#presenting-samples)
    -   [Retângulos de origem e de destino](#source-and-destination-rectangles)
    -   [Fim do fluxo](#end-of-stream)
-   [Revisão do quadro](#frame-stepping)
    -   [Implementando a revisão do quadro](#implementing-frame-stepping)
-   [Configurando o apresentador no EVR](#setting-the-presenter-on-the-evr)
    -   [Configurando o apresentador no DirectShow](#setting-the-presenter-in-directshow)
    -   [Configurando o apresentador no Media Foundation](#setting-the-presenter-in-media-foundation)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Antes de escrever um apresentador personalizado, você deve estar familiarizado com as seguintes tecnologias:

-   O processador de vídeo aprimorado. Consulte [processador de vídeo aprimorado](enhanced-video-renderer.md).
-   Gráficos do Direct3D. Você não precisa entender gráficos 3D para escrever um apresentador, mas deve saber como criar um dispositivo Direct3D e gerenciar superfícies de Direct3D. Se você não estiver familiarizado com o Direct3D, leia as seções "dispositivos Direct3D" e "recursos do Direct3D" na documentação do SDK de gráficos do DirectX.
-   Os gráficos de filtro do DirectShow ou o pipeline Media Foundation, dependendo da tecnologia que seu aplicativo usará para renderizar o vídeo.
-   [Transformações de Media Foundation](media-foundation-transforms.md). O mixer EVR é uma transformação Media Foundation e o apresentador chama métodos diretamente no mixer.
-   Implementando objetos COM. O apresentador é um objeto COM COM thread livre em processo.

## <a name="presenter-object-model"></a>Modelo de objeto do apresentador

Esta seção contém uma visão geral do modelo de objeto e das interfaces do apresentador.

### <a name="data-flow-inside-the-evr"></a>Fluxo de dados dentro do EVR

O EVR usa dois componentes de plug-in para renderizar o vídeo: o *mixer* e o *apresentador*. O mixer mescla os fluxos de vídeo e desentrelaça o vídeo, se necessário. O apresentador desenha (ou *apresenta*) o vídeo na exibição e agenda quando cada quadro é desenhado. Os aplicativos podem substituir qualquer um desses objetos por uma implementação personalizada.

O EVR tem um ou mais fluxos de entrada, e o mixer tem um número correspondente de fluxos de entrada. O fluxo 0 é sempre o *fluxo de referência*. Os outros fluxos são *subfluxos*, que o mixer Alpha mistura no fluxo de referência. O fluxo de referência determina a taxa de quadros mestre para o vídeo composto. Para cada quadro de referência, o mixer usa o quadro mais recente de cada Subfluxo, mistura-o alfa para o quadro de referência e gera um único quadro composto. O mixer também executa desentrelaçamento e conversão de cores de YUV para RGB, se necessário. O EVR sempre insere o mixer no pipeline de vídeo, independentemente do número de fluxos de entrada ou do formato de vídeo. A imagem a seguir ilustra esse processo.

![diagrama que mostra o fluxo de referência e o Subfluxo apontando para o mixer, que aponta para o apresentador, que aponta para a exibição](images/459338c4-cff8-4d20-bffd-ff1cbbe6f332.gif)

O apresentador executa as seguintes tarefas:

-   Define o formato de saída no mixer. Antes de o streaming começar, o apresentador define um tipo de mídia no fluxo de saída do mixer. Esse tipo de mídia define o formato da imagem compostada.
-   Cria o dispositivo Direct3D.
-   Aloca superfícies de Direct3D. O mixer blits os quadros compostos nessas superfícies.
-   Obtém a saída do mixer.
-   Agenda quando os quadros são apresentados. O EVR fornece o relógio de apresentação e o apresentador agenda quadros de acordo com esse relógio.
-   Apresenta cada quadro usando o Direct3D.
-   Executa a depuração e a limpeza do quadro.

### <a name="presenter-states"></a>Estados do apresentador

A qualquer momento, o apresentador está em um dos seguintes Estados:

-   *Iniciado*. O relógio de apresentação do EVR está em execução. O apresentador agenda quadros de vídeo para apresentação à medida que eles chegam.
-   Em *pausa*. O relógio de apresentação está suspenso. O apresentador não apresenta novos exemplos, mas mantém sua fila de exemplos agendados. Se novos exemplos forem recebidos, o apresentador os adicionará à fila.
-   *Parado*. O relógio de apresentação foi interrompido. O apresentador descarta quaisquer exemplos que foram agendados.
-   *Desligar*. O apresentador libera todos os recursos relacionados ao streaming, como superfícies de Direct3D. Este é o estado inicial do apresentador e o estado final antes de o apresentador ser destruído.

No código de exemplo neste tópico, o estado do apresentador é representado por uma enumeração:


```C++
enum RENDER_STATE
{
    RENDER_STATE_STARTED = 1,
    RENDER_STATE_STOPPED,
    RENDER_STATE_PAUSED,
    RENDER_STATE_SHUTDOWN,  // Initial state.
};
```



Algumas operações não são válidas enquanto o apresentador está no estado de desligamento. O código de exemplo verifica esse estado chamando um método auxiliar:


```C++
    HRESULT CheckShutdown() const
    {
        if (m_RenderState == RENDER_STATE_SHUTDOWN)
        {
            return MF_E_SHUTDOWN;
        }
        else
        {
            return S_OK;
        }
    }
```



### <a name="presenter-interfaces"></a>Interfaces do apresentador

Um apresentador é necessário para implementar as seguintes interfaces:



| Interface                                                                | Descrição                                                                                                                                                         |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)                           | Notifica o apresentador quando o relógio do EVR muda de estado. Consulte [implementando IMFClockStateSink](#implementing-imfclockstatesink).                                   |
| [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)                                   | Fornece uma maneira para o aplicativo e outros componentes no pipeline obter interfaces do apresentador.                                                       |
| [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) | Permite que o apresentador receba interfaces do EVR ou do mixer. Consulte [Implementando IMFTopologyServiceLookupClient](#implementing-imftopologyservicelookupclient). |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid)                             | Garante que o apresentador e o mixer usem tecnologias compatíveis. Consulte [Implementando IMFVideoDeviceID](#implementing-imfvideodeviceid).                          |
| [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter)                           | Processa mensagens do EVR. Consulte [Implementando IMFVideoPresenter](#implementing-imfvideopresenter).                                                             |



 

As seguintes interfaces são opcionais:



| Interface                                                | Descrição                                                                                                                                                               |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEVRTrustedVideoPlugin**](/windows/desktop/api/evr/nn-evr-ievrtrustedvideoplugin) | Permite que o apresentador funcione com mídia protegida. Implemente essa interface se o seu apresentador for um componente confiável projetado para funcionar no PMP (caminho de mídia protegido). |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)                 | Relata o intervalo de taxas de reprodução compatíveis com o apresentador. Consulte [Implementando IMFRateSupport](#implementing-imfratesupport).                                         |
| [**IMFVideoPositionMapper**](/windows/desktop/api/evr/nn-evr-imfvideopositionmapper) | Mapeia coordenadas no quadro de vídeo de saída para coordenadas no quadro de vídeo de entrada.                                                                                       |
| [**Iqualprop**](/previous-versions/windows/desktop/api/amvideo/nn-amvideo-iqualprop)                         | Relata informações de desempenho. O EVR usa essas informações para gerenciamento de controle de qualidade. Essa interface está documentada no SDK do DirectShow.                        |



 

Você também pode fornecer interfaces para que o aplicativo se comunique com o apresentador. O apresentador padrão implementa a interface [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) para essa finalidade. Você pode implementar essa interface ou definir sua própria. O aplicativo obtém interfaces do apresentador chamando [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) no EVR. Quando o GUID de serviço **MR_VIDEO_RENDER_SERVICE**, o EVR passa a **solicitação GetService** para o apresentador.

### <a name="implementing-imfvideodeviceid"></a>Implementando IMFVideoDeviceID

A interface [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) contém um método, [**GetDeviceID,**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)que retorna um GUID do dispositivo. O GUID do dispositivo garante que o apresentador e o mixer usem tecnologias compatíveis. Se os GUIDs do dispositivo não corresponderem, o EVR não será inicializado.

O mixer padrão e o apresentador usam o Direct3D 9, com o GUID do dispositivo igual **a IID_IDirect3DDevice9**. Se você pretende usar seu apresentador personalizado com o mixer padrão, o GUID do dispositivo do apresentador deve ser **IID_IDirect3DDevice9**. Se você substituir ambos os componentes, poderá definir um novo GUID do dispositivo. No restante deste artigo, supõe-se que o apresentador use o Direct3D 9. Aqui está a implementação padrão de [**GetDeviceID:**](/windows/desktop/api/evr/nf-evr-imfvideodeviceid-getdeviceid)


```C++
HRESULT EVRCustomPresenter::GetDeviceID(IID* pDeviceID)
{
    if (pDeviceID == NULL)
    {
        return E_POINTER;
    }

    *pDeviceID = __uuidof(IDirect3DDevice9);
    return S_OK;
}
```



O método deve ter êxito mesmo quando o apresentador é desligado.

### <a name="implementing-imftopologyservicelookupclient"></a>Implementando IMFTopologyServiceLookupClient

A interface [**IMFTopologyServiceLookupClient**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookupclient) permite que o apresentador receba ponteiros de interface do EVR e do mixer da seguinte forma:

1.  Quando o EVR inicializa o apresentador, ele chama o método [**IMFTopologyServiceLookupClient::InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) do apresentador. O argumento é um ponteiro para a interface [**IMFTopologyServiceLookup**](/windows/desktop/api/evr/nn-evr-imftopologyservicelookup) do EVR.
2.  O apresentador chama [**IMFTopologyServiceLookup::LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) para obter ponteiros de interface do EVR ou do mixer.

O [**método LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) é semelhante ao [**método IMFGetService::GetService.**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) Ambos os métodos têm um GUID de serviço e um IID (identificador de interface) como entrada, mas **LookupService** retorna uma matriz de ponteiros de interface, enquanto **GetService** retorna um único ponteiro. Na prática, no entanto, você sempre pode definir o tamanho da matriz como 1. O objeto consultado depende do GUID do serviço:

-   Se o GUID de serviço **MR_VIDEO_RENDER_SERVICE**, o EVR será consultado.
-   Se o GUID de serviço **MR_VIDEO_MIXER_SERVICE**, o mixer será consultado.

Em sua implementação de [**InitServicePointers,**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers)obter as seguintes interfaces do EVR:



| EVR Interface                                | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Imediaeventsink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) | Fornece uma maneira para o apresentador enviar mensagens para o EVR. Essa interface é definida no SDK do DirectShow, portanto, as mensagens seguem o padrão para eventos do DirectShow, não Media Foundation eventos.<br/>                                                                                                                                                                                                                                                                                                                                              |
| [**IMFClock**](/windows/desktop/api/mfidl/nn-mfidl-imfclock)                 | Representa o relógio do EVR. O apresentador usa essa interface para agendar exemplos para apresentação. O EVR pode ser executado sem um relógio, portanto, essa interface pode não estar disponível. Caso não, ignore o código de erro [**de LookupService.**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice)<br/> O relógio também implementa a interface [**IMFTimer.**](/windows/desktop/api/mfidl/nn-mfidl-imftimer) No pipeline Media Foundation, o relógio implementa a interface [**IMFPresentationClock.**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) Ele não implementa essa interface no DirectShow.<br/> |



 

Obter as seguintes interfaces do mixer:



| Mixer Interface                              | Descrição                                                |
|----------------------------------------------|------------------------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)         | Permite que o apresentador se comunique com o mixer.       |
| [**IMFVideoDeviceID**](/windows/desktop/api/evr/nn-evr-imfvideodeviceid) | Permite que o apresentador valide o GUID do dispositivo do mixer. |



 

O código a seguir implementa o [**método InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) :


```C++
HRESULT EVRCustomPresenter::InitServicePointers(
    IMFTopologyServiceLookup *pLookup
    )
{
    if (pLookup == NULL)
    {
        return E_POINTER;
    }

    HRESULT             hr = S_OK;
    DWORD               dwObjectCount = 0;

    EnterCriticalSection(&m_ObjectLock);

    // Do not allow initializing when playing or paused.
    if (IsActive())
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    // Ask for the clock. Optional, because the EVR might not have a clock.
    dwObjectCount = 1;

    (void)pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL,   // Not used.
        0,                          // Reserved.
        MR_VIDEO_RENDER_SERVICE,    // Service to look up.
        IID_PPV_ARGS(&m_pClock),    // Interface to retrieve.
        &dwObjectCount              // Number of elements retrieved.
        );

    // Ask for the mixer. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_MIXER_SERVICE, IID_PPV_ARGS(&m_pMixer), &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Make sure that we can work with this mixer.
    hr = ConfigureMixer(m_pMixer);
    if (FAILED(hr))
    {
        goto done;
    }

    // Ask for the EVR's event-sink interface. (Required.)
    dwObjectCount = 1;

    hr = pLookup->LookupService(
        MF_SERVICE_LOOKUP_GLOBAL, 0,
        MR_VIDEO_RENDER_SERVICE, IID_PPV_ARGS(&m_pMediaEventSink),
        &dwObjectCount
        );

    if (FAILED(hr))
    {
        goto done;
    }

    // Successfully initialized. Set the state to "stopped."
    m_RenderState = RENDER_STATE_STOPPED;

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Quando os ponteiros de interface obtidos de [**LookupService**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookup-lookupservice) não são mais válidos, o EVR chama [**IMFTopologyServiceLookupClient::ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers). Dentro desse método, libere todos os ponteiros de interface e de definir o estado do apresentador para desligar:


```C++
HRESULT EVRCustomPresenter::ReleaseServicePointers()
{
    // Enter the shut-down state.
    EnterCriticalSection(&m_ObjectLock);

    m_RenderState = RENDER_STATE_SHUTDOWN;

    LeaveCriticalSection(&m_ObjectLock);

    // Flush any samples that were scheduled.
    Flush();

    // Clear the media type and release related resources.
    SetMediaType(NULL);

    // Release all services that were acquired from InitServicePointers.
    SafeRelease(&m_pClock);
    SafeRelease(&m_pMixer);
    SafeRelease(&m_pMediaEventSink);

    return S_OK;
}
```



O EVR chama [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) por vários motivos, incluindo:

-   Desconectar ou reconectar pinos (DirectShow) ou adicionar ou remover os filtros de fluxo (Media Foundation).
-   Alterando o formato.
-   Definindo um novo relógio.
-   Desligamento final do EVR.

Durante o tempo de vida do apresentador, o EVR pode chamar [**InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) e [**ReleaseServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-releaseservicepointers) várias vezes.

### <a name="implementing-imfvideopresenter"></a>Implementando IMFVideoPresenter

A interface [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) herda [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) e adiciona dois métodos:



| Método                                                               | Descrição                                            |
|----------------------------------------------------------------------|--------------------------------------------------------|
| [**GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) | Retorna o tipo de mídia dos quadros de vídeo compostos. |
| [**Processmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage)           | Sinaliza o apresentador para executar várias ações.      |



 

O [**método GetCurrentMediaType**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-getcurrentmediatype) retorna o tipo de mídia do apresentador. (Para obter detalhes sobre como definir o tipo de mídia, consulte [Formatar formatos](#negotiating-formats).) O tipo de mídia é retornado como um ponteiro de interface [**IMFVideoMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfvideomediatype) O exemplo a seguir pressu que o apresentador armazena o tipo de mídia como um [**ponteiro IMFMediaType.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) Para obter a interface **IMFVideoMediaType do** tipo de mídia, chame **QueryInterface:**


```C++
HRESULT EVRCustomPresenter::GetCurrentMediaType(
    IMFVideoMediaType** ppMediaType
    )
{
    HRESULT hr = S_OK;

    if (ppMediaType == NULL)
    {
        return E_POINTER;
    }

    *ppMediaType = NULL;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_pMediaType == NULL)
    {
        hr = MF_E_NOT_INITIALIZED;
        goto done;
    }

    hr = m_pMediaType->QueryInterface(IID_PPV_ARGS(ppMediaType));

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



O [**método ProcessMessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) é o mecanismo principal para o EVR se comunicar com o apresentador. As mensagens a seguir são definidas. Os detalhes da implementação de cada mensagem são dados no restante deste tópico.



| Mensagem                                | Descrição                                                                                                                                                                                                                                        |
|----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MFVP_MESSAGE_INVALIDATEMEDIATYPE** | O tipo de mídia de saída do mixer é inválido. O apresentador deve negociar um novo tipo de mídia com o mixer. Consulte [negociando formatos](#negotiating-formats).                                                                                         |
| **MFVP_MESSAGE_BEGINSTREAMING**      | O streaming foi iniciado. Nenhuma ação específica é exigida por essa mensagem, mas você pode usá-la para alocar recursos.                                                                                                                                 |
| **MFVP_MESSAGE_ENDSTREAMING**        | O streaming foi encerrado. Libere todos os recursos que você alocou em resposta à mensagem de **MFVP_MESSAGE_BEGINSTREAMING** .                                                                                                                        |
| **MFVP_MESSAGE_PROCESSINPUTNOTIFY**  | O mixer recebeu um novo exemplo de entrada e pode ser capaz de gerar um novo quadro de saída. O apresentador deve chamar [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) no mixer. Consulte [processamento de saída](#processing-output). |
| **MFVP_MESSAGE_ENDOFSTREAM**         | A apresentação terminou. Consulte [fim do fluxo](#end-of-stream).                                                                                                                                                                                   |
| **MFVP_MESSAGE_FLUSH**               | O EVR está liberando os dados em seu pipeline de renderização. O apresentador deve descartar todos os quadros de vídeo agendados para apresentação.                                                                                                         |
| **MFVP_MESSAGE_STEP**                | Solicita que o apresentador passe a avançar N quadros. O apresentador deve descartar os próximos N-1 quadros e exibir o enésimo quadro. Confira [revisão de quadro](#frame-stepping).                                                                                |
| **MFVP_MESSAGE_CANCELSTEP**          | Cancela a revisão do quadro.                                                                                                                                                                                                                            |



 

### <a name="implementing-imfclockstatesink"></a>Implementando IMFClockStateSink

O apresentador deve implementar a interface [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink) como parte de sua implementação de [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter), que herda **IMFClockStateSink**. O EVR usa essa interface para notificar o apresentador sempre que o relógio do EVR muda de estado. Para obter mais informações sobre os Estados do relógio, consulte [relógio de apresentação](presentation-clock.md).

Aqui estão algumas diretrizes para implementar os métodos nesta interface. Todos os métodos devem falhar se o apresentador for desligado.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a></td>
<td><ol>
<li>Defina o estado do apresentador como iniciado.</li>
<li>Se o <em>llClockStartOffset</em> não for <strong>PRESENTATION_CURRENT_POSITION</strong>, libere a fila de exemplos do apresentador. (Isso é equivalente a receber uma mensagem de <strong>MFVP_MESSAGE_FLUSH</strong> .)</li>
<li>Se uma solicitação de etapa de quadro anterior ainda estiver pendente, processe a solicitação (Confira <a href="#frame-stepping">revisão de quadro</a>). Caso contrário, tente processar a saída do mixer (consulte <a href="#processing-output">processamento de saída</a>.</li>
</ol></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop"><strong>OnClockStop</strong></a></td>
<td><ol>
<li>Defina o estado do apresentador como parado.</li>
<li>Libere a fila de exemplos do apresentador.</li>
<li>Cancele qualquer operação de etapa de quadro pendente.</li>
</ol></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockpause"><strong>OnClockPause</strong></a></td>
<td>Defina o estado do apresentador como em pausa.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart"><strong>OnClockRestart</strong></a></td>
<td>Trate o mesmo que <a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart"><strong>OnClockStart</strong></a> , mas não libere a fila de amostras.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate"><strong>OnClockSetRate</strong></a></td>
<td><ol>
<li>Se a taxa estiver mudando de zero para zero, cancele a revisão do quadro.</li>
<li>Armazene a nova taxa de clock. A taxa de clock afeta quando exemplos são apresentados. Para obter mais informações, consulte <a href="#scheduling-samples">programação de exemplos</a>.</li>
</ol></td>
</tr>
</tbody>
</table>



 

### <a name="implementing-imfratesupport"></a>Implementando IMFRateSupport

Para dar suporte a taxas de reprodução diferentes de 1 × velocidade, o apresentador deve implementar a interface [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) . Aqui estão algumas diretrizes para implementar os métodos nesta interface. Todos os métodos devem falhar depois que o apresentador é desligado. Para obter mais informações sobre essa interface, consulte [controle de taxa](rate-control.md).



| Valor                                                          | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetSlowestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getslowestrate)   | Retorna zero para indicar que não há taxa de reprodução mínima.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate)   | Para reprodução não-finada, a taxa de reprodução não deve exceder a taxa de atualização do monitor: taxa máxima de atualização da *taxa*  =   (Hz)/ *taxa de quadros do vídeo* (FPS). A taxa de quadros de vídeo é especificada no tipo de mídia do apresentador. <br/> Para reprodução fina, a taxa de reprodução é desassociada; retornar o valor **FLT_MAX**. Na prática, a origem e o decodificador serão os fatores limitantes durante a reprodução fina. <br/> Para reprodução reversa, retorne o negativo da taxa máxima.<br/> |
| [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) | Retorne **MF_E_UNSUPPORTED_RATE** se o valor absoluto de *flRate* exceder a taxa de reprodução máxima do apresentador. Calcule a taxa máxima de reprodução conforme descrito para [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate).                                                                                                                                                                                                                                                                                    |



 

O exemplo a seguir mostra como implementar o método [**GetFastestRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-getfastestrate) :


```C++
float EVRCustomPresenter::GetMaxRate(BOOL bThin)
{
    // Non-thinned:
    // If we have a valid frame rate and a monitor refresh rate, the maximum
    // playback rate is equal to the refresh rate. Otherwise, the maximum rate
    // is unbounded (FLT_MAX).

    // Thinned: The maximum rate is unbounded.

    float   fMaxRate = FLT_MAX;
    MFRatio fps = { 0, 0 };
    UINT    MonitorRateHz = 0;

    if (!bThin && (m_pMediaType != NULL))
    {
        GetFrameRate(m_pMediaType, &fps);
        MonitorRateHz = m_pD3DPresentEngine->RefreshRate();

        if (fps.Denominator && fps.Numerator && MonitorRateHz)
        {
            // Max Rate = Refresh Rate / Frame Rate
            fMaxRate = (float)MulDiv(
                MonitorRateHz, fps.Denominator, fps.Numerator);
        }
    }

    return fMaxRate;
}
```



O exemplo anterior chama um método auxiliar, GetMaxRate, para calcular a taxa máxima de reprodução de encaminhamento:

O exemplo a seguir mostra como implementar o método [**IsRateSupported**](/windows/desktop/api/mfidl/nf-mfidl-imfratesupport-isratesupported) :


```C++
HRESULT EVRCustomPresenter::IsRateSupported(
    BOOL bThin,
    float fRate,
    float *pfNearestSupportedRate
    )
{
    EnterCriticalSection(&m_ObjectLock);

    float   fMaxRate = 0.0f;
    float   fNearestRate = fRate;  // If we support fRate, that is the nearest.

    HRESULT hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Find the maximum forward rate.
    // Note: We have no minimum rate (that is, we support anything down to 0).
    fMaxRate = GetMaxRate(bThin);

    if (fabsf(fRate) > fMaxRate)
    {
        // The (absolute) requested rate exceeds the maximum rate.
        hr = MF_E_UNSUPPORTED_RATE;

        // The nearest supported rate is fMaxRate.
        fNearestRate = fMaxRate;
        if (fRate < 0)
        {
            // Negative for reverse playback.
            fNearestRate = -fNearestRate;
        }
    }

    // Return the nearest supported rate.
    if (pfNearestSupportedRate != NULL)
    {
        *pfNearestSupportedRate = fNearestRate;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



### <a name="sending-events-to-the-evr"></a>Enviando eventos para o EVR

O apresentador deve notificar o EVR de vários eventos. Para fazer isso, ele usa a interface [**IMediaEventSink**](/windows/win32/api/strmif/nn-strmif-imediaeventsink) do EVR, obtida quando o EVR chama o método [**IMFTopologyServiceLookupClient:: InitServicePointers**](/windows/desktop/api/evr/nf-evr-imftopologyservicelookupclient-initservicepointers) do apresentador. (A interface **IMediaEventSink** é originalmente uma interface do DirectShow, mas é usada tanto no DirectShow EVR quanto no Media Foundation.) O código a seguir mostra como enviar um evento para o EVR:


```C++
    // NotifyEvent: Send an event to the EVR through its IMediaEventSink interface.
    void NotifyEvent(long EventCode, LONG_PTR Param1, LONG_PTR Param2)
    {
        if (m_pMediaEventSink)
        {
            m_pMediaEventSink->Notify(EventCode, Param1, Param2);
        }
    }
```



A tabela a seguir lista os eventos que o apresentador envia, juntamente com os parâmetros de evento.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Evento</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-complete"><strong>EC_COMPLETE</strong></a></td>
<td>O apresentador terminou de renderizar todos os quadros após a mensagem de MFVP_MESSAGE_ENDOFSTREAM.<br/>
<ul>
<li><em>Param1</em>: HRESULT que indica o status da operação.</li>
<li><em>Param2</em>: não usado.</li>
</ul>
Para obter mais informações, consulte <a href="#end-of-stream">end of Stream</a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-display-changed"><strong>EC_DISPLAY_CHANGED</strong></a></td>
<td>O dispositivo Direct3D foi alterado.<br/>
<ul>
<li><em>Param1</em>: não usado.</li>
<li><em>Param2</em>: não usado.</li>
</ul>
Para obter mais informações, consulte <a href="#managing-the-direct3d-device">Gerenciando o dispositivo Direct3D</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-errorabort"><strong>EC_ERRORABORT</strong></a></td>
<td>Ocorreu um erro que requer a interrupção do streaming.<br/>
<ul>
<li><em>Param1</em>: <strong>HRESULT</strong> que indica o erro que ocorreu.</li>
<li><em>Param2</em>: não usado.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-processing-latency"><strong>EC_PROCESSING_LATENCY</strong></a></td>
<td>Especifica a quantidade de tempo que o apresentador está demorando para renderizar cada quadro. (Opcional).<br/>
<ul>
<li><em>Param1</em>: ponteiro para um valor de <strong>LONGLONG</strong> constante que contém a quantidade de tempo para processar o quadro, em unidades de 100 a nanossegundos.</li>
<li><em>Param2</em>: não usado.</li>
</ul>
Para obter mais informações, consulte <a href="#processing-output">processamento de saída</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-sample-latency"><strong>EC_SAMPLE_LATENCY</strong></a></td>
<td>Especifica o tempo de retardo atual em exemplos de renderização. Se o valor for positivo, os exemplos estarão atrás da agenda. Se o valor for negativo, as amostras serão antecipadas ao agendamento. (Opcional).<br/>
<ul>
<li><em>Param1:</em>ponteiro para um valor <strong>LONGLONG constante</strong> que contém o tempo de retardo, em unidades de 100 nanossegundos.</li>
<li><em>Param2:</em>não usado.</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/ec-scrub-time"><strong>EC_SCRUB_TIME</strong></a></td>
<td>Enviado imediatamente após <strong>EC_STEP_COMPLETE</strong> se a taxa de reprodução for zero. Esse evento contém o carimbo de data/hora do quadro que foi exibido.<br/>
<ul>
<li><em>Param1:</em>32 bits inferiores do carimbo de data/hora.</li>
<li><em>Param2:</em>32 bits superiores do carimbo de data/hora.</li>
</ul>
Para obter mais informações, consulte <a href="#frame-stepping">Frame Stepping</a>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/ec-step-complete"><strong>EC_STEP_COMPLETE</strong></a></td>
<td>O apresentador concluiu ou cancelou uma etapa de quadro.<br/>
<ul>
<li><em>Param1:</em>não usado.</li>
<li><em>Param2:</em>não usado.</li>
</ul>
Para obter mais informações, consulte <a href="#frame-stepping">Frame Stepping</a>.<br/>
<blockquote>
[!Note]<br />
Uma versão anterior da documentação descrita <em>incorretamente param1.</em> Esse parâmetro não é usado para esse evento.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="negotiating-formats"></a>Negociando formatos

Sempre que o apresentador receber **uma MFVP_MESSAGE_INVALIDATEMEDIATYPE** do EVR, ele deverá definir o formato de saída no mixer, da seguinte forma:

1.  Chame [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) no mixer para obter um possível tipo de saída. Esse tipo descreve um formato que o mixer pode produzir considerando os fluxos de entrada e os recursos de processamento de vídeo do dispositivo gráfico.
2.  Verifique se o apresentador pode usar esse tipo de mídia como seu formato de renderização. Aqui estão algumas coisas a verificar, embora sua implementação possa ter seus próprios requisitos:

    -   O vídeo deve ser descompactado.
    -   O vídeo deve ter apenas quadros progressivos. Verifique se o [**MF_MT_INTERLACE_MODE**](mf-mt-interlace-mode-attribute.md) é **igual a MFVideoInterlace_Progressive**.
    -   O formato deve ser compatível com o dispositivo Direct3D.

    Se o tipo não for aceitável, retorne à etapa 1 e receba o próximo tipo proposto do mixer.

3.  Crie um novo tipo de mídia que seja um clone do tipo original e, em seguida, altere os seguintes atributos:

    -   De definido [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) atributo de valor igual à largura e à altura que você deseja para as superfícies direct3D que você alocará.
    -   De definido [**MF_MT_PAN_SCAN_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) atributo como **FALSE.**
    -   De definido [**MF_MT_PIXEL_ASPECT_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) atributo igual ao PAR da exibição (normalmente 1:1).
    -   De definir a abertura geométrica [**(MF_MT_GEOMETRIC_APERTURE**](mf-mt-geometric-aperture-attribute.md) atributo) igual a um retângulo dentro da superfície direct3D. Quando o mixer gera um quadro de saída, ele gera a imagem de origem nesse retângulo. A abertura geométrica pode ser tão grande quanto a superfície ou pode ser uma sub-estrutura dentro da superfície. Para obter mais informações, consulte [Retângulos de origem e destino.](#source-and-destination-rectangles)

4.  Para testar se o mixer aceitará o tipo de saída modificado, chame [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) com o **sinalizador MFT_SET_TYPE_TEST_ONLY.** Se o mixer rejeitar o tipo, volte para a etapa 1 e obter o próximo tipo.
5.  Aloce um pool de superfícies Direct3D, conforme descrito em [Alocando superfícies direct3D.](#allocating-direct3d-surfaces) O mixer usará essas superfícies quando desenhar os quadros de vídeo compostos.
6.  De definir o tipo de saída no mixer chamando [**SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) sem sinalizadores. Se a primeira chamada para **SetOutputType** tiver êxito na etapa 4, o método deverá ter êxito novamente.

Se o mixer ficar sem tipos, o [**método GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) retornará **MF_E_NO_MORE_TYPES**. Se o apresentador não puder encontrar um tipo de saída adequado para o mixer, o fluxo não poderá ser renderizado. Nesse caso, DirectShow ou Media Foundation pode tentar outro formato de fluxo. Portanto, o apresentador pode receber várias **MFVP_MESSAGE_INVALIDATEMEDIATYPE** mensagens em uma linha até que um tipo válido seja encontrado.

O mixer faz a caixa de texto automaticamente do vídeo, levando em conta a PAR (taxa de proporção de pixel) da origem e do destino. Para melhores resultados, a largura e a altura da superfície e a abertura geométrica devem ser iguais ao tamanho real que você deseja que o vídeo apareça na exibição. A imagem a seguir ilustra esse processo.

![diagrama mostrando uma fram composta que leva a uma superfície direct3d, o que leva a uma janela](images/b746edca-8830-4c88-aa59-0067b020d4af.gif)

O código a seguir mostra o contorno do processo. Algumas das etapas são colocadas em funções auxiliares, dos detalhes exatos dos quais dependerão dos requisitos do seu apresentador.


```C++
HRESULT EVRCustomPresenter::RenegotiateMediaType()
{
    HRESULT hr = S_OK;
    BOOL bFoundMediaType = FALSE;

    IMFMediaType *pMixerType = NULL;
    IMFMediaType *pOptimalType = NULL;
    IMFVideoMediaType *pVideoType = NULL;

    if (!m_pMixer)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Loop through all of the mixer's proposed output types.
    DWORD iTypeIndex = 0;
    while (!bFoundMediaType && (hr != MF_E_NO_MORE_TYPES))
    {
        SafeRelease(&pMixerType);
        SafeRelease(&pOptimalType);

        // Step 1. Get the next media type supported by mixer.
        hr = m_pMixer->GetOutputAvailableType(0, iTypeIndex++, &pMixerType);
        if (FAILED(hr))
        {
            break;
        }

        // From now on, if anything in this loop fails, try the next type,
        // until we succeed or the mixer runs out of types.

        // Step 2. Check if we support this media type.
        if (SUCCEEDED(hr))
        {
            // Note: None of the modifications that we make later in CreateOptimalVideoType
            // will affect the suitability of the type, at least for us. (Possibly for the mixer.)
            hr = IsMediaTypeSupported(pMixerType);
        }

        // Step 3. Adjust the mixer's type to match our requirements.
        if (SUCCEEDED(hr))
        {
            hr = CreateOptimalVideoType(pMixerType, &pOptimalType);
        }

        // Step 4. Check if the mixer will accept this media type.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, MFT_SET_TYPE_TEST_ONLY);
        }

        // Step 5. Try to set the media type on ourselves.
        if (SUCCEEDED(hr))
        {
            hr = SetMediaType(pOptimalType);
        }

        // Step 6. Set output media type on mixer.
        if (SUCCEEDED(hr))
        {
            hr = m_pMixer->SetOutputType(0, pOptimalType, 0);

            assert(SUCCEEDED(hr)); // This should succeed unless the MFT lied in the previous call.

            // If something went wrong, clear the media type.
            if (FAILED(hr))
            {
                SetMediaType(NULL);
            }
        }

        if (SUCCEEDED(hr))
        {
            bFoundMediaType = TRUE;
        }
    }

    SafeRelease(&pMixerType);
    SafeRelease(&pOptimalType);
    SafeRelease(&pVideoType);

    return hr;
}
```



Para obter mais informações sobre tipos de mídia de vídeo, consulte [Tipos de mídia de vídeo](video-media-types.md).

## <a name="managing-the-direct3d-device"></a>Gerenciando o dispositivo Direct3D

O apresentador cria o dispositivo Direct3D e lida com qualquer perda de dispositivo durante o streaming. O apresentador também hospeda o gerenciador de dispositivos Direct3D, que fornece uma maneira para outros componentes usarem o mesmo dispositivo. Por exemplo, o mixer usa o dispositivo Direct3D para misturar substreams, desinterversão e executar ajustes de cor. Os decodificadores podem usar o dispositivo Direct3D para decodificação acelerada por vídeo. (Para obter mais informações sobre aceleração de vídeo, consulte Aceleração de [vídeo DirectX 2.0](directx-video-acceleration-2-0.md).)

Para configurar o dispositivo Direct3D, execute as seguintes etapas:

1.  Crie o objeto Direct3D chamando **Direct3DCreate9** ou **Direct3DCreate9Ex.**
2.  Crie o dispositivo chamando **IDirect3D9::CreateDevice** ou **IDirect3D9Ex::CreateDevice.**
3.  Crie o gerenciador de dispositivos chamando [**DXVA2CreateDirect3DDeviceManager9**](/windows/desktop/api/dxva2api/nf-dxva2api-dxva2createdirect3ddevicemanager9).
4.  Defina o dispositivo no gerenciador de dispositivos chamando [**IDirect3DDeviceManager9::ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice).

Se outro componente de pipeline precisar do gerenciador de dispositivos, ele chamará [**IMFGetService::GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) no EVR, especificando MR_VIDEO_ACCELERATION_SERVICE **para** o GUID do serviço. O EVR passa a solicitação para o apresentador. Depois que o objeto obtém o ponteiro [**IDirect3DDeviceManager9,**](/windows/desktop/api/dxva2api/nn-dxva2api-idirect3ddevicemanager9) ele pode obter um identificador para o dispositivo chamando [**IDirect3DDeviceManager9::OpenDeviceHandle**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-opendevicehandle). Quando o objeto precisa usar o dispositivo, ele passa o identificador do dispositivo para o método [**IDirect3DDeviceManager9::LockDevice,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) que retorna um ponteiro **IDirect3DDevice9.**

Depois que o dispositivo for criado, se o apresentador destruir o dispositivo e criar um novo, o apresentador deverá chamar [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) novamente. O **método ResetDevice** invalida quaisquer alças de dispositivo existentes, o que faz [**com que LockDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-lockdevice) **retorne DXVA2_E_NEW_VIDEO_DEVICE**. Esse código de erro sinaliza a outros objetos usando o dispositivo que eles devem abrir um novo lidar com o dispositivo. Para obter mais informações sobre como usar o gerenciador de dispositivos, consulte [Direct3D Gerenciador de Dispositivos](direct3d-device-manager.md).

O apresentador pode criar o dispositivo no modo de janela ou no modo exclusivo de tela inteira. Para o modo em janelas, você deve fornecer uma maneira para o aplicativo especificar a janela de vídeo. O apresentador padrão implementa o [**método IMFVideoDisplayControl::SetVideoWindow**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow) para essa finalidade. Você deve criar o dispositivo quando o apresentador é criado pela primeira vez. Normalmente, você não conhecerá todos os parâmetros do dispositivo no momento, como a janela ou o formato de buffer de fundo. Você pode criar um dispositivo temporário e substituí-lo posteriormente&; lembre-se de chamar \# [**ResetDevice**](/windows/desktop/api/dxva2api/nf-dxva2api-idirect3ddevicemanager9-resetdevice) no gerenciador de dispositivos.

Se você criar um novo dispositivo ou se chamar **IDirect3DDevice9::Reset** ou **IDirect3DDevice9Ex::ResetEx** em um dispositivo existente, envie um [**evento EC_DISPLAY_CHANGED**](../directshow/ec-display-changed.md) para o EVR. Esse evento notifica o EVR para renegociar o tipo de mídia. O EVR ignora os parâmetros de evento para esse evento.

### <a name="allocating-direct3d-surfaces"></a>Alocando superfícies Direct3D

Depois que o apresentador define o tipo de mídia, ele pode alocar as superfícies direct3D, que o mixer usará para gravar os quadros de vídeo. A superfície deve corresponder ao tipo de mídia do apresentador:

-   O formato de superfície deve corresponder ao subtipo de mídia. Por exemplo, se o subtipo for **MFVideoFormat_RGB24**, o formato da superfície deverá ser **D3DFMT_X8R8G8B8**. Para obter mais informações sobre subtipos e formatos Direct3D, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).
-   A largura e a altura da superfície devem corresponder às dimensões fornecidas [**MF_MT_FRAME_SIZE**](mf-mt-frame-size-attribute.md) atributo do tipo de mídia.

A maneira recomendada de alocar superfícies depende se o apresentador é executado em janela ou em tela inteira.

Se o dispositivo Direct3D estiver em janelas, você poderá criar várias cadeias de permuta, cada uma com um único buffer de fundo. Usando essa abordagem, você pode apresentar cada superfície independentemente, pois apresentar uma cadeia de permuta não interferirá nas outras cadeias de permuta. O mixer pode gravar dados em uma superfície enquanto outra superfície está agendada para apresentação.

Primeiro, decida quantas cadeias de troca criar. É recomendável um mínimo de três. Para cada cadeia de permuta, faça o seguinte:

1.  Chame **IDirect3DDevice9::CreateAdditionalSwapChain** para criar a cadeia de permuta.
2.  Chame **IDirect3DSwapChain9::GetBackBuffer** para obter um ponteiro para a superfície de buffer de fundo da cadeia de permuta.
3.  Chame [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) e passe um ponteiro para a superfície. Essa função retorna um ponteiro para um objeto de exemplo de vídeo. O objeto de exemplo de vídeo implementa a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) e o apresentador usa essa interface para entregar a superfície ao mixer quando o apresentador chama o método [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) do mixer. Para obter mais informações sobre o objeto de exemplo de vídeo, consulte [Exemplos de vídeo](video-samples.md).
4.  Armazene [**o ponteiro IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) em uma fila. O apresentador efetuará pull de exemplos dessa fila durante o processamento, conforme descrito [em Processamento de Saída](#processing-output).
5.  Mantenha uma referência ao ponteiro **IDirect3DSwapChain9** para que a cadeia de permuta não seja liberada.

No modo exclusivo de tela inteira, o dispositivo não pode ter mais de uma cadeia de permuta. Essa cadeia de permuta é criada implicitamente quando você cria o dispositivo de tela inteira. A cadeia de permuta pode ter mais de um buffer de fundo. No entanto, se você apresentar um buffer de fundo enquanto escreve em outro buffer de fundo na mesma cadeia de permuta, não haverá uma maneira fácil de coordenar as duas operações. Isso se deve à maneira como o Direct3D implementa a invertia de superfície. Quando você chama Present, o driver de gráficos atualiza os ponteiros de superfície na memória de gráficos. Se você estiver mantendo ponteiros **IDirect3DSurface9** quando chamar **Present**, eles apontarão para buffers diferentes após o retorno **da chamada** Present.

A opção mais simples é criar um exemplo de vídeo para a cadeia de permuta. Se você escolher essa opção, siga as mesmas etapas fornecidas para o modo em janelas. A única diferença é que a fila de exemplo contém um único exemplo de vídeo. Outra opção é criar superfícies fora da tela e, em seguida, blit-las no buffer de fundo. As superfícies que você cria devem dar suporte ao método [**IDirectXVideoProcessor::VideoProcessBlt,**](/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessor-videoprocessblt) que o mixer usa para compor os quadros de saída.

### <a name="tracking-samples"></a>Exemplos de acompanhamento

Quando o apresentador aloca os exemplos de vídeo pela primeira vez, ele os coloca em uma fila. O apresentador desenha dessa fila sempre que precisa obter um novo quadro do mixer. Depois que o mixer saída do quadro, o apresentador move o exemplo para uma segunda fila. A segunda fila é para exemplos que estão aguardando seus horários de apresentação agendados.

Para facilitar o controle do status de cada exemplo, o objeto de exemplo de vídeo implementa a interface [**IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) Você pode usar essa interface da seguinte forma:

1.  Implemente a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) no seu apresentador.
2.  Antes de colocar um exemplo na fila agendada, consulte o objeto de exemplo de vídeo para a interface [**IMFTrackedSample.**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

3.  Chame [**IMFTrackedSample::SetAllocator com**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) um ponteiro para a interface de retorno de chamada.
4.  Quando o exemplo estiver pronto para apresentação, remova-o da fila agendada, apresente-o e libere todas as referências ao exemplo.
5.  O exemplo invoca o retorno de chamada. (O objeto de exemplo não é excluído nesse caso porque mantém uma contagem de referência em si mesmo até que o retorno de chamada seja invocado.)
6.  Dentro do retorno de chamada, retorne o exemplo para a fila disponível.

Um apresentador não é necessário para usar [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) para acompanhar exemplos; você pode implementar qualquer técnica que funcione melhor para seu design. Uma vantagem do **IMFTrackedSample** é que você pode mover as funções de programação e renderização do apresentador para objetos auxiliares, e esses objetos não precisam de nenhum mecanismo especial para chamar de volta ao apresentador quando eles lançam exemplos de vídeo porque o objeto de exemplo fornece esse mecanismo.

O código a seguir mostra como definir o retorno de chamada:


```C++
HRESULT EVRCustomPresenter::TrackSample(IMFSample *pSample)
{
    IMFTrackedSample *pTracked = NULL;

    HRESULT hr = pSample->QueryInterface(IID_PPV_ARGS(&pTracked));

    if (SUCCEEDED(hr))
    {
        hr = pTracked->SetAllocator(&m_SampleFreeCB, NULL);
    }

    SafeRelease(&pTracked);
    return hr;
}
```



No retorno de chamada, chame [**IMFAsyncResult::GetObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getobject) no objeto de resultado assíncrono para recuperar um ponteiro para o exemplo:


```C++
HRESULT EVRCustomPresenter::OnSampleFree(IMFAsyncResult *pResult)
{
    IUnknown *pObject = NULL;
    IMFSample *pSample = NULL;
    IUnknown *pUnk = NULL;

    // Get the sample from the async result object.
    HRESULT hr = pResult->GetObject(&pObject);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pObject->QueryInterface(IID_PPV_ARGS(&pSample));
    if (FAILED(hr))
    {
        goto done;
    }

    // If this sample was submitted for a frame-step, the frame step operation
    // is complete.

    if (m_FrameStep.state == FRAMESTEP_SCHEDULED)
    {
        // Query the sample for IUnknown and compare it to our cached value.
        hr = pSample->QueryInterface(IID_PPV_ARGS(&pUnk));
        if (FAILED(hr))
        {
            goto done;
        }

        if (m_FrameStep.pSampleNoRef == (DWORD_PTR)pUnk)
        {
            // Notify the EVR.
            hr = CompleteFrameStep(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Note: Although pObject is also an IUnknown pointer, it is not
        // guaranteed to be the exact pointer value returned through
        // QueryInterface. Therefore, the second QueryInterface call is
        // required.
    }

    /*** Begin lock ***/

    EnterCriticalSection(&m_ObjectLock);

    UINT32 token = MFGetAttributeUINT32(
        pSample, MFSamplePresenter_SampleCounter, (UINT32)-1);

    if (token == m_TokenCounter)
    {
        // Return the sample to the sample pool.
        hr = m_SamplePool.ReturnSample(pSample);
        if (SUCCEEDED(hr))
        {
            // A free sample is available. Process more data if possible.
            (void)ProcessOutputLoop();
        }
    }

    LeaveCriticalSection(&m_ObjectLock);

    /*** End lock ***/

done:
    if (FAILED(hr))
    {
        NotifyEvent(EC_ERRORABORT, hr, 0);
    }
    SafeRelease(&pObject);
    SafeRelease(&pSample);
    SafeRelease(&pUnk);
    return hr;
}
```



## <a name="processing-output"></a>Saída de processamento

Sempre que o mixer recebe um novo exemplo de entrada, o EVR envia uma **MFVP_MESSAGE_PROCESSINPUTNOTIFY** para o apresentador. Essa mensagem indica que o mixer pode ter um novo quadro de vídeo a ser entregue. Em resposta, o apresentador chama [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) no mixer. Se o método for bem-sucedido, o apresentador agenda o exemplo para apresentação.

Para obter a saída do mixer, execute as seguintes etapas:

1.  Verifique o estado do relógio. Se o relógio estiver em pausa, ignore a mensagem **MFVP_MESSAGE_PROCESSINPUTNOTIFY,** a menos que esse seja o primeiro quadro de vídeo. Se o relógio estiver em execução ou se esse for o primeiro quadro de vídeo, continue.
2.  Obter um exemplo da fila de exemplos disponíveis. Se a fila estiver vazia, isso significa que todos os exemplos alocados estão agendados para apresentação no momento. Nesse caso, ignore a mensagem **MFVP_MESSAGE_PROCESSINPUTNOTIFY** no momento. Quando o próximo exemplo ficar disponível, repita as etapas listadas aqui.
3.  (Opcional.) Se o relógio estiver disponível, obter a hora do relógio atual (*T1*) chamando [**IMFClock::GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime).
4.  Chame [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) no mixer. Se **ProcessOutput for** bem-sucedido, o exemplo conterá um quadro de vídeo. Se o método falhar, verifique o código de retorno. Os seguintes códigos de erro de **ProcessOutput** não são falhas críticas:

    

    | Código do erro                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                    |
    |-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **MF_E_TRANSFORM_NEED_MORE_INPUT** | O mixer precisa de mais entrada antes de produzir um novo quadro de saída.<br/> Se você receber esse código de erro, verifique se o EVR atingiu o final do fluxo e responda de acordo, conforme descrito [em End of Stream](#end-of-stream). Caso contrário, ignore essa **MF_E_TRANSFORM_NEED_MORE_INPUT** mensagem. O EVR enviará outro quando o mixer receber mais entrada.<br/> |
    | **MF_E_TRANSFORM_STREAM_CHANGE**    | O tipo de saída do mixer se tornou inválido, possivelmente devido a uma alteração de formato upstream.<br/> Se você receber esse código de erro, de definir o tipo de mídia do apresentador como **NULL.** O EVR solicitará um novo formato.<br/>                                                                                                                                                                         |
    | **MF_E_TRANSFORM_TYPE_NOT_SET**    | O mixer requer um novo tipo de mídia.<br/> Se você receber esse código de erro, renegociar o tipo de saída do mixer, conforme descrito em [Negociando formatos](#negotiating-formats).<br/>                                                                                                                                                                                                        |

    

     

    Se [**ProcessOutput for**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) bem-sucedido, continue.

5.  (Opcional.) Se o relógio estiver disponível, obter a hora do relógio atual (*T2*). A quantidade de latência introduzida pelo mixer é (*T2*  -  *T1*). Envie um **EC_PROCESSING_LATENCY** evento com esse valor para o EVR. O EVR usa esse valor para controle de qualidade. Se nenhum relógio estiver disponível, não haverá motivo para enviar o **EC_PROCESSING_LATENCY** evento.
6.  (Opcional.) Consulte o exemplo de [**IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) e chame [**IMFTrackedSample::SetAllocator,**](/windows/win32/api/mfidl/nf-mfidl-imftrackedsample-setallocator) conforme descrito em [Amostras de rastreamento.](#tracking-samples)
7.  Agende o exemplo para apresentação.

Essa sequência de etapas pode terminar antes que o apresentador obtém qualquer saída do mixer. Para garantir que nenhuma solicitação seja retirada, você deve repetir as mesmas etapas quando ocorrer o seguinte:

-   O método [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) ou **IMFClockStateSink::OnClockStart** do apresentador é chamado. Isso lida com o caso em que o mixer ignora a entrada porque o relógio está em pausa (etapa 1).
-   O [**retorno de chamada IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) é invocado. Isso lida com o caso em que o mixer recebe entrada, mas todos os exemplos de vídeo do apresentador estão em uso (etapa 2).

Os próximos exemplos de código mostram essas etapas mais detalhadamente. O apresentador chama o `ProcessInputNotify` método (mostrado no exemplo a seguir) quando ele obtém a **MFVP_MESSAGE_PROCESSINPUTNOTIFY** de texto.


```C++
//-----------------------------------------------------------------------------
// ProcessInputNotify
//
// Attempts to get a new output sample from the mixer.
//
// This method is called when the EVR sends an MFVP_MESSAGE_PROCESSINPUTNOTIFY
// message, which indicates that the mixer has a new input sample.
//
// Note: If there are multiple input streams, the mixer might not deliver an
// output sample for every input sample.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessInputNotify()
{
    HRESULT hr = S_OK;

    // Set the flag that says the mixer has a new sample.
    m_bSampleNotify = TRUE;

    if (m_pMediaType == NULL)
    {
        // We don't have a valid media type yet.
        hr = MF_E_TRANSFORM_TYPE_NOT_SET;
    }
    else
    {
        // Try to process an output sample.
        ProcessOutputLoop();
    }
    return hr;
}
```



Esse `ProcessInputNotify` método define um sinalizador booliana para registrar o fato de que o mixer tem nova entrada. Em seguida, ele chama `ProcessOutputLoop` o método , mostrado no próximo exemplo. Esse método tenta efetuar pull do máximo possível de amostras do mixer:


```C++
void EVRCustomPresenter::ProcessOutputLoop()
{
    HRESULT hr = S_OK;

    // Process as many samples as possible.
    while (hr == S_OK)
    {
        // If the mixer doesn't have a new input sample, break from the loop.
        if (!m_bSampleNotify)
        {
            hr = MF_E_TRANSFORM_NEED_MORE_INPUT;
            break;
        }

        // Try to process a sample.
        hr = ProcessOutput();

        // NOTE: ProcessOutput can return S_FALSE to indicate it did not
        // process a sample. If so, break out of the loop.
    }

    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        // The mixer has run out of input data. Check for end-of-stream.
        CheckEndOfStream();
    }
}
```



O `ProcessOutput` método , mostrado no exemplo a seguir, tenta obter um único quadro de vídeo do mixer. Se nenhum quadro de vídeo estiver disponível, retornará S_FALSE ou um código de erro, o que `ProcessSample` interromperá o loop em `ProcessOutputLoop` . A maior parte do trabalho é feita dentro do `ProcessOutput` método :


```C++
//-----------------------------------------------------------------------------
// ProcessOutput
//
// Attempts to get a new output sample from the mixer.
//
// Called in two situations:
// (1) ProcessOutputLoop, if the mixer has a new input sample.
// (2) Repainting the last frame.
//-----------------------------------------------------------------------------

HRESULT EVRCustomPresenter::ProcessOutput()
{
    assert(m_bSampleNotify || m_bRepaint);  // See note above.

    HRESULT     hr = S_OK;
    DWORD       dwStatus = 0;
    LONGLONG    mixerStartTime = 0, mixerEndTime = 0;
    MFTIME      systemTime = 0;
    BOOL        bRepaint = m_bRepaint; // Temporarily store this state flag.

    MFT_OUTPUT_DATA_BUFFER dataBuffer;
    ZeroMemory(&dataBuffer, sizeof(dataBuffer));

    IMFSample *pSample = NULL;

    // If the clock is not running, we present the first sample,
    // and then don't present any more until the clock starts.

    if ((m_RenderState != RENDER_STATE_STARTED) &&  // Not running.
         !m_bRepaint &&             // Not a repaint request.
         m_bPrerolled               // At least one sample has been presented.
         )
    {
        return S_FALSE;
    }

    // Make sure we have a pointer to the mixer.
    if (m_pMixer == NULL)
    {
        return MF_E_INVALIDREQUEST;
    }

    // Try to get a free sample from the video sample pool.
    hr = m_SamplePool.GetSample(&pSample);
    if (hr == MF_E_SAMPLEALLOCATOR_EMPTY)
    {
        // No free samples. Try again when a sample is released.
        return S_FALSE;
    }
    else if (FAILED(hr))
    {
        return hr;
    }

    // From now on, we have a valid video sample pointer, where the mixer will
    // write the video data.
    assert(pSample != NULL);

    // (If the following assertion fires, it means we are not managing the sample pool correctly.)
    assert(MFGetAttributeUINT32(pSample, MFSamplePresenter_SampleCounter, (UINT32)-1) == m_TokenCounter);

    if (m_bRepaint)
    {
        // Repaint request. Ask the mixer for the most recent sample.
        SetDesiredSampleTime(
            pSample,
            m_scheduler.LastSampleTime(),
            m_scheduler.FrameDuration()
            );

        m_bRepaint = FALSE; // OK to clear this flag now.
    }
    else
    {
        // Not a repaint request. Clear the desired sample time; the mixer will
        // give us the next frame in the stream.
        ClearDesiredSampleTime(pSample);

        if (m_pClock)
        {
            // Latency: Record the starting time for ProcessOutput.
            (void)m_pClock->GetCorrelatedTime(0, &mixerStartTime, &systemTime);
        }
    }

    // Now we are ready to get an output sample from the mixer.
    dataBuffer.dwStreamID = 0;
    dataBuffer.pSample = pSample;
    dataBuffer.dwStatus = 0;

    hr = m_pMixer->ProcessOutput(0, 1, &dataBuffer, &dwStatus);

    if (FAILED(hr))
    {
        // Return the sample to the pool.
        HRESULT hr2 = m_SamplePool.ReturnSample(pSample);
        if (FAILED(hr2))
        {
            hr = hr2;
            goto done;
        }
        // Handle some known error codes from ProcessOutput.
        if (hr == MF_E_TRANSFORM_TYPE_NOT_SET)
        {
            // The mixer's format is not set. Negotiate a new format.
            hr = RenegotiateMediaType();
        }
        else if (hr == MF_E_TRANSFORM_STREAM_CHANGE)
        {
            // There was a dynamic media type change. Clear our media type.
            SetMediaType(NULL);
        }
        else if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
        {
            // The mixer needs more input.
            // We have to wait for the mixer to get more input.
            m_bSampleNotify = FALSE;
        }
    }
    else
    {
        // We got an output sample from the mixer.

        if (m_pClock && !bRepaint)
        {
            // Latency: Record the ending time for the ProcessOutput operation,
            // and notify the EVR of the latency.

            (void)m_pClock->GetCorrelatedTime(0, &mixerEndTime, &systemTime);

            LONGLONG latencyTime = mixerEndTime - mixerStartTime;
            NotifyEvent(EC_PROCESSING_LATENCY, (LONG_PTR)&latencyTime, 0);
        }

        // Set up notification for when the sample is released.
        hr = TrackSample(pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Schedule the sample.
        if ((m_FrameStep.state == FRAMESTEP_NONE) || bRepaint)
        {
            hr = DeliverSample(pSample, bRepaint);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else
        {
            // We are frame-stepping (and this is not a repaint request).
            hr = DeliverFrameStepSample(pSample);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        m_bPrerolled = TRUE; // We have presented at least one sample now.
    }

done:
    SafeRelease(&pSample);

    // Important: Release any events returned from the ProcessOutput method.
    SafeRelease(&dataBuffer.pEvents);
    return hr;
}
```



Alguns comentários sobre este exemplo:

-   A *m_SamplePool* variável é assumida como um objeto de coleção que contém a fila de exemplos de vídeo disponíveis. O método do objeto `GetSample` retornará **MF_E_SAMPLEALLOCATOR_EMPTY** se a fila estiver vazia.
-   Se o método [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) do mixer retornar MF_E_TRANSFORM_NEED_MORE_INPUT, isso significa que o mixer não pode produzir mais saída, portanto, o apresentador limpa o sinalizador *m_fSampleNotify* saída.
-   O método , que define o retorno de chamada `TrackSample` [**IMFTrackedSample,**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample) é mostrado na seção [Amostras de rastreamento](#tracking-samples).

### <a name="repainting-frames"></a>Reainting Frames

Ocasionalmente, o apresentador pode precisar repintar o quadro de vídeo mais recente. Por exemplo, o apresentador padrão reintsimos o quadro nas seguintes situações:

-   No modo em janelas, em resposta **WM_PAINT** mensagens recebidas pela janela do aplicativo. Consulte [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo).
-   Se o retângulo de destino mudar quando o aplicativo chamar [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Use as etapas a seguir para solicitar que o mixer crie o quadro mais recente:

1.  Obtenha um exemplo de vídeo da fila.
2.  Consulte o exemplo para a interface [**IMFDesiredSample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample) .
3.  Chame [**IMFDesiredSample:: SetDesiredSampleTimeAndDuration**](/windows/desktop/api/evr/nf-evr-imfdesiredsample-setdesiredsampletimeandduration). Especifique o carimbo de data/hora do quadro de vídeo mais recente. (Você precisará armazenar esse valor em cache e atualizá-lo para cada quadro.)
4.  Chame [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) no mixer.

Ao repintar um quadro, você pode ignorar o relógio de apresentação e apresentar o quadro imediatamente.

### <a name="scheduling-samples"></a>Exemplos de agendamento

Os quadros de vídeo podem alcançar o EVR a qualquer momento. O apresentador é responsável por apresentar cada quadro no horário correto, com base no carimbo de data/hora do quadro. Quando o apresentador Obtém um novo exemplo do mixer, ele coloca o exemplo na fila agendada. Em um thread separado, o apresentador Obtém continuamente a primeira amostra do início da fila e determina se deve:

-   Apresente o exemplo.
-   Mantenha a amostra na fila porque ela é antecipada.
-   Descarte o exemplo porque ele está atrasado. Embora você deva evitar a remoção de quadros, se possível, talvez seja necessário se o apresentador ficar continuamente atrás.

Para obter o carimbo de data/hora de um quadro de vídeo, chame [**IMFSample:: Getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) no exemplo de vídeo. O carimbo de data/hora é relativo ao relógio de apresentação do EVR. Para obter a hora do relógio atual, chame [**IMFClock:: GetCorrelatedTime**](/windows/desktop/api/mfidl/nf-mfidl-imfclock-getcorrelatedtime). Se o EVR não tiver um relógio de apresentação ou se um exemplo não tiver um carimbo de data/hora, você poderá apresentar o exemplo imediatamente depois de obtê-lo.

Para obter a duração de cada amostra, chame [**IMFSample:: GetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampleduration). Se o exemplo não tiver uma duração, você poderá usar a função [**MFFrameRateToAverageTimePerFrame**](/windows/desktop/api/mfapi/nf-mfapi-mfframeratetoaveragetimeperframe) para calcular a duração da taxa de quadros.

Ao agendar exemplos, tenha em mente o seguinte:

-   Se a taxa de reprodução for mais rápida ou mais lenta do que a velocidade normal, o relógio será executado a uma taxa mais rápida ou mais lenta. Isso significa que o carimbo de data/hora em um exemplo sempre fornece o tempo de destino correto relativo ao relógio de apresentação. No entanto, se você traduzir os tempos de apresentação em algum outro horário de relógio (por exemplo, o contador desempenho de alta resolução), será necessário dimensionar os horários com base na velocidade do relógio. Se a velocidade do relógio for alterada, o EVR chamará o método [**IMFClockStateSink:: OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) do apresentador.
-   A taxa de reprodução pode ser negativa para reprodução reversa. Quando a taxa de reprodução é negativa, o relógio de apresentação é executado de forma retroativa. Em outras palavras, a hora *n* + 1 ocorre antes da hora *n*.

O exemplo a seguir calcula o quão cedo ou tarde é uma amostra, em relação ao relógio de apresentação:


```C++
    LONGLONG hnsPresentationTime = 0;
    LONGLONG hnsTimeNow = 0;
    MFTIME   hnsSystemTime = 0;

    BOOL bPresentNow = TRUE;
    LONG lNextSleep = 0;

    if (m_pClock)
    {
        // Get the sample's time stamp. It is valid for a sample to
        // have no time stamp.
        hr = pSample->GetSampleTime(&hnsPresentationTime);

        // Get the clock time. (But if the sample does not have a time stamp,
        // we don't need the clock time.)
        if (SUCCEEDED(hr))
        {
            hr = m_pClock->GetCorrelatedTime(0, &hnsTimeNow, &hnsSystemTime);
        }

        // Calculate the time until the sample's presentation time.
        // A negative value means the sample is late.
        LONGLONG hnsDelta = hnsPresentationTime - hnsTimeNow;
        if (m_fRate < 0)
        {
            // For reverse playback, the clock runs backward. Therefore, the
            // delta is reversed.
            hnsDelta = - hnsDelta;
        }
```



O relógio de apresentação geralmente é orientado pelo relógio do sistema ou pelo processador de áudio. (O processador de áudio deriva o tempo da taxa na qual a placa de som consome áudio.) Em geral, o relógio de apresentação não é sincronizado com a taxa de atualização do monitor.

Se os parâmetros de apresentação do Direct3D especificarem **D3DPRESENT_INTERVAL_DEFAULT** ou **D3DPRESENT_INTERVAL_ONE** para o intervalo de apresentação, a operação **atual** aguardará o rerastreamento vertical do monitor. Essa é uma maneira fácil de evitar a subdivisão, mas reduz a precisão do seu algoritmo de agendamento. Por outro lado, se o intervalo de apresentação for **D3DPRESENT_INTERVAL_IMMEDIATE**, o método **presente** será executado imediatamente, o que causa a subdivisão, a menos que o algoritmo de agendamento seja preciso o suficiente para que você chame **Present** somente durante o período de retrace vertical.

As funções a seguir podem ajudá-lo a obter informações precisas sobre o tempo:

-   **IDirect3DDevice9:: GetRasterStatus** retorna informações sobre a varredura, incluindo a linha de varredura atual e se a rasterização está no período vertical em branco.
-   **DwmGetCompositionTimingInfo** retorna informações de tempo para o Gerenciador de janelas da área de trabalho. Essas informações serão úteis se a composição de área de trabalho estiver habilitada.

### <a name="presenting-samples"></a>Apresentando exemplos

Esta seção pressupõe que você criou uma cadeia de permuta separada para cada superfície, conforme descrito em [alocando superfícies do Direct3D](#allocating-direct3d-surfaces). Para apresentar um exemplo, obtenha a cadeia de troca da amostra de vídeo da seguinte maneira:

1.  Chame [**IMFSample:: GetBufferByIndex**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbufferbyindex) no exemplo de vídeo para obter o buffer.
2.  Consulte o buffer para a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) .
3.  Chame [**IMFGetService:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) para obter a interface **IDirect3DSurface9** da superfície do Direct3D. (Você pode combinar essa etapa e a etapa anterior em uma chamando [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice).)
4.  Chame **IDirect3DSurface9:: GetContainer** na superfície para obter um ponteiro para a cadeia de permuta.
5.  Chame **IDirect3DSwapChain9::P reenviada** na cadeia de permuta.

O código a seguir mostra essas etapas:


```C++
HRESULT D3DPresentEngine::PresentSample(IMFSample* pSample, LONGLONG llTarget)
{
    HRESULT hr = S_OK;

    IMFMediaBuffer* pBuffer = NULL;
    IDirect3DSurface9* pSurface = NULL;
    IDirect3DSwapChain9* pSwapChain = NULL;

    if (pSample)
    {
        // Get the buffer from the sample.
        hr = pSample->GetBufferByIndex(0, &pBuffer);
        if (FAILED(hr))
        {
            goto done;
        }

        // Get the surface from the buffer.
        hr = MFGetService(pBuffer, MR_BUFFER_SERVICE, IID_PPV_ARGS(&pSurface));
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (m_pSurfaceRepaint)
    {
        // Redraw from the last surface.
        pSurface = m_pSurfaceRepaint;
        pSurface->AddRef();
    }

    if (pSurface)
    {
        // Get the swap chain from the surface.
        hr = pSurface->GetContainer(IID_PPV_ARGS(&pSwapChain));
        if (FAILED(hr))
        {
            goto done;
        }

        // Present the swap chain.
        hr = PresentSwapChain(pSwapChain, pSurface);
        if (FAILED(hr))
        {
            goto done;
        }

        // Store this pointer in case we need to repaint the surface.
        CopyComPointer(m_pSurfaceRepaint, pSurface);
    }
    else
    {
        // No surface. All we can do is paint a black rectangle.
        PaintFrameWithGDI();
    }

done:
    SafeRelease(&pSwapChain);
    SafeRelease(&pSurface);
    SafeRelease(&pBuffer);

    if (FAILED(hr))
    {
        if (hr == D3DERR_DEVICELOST || hr == D3DERR_DEVICENOTRESET || hr == D3DERR_DEVICEHUNG)
        {
            // We failed because the device was lost. Fill the destination rectangle.
            PaintFrameWithGDI();

            // Ignore. We need to reset or re-create the device, but this method
            // is probably being called from the scheduler thread, which is not the
            // same thread that created the device. The Reset(Ex) method must be
            // called from the thread that created the device.

            // The presenter will detect the state when it calls CheckDeviceState()
            // on the next sample.
            hr = S_OK;
        }
    }
    return hr;
}
```



### <a name="source-and-destination-rectangles"></a>Retângulos de origem e de destino

O *retângulo de origem* é a parte do quadro de vídeo a ser exibido. Ele é definido em relação a um sistema de coordenadas normalizado, no qual todo o quadro de vídeo ocupa um retângulo com coordenadas {0, 0, 1, 1}. O *retângulo de destino* é a área dentro da superfície de destino onde o quadro de vídeo é desenhado. O apresentador padrão permite que um aplicativo defina esses retângulos chamando [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition).

Há várias opções para aplicar retângulos de origem e de destino. A primeira opção é permitir que o mixer os aplique:

-   Defina o retângulo de origem usando o atributo [**VIDEO_ZOOM_RECT**](video-zoom-rect-attribute.md) . O mixer aplicará o retângulo de origem quando blits o vídeo à superfície de destino. O retângulo de origem padrão do mixer é o quadro inteiro.
-   Defina o retângulo de destino como a abertura geométrica no tipo de saída do mixer. Para obter mais informações, consulte [negociando formatos](#negotiating-formats).

A segunda opção é aplicar os retângulos quando você **IDirect3DSwapChain9::P reenviado** especificando os parâmetros *pSourceRect* e *pDestRect* no método **Present** . Você pode combinar essas opções. Por exemplo, você pode definir o retângulo de origem no mixer, mas aplicar o retângulo de destino no método **atual** .

Se o aplicativo alterar o retângulo de destino ou redimensionar a janela, talvez seja necessário alocar novas superfícies. Nesse caso, você deve ter cuidado para sincronizar essa operação com seu thread de agendamento. Libere a fila de agendamento e descarte os exemplos antigos antes de alocar novas superfícies.

### <a name="end-of-stream"></a>Fim do fluxo

Quando cada fluxo de entrada no EVR termina, o EVR envia uma mensagem de **MFVP_MESSAGE_ENDOFSTREAM** para o apresentador. No momento em que você recebe a mensagem, no entanto, pode haver alguns quadros de vídeo restantes para serem processados. Antes de responder à mensagem de fim de fluxo, você deve drenar toda a saída do mixer e apresentar todos os quadros restantes. Depois que o último quadro for apresentado, envie um evento de **EC_COMPLETE** para o EVR.

O exemplo a seguir mostra um método que envia o evento **EC_COMPLETE** se várias condições forem atendidas. Caso contrário, ele retornará S_OK sem enviar o evento:


```C++
HRESULT EVRCustomPresenter::CheckEndOfStream()
{
    if (!m_bEndStreaming)
    {
        // The EVR did not send the MFVP_MESSAGE_ENDOFSTREAM message.
        return S_OK;
    }

    if (m_bSampleNotify)
    {
        // The mixer still has input.
        return S_OK;
    }

    if (m_SamplePool.AreSamplesPending())
    {
        // Samples are still scheduled for rendering.
        return S_OK;
    }

    // Everything is complete. Now we can tell the EVR that we are done.
    NotifyEvent(EC_COMPLETE, (LONG_PTR)S_OK, 0);
    m_bEndStreaming = FALSE;
    return S_OK;
}
```



Esse método verifica os seguintes Estados:

-   Se a variável de *m_fSampleNotify* for **true**, significa que o mixer tem um ou mais quadros que ainda não foram processados. (Para obter detalhes, consulte [processamento de saída](#processing-output).)
-   A variável *m_fEndStreaming* é um sinalizador booliano cujo valor inicial é **false**. O apresentador define o sinalizador como **true** quando o EVR envia a mensagem de **MFVP_MESSAGE_ENDOFSTREAM** .
-   Presume-se que o `AreSamplesPending` método retorne **true** , desde que um ou mais quadros estejam aguardando na fila agendada.

No método [**IMFVideoPresenter::P rocessmessage**](/windows/desktop/api/evr/nf-evr-imfvideopresenter-processmessage) , defina *m_fEndStreaming* como **true** e chame `CheckEndOfStream` quando EVR enviar a mensagem de **MFVP_MESSAGE_ENDOFSTREAM** :


```C++
HRESULT EVRCustomPresenter::ProcessMessage(
    MFVP_MESSAGE_TYPE eMessage,
    ULONG_PTR ulParam
    )
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_ObjectLock);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    switch (eMessage)
    {
    // Flush all pending samples.
    case MFVP_MESSAGE_FLUSH:
        hr = Flush();
        break;

    // Renegotiate the media type with the mixer.
    case MFVP_MESSAGE_INVALIDATEMEDIATYPE:
        hr = RenegotiateMediaType();
        break;

    // The mixer received a new input sample.
    case MFVP_MESSAGE_PROCESSINPUTNOTIFY:
        hr = ProcessInputNotify();
        break;

    // Streaming is about to start.
    case MFVP_MESSAGE_BEGINSTREAMING:
        hr = BeginStreaming();
        break;

    // Streaming has ended. (The EVR has stopped.)
    case MFVP_MESSAGE_ENDSTREAMING:
        hr = EndStreaming();
        break;

    // All input streams have ended.
    case MFVP_MESSAGE_ENDOFSTREAM:
        // Set the EOS flag.
        m_bEndStreaming = TRUE;
        // Check if it's time to send the EC_COMPLETE event to the EVR.
        hr = CheckEndOfStream();
        break;

    // Frame-stepping is starting.
    case MFVP_MESSAGE_STEP:
        hr = PrepareFrameStep(LODWORD(ulParam));
        break;

    // Cancels frame-stepping.
    case MFVP_MESSAGE_CANCELSTEP:
        hr = CancelFrameStep();
        break;

    default:
        hr = E_INVALIDARG; // Unknown message. This case should never occur.
        break;
    }

done:
    LeaveCriticalSection(&m_ObjectLock);
    return hr;
}
```



Além disso, chame `CheckEndOfStream` se o método [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) do mixer retornar **MF_E_TRANSFORM_NEED_MORE_INPUT**. Esse código de erro indica que o mixer não tem mais exemplos de entrada (consulte [processamento de saída](#processing-output)).

## <a name="frame-stepping"></a>Revisão do quadro

O EVR foi projetado para dar suporte à depuração de quadro no DirectShow e na depuração em Media Foundation. Depuração e depuração de quadros são conceitualmente semelhantes. Em ambos os casos, o aplicativo solicita um quadro de vídeo por vez. Internamente, o apresentador usa o mesmo mecanismo para implementar os dois recursos.

A revisão do quadro no DirectShow funciona da seguinte maneira:

-   O aplicativo chama [**IVideoFrameStep:: Step**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-step). O número de etapas é fornecido no parâmetro *dwSteps* . O EVR envia uma mensagem de **MFVP_MESSAGE_STEP** para o apresentador, onde o parâmetro de mensagem (*ulParam*) é o número de etapas.
-   Se o aplicativo chamar [**IVideoFrameStep:: CancelStep**](/windows/win32/api/strmif/nf-strmif-ivideoframestep-cancelstep) ou alterar o estado do grafo (em execução, em pausa ou parado), o EVR enviará uma mensagem de **MFVP_MESSAGE_CANCELSTEP** .

A depuração no Media Foundation funciona da seguinte maneira:

-   O aplicativo define a taxa de reprodução como zero chamando [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate).
-   Para renderizar um novo quadro, o aplicativo chama [**IMFMediaSession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) com a posição desejada. O EVR envia uma mensagem de **MFVP_MESSAGE_STEP** com *ulParam* igual a 1.
-   Para interromper a depuração, o aplicativo define a taxa de reprodução para um valor diferente de zero. O EVR envia a mensagem de **MFVP_MESSAGE_CANCELSTEP** .

Depois de receber **a MFVP_MESSAGE_STEP,** o apresentador aguarda a chegada do quadro de destino. Se o número de etapas for *N*, o apresentador descartará as próximas amostras (*N* - 1) e apresentará a *amostra N.* Quando o apresentador conclui a etapa do quadro, ele envia um [**evento EC_STEP_COMPLETE**](../directshow/ec-step-complete.md) para o EVR com *lParam1* definido como **FALSE.** Além disso, se a taxa de reprodução for zero, o apresentador enviará um [**EC_SCRUB_TIME**](../directshow/ec-scrub-time.md) evento. Se o EVR cancelar a etapa do quadro enquanto uma operação de etapa de quadro ainda estiver pendente, o apresentador enviará um evento **EC_STEP_COMPLETE** com *lParam1* definido como **TRUE.**

O aplicativo pode enquadrar a etapa ou limpar  várias vezes, portanto, o apresentador pode receber várias mensagens MFVP_MESSAGE_STEP antes de receber uma **MFVP_MESSAGE_CANCELSTEP** mensagem. Além disso, o apresentador pode receber a **mensagem MFVP_MESSAGE_STEP** antes que o relógio seja iniciado ou enquanto o relógio estiver em execução.

### <a name="implementing-frame-stepping"></a>Implementando a execução de quadros

Esta seção descreve um algoritmo para implementar a execução de quadros. O algoritmo de passo a passo do quadro usa as seguintes variáveis:

-   *step_count*. Um inteiro sem sinal que especifica o número de etapas na operação de etapa de quadro atual.
-   *step_queue*. Uma fila de [**ponteiros IMFSample.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)
-   *step_state*. A qualquer momento, o apresentador pode estar em um dos seguintes estados em relação à revisão de quadro: 

    | Estado         | Descrição                                                                                                                                                                                                     |
    |---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | NOT_STEPPING | Não enquadrar em passo.                                                                                                                                                                                             |
    | AGUARDANDO       | O apresentador recebeu a mensagem **MFVP_MESSAGE_STEP,** mas o relógio não foi iniciado.                                                                                                                  |
    | PENDING       | O apresentador recebeu a mensagem **MFVP_MESSAGE_STEP** e o relógio foi iniciado, mas o apresentador está aguardando para receber o quadro de destino.                                                             |
    | Agendada     | O apresentador recebeu o quadro de destino e o agendou para apresentação, mas o quadro não foi apresentado.                                                                                        |
    | Completa      | O apresentador apresentou o quadro de destino e enviou o evento [**EC_STEP_COMPLETE,**](../directshow/ec-step-complete.md) e está aguardando o próximo MFVP_MESSAGE_STEP **ou** **MFVP_MESSAGE_CANCELSTEP** mensagem. |

    

     

    Esses estados são independentes dos estados de apresentador listados na seção [Estados do Apresentador](#presenter-states).

Os procedimentos a seguir são definidos para o algoritmo frame-stepping:

Procedimento PrepareFrameStep

1.  Incrementar *step_count*.
2.  De *step_state* como WAITING.
3.  Se o relógio estiver em execução, chame StartFrameStep.

Procedimento StartFrameStep

1.  Se *step_state* for IGUAL A ESPERA, *de* step_state como PENDENTE. Para cada exemplo no *step_queue*, chame DeliverFrameStepSample.
2.  Se *step_state* for igual NOT_STEPPING, remova todos os exemplos do step_queue *e* agende-os para apresentação.

Procedimento CompleteFrameStep

1.  De *step_state* como COMPLETE.
2.  Envie o EC_STEP_COMPLETE com *lParam1*  =  **FALSE.**
3.  Se a taxa de relógio for zero, envie o **evento EC_SCRUB_TIME** com a hora de exemplo.

Procedimento DeliverFrameStepSample

1.  Se a taxa de relógio for zero e o tempo *de duração* da amostra de tempo de  +    <  *exemplo for* zero, descarte o exemplo. Sair.
2.  Se *step_state* igual a SCHEDULED ou COMPLETE, adicione o exemplo a *step_queue*. Sair.
3.  Decrement *step_count*.
4.  Se *step_count* > 0, descarte o exemplo. Sair.
5.  Se *step_state* for IGUAL a WAITING, adicione o exemplo a *step_queue*. Sair.
6.  Agende o exemplo para apresentação.
7.  De *step_state* como SCHEDULED.

Procedimento CancelFrameStep

1.  Definir *step_state* como NOT_STEPPING
2.  Redefinir *step_count* para zero.
3.  Se o valor anterior de *step_state* era WAITING, PENDING ou SCHEDULED, envie EC_STEP_COMPLETE com *lParam1*  =  **TRUE.**

Chame estes procedimentos da seguinte forma:



| Mensagem ou método do apresentador                                                   | Procedimento           |
|-------------------------------------------------------------------------------|---------------------|
| **MFVP_MESSAGE_STEP** mensagem                                               | `PrepareFrameStep`  |
| **MFVP_MESSAGE_STEP** mensagem                                               | `CancelStep`        |
| [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart)     | `StartFrameStep`    |
| [**IMFClockStateSink::OnClockRestart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart) | `StartFrameStep`    |
| [**Retorno de chamada IMFTrackedSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)                         | `CompleteFrameStep` |
| [**IMFClockStateSink::OnClockStop**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstop)       | `CancelFrameStep`   |
| [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) | `CancelFrameStep`   |



 

O gráfico de fluxo a seguir mostra os procedimentos de passo a passo do quadro.

![fluxograma mostrando caminhos que começam com a etapa de mensagem mfvp e o processo de mensagem \- \- mfvpinputnotify e \- \- terminam em "state = complete"](images/d9baaa67-a9b1-4e27-9a32-08a45b0677d3.gif)

## <a name="setting-the-presenter-on-the-evr"></a>Definindo o apresentador no EVR

Depois de implementar o apresentador, a próxima etapa é configurar o EVR para usá-lo.

### <a name="setting-the-presenter-in-directshow"></a>Definindo o apresentador no DirectShow

Em um aplicativo DirectShow, de definir o apresentador no EVR da seguinte forma:

1.  Crie o filtro EVR chamando **CoCreateInstance.** O CLSID é **CLSID_EnhancedVideoRenderer**.
2.  Adicione o EVR ao grafo de filtro.
3.  Crie uma instância do seu apresentador. O apresentador pode dar suporte à criação de objeto COM padrão **por meio de IClassFactory,** mas isso não é obrigatório.
4.  Consulte o filtro EVR para a interface [**IMFVideoRenderer.**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
5.  Chame [**IMFVideoRenderer::InitializeRenderer.**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)

### <a name="setting-the-presenter-in-media-foundation"></a>Definindo o apresentador em Media Foundation

No Media Foundation, você tem várias opções, dependendo se você cria o sink de mídia EVR ou o objeto de ativação EVR. Para obter mais informações sobre objetos de ativação, consulte [Objetos de ativação](activation-objects.md).

Para o sink de mídia EVR, faça o seguinte:

1.  Chame [**MFCreateVideoRenderer para**](/windows/desktop/api/evr/nc-evr-mfcreatevideorenderer) criar o sink de mídia.
2.  Crie uma instância do seu apresentador.
3.  Consulte o sink de mídia EVR para a interface [**IMFVideoRenderer.**](/windows/desktop/api/evr/nn-evr-imfvideorenderer)
4.  Chame [**IMFVideoRenderer::InitializeRenderer.**](/windows/desktop/api/evr/nf-evr-imfvideorenderer-initializerenderer)

Para o objeto de ativação EVR, faça o seguinte:

1.  Chame [**MFCreateVideoRendererActivate para**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) criar o objeto de ativação.
2.  De definir um dos seguintes atributos no objeto de ativação: 

    | Atributo                                                                                                         | Descrição                                                                                                                                                                                                                               |
    |-------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_ACTIVATE**](mf-activate-custom-video-presenter-activate-attribute.md) | Ponteiro para um objeto de ativação para o apresentador.<br/> Com esse sinalizador, você deve fornecer um objeto de ativação para o seu apresentador. O objeto de ativação deve implementar a interface [**IMFActivate.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)<br/> |
    | [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md)       | CLSID do apresentador.<br/> Com esse sinalizador, o apresentador deve dar suporte à criação de objeto COM padrão por **meio de IClassFactory**.<br/>                                                                                         |

    

     

3.  Opcionalmente, de definir o [**MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS**](mf-activate-custom-video-presenter-flags-attribute.md) no objeto de ativação.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de vídeo aprimorada](enhanced-video-renderer.md)
</dt> <dt>

[Exemplo de EVRPresenter](evrpresenter-sample.md)
</dt> </dl>

 

 
