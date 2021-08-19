---
title: Buscando arquivos ASF (SDK Windows Media Format 11)
description: Saiba como o Leitor do WM ASF pode executar uma busca temporal muito precisa em um conteúdo baseado em mídia Windows que tenha um índice temporal no SDK Windows Media Format 11.
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- Windows SDK de Formato de Mídia, buscando em arquivos ASF
- Windows SDK de formato de mídia, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), buscando
- ASF (Formato de Sistemas Avançados), buscando
- DirectShow, buscando em arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6730f1535c9601cfd0697e374ddfa35b05250ed49fc4b575fa3458b69e389285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845891"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a>Buscando arquivos ASF (SDK Windows Media Format 11)

O [Leitor do WM ASF](wm-asf-reader-filter.md), por meio de sua interface **IMediaSeeking,** pode executar uma busca temporal muito precisa Windows conteúdo baseado em mídia que tem um índice temporal. (Todo o conteúdo indexado por quadro também contém um índice temporal.) A busca com precisão de quadro garantida não tem suporte direto no Leitor do WM ASF, mas há uma maneira de fazer isso se você precisar dessa funcionalidade. Primeiro, use o SDK de Formato de Mídia do Windows diretamente para criar uma instância do objeto de leitor síncrono, abra o arquivo, obtenha o carimbo de data/hora associado a um quadro especificado e, em seguida, use a interface **DirectShow IMediaSeeking** para buscar até esse momento. A DirectShow **interface IVideoFrameStep** não dá suporte à busca precisa de quadro Windows conteúdo baseado em mídia. O exemplo DSSeekFm no SDK Windows Formato de Mídia do Windows demonstra como executar a busca com precisão de quadro usando o Leitor do WM ASF.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Filtro de Leitor do WM ASF**](wm-asf-reader-filter.md)
</dt> </dl>

 

 




