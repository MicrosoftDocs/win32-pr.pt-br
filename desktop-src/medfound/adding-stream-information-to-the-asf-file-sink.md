---
description: O coletor de arquivos ASF é uma implementação de IMFMediaSink fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo. Para obter informações sobre o modelo de objeto de coletor de mídia ASF e uso geral, consulte coletores de mídia ASF.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Adicionando informações de fluxo ao coletor de arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e08c6997d9c77836f379d4ca7b75720ddea245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105814505"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a>Adicionando informações de fluxo ao coletor de arquivo ASF

O coletor de arquivos ASF é uma implementação de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo. Para obter informações sobre o modelo de objeto do coletor de mídia ASF e o uso geral, consulte [coletores de mídia ASF](asf-media-sinks.md).

Depois de instanciar o coletor de arquivos, ele deve ser configurado antes da criação da topologia. O coletor de arquivos precisa saber sobre os fluxos no arquivo de saída, as informações do modo de codificação e os metadados. Este tópico descreve o processo de adição de fluxo no coletor de arquivos.

-   [Adicionando fluxos no coletor de arquivo ASF](#adding-streams-in-the-asf-file-sink)
-   [Enumerando coletores de fluxo](#enumerating-stream-sinks)
-   [Tópicos relacionados](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a>Adicionando fluxos no coletor de arquivo ASF

O coletor de arquivos deve conhecer os fluxos de saída e suas propriedades para que possa gerar amostras de saída de forma adequada e adicioná-las ao arquivo ASF de saída. Essas configurações são gravadas no objeto de cabeçalho ASF final.

Para definir informações de fluxo, você deve ter uma referência ao objeto ASF ContentInfo do coletor de arquivos. Para obter informações, consulte [criando o coletor de arquivo ASF](creating-the-asf-file-sink.md).

O procedimento a seguir resume as etapas gerais para configurar o Stream usando o objeto de perfil ASF.

**Para configurar as informações de fluxo no coletor de arquivo ASF**

1.  Crie um objeto de perfil ASF chamando [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).
2.  Para cada fluxo no arquivo de saída, crie um tipo de mídia para o fluxo de destino a ser adicionado no coletor de arquivos. O tipo de mídia deve ser compatível com os tipos de saída com suporte dos codificadores de mídia do Windows.

    Para obter informações sobre como adicionar fluxos de áudio ao perfil, consulte Criando fluxos de áudio para codificação ASF.

    Para obter informações sobre como adicionar fluxos de vídeo ao perfil, consulte Criando fluxos de vídeo para codificação ASF.

3.  Crie fluxos com base nos tipos de mídia criados na etapa 2 chamando [**IMFASFProfile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).
4.  Atribua um número de fluxo para o fluxo recém-criado chamando o ponteiro de interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) recebido na etapa 3.
5.  Opcionalmente, configure o fluxo com as seguintes informações:
    -   Parâmetros de Bucket vazado definindo os atributos: [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) ou [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
    -   Extensão de carga, exclusão mútua chamando métodos [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) .
6.  Opcionalmente, defina o tamanho do pacote de dados para o perfil definindo os atributos [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) e [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) . O perfil ASF expõe a interface [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , à qual um aplicativo pode obter referência chamando **IMFASFProfile:: QueryInterface**.
7.  Defina as informações de codificação para o fluxo no coletor de arquivos. Discutido na [configuração de propriedades no coletor de arquivos](setting-properties-in-the-file-sink.md).
8.  Adicione o fluxo ao perfil chamando [**IMFASFProfile:: SetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream).
9.  Associe o perfil ao objeto ContentInfo chamando [**IMFASFContentInfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).

Para modificar um fluxo existente, o aplicativo pode obter uma referência à interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) do fluxo e reconfigurá-lo de acordo com os requisitos. Para adicionar ou remover fluxos, o aplicativo deve chamar [**IMFASFProfile:: RemoveStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream). Para aplicar essas alterações, as modificações ou a remoção do fluxo, você deve definir o perfil novamente no objeto ContentInfo. Isso substitui o perfil existente que já está associado ao objeto ContentInfo.


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a>Enumerando coletores de fluxo

Para cada fluxo no perfil do qual o objeto ContentInfo está ciente, o coletor de arquivo ASF cria e adiciona um coletor de fluxo que contém todas as propriedades do fluxo codificado. O coletor de arquivos ASF foi projetado para conter fluxos fixos. Isso significa que você não pode adicionar ou remover fluxos chamando [**IMFMediaSink:: AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) ou [**IMFMediaSink:: RemoveStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink). Essas chamadas no coletor de arquivos falham com o \_ \_ código de \_ erro fixo MF E STREAMSINKS. Adicionar ou remover fluxos no perfil não adiciona ou remove automaticamente os coletores de fluxo no coletor de arquivos. Você deve descartar a instância existente do arquivo e recriá-la com novas informações de fluxo se os fluxos no perfil tiverem sido alterados.

O procedimento a seguir resume as etapas gerais para enumerar coletores de fluxo no coletor de arquivo ASF.

**Para enumerar coletores de fluxo**

1.  Chame [**IMFMediaSink:: GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) para obter o número total de coletores de fluxo no coletor de arquivo asf.
2.  O loop pelos coletores de fluxo ang Obtém uma referência à interface [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) do coletor de fluxo.

    – ou –

    Chame [**IMFMediaSink:: GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) para obter o coletor de fluxo especificando o número do fluxo. Cada coletor de fluxo é identificado com o número de fluxo definido durante a criação do fluxo no perfil.

Se você estiver criando uma topologia parcial para codificar um arquivo de mídia, deverá adicionar o coletor de arquivo à topologia como um nó de topologia de saída. Você pode fazer isso especificando cada coletor de fluxo no coletor de arquivos ou definindo o objeto de ativação do coletor de arquivos e os identificadores do coletor de fluxo. Para obter mais informações e um exemplo de código, consulte [criando nós de saída](creating-output-nodes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coletores de mídia ASF](asf-media-sinks.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



