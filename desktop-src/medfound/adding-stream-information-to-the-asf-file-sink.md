---
description: Saiba mais sobre como adicionar informações de fluxo ao sink do arquivo ASF, que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Adicionando informações de fluxo ao sink do arquivo ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8202de8da5cb8e17534c334e3d39dddb3c4f99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404349"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a>Adicionando informações de fluxo ao sink do arquivo ASF

O sink de arquivo ASF é uma implementação de [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) fornecida pelo Media Foundation que um aplicativo pode usar para arquivar dados de mídia ASF em um arquivo. Para obter informações sobre o modelo de objeto e o uso geral dos sinks de mídia do ASF, consulte [AsF Media Sinks](asf-media-sinks.md).

Depois de criar uma instauência do sink de arquivo, ele deve ser configurado antes de criar a topologia. O sink de arquivo precisa saber sobre os fluxos no arquivo de saída, as informações do modo de codificação e os metadados. Este tópico descreve o processo de adição de fluxo no sink de arquivos.

-   [Adicionando fluxos no sink de arquivo ASF](#adding-streams-in-the-asf-file-sink)
-   [Enumerando os sinks de fluxo](#enumerating-stream-sinks)
-   [Tópicos relacionados](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a>Adicionando fluxos no sink de arquivo ASF

O sink de arquivo deve conhecer os fluxos de saída e suas propriedades para que ele possa gerar amostras de saída de acordo e adicioná-los ao arquivo ASF de saída. Essas configurações são escritas no objeto de header ASF final.

Para definir informações de fluxo, você deve ter uma referência ao objeto ContentInfo do asf do sink do arquivo. Para obter informações, consulte [Criando o sink de arquivo ASF](creating-the-asf-file-sink.md).

O procedimento a seguir resume as etapas gerais para configurar o fluxo usando o objeto de perfil ASF.

**Para configurar informações de fluxo no sink do arquivo ASF**

1.  Crie um objeto de perfil ASF chamando [**MFCreateASFProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile).
2.  Para cada fluxo no arquivo de saída, crie um tipo de mídia para o fluxo de destino a ser adicionado no sink de arquivo. O tipo de mídia deve ser compatível com os tipos de saída compatíveis com os codificadores de Mídia do Windows.

    Para obter informações sobre como adicionar fluxos de áudio ao perfil, consulte Criando fluxos de áudio para codificação ASF.

    Para obter informações sobre como adicionar fluxos de vídeo ao perfil, consulte Criando fluxos de vídeo para codificação ASF.

3.  Crie fluxos com base nos tipos de mídia criados na etapa 2 chamando [**IMFASFProfile::CreateStream.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream)
4.  Atribua um número de fluxo para o fluxo recém-criado chamando o ponteiro da interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) recebido na etapa 3.
5.  Opcionalmente, configure o fluxo com as seguintes informações:
    -   Parâmetros de bucket vazado definindo os atributos: [**\_ MF ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) [**ou \_ MF ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
    -   Extensão de carga, exclusão mútua chamando [**métodos IMFASFStreamConfig.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
6.  Opcionalmente, de definir o tamanho do pacote de dados para o perfil definindo atributos [**\_ MF ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) e [**\_ MF ASFPROFILE \_ MAXPACKETSIZE.**](mf-asfprofile-maxpacketsize-attribute.md) O perfil ASF expõe a interface [**IMFAttributes,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) à qual um aplicativo pode obter referência chamando **IMFASFProfile::QueryInterface**.
7.  Definir informações de codificação para o fluxo no sink de arquivo. Discutido na [configuração de propriedades no sink de arquivo](setting-properties-in-the-file-sink.md).
8.  Adicione o fluxo ao perfil chamando [**IMFASFProfile::SetStream.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream)
9.  Associe o perfil ao objeto ContentInfo chamando [**IMFASFContentInfo::SetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile).

Para modificar um fluxo existente, o aplicativo pode obter uma referência à interface [**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) do fluxo e reconfigurá-la de acordo com os requisitos. Para adicionar ou remover fluxos, o aplicativo deve chamar [**IMFASFProfile::RemoveStream.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) Para aplicar essas alterações, modificações de fluxo ou remoção, você deve definir o perfil novamente no objeto ContentInfo. Isso substitui o perfil existente que já está associado ao objeto ContentInfo.


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



## <a name="enumerating-stream-sinks"></a>Enumerando os sinks de fluxo

Para cada fluxo no perfil do que o objeto ContentInfo está ciente, o sink de arquivo ASF cria e adiciona um sink de fluxo que contém todas as propriedades do fluxo codificado. O sink de arquivo ASF foi projetado para conter fluxos fixos. Isso significa que você não pode adicionar ou remover fluxos chamando [**IMFMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) ou [**IMFMediaSink::RemoveStreamSink.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink) Essas chamadas no sink de arquivo falham com o código de erro MF \_ E \_ STREAMSINKS \_ FIXED. Adicionar ou remover fluxos no perfil não adiciona nem remove automaticamente os sinks de fluxo no sink de arquivo. Você deve descartar a instância existente do arquivo e recriá-la com novas informações de fluxo se os fluxos no perfil foram alterados.

O procedimento a seguir resume as etapas gerais para enumerar os sinks de fluxo no sink do arquivo ASF.

**Para enumerar os sinks de fluxo**

1.  Chame [**IMFMediaSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) para obter o número total de sinks de fluxo no sink do arquivo ASF.
2.  Loop pelos sinks de fluxo e obter uma referência à interface [**GetStreamSinkByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) do fluxo.

    – ou –

    Chame [**IMFMediaSink::GetStreamSinkById**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) para obter o sink de fluxo especificando o número do fluxo. Cada sink de fluxo é identificado com o número de fluxo definido durante a criação do fluxo no perfil.

Se você estiver criando uma topologia parcial para codificar um arquivo de mídia, deverá adicionar o sink de arquivo à topologia como um nó de topologia de saída. Você pode fazer isso especificando cada sink de fluxo no sink do arquivo ou definindo o objeto de ativação do sink de arquivo e os identificadores do sink de fluxo. Para obter mais informações e exemplo de código, consulte [Criando nós de saída](creating-output-nodes.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sinks de mídia do ASF](asf-media-sinks.md)
</dt> <dt>

[Suporte a ASF no Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



