---
title: Buscando arquivos ASF (SDK Windows Media Format 11)
description: Saiba como o Leitor do WM ASF pode executar uma busca temporal muito precisa no conteúdo baseado em Mídia do Windows que tem um índice temporal no SDK Windows Media Format 11.
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows Media Format SDK, buscando em arquivos ASF
- Windows Media Format SDK, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), buscando
- ASF (Formato de Sistemas Avançados), buscando
- DirectShow, buscando em arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 807631861cdc820457360058f22fca380fca29ea
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409879"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>Buscando arquivos ASF (SDK Windows Media Format 11)

O [Leitor do WM ASF,](wm-asf-reader-filter.md)por meio de sua interface **IMediaSeeking,** pode executar uma busca temporal muito precisa no conteúdo baseado em Mídia do Windows que tem um índice temporal. (Todo o conteúdo indexado por quadro também contém um índice temporal.) A busca com precisão de quadro garantida não tem suporte direto no Leitor do WM ASF, mas há uma maneira de fazer isso se você precisar dessa funcionalidade. Primeiro, use o SDK do Windows Media Format diretamente para criar uma instância do objeto de leitor síncrono, abra o arquivo, obtenha o carimbo de data/hora associado a um quadro especificado e, em seguida, use a interface **DirectShow IMediaSeeking** para buscar até esse momento. A interface **IVideoFrameStep** do DirectShow não dá suporte à busca precisa de quadros de conteúdo baseado em mídia do Windows. O exemplo DSSeekFm no SDK do Windows Media Format demonstra como executar a busca com precisão de quadro usando o Leitor do WM ASF.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Filtro de Leitor do WM ASF**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




