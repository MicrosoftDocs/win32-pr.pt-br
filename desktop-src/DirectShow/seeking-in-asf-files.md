---
description: Saiba como o leitor ASF do WM pode executar uma busca temporal muito precisa no conteúdo baseado no Windows Media que tem um índice temporal no DirectShow.
ms.assetid: da0d687b-f571-4623-9705-e697ba8bc04e
title: Procurando em arquivos ASF (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92ffc570536463b86a88e1f26be338bd748c790c
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405579"
---
# <a name="seeking-in-asf-files-directshow"></a>Procurando em arquivos ASF (DirectShow)

O [leitor ASF do WM](wm-asf-reader-filter.md), por meio de sua interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , pode executar uma busca temporal muito precisa no conteúdo baseado no Windows Media que tem um índice temporal. (Todo conteúdo indexado por quadro também contém um índice temporal.) A busca com precisão de quadro garantido não tem suporte direto no leitor ASF do WM, mas há uma maneira de fazer isso se você precisar dessa funcionalidade. Primeiro, use o SDK do Windows Media Format diretamente para criar uma instância do objeto leitor síncrono, abra o arquivo, obtenha o carimbo de data/hora associado a um quadro especificado e, em seguida, use a interface **IMediaSeeking** do DirectShow para buscar esse horário. A interface [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) não oferece suporte à busca de conteúdo baseado no Windows Media com precisão de quadro.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Lendo arquivos ASF no DirectShow](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



