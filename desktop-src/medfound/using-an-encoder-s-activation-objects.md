---
description: Para converter arquivos de mídia em formato ASF, você pode usar Windows de mídia. Saiba mais sobre como usar objetos de ativação de um codificador.
ms.assetid: 18c26619-6047-4f7f-bb65-ca418f02e5b1
title: Usando objetos de ativação de codificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24915020c1b888be6a1aeaca1e21af95d11cfc181a5c00a91c8359c3f780fa0e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972735"
---
# <a name="using-an-encoders-activation-objects"></a>Usando objetos de ativação de um codificador

Para converter arquivos de mídia em formato ASF, você pode usar Windows de mídia. Para usar esses codificadores, eles devem ser registrados no sistema.

Para obter informações sobre o registro do codificador, consulte [Instando um codificador MFT](instantiating-the-encoder-mft.md).

-   [Usando objetos de ativação de um codificador](#using-an-encoders-activation-objects)
-   [Enumeração do codificador no Windows 7 e posterior](#encoder-enumeration-in-windows-7-and-later)
-   [Tópicos relacionados](#related-topics)

## <a name="using-an-encoders-activation-objects"></a>Usando objetos de ativação de um codificador

Como alternativa ao uso da interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) de um codificador (descrita em Criando um codificador usando [CoCreateInstance),](using-an-encoder-s-imftransform--interface.md)você pode criar uma instância do objeto de ativação para o codificador. Os objetos de ativação facilitam a criação do codificador e Media Foundation fornece as duas funções a seguir para essa abordagem:

-   [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) para inferência do codificador de áudio Windows Media.
-   [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) para inferência do codificador de vídeo Windows Media.

Essas duas funções exigem a criação do tipo de mídia de destino e a definição das propriedades de codificação antes de chamar essas funções. Se seu aplicativo estiver usando componentes [ASF](pipeline-layer-asf-components.md) de camada de pipeline para codificar um arquivo no formato ASF e já tiver criado e configurado os Sinks de Mídia do [ASF,](asf-media-sinks.md)você poderá obter esse conjunto de informações do sink de mídia do ASF.

[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) e [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) definem o tipo de saída do codificador como o tipo de mídia especificado pelo aplicativo.

**Observação**  Se você estiver usando [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) e [**MFCreateWMVEncoderActivate,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) poderá ativar o codificador chamando [**IMFActivate::ActivateObject,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) mas não poderá alterar a entrada e os tipos de mídia de saída do codificador nem alterar nenhuma das propriedades de codificação.

Para obter mais informações sobre como criar objetos Media Foundation usando objetos de ativação, consulte [Objetos de ativação](activation-objects.md).

**Para obter o tipo de mídia de destino do sink de mídia do ASF**

1.  Obter um ponteiro para o ponteiro [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) do sink de mídia do ASF chamando **IMFMediaSink::QueryInterface** no sink de mídia do ASF e passando **\_ IID IMFASFContentInfo** como o identificador de interface.
2.  Obter o objeto de perfil ASF associado ao objeto ContentInfo.
3.  Enumerar os fluxos no perfil para obter o tipo de mídia do fluxo.

**Para obter as propriedades de codificação do sink de mídia do ASF**

1.  Se você tiver [](configuring-the-encoder.md) configurado as Propriedades de Codificação no sink de mídia (descrito em Configurando propriedades no sink de [arquivo),](setting-properties-in-the-file-sink.md)poderá fazer uma referência ao repositório de propriedades do sink chamando **IMFMediaSink::QueryInterface** no sink de mídia do ASF e passando **IID \_ IPropertyStore** como o identificador de interface.
2.  Se você tiver um ponteiro para o objeto ContentInfo do sink, poderá chamar [**IMFASFContentInfo::GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) para obter uma referência ao repositório de propriedades do sink de mídia.

    Certifique-se de que todas as propriedades de codificação definidas no sink de mídia ASF sejam refletidas no armazenamento de propriedades passado para [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) e [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate). O codificador é configurado automaticamente com base nas configurações especificadas pelo aplicativo.

Ao criar o nó de transformação na topologia de codificação, você pode definir o tipo de objeto como um ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recebido nessas duas chamadas. Quando a topologia é resolvida, a Sessão de Mídia usa o objeto de ativação para criar uma instância do codificador MFT.

## <a name="encoder-enumeration-in-windows-7-and-later"></a>Enumeração do codificador no Windows 7 e posterior

Para aplicativos em execução no Windows 7, além do [**MFTEnum,**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) você pode enumerar os MFTs do codificador chamando [**MFTEnumEx.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) Essa função retorna um ponteiro para o objeto de ativação do codificador MFT. A estrutura da função é muito semelhante à **MFTEnum** descrita acima, exceto que **MFTEnumEx** retorna uma matriz de ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) para os MFTs do codificador que corresponderem aos critérios de pesquisa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inciando um MFT codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Codificadores de mídia](windows-media-encoders.md)
</dt> <dt>

[Objetos de ativação](activation-objects.md)
</dt> </dl>

 

 



