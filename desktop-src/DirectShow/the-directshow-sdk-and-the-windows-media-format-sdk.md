---
description: O DirectShow SDK e o SDK Windows Formato de Mídia
ms.assetid: d9ac89cc-0d55-4c51-ae0a-592422d97383
title: O DirectShow SDK e o SDK Windows Formato de Mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993f7ea0c9ac47861547cc08662fcb7916c3587c566445960505fe05a5c3d37a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651753"
---
# <a name="the-directshow-sdk-and-the-windows-media-format-sdk"></a>O DirectShow SDK e o SDK Windows Formato de Mídia

DirectShow e o SDK Windows Formato de Mídia do Windows oferecem soluções complementares para escrever aplicativos que criam e reproduzem Windows de Formato de Mídia. Para obter mais informações, consulte a seção "[Áudio](../audio-and-video.md)e Vídeo " do Biblioteca MSDN.

O filtro AsF Writer aceita qualquer número de fluxos de entrada e cria um arquivo ASF. O filtro usa o SDK Windows Formato de Mídia para converter arquivos de áudio ou vídeo descompactados Windows conteúdo baseado em mídia. O conteúdo compactado é armazenado no formato de contêiner ASF. Se o conteúdo for somente áudio, o arquivo recebe uma extensão .wma e é chamado de arquivo Windows Media Audio. Se o conteúdo for somente vídeo ou vídeo e áudio, o arquivo recebe uma extensão .wmv e é conhecido como um arquivo Windows Vídeo de Mídia. Qualquer tipo de arquivo também pode incluir metadados.

Você pode usar o Gravador do WM ASF em vários cenários, incluindo captura de DV (vídeo digital), re Audio-Video compactação de áudio e conversão de arquivos de multimídia INTERcalados (AVI) ou MPEG para streaming de rede. Esse filtro fornece a única maneira de criar arquivos WMA (Microsoft® Windows Media™ Audio (WMA) e WMV (Windows Media Video) no DirectShow®. O filtro também pode criar arquivos protegidos pelo DRM (Digital Rights Management) e também pode criar conteúdo MPEG-4 usando o Codificador MpEG-4 da Microsoft. Esse conteúdo é armazenado no formato de contêiner ASF.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md)
</dt> </dl>

 

 
