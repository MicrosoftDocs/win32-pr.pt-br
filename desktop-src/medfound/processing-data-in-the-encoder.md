---
description: Processando dados no codificador
ms.assetid: 7be4c5e7-db2c-4063-8e5c-af6ffb861aa5
title: Processando dados no codificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 666c2a2ff2139aadcb489022eb9b324eff1de523551244c2fd12ad0e11f68f1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118238727"
---
# <a name="processing-data-in-the-encoder"></a>Processando dados no codificador

Depois de negociar o tipo de entrada e o tipo de saída para o MFT do codificador, conforme descrito em [negociação de tipo de mídia no codificador](media-type-negotiation-on-the-encoder.md), você pode iniciar o processamento de exemplos de dados de mídia. Os dados são passados na forma de amostras de mídia (interface [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) ) e também recebidos da saída como amostras de mídia.

Antes de enviar dados para o codificador para processamento, você deve alocar um exemplo de mídia e adicionar um ou mais buffers de mídia que contenham dados de mídia que precisam ser codificados. Chame [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) e passe um ponteiro para o exemplo de mídia alocado. Além do exemplo de mídia, o **ProcessInput** também precisa do identificador de fluxo de entrada. Para obter o identificador de fluxo, chame [**IMFTransform:: GetStreamIDs**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamids). Como um codificador é projetado para ter apenas uma e uma saída, esses identificadores de fluxo sempre têm o valor de 0.

Para obter dados do codificador, chame [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput). Antes de chamar o [**ProcessOutput**](/windows/desktop/api/mfidl/nf-mfidl-imfqualitymanager-notifyprocessoutput), você precisa descobrir se o codificador aloca os exemplos de mídia de saída ou deve fazê-lo explicitamente. Para fazer isso, chame [**IMFTransform:: GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo). Isso retorna informações de exemplo de mídia de saída na estrutura de [**informações do fluxo de saída do MFT \_ \_ \_**](/windows/desktop/api/mftransform/ns-mftransform-mft_output_stream_info) . Se o codificador aloca amostras de mídia, ele retorna o fluxo de saída do MFT \_ \_ fornece um sinalizador de \_ \_ exemplos no membro **dwFlags** e o membro **cbSize** contém zero. Se o codificador espera que você aloque o buffer de saída, crie o exemplo de mídia de saída e o buffer de mídia associado com base no tamanho retornado em **cbSize**. Ao chamar [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample), passe um ponteiro para o exemplo de mídia recém-criado. Durante a sessão de codificação, o codificador preenche os buffers de mídia, apontados pelo exemplo de mídia de saída, com os dados codificados.

Para iniciar a sessão de codificação, passe o exemplo de mídia de entrada para o codificador chamando [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput). O codificador inicia o processamento e os dados e produz um ou mais exemplos de mídia de saída que devem ser recuperados pelo [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) , contanto que ele retorne MF \_ E \_ transformação \_ precise de \_ mais \_ entradas. Se você chamar **ProcessInput** para passar mais entradas, contanto que haja dados de saída a serem recuperados, o **ProcessInput** falhará com MF \_ E não \_ aceitar. O codificador não aceita mais nenhuma entrada até que o cliente chame **ProcessOutput** pelo menos uma vez.

Você deve definir carimbos e durações de tempo precisos para todos os exemplos de entrada passados. Os carimbos de data/hora não são estritamente necessários, mas ajudam a manter a sincronização de áudio/vídeo. Se você não tiver carimbos de data/hora para suas amostras, é melhor deixá-las fora do que usar valores incertos.

## <a name="encoder-processing-example"></a>Exemplo de processamento do codificador

O código de exemplo a seguir mostra como chamar [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) para obter um exemplo codificado. Para obter o contexto completo deste exemplo, consulte [código de exemplo do codificador](encoder-example-code.md).


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Multiplexador ASF](asf-multiplexer.md)
</dt> <dt>

[Criando uma instância de um MFT do codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificadores de mídia](windows-media-encoders.md)
</dt> </dl>

 

 



