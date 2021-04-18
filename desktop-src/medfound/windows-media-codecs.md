---
description: Os codecs de áudio e vídeo do Windows Media são uma coleção de objetos que você pode usar para compactar e descompactar dados de mídia digital.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Codificações de mídia do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec98f98fbd0561b291dfc4cc18e4270bf363baf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105781375"
---
# <a name="windows-media-codecs"></a>Codificações de mídia do Windows

Os codecs de áudio e vídeo do Windows Media são uma coleção de objetos que você pode usar para compactar e descompactar dados de mídia digital. Cada codec consiste em dois objetos, um codificador e um decodificador. Esta parte da documentação descreve como usar os recursos dos codecs de áudio e vídeo do Windows Media para produzir e consumir fluxos de dados compactados.

> [!Note]  
> Esta documentação destina-se principalmente aos desenvolvedores que desejam usar os codecs de mídia do Windows em seus aplicativos de mídia baseados em C++. Para obter uma visão geral técnica dos recursos dos codecs de mídia do Windows, consulte [sobre os codecs de mídia do Windows](about-the-windows-media-codecs.md).

 

O termo *codec* é uma ajuntamento do compressor de termos e do descompactador. Um codec geralmente é implementado como um par de objetos COM: um para codificar conteúdo e outro para decodificar conteúdo. Em alguns casos, os objetos COM ocupam a mesma biblioteca de vínculos dinâmicos (DLL).

Cada objeto de codec implementa duas interfaces separadas, mas semelhantes:



| Interface                              | Descrição                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatível com Microsoft Media Foundation. |
| [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatível com o DirectShow.                 |



 

Não só há codecs diferentes para áudio e vídeo, mas também codecs diferentes para tipos diferentes de conteúdo que você pode querer colocar em um arquivo de áudio ou de vídeo. Os algoritmos usados para compactar e descompactar dados de palavras faladas diferem dos algoritmos usados para compactar e descompactar dados de música.

## <a name="codec-descriptions"></a>Descrições de codec

A tabela a seguir descreve os usos pretendidos dos codecs de mídia do Windows.



| Codec                                                                     | Descrição                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Áudio do Windows Media](windowsmediaaudioencoder.md)                       | Um codec de áudio que dá suporte a três categorias de conteúdo codificado: Standard, Professional e Lossless.                                                                                                                                                                                      |
| [Voz de áudio do Windows Media](windowsmediaaudiovoiceencoder.md)            | Codec de áudio otimizado para codificar a voz humana em altas taxas de compactação. Esse é o codec preferencial para fluxos que consistem principalmente em palavras faladas. Para o conteúdo que é música e fala mista, esse codec pode alterar dinamicamente o algoritmo de codificação usado para obter a qualidade ideal. |
| [Vídeo do Windows Media 9](windowsmediavideo9encoder.md)                    | Um codec de vídeo que dá suporte a quatro categorias de conteúdo codificado: perfil simples, perfil principal, perfil avançado e imagem..                                                                                                                                                                  |
| [Tela do Windows Media Video 9](usingthewindowsmediavideo9screencodec.md) | Codec de vídeo otimizado para codificação de capturas de tela sequenciais de monitores de computador. Esse codec é geralmente usado para treinamento de software ou suporte ao gravar imagens de monitor enquanto os aplicativos de computador estão sendo usados.                                                                         |



 

As versões mais recentes dos objetos de codec também habilitam o acesso a alguns codecs herdados, incluindo o Windows Media Video 7 e 8, Windows Media tela 7, os codecs mais antigos do Microsoft MPEG-4 e os codecs ISO MPEG-4 da Microsoft.

> [!Note]  
> Esta documentação não aborda esses codecs herdados; Ele abrange apenas as versões atuais dos codecs.

 

Para codecs mais antigos, use os mesmos procedimentos que ao usar os codecs atuais; no entanto, lembre-se de que nem todos os recursos têm suporte em todos os codecs.

## <a name="in-this-section"></a>Nesta seção

-   [Sobre os codecs de mídia do Windows](about-the-windows-media-codecs.md)
-   [Usando os objetos codec e DSP](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [Métodos de codificação](encodingmethods.md)
-   [Implementação de codec](codecimplementation.md)
-   [O modelo de buffer de buckets vazados](the-leaky-bucket-buffer-model.md)
-   [Trabalhando com codec DMOs](workingwithcodecdmos.md)
-   [Trabalhando com codec MFTs](workingwithcodecmfts.md)
-   [Trabalhando com áudio](workingwithaudio.md)
-   [Trabalhando com vídeo](workingwithvideo.md)
-   [Armazenando mídia compactada em arquivos AVI](storingcompressedmediainavifiles.md)
-   [Usando a codificação de VBR](usingvbrencoding.md)
-   [Usando a codificação Two-Pass](usingtwoencodingpasses.md)
-   [Obtendo estatísticas de codificação](gettingencodingstatistics.md)
-   [Usando extensões de unidade de dados](usingdataunitextensions.md)
-   [Constantes IPropertyBag de codec e DSP](codecanddspproperties.md)
-   [Analisador de Sumário](toc-parser.md)
-   [Perguntas frequentes sobre o Windows Media Codec](frequentlyaskedquestions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Tecnologias de mídia para Windows](/previous-versions/bg125389(v=msdn.10))
</dt> </dl>

 

 
