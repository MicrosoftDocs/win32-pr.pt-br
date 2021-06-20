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
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a><span data-ttu-id="9b026-110">Buscando arquivos ASF (SDK Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="9b026-110">Seeking in ASF Files (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="9b026-111">O [Leitor do WM ASF,](wm-asf-reader-filter.md)por meio de sua interface **IMediaSeeking,** pode executar uma busca temporal muito precisa no conteúdo baseado em Mídia do Windows que tem um índice temporal.</span><span class="sxs-lookup"><span data-stu-id="9b026-111">The [WM ASF Reader](wm-asf-reader-filter.md), through its **IMediaSeeking** interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="9b026-112">(Todo o conteúdo indexado por quadro também contém um índice temporal.) A busca com precisão de quadro garantida não tem suporte direto no Leitor do WM ASF, mas há uma maneira de fazer isso se você precisar dessa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="9b026-112">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="9b026-113">Primeiro, use o SDK do Windows Media Format diretamente para criar uma instância do objeto de leitor síncrono, abra o arquivo, obtenha o carimbo de data/hora associado a um quadro especificado e, em seguida, use a interface **DirectShow IMediaSeeking** para buscar até esse momento.</span><span class="sxs-lookup"><span data-stu-id="9b026-113">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="9b026-114">A interface **IVideoFrameStep** do DirectShow não dá suporte à busca precisa de quadros de conteúdo baseado em mídia do Windows.</span><span class="sxs-lookup"><span data-stu-id="9b026-114">The DirectShow **IVideoFrameStep** interface does not support frame-accurate seeking of Windows Media–based content.</span></span> <span data-ttu-id="9b026-115">O exemplo DSSeekFm no SDK do Windows Media Format demonstra como executar a busca com precisão de quadro usando o Leitor do WM ASF.</span><span class="sxs-lookup"><span data-stu-id="9b026-115">The DSSeekFm sample in the Windows Media Format SDK demonstrates how to perform frame-accurate seeking using the WM ASF Reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9b026-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9b026-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b026-117">**Filtro de Leitor do WM ASF**</span><span class="sxs-lookup"><span data-stu-id="9b026-117">**WM ASF Reader Filter**</span></span>](wm-asf-reader-filter.md)
</dt> </dl>

 

 




