---
title: Escrevendo amostras de imagens de vídeo
description: Escrevendo amostras de imagens de vídeo
ms.assetid: 1d375186-230a-4a18-a995-b331c72a76e7
keywords:
- ASF (Advanced Systems Format), escrevendo amostras de imagens de vídeo
- ASF (formato de sistemas avançados), escrevendo amostras de imagens de vídeo
- imagens de vídeo, como escrever amostras
- fluxos, escrevendo amostras de imagens de vídeo
- codecs, escrevendo amostras de imagens de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fbac644d7938477ba3d2e8b21ebb6e631a47708
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293764"
---
# <a name="writing-video-image-samples"></a>Escrevendo amostras de imagens de vídeo

Um fluxo de imagem de vídeo é um vídeo que contém uma série de imagens ainda. As imagens podem ser movidas dentro do quadro e cada imagem pode misturar para a próxima. Os fluxos de imagem de vídeo são codificados usando o codec do Windows Media Video 9 Image v2. O vídeo de saída é semelhante ao criado pelo codec do Windows Media Video 9.

Para criar um perfil que contenha um fluxo de imagem de vídeo, comece enumerando os codecs de vídeo, conforme descrito em [obtendo informações de configuração de fluxo de codecs](getting-stream-configuration-information-from-codecs.md). Procure o codec que dá suporte ao \_ subtipo WMMEDIASUBTYPE WVP2.

Depois de definir o perfil no objeto do gravador, chame [**IWMWriter:: GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops) para obter as propriedades de mídia para o fluxo de entrada da imagem de vídeo. Obtenha o tipo de mídia do objeto de propriedades de mídia chamando [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)e altere o subtipo para WMMEDIASUBTYPE \_ VIDEOIMAGE. Você deve definir a largura e a altura do vídeo para as dimensões máximas necessárias para abranger as imagens que serão adicionadas ao fluxo. Em seguida, chame [**IWMMediaProps:: SetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-setmediatype) com o tipo de entrada modificado. Agora você está pronto para começar a enviar amostras para o objeto gravador.

Cada exemplo deve começar com uma estrutura **WMT \_ VIDEOIMAGE \_ SAMPLE2** . Além disso, os exemplos podem conter imagens de bitmap. Uma imagem é anexada apenas a um exemplo do primeiro quadro no qual ela aparece. Todos os quadros adicionais que usam essa imagem precisam apenas de informações na estrutura. Os bitmaps de entrada devem ser formatados como RGB, 24 bits por pixel.

Os arquivos de bitmap armazenam os dados da imagem para que os dados de cada linha da imagem demorem um número de bytes divisível por quatro. (Isso é chamado de Stride do bitmap.) Isso força o início de cada linha de vídeo a um limite **DWORD** , o que torna a cópia mais eficiente. Se as linhas de imagem não forem divisíveis igualmente por quatro, a linha será preenchida para o próximo múltiplo mais alto de quatro bytes. Ao anexar dados de imagem, você deve remover qualquer preenchimento que exista no final dos dados para cada linha.

O codec Windows Media Video 9 Image v2 mantém até duas imagens na memória por vez. Essas imagens são chamadas de imagem anterior e imagem atual. Cada imagem tem um conjunto de membros na estrutura **WMT \_ VIDEOIMAGE \_ SAMPLE2** , que determinam como a imagem é apresentada no quadro. Você pode adicionar uma imagem definindo o membro dwControlFlags de **WMT \_ VIDEOIMAGE \_ SAMPLE2** no quadro de \_ entrada de exemplo WMT VIDEOIMAGE \_ \_ \_ . Quando você passa um quadro de entrada para o codec, essa imagem torna-se a imagem atual. A imagem que era a imagem atual no exemplo anterior geralmente se torna a imagem anterior e a imagem que foi a imagem anterior no exemplo anterior é descartada. Você pode configurar o codec para manter a imagem anterior antiga definindo o membro **bKeepPrevImage** como **true**. Nesse caso, a imagem que foi a imagem atual no exemplo anterior é descartada.

A composição básica de um quadro de imagem de vídeo é determinada por dois fatores para cada imagem: região de interesse e coeficiente de mistura. A região de interesse de uma imagem é definida por um ponto de origem, largura e altura. A parte de uma imagem descrita pela região de interesse preenche o quadro de saída. Se a região de interesse for um tamanho diferente do quadro de saída, o codec o redimensionará. O coeficiente de mistura da imagem determina a mistura das duas imagens. Os coeficientes de Blend para as imagens atuais e anteriores devem totalizar 1,0. Por exemplo, se **fCurrBlendCoef** for definido como 0,5 e **fPrevBlendCoef** for definido como 0,5, o quadro de saída será composto de uma combinação igual das regiões de interesse de ambas as imagens.

Ao manipular a região de interesse de uma imagem, você pode criar efeitos panorâmicos e de zoom. Os coeficientes de Blend permitem que você entre gradualmente (dissolver) entre imagens. Além desses efeitos, você pode usar uma das transições predefinidas para criar quadros mais complexos. As transições disponíveis são descritas na seção [transições de imagem de vídeo](video-image-transitions.md) desta documentação. Ao usar uma transição, você deve configurar cada quadro. A maneira mais fácil de fazer isso é criar uma função que altere de forma incremental os membros da estrutura **WMT \_ VIDEOIMAGE \_ SAMPLE2** para um efeito completo.

Para obter mais informações sobre os valores a serem definidos para as deformações, consulte [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2).

**Observação** Se desejar incluir áudio em um arquivo com um fluxo de imagem de vídeo, você deverá usar a entrada de áudio não compactada. Para combinar um fluxo de imagem de vídeo com um fluxo de áudio compactado existente, você deve descompactar o áudio e passar os exemplos em não compactado. Se você passar amostras compactadas para o gravador ao gravar um fluxo de imagem de vídeo, ocorrerá um erro, resultando em amostras sendo descartadas do vídeo.

Além disso, arquivos de imagem de vídeo compactados sem fluxos de áudio podem conter vários quadros de vídeo muito pequenos e altamente compactados em um único pacote ASF, o que pode resultar em uma experiência de reprodução ruim em versões anteriores do Windows Media Player. Para evitar esse problema, a melhor solução é inserir um fluxo de áudio silencioso no arquivo, embora isso também aumente o tamanho do arquivo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Imagem de vídeo**](video-image.md)
</dt> <dt>

[**Gravando arquivos ASF**](writing-asf-files.md)
</dt> </dl>

 

 




