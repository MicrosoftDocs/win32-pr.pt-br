---
description: Para converter arquivos de mídia em formato ASF, você pode usar codificadores de mídia do Windows. Para usar esses codificadores, eles devem ser registrados com o sistema.
ms.assetid: 18c26619-6047-4f7f-bb65-ca418f02e5b1
title: Usando um objeto de ativação de codificadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd44a1b97ad0f133b7215ff4474835ddfba66bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827797"
---
# <a name="using-an-encoders-activation-objects"></a>Usando objetos de ativação de um codificador

Para converter arquivos de mídia em formato ASF, você pode usar codificadores de mídia do Windows. Para usar esses codificadores, eles devem ser registrados com o sistema.

Para obter informações sobre o registro do codificador, consulte [instanciando um MFT do codificador](instantiating-the-encoder-mft.md).

-   [Usando objetos de ativação de um codificador](#using-an-encoders-activation-objects)
-   [Enumeração de codificador no Windows 7 e posterior](#encoder-enumeration-in-windows-7-and-later)
-   [Tópicos relacionados](#related-topics)

## <a name="using-an-encoders-activation-objects"></a>Usando objetos de ativação de um codificador

Como alternativa ao uso da interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) de um codificador (descrita na [criação de um codificador usando CoCreateInstance](using-an-encoder-s-imftransform--interface.md)), você pode criar uma instância do objeto de ativação para o codificador. Os objetos de ativação facilitam a criação do codificador e o Media Foundation fornece as duas funções a seguir para essa abordagem:

-   [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) para instanciar o codificador de áudio do Windows Media.
-   [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) para instanciar o codificador de vídeo do Windows Media.

Ambas as funções exigem que você crie o tipo de mídia de destino e defina as propriedades de codificação antes de chamar essas funções. Se seu aplicativo estiver usando [componentes ASF da camada de pipeline](pipeline-layer-asf-components.md) para codificar um arquivo para o formato ASF e já tiver criado e configurado os [coletores de mídia ASF](asf-media-sinks.md), você poderá obter esse conjunto de informações do coletor de mídia ASF.

[**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) e [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) definem o tipo de saída do codificador para o tipo de mídia especificado pelo aplicativo.

**Observação**  Se você estiver usando [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) e [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate) , poderá ativar o codificador chamando [**IMFActivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) , mas não poderá alterar a entrada e os tipos de mídia de saída do codificador, nem pode alterar as propriedades de codificação.

Para obter mais informações sobre como criar objetos de Media Foundation usando objetos de ativação, consulte [objetos de ativação](activation-objects.md).

**Para obter o tipo de mídia de destino do coletor de mídia do ASF**

1.  Obtenha um ponteiro para o ponteiro [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) do coletor de mídia do ASF chamando **IMFMediaSink:: QueryInterface** no coletor de mídia ASF e passando **\_ IMFASFContentInfo de IID** como o identificador de interface.
2.  Obtenha o objeto de perfil ASF associado ao objeto ContentInfo.
3.  Enumere os fluxos no perfil para obter o tipo de mídia do fluxo.

**Para obter as propriedades de codificação do coletor de mídia ASF**

1.  Se você tiver configurado as [Propriedades de codificação](configuring-the-encoder.md) no coletor de mídia (descrito [em Propriedades de configuração no coletor de arquivos](setting-properties-in-the-file-sink.md)), poderá uma referência ao repositório de propriedades do coletor chamando **IMFMediaSink:: QUERYINTERFACE** no coletor de mídia ASF e passando **\_ IPropertyStore de IID** como o identificador de interface.
2.  Se você tiver um ponteiro para o objeto ContentInfo do coletor, poderá chamar [**IMFASFContentInfo:: GetEncodingConfigurationPropertyStore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) para obter uma referência ao repositório de propriedades do coletor de mídia.

    Certifique-se de que todas as propriedades de codificação definidas no coletor de mídia ASF sejam refletidas no repositório de Propriedades passado para [**MFCreateWMAEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) e [**MFCreateWMVEncoderActivate**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate). O codificador é configurado automaticamente com base nas configurações especificadas pelo aplicativo.

Ao criar o nó de transformação na topologia de codificação, você pode definir o tipo de objeto como um ponteiro [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) recebido nessas duas chamadas. Quando a topologia é resolvida, a sessão de mídia usa o objeto de ativação para criar uma instância do MFT do codificador.

## <a name="encoder-enumeration-in-windows-7-and-later"></a>Enumeração de codificador no Windows 7 e posterior

Para aplicativos em execução no Windows 7, além de [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) , você pode enumerar o codificador MFTs chamando [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). Essa função retorna um ponteiro para o objeto de ativação do MFT do codificador. A estrutura da função é muito semelhante à **MFTEnum** descrita acima, exceto que **MFTEnumEx** retorna uma matriz de ponteiros [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) para a MFTs do codificador que corresponde aos critérios de pesquisa.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando uma instância de um MFT do codificador](instantiating-the-encoder-mft.md)
</dt> <dt>

[Codificadores de mídia do Windows](windows-media-encoders.md)
</dt> <dt>

[Objetos de ativação](activation-objects.md)
</dt> </dl>

 

 



