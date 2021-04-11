---
title: Procurando arquivos ASF (SDK do Windows Media Format 11)
description: Procurando em arquivos ASF
ms.assetid: a1717cb4-9f41-4148-b088-a6517be7da9b
keywords:
- SDK do Windows Media Format, buscando arquivos ASF
- SDK do Windows Media Format, DirectShow
- ASF (Advanced Systems Format), DirectShow
- ASF (formato de sistemas avançados), DirectShow
- ASF (Advanced Systems Format), buscando
- ASF (formato de sistemas avançados), buscando
- DirectShow, buscando arquivos ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18389ded80f0202564cba0ce6384b5ff02d26fdd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008693"
---
# <a name="seeking-in-asf-files-windows-media-format-11-sdk"></a><span data-ttu-id="c7521-110">Procurando arquivos ASF (SDK do Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="c7521-110">Seeking in ASF Files (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="c7521-111">O [leitor ASF do WM](wm-asf-reader-filter.md), por meio de sua interface **IMediaSeeking** , pode executar uma busca temporal muito precisa no conteúdo baseado no Windows Media que tem um índice temporal.</span><span class="sxs-lookup"><span data-stu-id="c7521-111">The [WM ASF Reader](wm-asf-reader-filter.md), through its **IMediaSeeking** interface, can perform very accurate temporal seeking on Windows Media–based content that has a temporal index.</span></span> <span data-ttu-id="c7521-112">(Todo conteúdo indexado por quadro também contém um índice temporal.) A busca com precisão de quadro garantido não tem suporte direto no leitor ASF do WM, mas há uma maneira de fazer isso se você precisar dessa funcionalidade.</span><span class="sxs-lookup"><span data-stu-id="c7521-112">(All frame-indexed content also contains a temporal index.) Guaranteed frame-accurate seeking is not directly supported in the WM ASF Reader, but there is a way to do it if you require this functionality.</span></span> <span data-ttu-id="c7521-113">Primeiro, use o SDK do Windows Media Format diretamente para criar uma instância do objeto leitor síncrono, abra o arquivo, obtenha o carimbo de data/hora associado a um quadro especificado e, em seguida, use a interface **IMediaSeeking** do DirectShow para buscar esse horário.</span><span class="sxs-lookup"><span data-stu-id="c7521-113">First, use the Windows Media Format SDK directly to create an instance of the synchronous reader object, open the file, obtain the time stamp associated with a specified frame, and then use the DirectShow **IMediaSeeking** interface to seek to that time.</span></span> <span data-ttu-id="c7521-114">A interface do **IVideoFrameStep** do DirectShow não oferece suporte à busca de conteúdo baseado no Windows Media com precisão de quadro.</span><span class="sxs-lookup"><span data-stu-id="c7521-114">The DirectShow **IVideoFrameStep** interface does not support frame-accurate seeking of Windows Media–based content.</span></span> <span data-ttu-id="c7521-115">O exemplo DSSeekFm no SDK do Windows Media Format demonstra como executar a busca precisa de quadros usando o leitor ASF do WM.</span><span class="sxs-lookup"><span data-stu-id="c7521-115">The DSSeekFm sample in the Windows Media Format SDK demonstrates how to perform frame-accurate seeking using the WM ASF Reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7521-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c7521-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7521-117">**Filtro de leitor ASF do WM**</span><span class="sxs-lookup"><span data-stu-id="c7521-117">**WM ASF Reader Filter**</span></span>](wm-asf-reader-filter.md)
</dt> </dl>

 

 




