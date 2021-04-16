---
description: Processando dados no codificador
ms.assetid: 7be4c5e7-db2c-4063-8e5c-af6ffb861aa5
title: Processando dados no codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b7fedef50df61851408d084b511497eacd0288
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105765042"
---
# <a name="processing-data-in-the-encoder"></a><span data-ttu-id="71bca-103">Processando dados no codificador</span><span class="sxs-lookup"><span data-stu-id="71bca-103">Processing Data in the Encoder</span></span>

<span data-ttu-id="71bca-104">Depois de negociar o tipo de entrada e o tipo de saída para o MFT do codificador, conforme descrito em [negociação de tipo de mídia no codificador](media-type-negotiation-on-the-encoder.md), você pode iniciar o processamento de exemplos de dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="71bca-104">After you have negotiated the input type and output type for the encoder MFT, as described in [Media Type Negotiation on the Encoder](media-type-negotiation-on-the-encoder.md), you can start processing media data samples.</span></span> <span data-ttu-id="71bca-105">Os dados são passados na forma de amostras de mídia (interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ) e também recebidos da saída como amostras de mídia.</span><span class="sxs-lookup"><span data-stu-id="71bca-105">The data is passed in form of media samples ([**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface) and also received from the output as media samples.</span></span>

<span data-ttu-id="71bca-106">Antes de enviar dados para o codificador para processamento, você deve alocar um exemplo de mídia e adicionar um ou mais buffers de mídia que contenham dados de mídia que precisam ser codificados.</span><span class="sxs-lookup"><span data-stu-id="71bca-106">Before sending data to the encoder for processing, you must allocate a media sample and add one of more media buffers containing media data that needs to be encoded.</span></span> <span data-ttu-id="71bca-107">Chame [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e passe um ponteiro para o exemplo de mídia alocado.</span><span class="sxs-lookup"><span data-stu-id="71bca-107">Call [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) and pass a pointer to the allocated media sample.</span></span> <span data-ttu-id="71bca-108">Além do exemplo de mídia, o **ProcessInput** também precisa do identificador de fluxo de entrada.</span><span class="sxs-lookup"><span data-stu-id="71bca-108">In addition to the media sample, **ProcessInput** also needs the input stream identifier.</span></span> <span data-ttu-id="71bca-109">Para obter o identificador de fluxo, chame [**IMFTransform:: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids).</span><span class="sxs-lookup"><span data-stu-id="71bca-109">To get the stream identifier, call [**IMFTransform::GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids).</span></span> <span data-ttu-id="71bca-110">Como um codificador é projetado para ter apenas uma e uma saída, esses identificadores de fluxo sempre têm o valor de 0.</span><span class="sxs-lookup"><span data-stu-id="71bca-110">Because an encoder is designed to have only one and one output, these stream identifiers always have the value of 0.</span></span>

<span data-ttu-id="71bca-111">Para obter dados do codificador, chame [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="71bca-111">To get data from the encoder, call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="71bca-112">Antes de chamar o [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), você precisa descobrir se o codificador aloca os exemplos de mídia de saída ou deve fazê-lo explicitamente.</span><span class="sxs-lookup"><span data-stu-id="71bca-112">Before you call [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), you need to find out whether the encoder allocates the output media samples or you must do so explicitly.</span></span> <span data-ttu-id="71bca-113">Para fazer isso, chame [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).</span><span class="sxs-lookup"><span data-stu-id="71bca-113">To do this, call [**IMFTransform::GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo).</span></span> <span data-ttu-id="71bca-114">Isso retorna informações de exemplo de mídia de saída na estrutura de [**informações do fluxo de saída do MFT \_ \_ \_**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) .</span><span class="sxs-lookup"><span data-stu-id="71bca-114">This returns output media sample information in the [**MFT\_OUTPUT\_STREAM\_INFO**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) structure.</span></span> <span data-ttu-id="71bca-115">Se o codificador aloca amostras de mídia, ele retorna o fluxo de saída do MFT \_ \_ fornece um sinalizador de \_ \_ exemplos no membro **dwFlags** e o membro **cbSize** contém zero.</span><span class="sxs-lookup"><span data-stu-id="71bca-115">If the encoder allocates media samples, it returns the MFT\_OUTPUT\_STREAM\_PROVIDES\_SAMPLES flag in the **dwFlags** member and the **cbSize** member contains zero.</span></span> <span data-ttu-id="71bca-116">Se o codificador espera que você aloque o buffer de saída, crie o exemplo de mídia de saída e o buffer de mídia associado com base no tamanho retornado em **cbSize**.</span><span class="sxs-lookup"><span data-stu-id="71bca-116">If the encoder expects you to allocate the output buffer, create the output media sample and the associated media buffer based on the size returned in **cbSize**.</span></span> <span data-ttu-id="71bca-117">Ao chamar [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), passe um ponteiro para o exemplo de mídia recém-criado.</span><span class="sxs-lookup"><span data-stu-id="71bca-117">When you call [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), pass a pointer to the newly created media sample.</span></span> <span data-ttu-id="71bca-118">Durante a sessão de codificação, o codificador preenche os buffers de mídia, apontados pelo exemplo de mídia de saída, com os dados codificados.</span><span class="sxs-lookup"><span data-stu-id="71bca-118">During the encoding session, the encoder fills the media buffers, pointed by the output media sample, with the encoded data.</span></span>

<span data-ttu-id="71bca-119">Para iniciar a sessão de codificação, passe o exemplo de mídia de entrada para o codificador chamando [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span><span class="sxs-lookup"><span data-stu-id="71bca-119">To start the encoding session, pass the input media sample to the encoder by calling [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="71bca-120">O codificador inicia o processamento e os dados e produz um ou mais exemplos de mídia de saída que devem ser recuperados pelo [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) , contanto que ele retorne MF \_ E \_ transformação \_ precise de \_ mais \_ entradas.</span><span class="sxs-lookup"><span data-stu-id="71bca-120">The encoder starts processing and the data and produces one or more output media samples that must be retrieved by [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) as long as it returns MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT.</span></span> <span data-ttu-id="71bca-121">Se você chamar **ProcessInput** para passar mais entradas, contanto que haja dados de saída a serem recuperados, o **ProcessInput** falhará com MF \_ E não \_ aceitar.</span><span class="sxs-lookup"><span data-stu-id="71bca-121">If you call **ProcessInput** to pass more input as long as there is output data to be retrieved, **ProcessInput** fails with MF\_E\_NOTACCEPTING.</span></span> <span data-ttu-id="71bca-122">O codificador não aceita mais nenhuma entrada até que o cliente chame **ProcessOutput** pelo menos uma vez.</span><span class="sxs-lookup"><span data-stu-id="71bca-122">The encoder does not accept any more input until the client calls **ProcessOutput** at least once.</span></span>

<span data-ttu-id="71bca-123">Você deve definir carimbos e durações de tempo precisos para todos os exemplos de entrada passados.</span><span class="sxs-lookup"><span data-stu-id="71bca-123">You should set accurate time stamps and durations for all input samples passed.</span></span> <span data-ttu-id="71bca-124">Os carimbos de data/hora não são estritamente necessários, mas ajudam a manter a sincronização de áudio/vídeo.</span><span class="sxs-lookup"><span data-stu-id="71bca-124">Time stamps are not strictly required but help maintain audio/video synchronization.</span></span> <span data-ttu-id="71bca-125">Se você não tiver carimbos de data/hora para suas amostras, é melhor deixá-las fora do que usar valores incertos.</span><span class="sxs-lookup"><span data-stu-id="71bca-125">If you do not have the time stamps for your samples it is better to leave them out than to use uncertain values.</span></span>

## <a name="encoder-processing-example"></a><span data-ttu-id="71bca-126">Exemplo de processamento do codificador</span><span class="sxs-lookup"><span data-stu-id="71bca-126">Encoder Processing Example</span></span>

<span data-ttu-id="71bca-127">O código de exemplo a seguir mostra como chamar [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obter um exemplo codificado.</span><span class="sxs-lookup"><span data-stu-id="71bca-127">The following example code shows how to call [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) to get an encoded sample.</span></span> <span data-ttu-id="71bca-128">Para obter o contexto completo deste exemplo, consulte [código de exemplo do codificador](encoder-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="71bca-128">For the complete context of this example, see [Encoder Example Code](encoder-example-code.md).</span></span>


```C++
HRESULT CWmaEncoder::ProcessOutput(IMFSample **ppSample)
{
    if (m_pMFT == NULL)
    {
        return MF_E_NOT_INITIALIZED;
    }

    *ppSample = NULL;

    IMFMediaBuffer* pBufferOut = NULL;
    IMFSample* pSampleOut = NULL;

    DWORD dwStatus;
  
    MFT_OUTPUT_STREAM_INFO mftStreamInfo = { 0 };
    MFT_OUTPUT_DATA_BUFFER mftOutputData = { 0 };

    HRESULT hr = m_pMFT->GetOutputStreamInfo(m_dwOutputID, &mftStreamInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    //create a buffer for the output sample
    hr = MFCreateMemoryBuffer(mftStreamInfo.cbSize, &pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the output sample
    hr = MFCreateSample(&pSampleOut);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output buffer 
    hr = pSampleOut->AddBuffer(pBufferOut);
    if (FAILED(hr))
    {
        goto done;
    }
 
    //Set the output sample
    mftOutputData.pSample = pSampleOut;

    //Set the output id
    mftOutputData.dwStreamID = m_dwOutputID;

    //Generate the output sample
    hr = m_pMFT->ProcessOutput(0, 1, &mftOutputData, &dwStatus);
    if (hr == MF_E_TRANSFORM_NEED_MORE_INPUT)
    {
        hr = S_OK;
        goto done;
    }

    // TODO: Handle MF_E_TRANSFORM_STREAM_CHANGE

    if (FAILED(hr))
    {
        goto done;
    }

    *ppSample = pSampleOut;
    (*ppSample)->AddRef();

done:
    SafeRelease(&pBufferOut);
    SafeRelease(&pSampleOut);
    return hr;
};
```



## <a name="related-topics"></a><span data-ttu-id="71bca-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="71bca-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71bca-130">Multiplexador ASF</span><span class="sxs-lookup"><span data-stu-id="71bca-130">ASF Multiplexer</span></span>](asf-multiplexer.md)
</dt> <dt>

[<span data-ttu-id="71bca-131">Criando uma instância de um MFT do codificador</span><span class="sxs-lookup"><span data-stu-id="71bca-131">Instantiating an Encoder MFT</span></span>](instantiating-the-encoder-mft.md)
</dt> <dt>

[<span data-ttu-id="71bca-132">Codificadores de mídia do Windows</span><span class="sxs-lookup"><span data-stu-id="71bca-132">Windows Media Encoders</span></span>](windows-media-encoders.md)
</dt> </dl>

 

 



