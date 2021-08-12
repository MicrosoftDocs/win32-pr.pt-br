---
description: Usando Windows mídia em DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Usando Windows mídia em DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fea308943d4be732c75e774d3e0c3cb09ac7c6609a8399d2e6eca4666d99e6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651082"
---
# <a name="using-windows-media-in-directshow"></a>Usando Windows mídia em DirectShow

Esta seção descreve como usar o DirectShow para reproduzir e gravar arquivos ASF (Advanced Systems Format). Os arquivos ASF normalmente contêm conteúdo de áudio e vídeo codificado usando os codecs Windows Media Audio and Video. No entanto, o ASF pode conter qualquer tipo de dados.

Os seguintes filtros DirectShow suporte à leitura e à escrita de arquivos ASF:

-   [Filtro de Leitor do WM ASF](wm-asf-reader-filter.md). Lê arquivos ASF.
-   [Filtro do Wm ASF Writer](wm-asf-writer-filter.md). Wrties arquivos ASF.
-   [DMO filtro wrapper](dmo-wrapper-filter.md). Envolve os DMOs Windows decodificador e codificador de mídia.

### <a name="versions"></a>Versões

Os filtros Wm ASF Reader e WM ASF Writer são empacotados na DLL chamada qasf.dll, e os filtros são coletivamente chamados de "componentes QASF". Esses filtros são wrappers para o SDK Windows Formato de Mídia. A DLL (qasf.dll) foi publicada pela primeira vez no SDK do DirectX, mas foi atualizada posteriormente no SDK Windows Formato de Mídia. Este é o histórico de versão dos filtros qaSF:

-   DirectShow 8.1 dá suporte Windows SDK de Formato de Mídia versão 7.0.
-   DirectShow 9.0 dá suporte Windows SDK de Formato de Mídia versão 7.1.
-   Windows O XP Service Pack 2 dá suporte Windows SDK de Formato de Mídia 9.
-   Windows O Vista dá suporte Windows SDK de Formato de Mídia 11.
-   Windows O SDK de Formato de Mídia 9 e posteriores contêm versões correspondentes do QASF.

Para obter a versão mais recente do QASF, sempre baixe o SDK Windows Formato de Mídia mais recente.

### <a name="legacy-windows-media-source-filter"></a>Filtro de fonte Windows mídia herdado

No Windows XP Service Pack 1 e anterior, o filtro de origem padrão para arquivos ASF (extensões de arquivo .asf, .wmv e .wma) é o filtro de fonte de mídia obsoleto [Windows](windows-media-source-filter.md). Esse comportamento foi mantido para garantir a compatibilidade com aplicativos que usaram o Windows Media Player 6.4. Novos aplicativos devem usar as versões mais recentes do QASF, que fazem com que o Leitor do WM ASF filtre o filtro padrão para reprodução de arquivos ASF.

Para obter mais informações sobre o Windows media de kits de desenvolvimento de software, consulte a seção [Áudio](../audio-and-video.md) e Vídeo da Biblioteca MDSN.

Este artigo contém os seguintes tópicos:

-   [Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
-   [Criando arquivos ASF no DirectShow](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando DirectShow](using-directshow.md)
</dt> </dl>

 

 
