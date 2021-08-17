---
description: Os Windows codecs de Áudio e Vídeo de Mídia são uma coleção de objetos que você pode usar para compactar e descompactar dados de mídia digital.
ms.assetid: 74de2e75-b1ee-436d-8d78-efe366ab7aa6
title: Codificações de mídia do Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 863bb21e17200016317ce273ecb8e2493b9d6bea7d19f92f3f397fb61b88eba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972525"
---
# <a name="windows-media-codecs"></a>Codificações de mídia do Windows

Os Windows codecs de Áudio e Vídeo de Mídia são uma coleção de objetos que você pode usar para compactar e descompactar dados de mídia digital. Cada codec consiste em dois objetos, um codificador e um decodificador. Esta parte da documentação descreve como usar os recursos dos codecs Windows Media Audio and Video para produzir e consumir fluxos de dados compactados.

> [!Note]  
> Esta documentação é principalmente para desenvolvedores que querem usar Windows de mídia em seus aplicativos de mídia baseados em C++. Para uma visão geral técnica dos recursos dos codecs Windows Media, consulte Sobre os [codecs Windows de mídia.](about-the-windows-media-codecs.md)

 

O termo *codec* é uma acumulação dos termos que você e o descompactador. Um codec geralmente é implementado como um par de objetos COM: um para codificação de conteúdo e outro para decodificação de conteúdo. Em alguns casos, os objetos COM ocupam a mesma DLL (biblioteca vinculada dinamicamente).

Cada objeto codec implementa duas interfaces separadas, mas semelhantes:



| Interface                              | Descrição                                 |
|----------------------------------------|---------------------------------------------|
| [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)   | Compatível com Microsoft Media Foundation. |
| [**Imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) | Compatível com DirectShow.                 |



 

Não apenas há codecs diferentes para áudio e vídeo, mas também codecs diferentes para diferentes tipos de conteúdo que você talvez queira colocar em um arquivo de áudio ou vídeo. Os algoritmos usados para compactar e descompactar dados para palavras faladas diferem dos algoritmos usados para compactar e descompactar dados de música.

## <a name="codec-descriptions"></a>Descrições do Codec

A tabela a seguir descreve os usos pretendido dos codecs Windows Media.



| Codec                                                                     | Descrição                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Áudio do Windows Media](windowsmediaaudioencoder.md)                       | Um codec de áudio que dá suporte a três categorias de conteúdo codificado: Standard, Professional e Lossless.                                                                                                                                                                                      |
| [Windows Voz de Áudio de Mídia](windowsmediaaudiovoiceencoder.md)            | Codec de áudio otimizado para codificar a voz humana em altas taxas de compactação. Esse é o codec preferencial para fluxos que consistem principalmente em palavras faladas. Para conteúdo que é música misturada e fala, esse codec pode alterar dinamicamente o algoritmo de codificação usado para obter a qualidade ideal. |
| [Windows Vídeo de mídia 9](windowsmediavideo9encoder.md)                    | Um codec de vídeo que dá suporte a quatro categorias de conteúdo codificado: Perfil Simples, Perfil Principal, Perfil Avançado e Imagem..                                                                                                                                                                  |
| [Windows Tela 9 do Vídeo de Mídia](usingthewindowsmediavideo9screencodec.md) | Codec de vídeo otimizado para codificar capturas de tela sequenciais de monitores de computador. Esse codec geralmente é usado para treinamento ou suporte de software gravando imagens de monitor enquanto os aplicativos de computador estão sendo usados.                                                                         |



 

As versões mais recentes dos objetos codec também permitem o acesso a alguns codecs herdados, incluindo o Vídeo de Mídia do Windows 7 e 8, a Tela de Mídia do Windows 7, os codecs do Microsoft MPEG-4 mais antigos e os codecs MPEG-4 do Microsoft ISO.

> [!Note]  
> Esta documentação não abrange esses codecs herddos; ele abrange apenas as versões atuais de codecs.

 

Para codecs mais antigos, use os mesmos procedimentos que ao usar os codecs atuais; no entanto, lembre-se de que nem todos os recursos têm suporte em todos os codecs.

## <a name="in-this-section"></a>Nesta seção

-   [Sobre os codecs Windows de mídia](about-the-windows-media-codecs.md)
-   [Usando os objetos Codec e DSP](decidinghowtousethewindowsmediaaudioandvideocodecs.md)
-   [Métodos de codificação](encodingmethods.md)
-   [Implementação do Codec](codecimplementation.md)
-   [O modelo de buffer de bucket vazado](the-leaky-bucket-buffer-model.md)
-   [Trabalhando com DMOs codec](workingwithcodecdmos.md)
-   [Trabalhando com MFTs codec](workingwithcodecmfts.md)
-   [Trabalhando com áudio](workingwithaudio.md)
-   [Trabalhando com vídeo](workingwithvideo.md)
-   [Armazenar mídia compactada em arquivos AVI](storingcompressedmediainavifiles.md)
-   [Usando a codificação VBR](usingvbrencoding.md)
-   [Usando Two-Pass codificação](usingtwoencodingpasses.md)
-   [Obter estatísticas de codificação](gettingencodingstatistics.md)
-   [Usando extensões de unidade de dados](usingdataunitextensions.md)
-   [Constantes Codec e DSP IPropertyBag](codecanddspproperties.md)
-   [Analisador de Tabela de Conteúdo](toc-parser.md)
-   [Windows Perguntas frequentes sobre Codec de Mídia](frequentlyaskedquestions.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia Media Foundation programação do Media Foundation](media-foundation-programming-guide.md)
</dt> <dt>

[Tecnologias de mídia para Windows](/previous-versions/bg125389(v=msdn.10))
</dt> </dl>

 

 
