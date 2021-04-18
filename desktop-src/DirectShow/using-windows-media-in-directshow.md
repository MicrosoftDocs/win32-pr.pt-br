---
description: Usando o Windows Media no DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Usando o Windows Media no DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104370820"
---
# <a name="using-windows-media-in-directshow"></a>Usando o Windows Media no DirectShow

Esta seção descreve como usar o DirectShow para reproduzir e gravar arquivos ASF (Advanced Systems Format). Normalmente, os arquivos ASF contêm conteúdo de áudio e vídeo codificado usando os codecs de áudio e vídeo do Windows Media. No entanto, o ASF pode conter qualquer tipo de dados.

Os seguintes filtros do DirectShow dão suporte à leitura e gravação de arquivos ASF:

-   [Filtro de leitor ASF do WM](wm-asf-reader-filter.md). Lê arquivos ASF.
-   [Filtro de gravador ASF do WM](wm-asf-writer-filter.md). Arquivos ASF Wrties.
-   [Filtro de invólucro de DMO](dmo-wrapper-filter.md). Encapsula o codificador do Windows Media e o decodificador DMOs.

### <a name="versions"></a>Versões

Os filtros do gravador ASF do WM e do escritor ASF do WM são empacotados na DLL chamada qasf.dll e os filtros são coletivamente nomeados "componentes QASF". Esses filtros são wrappers para o Windows Media Format SDK. A DLL (qasf.dll) foi publicada pela primeira vez no SDK do DirectX, mas foi atualizada posteriormente no SDK do Windows Media Format. Este é o histórico de versão dos filtros QASF:

-   O DirectShow 8,1 dá suporte à versão 7,0 do Windows Media Format SDK.
-   O DirectShow 9,0 dá suporte à versão 7,1 do Windows Media Format SDK.
-   O Windows XP Service Pack 2 dá suporte ao SDK do Windows Media Format 9.
-   O Windows Vista dá suporte ao SDK do Windows Media Format 11.
-   O SDK do Windows Media Format 9 e posterior contém versões correspondentes do QASF.

Para obter a versão mais recente do QASF, sempre Baixe o SDK do Windows Media Format mais recente.

### <a name="legacy-windows-media-source-filter"></a>Filtro de origem de mídia do Windows herdado

No Windows XP Service Pack 1 e versões anteriores, o filtro de origem padrão para arquivos ASF (. ASF,. wmv e extensões de arquivo. WMA) é o [filtro de origem de mídia do Windows](windows-media-source-filter.md)obsoleto. Esse comportamento foi mantido para garantir a compatibilidade com versões anteriores com aplicativos que usavam o Windows Media Player 6,4. Novos aplicativos devem usar as versões mais recentes do QASF, que tornam o filtro de leitor ASF do WM o filtro padrão para a reprodução de arquivos ASF.

Para obter mais informações sobre o Windows Media Suite dos kits de desenvolvimento de software, consulte a seção [áudio e vídeo](../audio-and-video.md) da biblioteca MSDN.

Este artigo contém os seguintes tópicos:

-   [Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
-   [Criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando o DirectShow](using-directshow.md)
</dt> </dl>

 

 
