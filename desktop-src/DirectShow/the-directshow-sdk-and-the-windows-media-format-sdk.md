---
description: O SDK do DirectShow e o Windows Media Format SDK
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: O SDK do DirectShow e o Windows Media Format SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f85c5553c9a1cdd3f62380c9fc90d836a47a650
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297981"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a>O SDK do DirectShow e o Windows Media Format SDK

O DirectShow e o Windows Media Format SDK oferecem soluções complementares para a gravação de aplicativos que criam e reproduzem fluxos de formato de mídia do Windows. Para obter mais informações, consulte a seção "[áudio e vídeo](../audio-and-video.md)" da biblioteca MSDN.

O filtro do gravador ASF aceita qualquer número de fluxos de entrada e cria um arquivo ASF. O filtro usa o Windows Media Format SDK para converter arquivos de áudio ou vídeo não compactados em conteúdo baseado no Windows Media. O conteúdo compactado é armazenado no formato de contêiner ASF. Se o conteúdo for somente áudio, o arquivo receberá uma extensão. WMA e será chamado de arquivo de áudio do Windows Media. Se o conteúdo for somente vídeo ou vídeo e áudio, o arquivo receberá uma extensão. wmv e será chamado de arquivo de vídeo do Windows Media. Qualquer um dos tipos de arquivo também pode incluir metadados.

Você pode usar o gravador ASF do WM em vários cenários, incluindo captura Audio-Video de vídeo digital (DV), recompactação de áudio e conversão de arquivos multimídia intercalados (AVI) ou MPEG para transmissão de rede. Esse filtro fornece a única maneira de criar arquivos do Microsoft® Windows Media™ Audio (WMA) e do Windows Media Video (WMV) no DirectShow®. O filtro também pode criar arquivos protegidos por DRM (Rights Management digital) e também pode criar conteúdo MPEG-4 usando o codificador MPEG-4 da Microsoft. Esse conteúdo é armazenado no formato de contêiner ASF.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
