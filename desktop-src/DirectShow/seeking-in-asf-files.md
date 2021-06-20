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
# <a name="seeking-in-asf-files-directshow"></a><span data-ttu-id="d1012-103">Procurando em arquivos ASF (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="d1012-103">Seeking in ASF Files (DirectShow)</span></span>

<span data-ttu-id="d1012-104">O [leitor ASF do WM](wm-asf-reader-filter.md), por meio de sua interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) , pode executar uma busca temporal muito precisa no conteúdo baseado no Windows Media que tem um índice temporal.</span><span class="sxs-lookup"><span data-stu-id="d1012-104">The [WM ASF Reader](wm-asf-reader-filter.md), through its [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="d1012-105">(Todo conteúdo indexado por quadro também contém um índice temporal.) A busca com precisão de quadro garantido não tem suporte direto no leitor ASF do WM, mas há uma maneira de fazer isso se você precisar dessa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="d1012-105">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="d1012-106">Primeiro, use o SDK do Windows Media Format diretamente para criar uma instância do objeto leitor síncrono, abra o arquivo, obtenha o carimbo de data/hora associado a um quadro especificado e, em seguida, use a interface **IMediaSeeking** do DirectShow para buscar esse horário.</span><span class="sxs-lookup"><span data-stu-id="d1012-106">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="d1012-107">A interface [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) não oferece suporte à busca de conteúdo baseado no Windows Media com precisão de quadro.</span><span class="sxs-lookup"><span data-stu-id="d1012-107">The [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface does not support frame-accurate seeking of Windows Media–based content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d1012-108">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d1012-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1012-109">Lendo arquivos ASF no DirectShow</span><span class="sxs-lookup"><span data-stu-id="d1012-109">Reading ASF Files in DirectShow</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 



