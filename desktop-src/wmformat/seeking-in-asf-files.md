---
title: procurando arquivos ASF (Windows Media Format 11 SDK)
description: saiba como o leitor ASF do WM pode executar uma busca temporal muito precisa em Windows conteúdo baseado em mídia que tem um índice temporal no SDK do formato de mídia 11 do Windows.
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows SDK do formato de mídia, buscando arquivos ASF
- Windows SDK do formato de mídia, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), buscando
- ASF (formato de sistemas avançados), buscando
- DirectShow, buscando arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6730f1535c9601cfd0697e374ddfa35b05250ed49fc4b575fa3458b69e389285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845891"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>procurando arquivos ASF (Windows Media Format 11 SDK)

o [leitor ASF do WM](wm-asf-reader-filter.md), por meio de sua interface **IMediaSeeking** , pode executar uma busca temporal muito precisa em Windows conteúdo baseado em mídia que tem um índice temporal. (Todo conteúdo indexado por quadro também contém um índice temporal.) A busca com precisão de quadro garantido não tem suporte direto no leitor ASF do WM, mas há uma maneira de fazer isso se você precisar dessa funcionalidade. primeiro, use o SDK do formato de mídia Windows diretamente para criar uma instância do objeto leitor síncrono, abra o arquivo, obtenha o carimbo de data/hora associado a um quadro especificado e, em seguida, use a interface **IMediaSeeking** DirectShow para buscar esse horário. a interface do DirectShow **IVideoFrameStep** não dá suporte à busca com precisão de quadro de conteúdo baseado em mídia de Windows. o exemplo DSSeekFm no SDK do formato de mídia Windows demonstra como executar a busca precisa de quadro usando o leitor ASF do WM.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Filtro de leitor ASF do WM**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




