---
title: Para obter estatísticas do gravador
description: Para obter estatísticas do gravador
ms.assetid: 81d7f567-0d99-4199-9248-1a497dc2eaab
keywords:
- Formato de sistema avançado (ASF), estatísticas do gravador
- ASF (formato de sistemas avançados), estatísticas do gravador
- estatísticas do gravador, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8c6620a2410b08d4d605c4dc116366c24b1e52c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103917068"
---
# <a name="to-get-writer-statistics"></a><span data-ttu-id="dd061-106">Para obter estatísticas do gravador</span><span class="sxs-lookup"><span data-stu-id="dd061-106">To Get Writer Statistics</span></span>

<span data-ttu-id="dd061-107">O gravador pode fornecer informações estatísticas sobre as operações de gravação.</span><span class="sxs-lookup"><span data-stu-id="dd061-107">The writer can provide statistical information about writing operations.</span></span> <span data-ttu-id="dd061-108">Há dois métodos para a coleta de estatísticas do gravador: [**IWMWriterAdvanced:: Getstatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) e [**IWMWriterAdvanced3:: GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex).</span><span class="sxs-lookup"><span data-stu-id="dd061-108">There are two methods for gathering writer statistics: [**IWMWriterAdvanced::GetStatistics**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics) and [**IWMWriterAdvanced3::GetStatisticsEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex).</span></span> <span data-ttu-id="dd061-109">As informações recuperadas pelo **GetStatisticsEx** são mais específicas do que as informações recuperadas por **getstatistics**.</span><span class="sxs-lookup"><span data-stu-id="dd061-109">The information retrieved by **GetStatisticsEx** is more specific than the information retrieved by **GetStatistics**.</span></span>

<span data-ttu-id="dd061-110">Ambos os métodos populam estruturas com informações estatísticas.</span><span class="sxs-lookup"><span data-stu-id="dd061-110">Both methods populate structures with statistical information.</span></span> <span data-ttu-id="dd061-111">**Getstatistics** usa a estrutura de [**\_ \_ estatísticas do gravador do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) e o **GetStatisticsEx** usa a estrutura de exemplo de [**estatísticas do gravador do WM \_ \_ \_**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) .</span><span class="sxs-lookup"><span data-stu-id="dd061-111">**GetStatistics** uses the [**WM\_WRITER\_STATISTICS**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics) structure, and **GetStatisticsEx** uses the [**WM\_WRITER\_STATISTICS\_EX**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex) structure.</span></span> <span data-ttu-id="dd061-112">**GetStatisticsEx** não duplica os dados obtidos por **getstatistics**.</span><span class="sxs-lookup"><span data-stu-id="dd061-112">**GetStatisticsEx** does not duplicate the data obtained by **GetStatistics**.</span></span> <span data-ttu-id="dd061-113">Para obter as informações mais completas, você deve chamar os dois métodos.</span><span class="sxs-lookup"><span data-stu-id="dd061-113">For the most complete information, you should call both methods.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dd061-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dd061-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd061-115">**Interface IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="dd061-115">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="dd061-116">**Interface IWMWriterAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="dd061-116">**IWMWriterAdvanced3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3)
</dt> <dt>

[<span data-ttu-id="dd061-117">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="dd061-117">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




