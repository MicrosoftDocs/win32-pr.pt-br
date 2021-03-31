---
title: Para buscar por número de quadro usando o leitor síncrono
description: Para buscar por número de quadro usando o leitor síncrono
ms.assetid: 755e0124-de57-4699-af8e-c594567b5523
keywords:
- ASF (Advanced Systems Format), buscando por números de quadro
- ASF (formato de sistemas avançados), busca por números de quadro
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- leitores síncronos, procurando por números de quadro
- fluxos de vídeo, buscando por números de quadro
- fluxos de vídeo, leitores síncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c26711d2d839e47279e7e52a50f5dc82c6e81da
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293770"
---
# <a name="to-seek-by-frame-number-using-the-synchronous-reader"></a><span data-ttu-id="496b5-110">Para buscar por número de quadro usando o leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="496b5-110">To Seek By Frame Number Using the Synchronous Reader</span></span>

<span data-ttu-id="496b5-111">Para procurar dados por número de quadro usando o leitor síncrono, especifique um intervalo para reprodução.</span><span class="sxs-lookup"><span data-stu-id="496b5-111">To seek for data by frame number using the synchronous reader, you specify a range for playback.</span></span> <span data-ttu-id="496b5-112">Um intervalo é definido por um número de quadro inicial em um fluxo de vídeo específico e um número de quadros a serem reproduzidos.</span><span class="sxs-lookup"><span data-stu-id="496b5-112">A range is defined by a starting frame number in a specific video stream and a number of frames to play.</span></span>

<span data-ttu-id="496b5-113">Para buscar dados em um arquivo ASF por número de quadro usando o leitor síncrono, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="496b5-113">To seek data in an ASF file by frame number using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="496b5-114">Defina o número do quadro inicial e o número de quadros a serem lidos para a entrega de exemplo chamando [**IWMSyncReader:: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span><span class="sxs-lookup"><span data-stu-id="496b5-114">Set the starting frame number and number of frames to read for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="496b5-115">Você deve especificar o número de fluxo de um fluxo de vídeo indexado por quadro.</span><span class="sxs-lookup"><span data-stu-id="496b5-115">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="496b5-116">O leitor sincronizará o restante das saídas com o tempo de apresentação do quadro especificado do fluxo especificado e começará a fornecer amostras de saída.</span><span class="sxs-lookup"><span data-stu-id="496b5-116">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
2.  <span data-ttu-id="496b5-117">Comece a recuperar exemplos com chamadas para [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="496b5-117">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="496b5-118">Prossiga normalmente com o leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="496b5-118">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="496b5-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="496b5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="496b5-120">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="496b5-120">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="496b5-121">**Lendo arquivos com o leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="496b5-121">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




