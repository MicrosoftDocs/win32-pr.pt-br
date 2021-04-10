---
description: Este tópico faz uma análise detalhada do exemplo de SDK de origem de mídia MPEG-1.
ms.assetid: d392f30c-c963-4eb3-add2-1bb986919c0b
title: 'Estudo de caso: fonte de mídia MPEG-1'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87e1f72cc6ae6df119439bdae1942732bf8d2fa2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104011918"
---
# <a name="case-study-mpeg-1-media-source"></a>Estudo de caso: fonte de mídia MPEG-1

No Microsoft Media Foundation, o objeto que apresenta os dados de mídia no pipeline de dados é chamado de *fonte de mídia*. Este tópico faz uma análise detalhada do exemplo de SDK de [origem de mídia MPEG-1](mpeg1source-sample.md) .

-   [Pré-requisitos](#prerequisites)
-   [Classes C++ usadas na origem MPEG-1](#c-classes-used-in-the-mpeg-1-source)
-   [Manipulador de fluxo de bytes](#byte-stream-handler)
-   [Descritor de apresentação](#presentation-descriptor)
-   [Estados de streaming](#streaming-states)
    -   [Iniciar](#start)
    -   [Pausar](#pause)
    -   [Parar](#stop)
-   [Solicitações de amostra](#sample-requests)
-   [Fim do fluxo](#end-of-stream)
-   [Operações assíncronas](#asynchronous-operations)
    -   [Fila de operações](#operation-queue)
-   [Tópicos relacionados](#related-topics)

## <a name="prerequisites"></a>Pré-requisitos

Antes de ler este tópico, você deve entender os seguintes conceitos de Media Foundation:

-   [Modelo de objeto de origem de mídia](media-source-object-model.md)
-   [Métodos de retorno de chamada assíncrono](asynchronous-callback-methods.md).
-   [Filas de trabalho](work-queues.md)
-   [Geradores de eventos de mídia](media-event-generators.md)
-   [Buffers de mídia](media-buffers.md)
-   [Amostras de mídia](media-samples.md)
-   [Tipos de mídia](media-types.md)

Você também deve ter um entendimento básico da arquitetura de Media Foundation, particularmente a função das fontes de mídia no pipeline. (Para obter mais informações, consulte [fontes de mídia](media-sources.md).)

Além disso, talvez você queira ler o tópico [escrevendo uma fonte de mídia personalizada](writing-a-custom-media-source.md), que fornece uma visão geral mais geral das etapas descritas aqui.

Este tópico não reproduz todo o código do exemplo do SDK, porque o exemplo é bastante grande.

## <a name="c-classes-used-in-the-mpeg-1-source"></a>Classes C++ usadas na origem MPEG-1

A fonte MPEG-1 de exemplo é implementada com as seguintes classes C++:

-   `MPEG1ByteStreamHandler`. Implementa o manipulador de fluxo de bytes para a origem da mídia. Dado um fluxo de bytes, o manipulador de fluxo de bytes cria uma instância da origem.
-   `MPEG1Source`. Implementa a origem da mídia.
-   `MPEG1Stream`. Implementa os objetos de fluxo de mídia. A origem de mídia cria um `MPEG1Stream` objeto para cada fluxo de áudio ou vídeo no fragmentado MPEG-1.
-   `Parser`. Analisa o fragmentado MPEG-1. Para a maior parte, os detalhes dessa classe não são relevantes para as APIs de Media Foundation.
-   SourceOp, OpQueue: essas duas classes gerenciam operações assíncronas na origem da mídia. (Consulte [operações assíncronas](#asynchronous-operations)).

Outras classes auxiliares diversas são descritas posteriormente no tópico.

## <a name="byte-stream-handler"></a>Manipulador de Byte-Stream

O manipulador de *fluxo de bytes* é o objeto que cria a origem de mídia. O manipulador de fluxo de bytes é criado pelo resolvedor de origem; os aplicativos não interagem diretamente com o manipulador de fluxo de bytes. O resolvedor de origem descobre o manipulador de fluxo de bytes examinando o registro. O manipulador é registrado por extensão de nome de arquivo ou tipo MIME. Para a origem MPEG-1, o manipulador de fluxo de bytes é registrado para a extensão de nome de arquivo ". mpg".

> [!Note]  
> Se você quiser dar suporte a esquemas de URL personalizados, também poderá escrever um *manipulador de esquema*. A fonte MPEG-1 foi projetada para arquivos locais e Media Foundation já fornece um manipulador de esquema para URLs "file://".

 

O manipulador byte-Stream implementa a interface [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) . Essa interface tem dois métodos mais importantes que devem ser implementados:

-   [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject). Inicia uma operação assíncrona para criar a origem da mídia.
-   [](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject). Conclui a chamada assíncrona.

Dois outros métodos são opcionais e não são implementados no exemplo do SDK:

-   [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation). Cancela o método [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) . Esse método é útil para uma fonte de rede que pode ter uma alta latência na inicialização.
-   [**GetMaxNumberOfBytesRequiredForResolution**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-getmaxnumberofbytesrequiredforresolution). Obtém o número máximo de bytes que o manipulador lerá do fluxo de origem. Implemente esse método se você souber a quantidade de dados que o manipulador de fluxo de bytes antes de poder criar a origem de mídia. Caso contrário, basta retornar **E \_ NOTIMPL**.

Aqui está a implementação do método [**BeginCreateObject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) :


```C++
HRESULT MPEG1ByteStreamHandler::BeginCreateObject(
        /* [in] */ IMFByteStream *pByteStream,
        /* [in] */ LPCWSTR pwszURL,
        /* [in] */ DWORD dwFlags,
        /* [in] */ IPropertyStore *pProps,
        /* [out] */ IUnknown **ppIUnknownCancelCookie,  // Can be NULL
        /* [in] */ IMFAsyncCallback *pCallback,
        /* [in] */ IUnknown *punkState                  // Can be NULL
        )
{
    if (pByteStream == NULL)
    {
        return E_POINTER;
    }

    if (pCallback == NULL)
    {
        return E_POINTER;
    }

    if ((dwFlags & MF_RESOLUTION_MEDIASOURCE) == 0)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFAsyncResult *pResult = NULL;
    MPEG1Source    *pSource = NULL;

    // Create an instance of the media source.
    hr = MPEG1Source::CreateInstance(&pSource);

    // Create a result object for the caller's async callback.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateAsyncResult(NULL, pCallback, punkState, &pResult);
    }

    // Start opening the source. This is an async operation.
    // When it completes, the source will invoke our callback
    // and then we will invoke the caller's callback.
    if (SUCCEEDED(hr))
    {
        hr = pSource->BeginOpen(pByteStream, this, NULL);
    }

    if (SUCCEEDED(hr))
    {
        if (ppIUnknownCancelCookie)
        {
            *ppIUnknownCancelCookie = NULL;
        }

        m_pSource = pSource;
        m_pSource->AddRef();

        m_pResult = pResult;
        m_pResult->AddRef();
    }

// cleanup
    SafeRelease(&pSource);
    SafeRelease(&pResult);
    return hr;
}
```



O método executa as seguintes etapas:

1.  Cria uma nova instância do objeto `MPEG1Source`.
2.  Crie um objeto de resultado assíncrono. Esse objeto é usado posteriormente para invocar o método de retorno de chamada do resolvedor de origem.
3.  Chama `MPEG1Source::BeginOpen` , um método assíncrono definido na `MPEG1Source` classe.
4.  Define *ppIUnknownCancelCookie* como **NULL**, que informa ao chamador que não há suporte para [**CancelObjectCreation**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-cancelobjectcreation) .

O `MPEG1Source::BeginOpen` método faz o trabalho real de ler o fluxo de bytes e inicializar o `MPEG1Source` objeto. Esse método não faz parte da API pública. Você pode definir qualquer mecanismo entre o manipulador e a fonte de mídia que atenda às suas necessidades. Colocar a maior parte da lógica na origem da mídia mantém o manipulador de fluxo de bytes relativamente simples.

Resumindo, `BeginOpen` o seguinte:

1.  Chama [**IMFByteStream:: GetCapabilities**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-getcapabilities) para verificar se o fluxo de bytes de origem é legível e pesquisável.
2.  Chama [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) para iniciar uma solicitação de e/s assíncrona.

O restante da inicialização ocorre de forma assíncrona. A origem da mídia lê dados suficientes do fluxo para analisar os cabeçalhos de sequência MPEG-1. Em seguida, ele cria um *descritor de apresentação*, que é o objeto usado para descrever os fluxos de áudio e vídeo no arquivo. (Para obter mais informações, consulte [descritor de apresentação](#presentation-descriptor).) Quando a `BeginOpen` operação é concluída, o manipulador de fluxo de bytes invoca o método de retorno de chamada do resolvedor de origem. Nesse ponto, o resolvedor de origem chama [**IMFByteStreamHandler:: Endcreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-endcreateobject). O método **Endcreateobject** retorna o status da operação.


```C++
HRESULT MPEG1ByteStreamHandler::EndCreateObject(
        /* [in] */ IMFAsyncResult *pResult,
        /* [out] */ MF_OBJECT_TYPE *pObjectType,
        /* [out] */ IUnknown **ppObject)
{
    if (pResult == NULL || pObjectType == NULL || ppObject == NULL)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    *pObjectType = MF_OBJECT_INVALID;
    *ppObject = NULL;

    hr = pResult->GetStatus();

    if (SUCCEEDED(hr))
    {
        *pObjectType = MF_OBJECT_MEDIASOURCE;

        assert(m_pSource != NULL);

        hr = m_pSource->QueryInterface(IID_PPV_ARGS(ppObject));
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pResult);
    return hr;
}
```



Se ocorrer um erro a qualquer momento durante esse processo, o retorno de chamada será invocado com um código de status de erro.

## <a name="presentation-descriptor"></a>Descritor de apresentação

O descritor de apresentação descreve o conteúdo do arquivo MPEG-1, incluindo as seguintes informações:

-   O número de fluxos.
-   O formato de cada fluxo.
-   Identificadores de fluxo.
-   O status de seleção de cada fluxo (selecionado ou desmarcado).

Em termos da arquitetura de Media Foundation, o descritor de apresentação contém um ou mais descritores de *fluxo*. Cada descritor de fluxo contém um *manipulador de tipo de mídia*, que é usado para obter ou definir tipos de mídia no fluxo. Media Foundation fornece implementações de estoque para o descritor de apresentação e o descritor de fluxo; Eles são adequados para a maioria das fontes de mídia.

Para criar um descritor de apresentação, execute as seguintes etapas:

1.  Para cada fluxo:
    1.  Forneça uma ID de fluxo e uma matriz de tipos de mídia possíveis. Se o fluxo der suporte a mais de um tipo de mídia, ordene a lista de tipos de mídia por preferência, se houver. (Coloque o tipo ideal primeiro e o tipo menos ideal por último.)
    2.  Chame [**MFCreateStreamDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatestreamdescriptor) para criar o descritor de fluxo.
    3.  Chame [**IMFStreamDescriptor:: GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) no descritor de fluxo recém-criado.
    4.  Chame [**IMFMediaTypeHandler:: SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) para definir o formato padrão para o fluxo. Se houver mais de um tipo de mídia, você geralmente deve definir o primeiro tipo na lista.
2.  Chame [**MFCreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) e transmita a matriz de ponteiros de descritor de fluxo.
3.  Para cada fluxo, chame [**IMFPresentationDescriptor:: SelectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-selectstream) ou [**DeselectStream**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-deselectstream) para definir o estado de seleção padrão. Se houver mais de um fluxo do mesmo tipo (áudio ou vídeo), somente um deverá ser selecionado por padrão.

O `MPEG1Source` objeto cria o descritor de apresentação em seu `InitPresentationDescriptor` método:


```C++
HRESULT MPEG1Source::InitPresentationDescriptor()
{
    HRESULT hr = S_OK;
    DWORD cStreams = 0;

    assert(m_pPresentationDescriptor == NULL);
    assert(m_state == STATE_OPENING);

    if (m_pHeader == NULL)
    {
        return E_FAIL;
    }

    // Get the number of streams, as declared in the MPEG-1 header, skipping
    // any streams with an unsupported format.
    for (DWORD i = 0; i < m_pHeader->cStreams; i++)
    {
        if (IsStreamTypeSupported(m_pHeader->streams[i].type))
        {
            cStreams++;
        }
    }

    // How many streams do we actually have?
    if (cStreams > m_streams.GetCount())
    {
        // Keep reading data until we have seen a packet for each stream.
        return S_OK;
    }

    // We should never create a stream we don't support.
    assert(cStreams == m_streams.GetCount());

    // Ready to create the presentation descriptor.

    // Create an array of IMFStreamDescriptor pointers.
    IMFStreamDescriptor **ppSD =
            new (std::nothrow) IMFStreamDescriptor*[cStreams];

    if (ppSD == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }

    ZeroMemory(ppSD, cStreams * sizeof(IMFStreamDescriptor*));

    // Fill the array by getting the stream descriptors from the streams.
    for (DWORD i = 0; i < cStreams; i++)
    {
        hr = m_streams[i]->GetStreamDescriptor(&ppSD[i]);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Create the presentation descriptor.
    hr = MFCreatePresentationDescriptor(cStreams, ppSD,
        &m_pPresentationDescriptor);

    if (FAILED(hr))
    {
        goto done;
    }

    // Select the first video stream (if any).
    for (DWORD i = 0; i < cStreams; i++)
    {
        GUID majorType = GUID_NULL;

        hr = GetStreamMajorType(ppSD[i], &majorType);
        if (FAILED(hr))
        {
            goto done;
        }

        if (majorType == MFMediaType_Video)
        {
            hr = m_pPresentationDescriptor->SelectStream(i);
            if (FAILED(hr))
            {
                goto done;
            }
            break;
        }
    }

    // Switch state from "opening" to stopped.
    m_state = STATE_STOPPED;

    // Invoke the async callback to complete the BeginOpen operation.
    hr = CompleteOpen(S_OK);

done:
    // clean up:
    if (ppSD)
    {
        for (DWORD i = 0; i < cStreams; i++)
        {
            SafeRelease(&ppSD[i]);
        }
        delete [] ppSD;
    }
    return hr;
}
```



O aplicativo obtém o descritor de apresentação chamando [**IMFMediaSource:: CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor). Esse método cria uma cópia superficial do descritor de apresentação chamando [**IMFPresentationDescriptor:: clone**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-clone). (A cópia contém ponteiros para os descritores de fluxo originais.) O aplicativo pode usar o descritor de apresentação para definir o tipo de mídia, selecionar um fluxo ou anular a seleção de um fluxo.

Opcionalmente, os descritores de apresentação e os descritores de fluxo podem conter atributos que fornecem informações adicionais sobre a origem. Para obter uma lista desses atributos, consulte os seguintes tópicos:

-   [Atributos do descritor de apresentação](presentation-descriptor-attributes.md)
-   [Atributos do descritor de fluxo](stream-descriptor-attributes.md)

Um atributo merece menção especial: o atributo de [**\_ \_ duração de PD de MF**](mf-pd-duration-attribute.md) contém a duração total da origem. Defina este atributo se souber a duração antecipada; por exemplo, a duração pode ser especificada nos cabeçalhos de arquivo, dependendo do formato de arquivo. O aplicativo pode exibir esse valor ou usá-lo para definir uma barra de progresso ou uma barra de busca.

## <a name="streaming-states"></a>Estados de streaming

Uma fonte de mídia define os seguintes Estados:



| Estado    | Descrição                                                                                                     |
|----------|-----------------------------------------------------------------------------------------------------------------|
| Iniciado  | A origem aceita e processa solicitações de exemplo.                                                               |
| Em Pausa   | A origem aceita solicitações de exemplo, mas não as processa. As solicitações são enfileiradas até que a origem seja iniciada. |
| Stopped. | A origem rejeita solicitações de exemplo.                                                                             |



 

### <a name="start"></a>Iniciar

O método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) inicia a origem da mídia. Ele usa os seguintes parâmetros:

-   Um descritor de apresentação.
-   Um GUID de formato temporal.
-   Uma posição inicial.

O aplicativo deve obter o descritor de apresentação chamando [**CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepresentationdescriptor) na origem. Não há um mecanismo definido para validar um descritor de apresentação. Se o aplicativo especificar o descritor de apresentação errado, os resultados serão indefinidos.

O GUID de formato de tempo especifica como interpretar a posição inicial. O formato padrão é de 100-nanossegundos (ns), indicado por GUID \_ NULL. Cada fonte de mídia deve dar suporte a unidades 100-NS. Opcionalmente, uma fonte pode dar suporte a outras unidades de tempo, como um número de quadro ou código de tempo. No entanto, não há uma maneira padrão de consultar uma fonte de mídia para a lista de formatos de hora com suporte.

A posição inicial é fornecida como um **PROPVARIANT**, permitindo tipos de dados diferentes, dependendo do formato de hora. Para 100-NS, o tipo **PROPVARIANT** é **VT \_ i8** ou **VT \_ vazio**. Se **VT \_ i8**, o **PROPVARIANT** conterá a posição inicial nas unidades 100-NS. O valor **VT \_ vazio** tem o significado especial "Iniciar na posição atual".

Implemente o método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) da seguinte maneira:

1.  Validar parâmetros e estado:
    -   Verifique se há parâmetros **nulos** .
    -   Verifique o GUID de formato de hora. Se o valor for inválido, retorne **MF \_ E \_ formato de \_ hora \_ sem suporte**.
    -   Verifique o tipo de dados do **PROPVARIANT** que contém a posição inicial.
    -   Validar a posição inicial. Se for inválido, retorne **MF \_ E \_ INVALIDREQUEST**.
    -   Se a origem tiver sido desligada, retorne o **MF \_ E o \_ desligamento**.
2.  Se nenhum erro ocorrer na etapa 1, enfileirar uma operação assíncrona. Tudo depois dessa etapa ocorre em um thread de fila de trabalho.
3.  Para cada fluxo:
    1.  Verifique se o fluxo já está ativo de uma solicitação de [**início**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) anterior.
    2.  Chame [**IMFPresentationDescriptor:: GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) para verificar se o aplicativo selecionou ou desselecionou o fluxo.
    3.  Se um fluxo selecionado anteriormente agora estiver desmarcado, libere quaisquer amostras não entregues para esse fluxo.
    4.  Se o fluxo estiver ativo, a origem da mídia (não o fluxo) enviará um dos seguintes eventos:
        -   Ele envia [MEUpdatedStream](meupdatedstream.md) se o fluxo estava ativo anteriormente.
        -   Caso contrário, ele envia [MENewStream](menewstream.md).

        Para ambos os eventos, os dados do evento são o ponteiro [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) para o fluxo.
    5.  Se a origem estiver reiniciando no estado pausado, pode haver solicitações de exemplo pendentes. Nesse caso, entregue-os agora.
    6.  Se a origem estiver buscando uma nova posição, cada objeto de fluxo enviará um evento [MEStreamSeeked](mestreamseeked.md) . Caso contrário, cada fluxo envia um evento [MEStreamStarted](mestreamstarted.md) .
4.  Se a origem estiver buscando uma nova posição, a origem da mídia enviará um evento [MESourceSeeked](mesourceseeked.md) . Caso contrário, ele envia um evento [MESourceStarted](mesourcestarted.md) .

Se ocorrer um erro a qualquer momento após a etapa 2, a origem enviará um evento [MESourceStarted](mesourcestarted.md) com um código de erro. Isso alerta o aplicativo de que o método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) falhou de forma assíncrona.

O código a seguir mostra as etapas 1 a 2:


```C++
HRESULT MPEG1Source::Start(
        IMFPresentationDescriptor* pPresentationDescriptor,
        const GUID* pguidTimeFormat,
        const PROPVARIANT* pvarStartPos
    )
{

    HRESULT hr = S_OK;
    SourceOp *pAsyncOp = NULL;

    // Check parameters.

    // Start position and presentation descriptor cannot be NULL.
    if (pvarStartPos == NULL || pPresentationDescriptor == NULL)
    {
        return E_INVALIDARG;
    }

    // Check the time format.
    if ((pguidTimeFormat != NULL) && (*pguidTimeFormat != GUID_NULL))
    {
        // Unrecognized time format GUID.
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    // Check the data type of the start position.
    if ((pvarStartPos->vt != VT_I8) && (pvarStartPos->vt != VT_EMPTY))
    {
        return MF_E_UNSUPPORTED_TIME_FORMAT;
    }

    EnterCriticalSection(&m_critSec);

    // Check if this is a seek request. This sample does not support seeking.

    if (pvarStartPos->vt == VT_I8)
    {
        // If the current state is STOPPED, then position 0 is valid.
        // Otherwise, the start position must be VT_EMPTY (current position).

        if ((m_state != STATE_STOPPED) || (pvarStartPos->hVal.QuadPart != 0))
        {
            hr = MF_E_INVALIDREQUEST;
            goto done;
        }
    }

    // Fail if the source is shut down.
    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    // Fail if the source was not initialized yet.
    hr = IsInitialized();
    if (FAILED(hr))
    {
        goto done;
    }

    // Perform a basic check on the caller's presentation descriptor.
    hr = ValidatePresentationDescriptor(pPresentationDescriptor);
    if (FAILED(hr))
    {
        goto done;
    }

    // The operation looks OK. Complete the operation asynchronously.
    hr = SourceOp::CreateStartOp(pPresentationDescriptor, &pAsyncOp);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAsyncOp->SetData(*pvarStartPos);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = QueueOperation(pAsyncOp);

done:
    SafeRelease(&pAsyncOp);
    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



As etapas restantes são mostradas no exemplo a seguir:


```C++
HRESULT MPEG1Source::DoStart(StartOp *pOp)
{
    assert(pOp->Op() == SourceOp::OP_START);

    IMFPresentationDescriptor *pPD = NULL;
    IMFMediaEvent  *pEvent = NULL;

    HRESULT     hr = S_OK;
    LONGLONG    llStartOffset = 0;
    BOOL        bRestartFromCurrentPosition = FALSE;
    BOOL        bSentEvents = FALSE;

    hr = BeginAsyncOp(pOp);

    // Get the presentation descriptor from the SourceOp object.
    // This is the PD that the caller passed into the Start() method.
    // The PD has already been validated.
    if (SUCCEEDED(hr))
    {
        hr = pOp->GetPresentationDescriptor(&pPD);
    }

    // Because this sample does not support seeking, the start
    // position must be 0 (from stopped) or "current position."

    // If the sample supported seeking, we would need to get the
    // start position from the PROPVARIANT data contained in pOp.

    if (SUCCEEDED(hr))
    {
        // Select/deselect streams, based on what the caller set in the PD.
        // This method also sends the MENewStream/MEUpdatedStream events.
        hr = SelectStreams(pPD, pOp->Data());
    }

    if (SUCCEEDED(hr))
    {
        m_state = STATE_STARTED;

        // Queue the "started" event. The event data is the start position.
        hr = m_pEventQueue->QueueEventParamVar(
            MESourceStarted,
            GUID_NULL,
            S_OK,
            &pOp->Data()
            );
    }

    if (FAILED(hr))
    {
        // Failure. Send the error code to the application.

        // Note: It's possible that QueueEvent itself failed, in which case it
        // is likely to fail again. But there is no good way to recover in
        // that case.

        (void)m_pEventQueue->QueueEventParamVar(
            MESourceStarted, GUID_NULL, hr, NULL);
    }

    CompleteAsyncOp(pOp);

    SafeRelease(&pEvent);
    SafeRelease(&pPD);
    return hr;
}
```



### <a name="pause"></a>Pausar

O método [**IMFMediaSource::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) faz uma pausa na origem da mídia. Implemente esse método da seguinte maneira:

1.  Enfileirar uma operação assíncrona.
2.  Cada fluxo ativo envia um evento [MEStreamPaused](mestreampaused.md) .
3.  A origem de mídia envia um evento [MESourcePaused](mesourcepaused.md) .

Enquanto está em pausa, as filas de origem são solicitações de amostra sem processá-las. (Consulte [exemplos de solicitações](#sample-requests).)

### <a name="stop"></a>Stop

O método [**IMFMediaSource:: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) interrompe a origem da mídia. Implemente esse método da seguinte maneira:

1.  Enfileirar uma operação assíncrona.
2.  Cada fluxo ativo envia um evento [MEStreamStopped](mestreamstopped.md) .
3.  Limpe todas as amostras em fila e as solicitações de exemplo.
4.  A origem de mídia envia um evento [MESourceStopped](mesourcestopped.md) .

Enquanto é interrompido, a origem rejeita todas as solicitações de exemplos.

Se a origem for interrompida enquanto uma solicitação de e/s estiver em andamento, a solicitação de e/s poderá ser concluída depois que a origem entrar no estado parado. Nesse caso, a origem deve descartar o resultado dessa solicitação de e/s.

## <a name="sample-requests"></a>Solicitações de Amostra

Media Foundation usar um modelo de *pull* , no qual o pipeline solicita amostras da origem de mídia. Isso difere do modelo usado pelo DirectShow, no qual as fontes "enviam" exemplos.

Para solicitar um novo exemplo, o pipeline de Media Foundation chama [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample). Esse método usa um ponteiro **IUnknown** que representa um objeto de *token* . A implementação do objeto de token é até o chamador; Ele simplesmente fornece uma maneira para o chamador controlar as solicitações de exemplo. O parâmetro de token também pode ser **nulo**.

Supondo que a origem use solicitações de e/s assíncronas para ler dados, a geração de amostra não será sincronizada com solicitações de exemplo. Para sincronizar as solicitações de exemplo com a geração de exemplo, uma fonte de mídia faz o seguinte:

1.  Os tokens de solicitação são colocados em uma fila.
2.  Como os exemplos são gerados, eles são colocados em uma segunda fila.
3.  A origem da mídia conclui uma solicitação de exemplo, obtendo um token de solicitação da primeira fila e um exemplo da segunda fila.
4.  A origem de mídia envia um evento MEMediaSample. O evento contém um ponteiro para o exemplo, e o exemplo contém um ponteiro para o token.

O diagrama a seguir mostra a relação entre o evento [MEMediaSample](memediasample.md) , o exemplo e o token de solicitação.

![diagrama mostrando memediasample e uma fila de exemplo apontando para imfsample; imfsample e o ponto da fila de solicitação para IUnknown](images/mediasourceimpl01.png)

O exemplo de origem MPEG-1 implementa esse processo da seguinte maneira:

1.  O método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) coloca a solicitação em uma fila FIFO.
2.  À medida que as solicitações de e/s são concluídas, a origem da mídia cria novos exemplos e os coloca em uma segunda fila FIFO. (Essa fila tem um tamanho máximo, para impedir que a origem leia muito bem.)
3.  Sempre que ambas as filas tiverem pelo menos um item (uma solicitação e uma amostra), a origem da mídia concluirá a primeira solicitação da fila de solicitações enviando a primeira amostra da fila de exemplo.
4.  Para fornecer um exemplo, o objeto de fluxo (não o objeto de origem) envia um evento [MEMediaSample](memediasample.md) .
    -   Os dados do evento são um ponteiro para a interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) do exemplo.
    -   Se a solicitação incluir um token, anexe o token ao exemplo definindo o atributo de [**\_ token MFSampleExtension**](mfsampleextension-token-attribute.md) no exemplo.

Neste ponto, há três possibilidades:

-   Há outro exemplo na fila de exemplo, mas nenhuma solicitação correspondente.
-   Há uma solicitação, mas nenhuma amostra.
-   Ambas as filas estão vazias; Não há amostras e nenhuma solicitação.

Se a fila de exemplo estiver vazia, a origem verificará o fim do fluxo (consulte [fim do fluxo](#end-of-stream)). Caso contrário, ele iniciará outra solicitação de e/s para dados. Se ocorrer algum erro durante esse processo, o fluxo enviará um evento [MEError](meerror.md) .

O código a seguir implementa o método [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) :


```C++
HRESULT MPEG1Stream::RequestSample(IUnknown* pToken)
{
    HRESULT hr = S_OK;
    IMFMediaSource *pSource = NULL;

    // Hold the media source object's critical section.
    SourceLock lock(m_pSource);

    hr = CheckShutdown();
    if (FAILED(hr))
    {
        goto done;
    }

    if (m_state == STATE_STOPPED)
    {
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (!m_bActive)
    {
        // If the stream is not active, it should not get sample requests.
        hr = MF_E_INVALIDREQUEST;
        goto done;
    }

    if (m_bEOS && m_Samples.IsEmpty())
    {
        // This stream has already reached the end of the stream, and the
        // sample queue is empty.
        hr = MF_E_END_OF_STREAM;
        goto done;
    }

    hr = m_Requests.InsertBack(pToken);
    if (FAILED(hr))
    {
        goto done;
    }

    // Dispatch the request.
    hr = DispatchSamples();
    if (FAILED(hr))
    {
        goto done;
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        hr = m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }
    return hr;
}
```



O `DispatchSamples` método extrai amostras da fila de exemplo, corresponde a elas com solicitações de exemplo pendentes e enfileira eventos de [MEMediaSample](memediasample.md) :


```C++
HRESULT MPEG1Stream::DispatchSamples()
{
    HRESULT hr = S_OK;
    BOOL bNeedData = FALSE;
    BOOL bEOS = FALSE;

    SourceLock lock(m_pSource);

    // An I/O request can complete after the source is paused, stopped, or
    // shut down. Do not deliver samples unless the source is running.
    if (m_state != STATE_STARTED)
    {
        return S_OK;
    }

    IMFSample *pSample = NULL;
    IUnknown  *pToken = NULL;

    // Deliver as many samples as we can.
    while (!m_Samples.IsEmpty() && !m_Requests.IsEmpty())
    {
        // Pull the next sample from the queue.
        hr = m_Samples.RemoveFront(&pSample);
        if (FAILED(hr))
        {
            goto done;
        }

        // Pull the next request token from the queue. Tokens can be NULL.
        hr = m_Requests.RemoveFront(&pToken);
        if (FAILED(hr))
        {
            goto done;
        }

        if (pToken)
        {
            // Set the token on the sample.
            hr = pSample->SetUnknown(MFSampleExtension_Token, pToken);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        // Send an MEMediaSample event with the sample.
        hr = m_pEventQueue->QueueEventParamUnk(
            MEMediaSample, GUID_NULL, S_OK, pSample);

        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pSample);
        SafeRelease(&pToken);
    }

    if (m_Samples.IsEmpty() && m_bEOS)
    {
        // The sample queue is empty AND we have reached the end of the source
        // stream. Notify the pipeline by sending the end-of-stream event.

        hr = m_pEventQueue->QueueEventParamVar(
            MEEndOfStream, GUID_NULL, S_OK, NULL);

        if (FAILED(hr))
        {
            goto done;
        }

        // Notify the source. It will send the end-of-presentation event.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_END_OF_STREAM);
        if (FAILED(hr))
        {
            goto done;
        }
    }
    else if (NeedsData())
    {
        // The sample queue is empty; the request queue is not empty; and we
        // have not reached the end of the stream. Ask for more data.
        hr = m_pSource->QueueAsyncOperation(SourceOp::OP_REQUEST_DATA);
        if (FAILED(hr))
        {
            goto done;
        }
    }

done:
    if (FAILED(hr) && (m_state != STATE_SHUTDOWN))
    {
        // An error occurred. Send an MEError even from the source,
        // unless the source is already shut down.
        m_pSource->QueueEvent(MEError, GUID_NULL, hr, NULL);
    }

    SafeRelease(&pSample);
    SafeRelease(&pToken);
    return S_OK;
}
```



O `DispatchSamples` método é chamado nas seguintes circunstâncias:

-   Dentro do método [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .
-   Quando a origem da mídia é reiniciada a partir do estado em pausa.
-   Quando uma solicitação de e/s é concluída.

## <a name="end-of-stream"></a>Fim do fluxo

Quando um fluxo não tem mais dados, e todos os exemplos desse fluxo foram entregues, os objetos de fluxo enviam um evento [MEEndOfStream](meendofstream.md) .

Quando todos os fluxos ativos são concluídos, a origem da mídia envia um evento [MEEndOfPresentation](meendofpresentation.md) .

## <a name="asynchronous-operations"></a>Operações assíncronas

Talvez a parte mais difícil de escrever uma fonte de mídia esteja compreendendo o modelo assíncrono Media Foundation.

Todos os métodos em uma fonte de mídia que controlam o streaming são assíncronos. Em cada caso, o método faz alguma validação inicial, como verificar parâmetros. A origem, em seguida, distribui o restante do trabalho para uma fila de trabalho. Após a conclusão da operação, a origem da mídia envia um evento de volta para o chamador, por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) da fonte de mídia. Portanto, é importante entender as filas de trabalho.

Para colocar um item em uma fila de trabalho, você pode chamar [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) ou [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). A origem MPEG-1 acontece com o uso de **MFPutWorkItem**, mas as duas funções fazem a mesma coisa. A função **MFPutWorkItem** usa os seguintes parâmetros:

-   Um valor **DWORD** que identifica a fila de trabalho. Você pode criar uma fila de trabalho particular ou usar o **\_ padrão de fila de retorno de chamada \_ \_ MFASYNC**.
-   Um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . Essa interface de retorno de chamada é invocada para executar o trabalho.
-   Um objeto de estado opcional, que deve implementar **IUnknown**.

A fila de trabalho é atendida por um ou mais threads de trabalho que recebem continuamente o próximo item de trabalho da fila e invocam o método [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) da interface de retorno de chamada.

Não há garantia de que os itens de trabalho sejam executados na mesma ordem em que você os coloca na fila. Lembre-se de que mais de um thread pode atender à mesma fila de trabalho, portanto, [**invocar**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) chamadas pode se sobrepor ou ocorrer fora de ordem. Portanto, cabe à origem da mídia manter o estado interno correto, enviando itens da fila de trabalho na ordem correta. Somente quando a operação anterior for concluída, a origem iniciará a próxima operação.

Para representar operações pendentes, a origem MPEG-1 define uma classe chamada `SourceOp` :


```C++
// Represents a request for an asynchronous operation.

class SourceOp : public IUnknown
{
public:

    enum Operation
    {
        OP_START,
        OP_PAUSE,
        OP_STOP,
        OP_REQUEST_DATA,
        OP_END_OF_STREAM
    };

    static HRESULT CreateOp(Operation op, SourceOp **ppOp);
    static HRESULT CreateStartOp(IMFPresentationDescriptor *pPD, SourceOp **ppOp);

    // IUnknown
    STDMETHODIMP QueryInterface(REFIID iid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    SourceOp(Operation op);
    virtual ~SourceOp();

    HRESULT SetData(const PROPVARIANT& var);

    Operation Op() const { return m_op; }
    const PROPVARIANT& Data() { return m_data;}

protected:
    long        m_cRef;     // Reference count.
    Operation   m_op;
    PROPVARIANT m_data;     // Data for the operation.
};
```



A `Operation` enumeração identifica qual operação está pendente. A classe também contém um **PROPVARIANT** para transmitir quaisquer dados adicionais para a operação.

### <a name="operation-queue"></a>Fila de operações

Para serializar operações, a origem da mídia mantém uma fila de `SourceOp` objetos. Ele usa uma classe auxiliar para gerenciar a fila:


```C++
template <class OP_TYPE>
class OpQueue : public IUnknown
{
public:

    typedef ComPtrList<OP_TYPE>   OpList;

    HRESULT QueueOperation(OP_TYPE *pOp);

protected:

    HRESULT ProcessQueue();
    HRESULT ProcessQueueAsync(IMFAsyncResult *pResult);

    virtual HRESULT DispatchOperation(OP_TYPE *pOp) = 0;
    virtual HRESULT ValidateOperation(OP_TYPE *pOp) = 0;

    OpQueue(CRITICAL_SECTION& critsec)
        : m_OnProcessQueue(this, &OpQueue::ProcessQueueAsync),
          m_critsec(critsec)
    {
    }

    virtual ~OpQueue()
    {
    }

protected:
    OpList                  m_OpQueue;         // Queue of operations.
    CRITICAL_SECTION&       m_critsec;         // Protects the queue state.
    AsyncCallback<OpQueue>  m_OnProcessQueue;  // ProcessQueueAsync callback.
};
```



A `OpQueue` classe foi projetada para ser herdada pelo componente que executa itens de trabalho assíncronos. O parâmetro de modelo de *\_ tipo OP* é o tipo de objeto usado para representar itens de trabalho na fila — nesse caso, o *\_ tipo OP* será `SourceOp` . A `OpQueue` classe implementa os seguintes métodos:

-   `QueueOperation` coloca um novo item na fila.
-   `ProcessQueue` Despacha a próxima operação da fila. Esse método é assíncrono.
-   `ProcessQueueAsync` conclui o método assíncrono `ProcessQueue` .

Outros dois métodos devem ser implementados pela classe derivada:

-   `ValidateOperation` verifica se é válido executar uma operação especificada, considerando o estado atual da origem da mídia.
-   `DispatchOperation` executa o item de trabalho assíncrono.

A fila de operação é usada da seguinte maneira:

1.  O pipeline de Media Foundation chama um método assíncrono na origem da mídia, como [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).
2.  As chamadas de método assíncrono `QueueOperation` , que coloca a operação de [**inicialização**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) na fila e as chama `ProcessQueue` (na forma de um `SourceOp` objeto).
3.  `ProcessQueue` chama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem).
4.  O thread de fila de trabalho chama `ProcessQueueAsync` .
5.  O `ProcessQueueAsync` método chama `ValidateOperation` e `DispatchOperation` .

O código a seguir enfileira uma nova operação na fonte MPEG-1:


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::QueueOperation(OP_TYPE *pOp)
{
    HRESULT hr = S_OK;

    EnterCriticalSection(&m_critsec);

    hr = m_OpQueue.InsertBack(pOp);
    if (SUCCEEDED(hr))
    {
        hr = ProcessQueue();
    }

    LeaveCriticalSection(&m_critsec);
    return hr;
}
```



O código a seguir processa a fila:


```C++
template <class OP_TYPE>
HRESULT OpQueue<OP_TYPE>::ProcessQueue()
{
    HRESULT hr = S_OK;
    if (m_OpQueue.GetCount() > 0)
    {
        hr = MFPutWorkItem(
            MFASYNC_CALLBACK_QUEUE_STANDARD,    // Use the standard work queue.
            &m_OnProcessQueue,                  // Callback method.
            NULL                                // State object.
            );
    }
    return hr;
}
```



O `ValidateOperation` método verifica se a origem MPEG-1 pode enviar a próxima operação na fila. Se outra operação estiver em andamento, `ValidateOperation` retornará **MF \_ E não \_ aceitar**. Isso garante que o `DispatchOperation` não seja chamado enquanto houver outra operação pendente.


```C++
HRESULT MPEG1Source::ValidateOperation(SourceOp *pOp)
{
    if (m_pCurrentOp != NULL)
    {
        return MF_E_NOTACCEPTING;
    }
    return S_OK;
}
```



O método DispatchOperation alterna para o tipo de operação:


```C++
//-------------------------------------------------------------------
// DispatchOperation
//
// Performs the asynchronous operation indicated by pOp.
//
// NOTE:
// This method implements the pure-virtual OpQueue::DispatchOperation
// method. It is always called from a work-queue thread.
//-------------------------------------------------------------------

HRESULT MPEG1Source::DispatchOperation(SourceOp *pOp)
{
    EnterCriticalSection(&m_critSec);

    HRESULT hr = S_OK;

    if (m_state == STATE_SHUTDOWN)
    {
        LeaveCriticalSection(&m_critSec);

        return S_OK; // Already shut down, ignore the request.
    }

    switch (pOp->Op())
    {

    // IMFMediaSource methods:

    case SourceOp::OP_START:
        hr = DoStart((StartOp*)pOp);
        break;

    case SourceOp::OP_STOP:
        hr = DoStop(pOp);
        break;

    case SourceOp::OP_PAUSE:
        hr = DoPause(pOp);
        break;

    // Operations requested by the streams:

    case SourceOp::OP_REQUEST_DATA:
        hr = OnStreamRequestSample(pOp);
        break;

    case SourceOp::OP_END_OF_STREAM:
        hr = OnEndOfStream(pOp);
        break;

    default:
        hr = E_UNEXPECTED;
    }

    if (FAILED(hr))
    {
        StreamingError(hr);
    }

    LeaveCriticalSection(&m_critSec);
    return hr;
}
```



Para resumir:

1.  O pipeline chama um método assíncrono, como [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start).
2.  O método assíncrono chama `OpQueue::QueueOperation` , passando um ponteiro para um `SourceOp` objeto.
3.  O `QueueOperation` método coloca a operação na fila *m \_ OpQueue* e chama `OpQueue::ProcessQueue` .
4.  O `ProcessQueue` método chama [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem). A partir desse ponto, tudo acontece em um thread de fila de trabalho Media Foundation. O método assíncrono retorna ao chamador.
5.  O thread de fila de trabalho chama o `OpQueue::ProcessQueueAsync` método.
6.  O `ProcessQueueAsync` método chama `MPEG1Source:ValidateOperation` para validar a operação.
7.  O `ProcessQueueAsync` método chama `MPEG1Source::DispatchOperation` para processar a operação.

Há vários benefícios para esse design:

-   Os métodos são assíncronos, portanto, não bloqueiam o thread do aplicativo de chamada.
-   As operações são expedidas em um Media Foundation thread de fila de trabalho, que é compartilhado entre componentes de pipeline. Portanto, a origem da mídia não cria seu próprio thread, reduzindo o número total de threads que são criados.
-   A origem da mídia não é bloqueada enquanto aguarda a conclusão das operações. Isso reduz a chance de que uma fonte de mídia cause acidentalmente um deadlock e ajuda a reduzir a alternância de contexto.
-   A origem da mídia pode usar e/s assíncrona para ler o arquivo de origem (chamando [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread)). A origem da mídia não precisa ser bloqueada enquanto aguarda a conclusão da rotina de e/s.

Se você seguir o padrão mostrado no exemplo de SDK, poderá se concentrar nos detalhes específicos de sua fonte de mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fontes de mídia](media-sources.md)
</dt> <dt>

[Gravando uma fonte de mídia personalizada](writing-a-custom-media-source.md)
</dt> </dl>

 

 



