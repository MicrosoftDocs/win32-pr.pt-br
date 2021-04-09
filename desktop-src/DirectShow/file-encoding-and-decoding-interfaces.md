---
description: Codificação de arquivos e interfaces de decodificação
ms.assetid: 5456392d-2557-43b6-93b7-b2ebde218d12
title: Codificação de arquivos e interfaces de decodificação
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f73de2304f2b473a634127755ca900b99592ed63
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104088803"
---
# <a name="file-encoding-and-decoding-interfaces"></a>Codificação de arquivos e interfaces de decodificação

Essas interfaces dão suporte à codificação e decodificação de arquivos.



| Interface                                                    | Descrição                                                                                                  |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent)                   | Recupere metadados de um fluxo, como o autor e o título.                                              |
| [**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress)                   | Determine o progresso de uma operação de abertura de arquivo.                                                             |
| [**IAMParse**](/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse)                                 | Consulte e defina o tempo de análise para a posição atual em um fluxo MPEG.                                     |
| [**IAMStreamSelect**](/windows/desktop/api/Strmif/nn-strmif-iamstreamselect)                   | Controlar quais fluxos lógicos são reproduzidos e recuperar informações sobre eles.                               |
| [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs)       | Exibir caixas de diálogo fornecidas por codecs VFW.                                                                 |
| [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression)           | Defina os parâmetros de compactação de vídeo.                                                                            |
| [**IConfigAsfWriter**](/previous-versions/windows/desktop/api/Dshowasf/nn-dshowasf-iconfigasfwriter)                 | Controle como o filtro do [gravador ASF do WM](wm-asf-writer-filter.md) grava arquivos ASF (Advanced Systems Format). |
| [**IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux)                       | Controle como o filtro [AVI Mux](avi-mux-filter.md) grava arquivos AVI.                                       |
| [**IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving)           | Configure a intercalação quando o filtro AVI Mux gravar arquivos AVI.                                             |
| [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc)                                     | Defina a resolução de codificação no filtro do [codificador de vídeo DV](dv-video-encoder-filter.md) .                   |
| [**IDVSplitter**](/windows/desktop/api/Strmif/nn-strmif-idvsplitter)                           | Fazer downgrade da taxa de quadros em um fluxo de vídeo digital (DV)                                                      |
| [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec)                                 | Defina a resolução de decodificação no filtro do [decodificador de vídeo DV](dv-video-decoder-filter.md) .                   |
| [**IPersistMediaPropertyBag**](/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag) | Definir e recuperar informações e partes de DISP em fluxos AVI.                                                        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces](interfaces.md)
</dt> </dl>

 

 



