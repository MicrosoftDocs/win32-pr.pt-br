---
description: Formatos de hora para comandos de busca
ms.assetid: d9c1b860-f75f-4886-95d6-c62e9e5b69eb
title: Formatos de hora para comandos de busca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8217873a9443c2b56c60523f95a6fe599ee045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506285"
---
# <a name="time-formats-for-seek-commands"></a><span data-ttu-id="90935-103">Formatos de hora para comandos de busca</span><span class="sxs-lookup"><span data-stu-id="90935-103">Time Formats For Seek Commands</span></span>

<span data-ttu-id="90935-104">Muitos dos métodos na interface **IMediaSeeking** têm parâmetros que expressam valores de posição, como posição atual ou posição de parada.</span><span class="sxs-lookup"><span data-stu-id="90935-104">Many of the methods in the **IMediaSeeking** interface have parameters that express position values, such as current position or stop position.</span></span> <span data-ttu-id="90935-105">Por padrão, esses parâmetros são expressos em unidades de 100 nanossegundos, também chamados de tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="90935-105">By default, these parameters are expressed in units of 100 nanoseconds, also called reference time.</span></span> <span data-ttu-id="90935-106">Qualquer filtro que possa buscar deve dar suporte à busca por tempo de referência.</span><span class="sxs-lookup"><span data-stu-id="90935-106">Any filter that can seek must support seeking by reference time.</span></span> <span data-ttu-id="90935-107">Alguns filtros também podem buscar usando outras unidades de tempo, como procurar um número de quadro específico ou procurar um determinado deslocamento de byte dentro de um fluxo.</span><span class="sxs-lookup"><span data-stu-id="90935-107">Some filters can seek using other units of time as well, such as seeking to a particular frame number, or seeking to a given byte offset within a stream.</span></span> <span data-ttu-id="90935-108">Cada uma dessas unidades de tempo é chamada de formato de hora e é definida por um GUID (identificador global exclusivo).</span><span class="sxs-lookup"><span data-stu-id="90935-108">Each of these time units is called a time format, and is defined by a globally unique identifier (GUID).</span></span> <span data-ttu-id="90935-109">Para obter uma lista dos formatos de hora definidos pelo DirectShow, consulte [**GUIDs de formato de tempo**](time-format-guids.md).</span><span class="sxs-lookup"><span data-stu-id="90935-109">For a list of the time formats that are defined by DirectShow, see [**Time Format GUIDs**](time-format-guids.md).</span></span> <span data-ttu-id="90935-110">Terceiros também podem definir GUIDs para formatos de hora personalizados.</span><span class="sxs-lookup"><span data-stu-id="90935-110">Third parties can also define GUIDs for custom time formats.</span></span>

<span data-ttu-id="90935-111">Para determinar se os filtros atualmente no grafo de filtro dão suporte a um formato de hora específico, chame o método [**IMediaSeeking:: IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) .</span><span class="sxs-lookup"><span data-stu-id="90935-111">To determine whether the filters currently in the filter graph support a particular time format, call the [**IMediaSeeking::IsFormatSupported**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isformatsupported) method.</span></span> <span data-ttu-id="90935-112">O método retornará S \_ OK se o formato tiver suporte.</span><span class="sxs-lookup"><span data-stu-id="90935-112">The method returns S\_OK if the format is supported.</span></span> <span data-ttu-id="90935-113">Caso contrário, retornará S \_ false ou um código de erro.</span><span class="sxs-lookup"><span data-stu-id="90935-113">Otherwise, it returns S\_FALSE or an error code.</span></span> <span data-ttu-id="90935-114">Se houver suporte para um formato, você poderá alternar para esse formato chamando o método [**IMediaSeeking:: SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) .</span><span class="sxs-lookup"><span data-stu-id="90935-114">If a format is supported, you can switch to that format by calling the [**IMediaSeeking::SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method.</span></span> <span data-ttu-id="90935-115">Se o método **SetTimeFormat** for executado com sucesso, os comandos de busca subsequentes serão expressos usando o novo formato de hora.</span><span class="sxs-lookup"><span data-stu-id="90935-115">If the **SetTimeFormat** method succeeds, subsequent seek commands are expressed using the new time format.</span></span>

<span data-ttu-id="90935-116">O exemplo a seguir verifica se o grafo dá suporte à busca por número de quadro.</span><span class="sxs-lookup"><span data-stu-id="90935-116">The follow example checks whether the graph supports seeking by frame number.</span></span> <span data-ttu-id="90935-117">Nesse caso, ele procura o número de quadro 20:</span><span class="sxs-lookup"><span data-stu-id="90935-117">If so, it seeks to frame number 20:</span></span>


```C++
hr = pSeek->IsFormatSupported(&TIME_FORMAT_FRAME);
if (hr == S_OK)
{
    hr = pSeek->SetTimeFormat(&TIME_FORMAT_FRAME);
    if (SUCCEEDED(hr))
    {
        // Seek to frame number 20.
        LONGLONG rtNow = 20;
        hr = pSeek->SetPositions(
            &rtNow, AM_SEEKING_AbsolutePositioning, 
            0, AM_SEEKING_NoPositioning);
    }
}
```



<span data-ttu-id="90935-118">Observe que os formatos de hora se aplicam apenas aos comandos de busca.</span><span class="sxs-lookup"><span data-stu-id="90935-118">Note that time formats only apply to seek commands.</span></span> <span data-ttu-id="90935-119">Eles não afetam a reprodução do grafo ou outras ações.</span><span class="sxs-lookup"><span data-stu-id="90935-119">They do not affect graph playback or other actions.</span></span>

 

 



