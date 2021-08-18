---
description: Usando os codecs de mídia de janela DirectShow
ms.assetid: 5b930447-6bf2-4bb3-8dfb-05f4c1e7cd64
title: Usando os codecs de mídia de janela DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495a2675335474351da80b9845fba67f9e967d637d7c9d9c749ffc2f12ce3ea4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012176"
---
# <a name="using-the-window-media-codecs-in-directshow"></a>Usando os codecs de mídia de janela DirectShow

Os objetos codificador e decodificador Windows Media Audio and Video foram originalmente projetados e otimizados para funcionar com o formato de contêiner de arquivo ASF e o SDK de Formato de Mídia Windows. Os objetos codec funcionam bem em DirectShow determinados cenários, ou seja, CBR de passagem única e codificação VBR baseada em qualidade de fluxos de vídeo. Mas se você estiver considerando usar os objetos codec diretamente no DirectShow usando contêineres de arquivo diferentes do ASF, há alguns comportamentos e problemas que você deve estar ciente com antecedência.

> [!Note]  
> Se você pretende usar codecs autônomos com DirectShow, provavelmente será melhor usá-los apenas como DMOs. Em outras palavras, você estará usando a interface [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) em vez de [**IMFTransform.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

 

## <a name="wm-audio-in-avi-files"></a>Áudio WM em arquivos AVI

Você pode usar DirectShow para codificar fluxos WMA em qualquer formato de contêiner de arquivo para o qual você tenha um filtro multiplexador. No entanto, as interfaces de codec de áudio e vídeo de mídia do Windows não são suportadas por WMA em arquivos AVI porque é impossível, usando os filtros de reprodução PADRÃO DirectShow AVI, manter a sincronização de áudio e vídeo em um arquivo AVI com um fluxo WMA. Para obter mais informações, [consulte Armazenamento de mídia compactada em arquivos AVI.](storingcompressedmediainavifiles.md)

O codificador de DMO saídas de amostras de duração variável, mesmo quando no modo de "taxa de bits constante". Portanto, ele funciona melhor com formatos de contêiner de arquivo que usam carimbos de data/hora. Os arquivos AVI não fornecem um carimbo de data/hora para cada amostra de áudio ou grupo de exemplos. No DirectShow, o filtro divisor AVI fabrica carimbos de data/hora para cada grupo de amostras (cada quadro de áudio) com base no valor **nAvgBytesPerSec** na estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) no header de fluxo AVI.

A suposição subjacente a esse cálculo é que todas as amostras de áudio no fluxo têm a mesma duração; no entanto, as amostras de saída pelo DMO não têm duração igual e, portanto, os carimbos de data/hora aplicados pelo divisor AVI não são precisos. Portanto, não é possível, sem modificar o divisor AVI ou o DMO do decodificador de áudio, para usar qualquer aplicativo baseado em DirectShow para reproduzir arquivos AVI com fluxos de áudio e vídeo em sincronia. O codec Windows Media Audio 9 Voice funcionará em alguns casos, mas até mesmo isso perderá a sincronização após qualquer operação de busca, portanto, ele realmente não pode ser considerado uma solução viável.

Se você tiver um codificador MP3, poderá criar arquivos AVI com WMV e MP3 para o fluxo de áudio. Esses arquivos serão reproduzir e buscar corretamente em Windows Media Player e outros aplicativos baseados em DirectShow, porque o divisor AVI contém código de manipulação especial para fluxos MP3. Outra opção é usar áudio PCM descompactado, embora obviamente o tamanho do arquivo resultante seja muito maior do que com um fluxo de áudio compactado. Como o DirectShow aplicativo de exemplo cria arquivos AVI, ele não demonstra como usar o codificador de áudio DMO.

## <a name="one-pass-encoding"></a>Codificação de uma passagem

O codificador de DMO funciona facilmente DirectShow para dois modos de codificação: CBR e VBR baseado em qualidade. Desde que você siga a ordem correta das operações ao criar o grafo de filtro, conforme demonstrado no aplicativo de exemplo, é relativamente simples colocar conteúdo WMV em um arquivo AVI usando o Multiplexador AVI e o File Writer.

## <a name="two-pass-encoding"></a>Codificação de duas passs

Os modos de codificação de duas passagem exigem uma abordagem mais complexa para a criação e o streaming de grafo a fim de impedir que o DMO libera seu conteúdo da primeira passagem antes de iniciar a segunda passagem. Na codificação de duas passões, é necessário executar o grafo uma vez para que o DMO possa executar sua análise de pré-processamento dos dados do arquivo e, em seguida, retroceder o grafo e executar novamente para que o DMO possa fazer a codificação real.

Quando o grafo entra em um estado de run para a segunda passagem, o wrapper DMO define o sinalizador DISCONTINUITY no primeiro exemplo, porque o carimbo de data/hora não é sequencial com o último carimbo de data/hora na primeira passagem. Quando o DMO, que não foi projetado para funcionar no DirectShow dessa forma, recebe o sinalizador DISCONTINUITY, ele executa uma liberação e perde os dados armazenados da primeira passagem. Para resolver esse problema, a melhor solução é, provavelmente, escrever um filtro DMO Wrapper personalizado que não definirá o sinalizador DISCONTINUITY quando o grafo for buscado após a primeira passagem. O exemplo de vídeo Windows (VfW) neste SDK demonstra como executar a codificação de duas passões.

## <a name="interlaced-content"></a>Conteúdo entrelaçado

O codificador WMV DMO é capaz de codificar o conteúdo entrelaçado preservando a entrelaçamento, o que é útil para o conteúdo capturado de uma TV e também pode ser tocado novamente em uma TV. No entanto, não é possível preservar o entrelaçamento usando o wrapper de DMO padrão, porque esse filtro não dá suporte a [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) em seus exemplos de entrada.

O DMO usa essa interface para obter as configurações entrelaçadas para cada amostra que recebe. Se a interface não for encontrada, como é o caso com o wrapper DMO, o DMO simplesmente tratará os exemplos de entrada como não entrelaçados. Para executar a codificação entrelaçadas DirectShow, há várias alternativas. A abordagem mais fácil provavelmente é usar o SDK da série Windows Media Format 9 diretamente ou usando o filtro de DirectShow do WM ASF para criar um arquivo ASF entrelaçado. Em seguida, você pode transcodificar esse arquivo em algum outro formato. Se você transcodificar para o AVI, terá um arquivo entrelaçado, mas os filtros de reprodução PADRÃO DirectShow AVI não o reconhecerão como tal porque não são suportados por [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2). Outra abordagem é escrever seu próprio filtro DMO Wrapper que dá suporte à interface [**INSSBuffer.**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Trabalhando com DMOs codec](workingwithcodecdmos.md)
</dt> </dl>

 

 
