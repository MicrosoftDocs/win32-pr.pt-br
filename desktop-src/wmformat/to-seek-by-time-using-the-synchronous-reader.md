---
title: Para buscar por tempo usando o leitor síncrono
description: Para buscar por tempo usando o leitor síncrono
ms.assetid: 143f72b0-9d71-4efa-b8d4-5cde53a2aa2a
keywords:
- ASF (Advanced Systems Format), buscando por tempo
- ASF (formato de sistemas avançados), buscando por tempo
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- leitores síncronos, buscando por tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a43e914a6fc0d320860db61f4747cbee3033e9
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640161"
---
# <a name="to-seek-by-time-using-the-synchronous-reader"></a><span data-ttu-id="fd7d5-108">Para buscar por tempo usando o leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="fd7d5-108">To Seek By Time Using the Synchronous Reader</span></span>

<span data-ttu-id="fd7d5-109">Para procurar dados usando o leitor síncrono, especifique um intervalo para reprodução.</span><span class="sxs-lookup"><span data-stu-id="fd7d5-109">To seek for data using the synchronous reader, you specify a range for playback.</span></span> <span data-ttu-id="fd7d5-110">Um intervalo é definido por uma hora de apresentação inicial e uma duração, tanto em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="fd7d5-110">A range is defined by a starting presentation time and a duration, both in 100-nanosecond units.</span></span>

<span data-ttu-id="fd7d5-111">Para buscar dados em um arquivo ASF por hora de apresentação usando o leitor síncrono, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="fd7d5-111">To seek data in an ASF file by presentation time using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="fd7d5-112">Especifique uma hora e duração de início para a entrega de exemplo chamando [**IWMSyncReader:: SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange).</span><span class="sxs-lookup"><span data-stu-id="fd7d5-112">Specify a starting time and duration for sample delivery by calling [**IWMSyncReader::SetRange**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrange).</span></span> <span data-ttu-id="fd7d5-113">Esse método não exige que você especifique um número de fluxo porque os horários de apresentação de cada fluxo já devem estar sincronizados.</span><span class="sxs-lookup"><span data-stu-id="fd7d5-113">This method does not require you to specify a stream number because the presentation times of each stream should already be synchronized.</span></span>
2.  <span data-ttu-id="fd7d5-114">Comece a recuperar exemplos com chamadas para [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="fd7d5-114">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="fd7d5-115">Prossiga normalmente com o leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="fd7d5-115">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fd7d5-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fd7d5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd7d5-117">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="fd7d5-117">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="fd7d5-118">**Lendo arquivos com o leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="fd7d5-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




