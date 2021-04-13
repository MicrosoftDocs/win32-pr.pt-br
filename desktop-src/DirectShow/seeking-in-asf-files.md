---
description: Procurando em arquivos ASF
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Procurando em arquivos ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e957fbdf7ed7df1a9cb38b14e39d384b15ab25b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500359"
---
# <a name="seeking-in-asf-files-directshow"></a>Procurando em arquivos ASF (DirectShow)

O [leitor ASF do WM](wm-asf-reader-filter.md), por meio de sua interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , pode executar uma busca temporal muito precisa no conteúdo baseado no Windows Media que tem um índice temporal. (Todo conteúdo indexado por quadro também contém um índice temporal.) A busca com precisão de quadro garantido não tem suporte direto no leitor ASF do WM, mas há uma maneira de fazer isso se você precisar dessa funcionalidade. Primeiro, use o SDK do Windows Media Format diretamente para criar uma instância do objeto leitor síncrono, abra o arquivo, obtenha o carimbo de data/hora associado a um quadro especificado e, em seguida, use a interface **IMediaSeeking** do DirectShow para buscar esse horário. A interface [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) não oferece suporte à busca de conteúdo baseado no Windows Media com precisão de quadro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



