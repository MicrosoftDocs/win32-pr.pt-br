---
description: Usando os codecs de mídia do Windows no DirectShow
ms.assetid: 5b930447-6bf2-4bb3-8dfb-05f4c1e7cd64
title: Usando os codecs de mídia do Windows no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb521c0e3897dc2415fbd613f97b755a146657d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780210"
---
# <a name="using-the-window-media-codecs-in-directshow"></a>Usando os codecs de mídia do Windows no DirectShow

Os objetos de codificador e codificador de áudio e vídeo do Windows Media foram originalmente projetados e otimizados para funcionar com o formato de contêiner do arquivo ASF e o Windows Media Format SDK. Os objetos de codec funcionam bem no DirectShow para determinados cenários, ou seja, uma passagem de CBR e codificação de VBR com base em qualidade de fluxos de vídeo. Mas se você estiver pensando em usar os objetos de codec diretamente no DirectShow usando contêineres de arquivos diferentes do ASF, há certos comportamentos e problemas que você deve estar atento com antecedência.

> [!Note]  
> Se você pretende usar codecs autônomos com o DirectShow, provavelmente desejará usá-los como somente DMOs. Em outras palavras, você usará a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) em vez de [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform).

 

## <a name="wm-audio-in-avi-files"></a>Áudio do WM em arquivos AVI

Você pode usar o DirectShow para codificar fluxos de WMA em qualquer formato de contêiner de arquivos para o qual você tenha um filtro de Multiplexador. No entanto, as interfaces do codec de áudio e vídeo do Windows Media não oferecem suporte a WMA em arquivos AVI porque é impossível, usando os filtros de reprodução AVI do DirectShow padrão, para manter a sincronização de vídeo em um arquivo AVI com um fluxo WMA. Para obter mais informações, consulte [armazenando mídia compactada em arquivos AVI](storingcompressedmediainavifiles.md).

O codificador de áudio DMO gera amostras de duração variável, mesmo quando estiver no modo "taxa de bits constante". Portanto, ele funciona melhor com formatos de contêiner de arquivo que usam carimbos de data/hora. Os arquivos AVI não fornecem um carimbo de data/hora para cada amostra de áudio ou grupo de amostras. No DirectShow, o filtro de Splitter AVI fabrica carimbos de data/hora para cada grupo de amostras (cada quadro de áudio) com base no valor **nAvgBytesPerSec** na estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) no cabeçalho do fluxo avi.

A suposição subjacente a esse cálculo é que todos os exemplos de áudio no fluxo são de duração igual; no entanto, os exemplos de saída do DMO não são de duração igual e, portanto, os carimbos de data/hora aplicados pelo divisor AVI não são precisos. Portanto, não é possível, sem modificar o divisor AVI ou o áudio Decoder DMO, para usar qualquer aplicativo baseado em DirectShow para reproduzir arquivos AVI com fluxos de áudio e vídeo sincronizados. O codec de voz do Windows Media Audio 9 funcionará em alguns casos, mas mesmo isso perderá a sincronização após qualquer operação de busca, portanto, ela não pode ser considerada uma solução viável.

Se você tiver um codificador MP3, poderá criar arquivos AVI com WMV e MP3 para o fluxo de áudio. Esses arquivos serão reproduzidos e buscarão corretamente no Windows Media Player e em outros aplicativos baseados no DirectShow, pois o divisor AVI contém um código de tratamento especial para fluxos de MP3. Outra opção é usar áudio PCM não compactado, embora, obviamente, o tamanho do arquivo resultante seja muito maior do que com um fluxo de áudio compactado. Como o aplicativo de exemplo do DirectShow cria arquivos AVI, ele não demonstra como usar o codificador de áudio DMO.

## <a name="one-pass-encoding"></a>Codificação de passagem única

O Video Encoder DMO funciona facilmente no DirectShow para dois modos de codificação: CBR e taxa de bits baseada em qualidade. Desde que você siga a ordem correta das operações ao criar o gráfico de filtro, conforme demonstrado no aplicativo de exemplo, é relativamente simples inserir o conteúdo de WMV em um arquivo AVI usando o multiplexador AVI e o gravador de arquivos.

## <a name="two-pass-encoding"></a>Codificação de duas passagens

Os modos de codificação de duas passagens exigem uma abordagem mais complexa para criação e streaming de grafo para impedir que o DMO libere seu conteúdo da primeira passagem antes de iniciar a segunda passagem. Em codificação de dois passos, é necessário executar o grafo uma vez para que o DMO possa executar sua análise de pré-processamento dos dados do arquivo e, em seguida, retroceder o grafo e executá-lo novamente para que o DMO possa fazer a codificação real.

Quando o grafo entra em um estado de execução para a segunda passagem, o wrapper de DMO define o sinalizador de discontinuidade no primeiro exemplo, porque o carimbo de data/hora não é sequencial com o último carimbo de data/hora na primeira passagem. Quando o DMO, que não foi projetado para funcionar no DirectShow dessa forma, o recebe o sinalizador de descontinuidade, ele executa uma liberação e perde os dados armazenados da primeira passagem. Para contornar esse problema, é provável que a melhor solução seja escrever um filtro de wrapper de DMO personalizado que não defina o sinalizador de descontinuidade quando o grafo for buscado após a primeira passagem. O exemplo de vídeo para Windows (VfW) neste SDK demonstra como executar a codificação de duas passagens.

## <a name="interlaced-content"></a>Conteúdo entrelaçado

O WMV Encoder DMO é capaz de codificar conteúdo entrelaçado enquanto preserva o entrelaçamento, que é útil para o conteúdo que é capturado de uma TV e também pode ser reproduzido em uma TV. No entanto, não é possível preservar o entrelaçamento usando o wrapper de DMO padrão, pois esse filtro não oferece suporte a [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) em seus exemplos de entrada.

O DMO usa essa interface para obter as configurações entrelaçadas de cada amostra que recebe. Se a interface não for encontrada, como é o caso com o invólucro de DMO, o DMO simplesmente tratará os exemplos de entrada como não entrelaçados. Para executar a codificação entrelaçada no DirectShow, há várias alternativas. A abordagem mais fácil provavelmente usará o SDK do Windows Media Format 9 Series diretamente ou usando o filtro do WM ASF Writer DirectShow, para criar um arquivo ASF entrelaçado. Em seguida, você pode transcodificar esse arquivo em algum outro formato. Se você transcodificar em AVI, terá um arquivo entrelaçado, mas os filtros de reprodução AVI do DirectShow padrão não serão reconhecidos como tal porque não dão suporte a [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). Outra abordagem é escrever seu próprio filtro de invólucro de DMO que dê suporte à interface [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com codec DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
