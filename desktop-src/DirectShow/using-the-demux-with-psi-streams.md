---
description: Usando o demux com fluxos PSI
ms.assetid: 355e905e-ff21-4bde-a018-ed9631ef5ed5
title: Usando o demux com fluxos PSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 659e4a12bfef25f24a5e6cac38d191f86ab80b4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105780551"
---
# <a name="using-the-demux-with-psi-streams"></a><span data-ttu-id="3e035-103">Usando o demux com fluxos PSI</span><span class="sxs-lookup"><span data-stu-id="3e035-103">Using the Demux with PSI Streams</span></span>

<span data-ttu-id="3e035-104">Para obter informações de PSI de um fluxo de transporte MPEG-2 usando o Filtro Demux MPEG-2, crie um PIN de saída no demux com o seguinte tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="3e035-104">To get PSI information from an MPEG-2 transport stream using the MPEG-2 demux filter, create an output pin on the demux with the following media type:</span></span>

-   <span data-ttu-id="3e035-105">Tipo principal: KSDATAFORMAT \_ tipo \_ de \_ seções MPEG2</span><span class="sxs-lookup"><span data-stu-id="3e035-105">Major type: KSDATAFORMAT\_TYPE\_MPEG2\_SECTIONS</span></span>
-   <span data-ttu-id="3e035-106">Subtipo: MEDIASUBTYPE \_ None</span><span class="sxs-lookup"><span data-stu-id="3e035-106">Subtype: MEDIASUBTYPE\_None</span></span>
-   <span data-ttu-id="3e035-107">Tipo de formato: GUID \_ NULL</span><span class="sxs-lookup"><span data-stu-id="3e035-107">Format type: GUID\_NULL</span></span>

<span data-ttu-id="3e035-108">Em seguida, chame o método [**IMPEG2PIDMap:: MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) do pino de saída com o PID desejado e o sinalizador de mídia \_ MPEG2 \_ psi.</span><span class="sxs-lookup"><span data-stu-id="3e035-108">Then call the output pin's [**IMPEG2PIDMap::MapPID**](/previous-versions/windows/desktop/api/Bdaiface/nf-bdaiface-impeg2pidmap-mappid) method with the desired PID and the flag MEDIA\_MPEG2\_PSI.</span></span>


```C++
// Query the demux filter for IMpeg2Demultiplexer.
IMpeg2Demultiplexer *pDemux = NULL;
hr = pFilter->QueryInterface(IID_IMpeg2Demultiplexer, (void**)&pDemux);
if (SUCCEEDED(hr))
{
    // Define the media type.
    AM_MEDIA_TYPE mt;
    ZeroMemory(&mt, sizeof(AM_MEDIA_TYPE));
    mt.majortype = KSDATAFORMAT_TYPE_MPEG2_SECTIONS;
    mt.subtype = MEDIASUBTYPE_None;

    // Create a new output pin.
    IPin *pPin;
    hr = pDemux->CreateOutputPin(&mt, L"PSI Pin", &pPin);
    if (SUCCEEDED(hr))
    {
        // Map the PID.
        IMPEG2PIDMap *pPidMap = NULL;
        hr = pPin->QueryInterface(IID_IMPEG2PIDMap, (void**)&pPidMap);
        if (SUCCEEDED(hr))
        {
            ULONG Pid[] = { 0x00 }; // Map any desired PIDs. 
            ULONG cPid = 1;
            hr = pPidMap->MapPID(cPid, Pid, MEDIA_MPEG2_PSI);
            pPidMap->Release();
        }
        pPin->Release();
    }
    pDemux->Release();
}
```



<span data-ttu-id="3e035-109">Cada seção PSI completa é entregue em um exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="3e035-109">Each complete PSI section is delivered in one media sample.</span></span> <span data-ttu-id="3e035-110">Para recuperar o número de PID associado a uma seção de tabela, chame [**IMediaSample2:: GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) no exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="3e035-110">To retrieve the PID number associated with a table section, call [**IMediaSample2::GetProperties**](/windows/desktop/api/Strmif/nf-strmif-imediasample2-getproperties) on the media sample.</span></span> <span data-ttu-id="3e035-111">O PID é fornecido nos baixos 13 bits do sinalizador **dwTypeSpecificFlags** na estrutura de **Propriedades am \_ SAMPLE2 \_** .</span><span class="sxs-lookup"><span data-stu-id="3e035-111">The PID is given in the low 13 bits of the **dwTypeSpecificFlags** flag in the **AM\_SAMPLE2\_PROPERTIES** structure.</span></span> <span data-ttu-id="3e035-112">Isso será útil se você mapear vários PIDs do PSI para o mesmo pino de saída.</span><span class="sxs-lookup"><span data-stu-id="3e035-112">This is useful if you map multiple PSI PIDs to the same output pin.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e035-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3e035-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e035-114">Usando o demultiplexador MPEG-2</span><span class="sxs-lookup"><span data-stu-id="3e035-114">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



