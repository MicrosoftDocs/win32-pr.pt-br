---
description: Obtendo o código de code do dispositivo
ms.assetid: e3d06e0c-a595-4bc3-be62-168bd5122397
title: Obtendo o código de code do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5787cf328214c1a266b7f129e4e517716b1d04f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105747361"
---
# <a name="getting-timecode-from-the-device"></a><span data-ttu-id="a3811-103">Obtendo o código de code do dispositivo</span><span class="sxs-lookup"><span data-stu-id="a3811-103">Getting Timecode from the Device</span></span>

<span data-ttu-id="a3811-104">Enquanto uma fita de vídeo digital está sendo reproduzida ou está no modo de pausa de registro, você pode recuperar o código de tempo SMPTE ou o número de faixa absoluto.</span><span class="sxs-lookup"><span data-stu-id="a3811-104">While a DV tape is playing or is in record-pause mode, you can retrieve the SMPTE timecode or the absolute track number.</span></span> <span data-ttu-id="a3811-105">Para fazer isso, chame o método [**IAMTimecodeReader:: GetCode-código**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) .</span><span class="sxs-lookup"><span data-stu-id="a3811-105">To do this, call the [**IAMTimecodeReader::GetTimecode**](/windows/desktop/api/Strmif/nf-strmif-iamtimecodereader-gettimecode) method.</span></span> <span data-ttu-id="a3811-106">Esse método usa um ponteiro para uma estrutura de [**\_ exemplo de código**](/windows/win32/api/strmif/ns-strmif-timecode_sample) de ponto, que descreve o código de ponto.</span><span class="sxs-lookup"><span data-stu-id="a3811-106">This method takes a pointer to a [**TIMECODE\_SAMPLE**](/windows/win32/api/strmif/ns-strmif-timecode_sample) structure, which describes the timecode.</span></span> <span data-ttu-id="a3811-107">Antes de chamar o método, inicialize o membro **dwFlags** da estrutura.</span><span class="sxs-lookup"><span data-stu-id="a3811-107">Before calling the method, initialize the **dwFlags** member of the structure.</span></span> <span data-ttu-id="a3811-108">Use o valor ED \_ DEVCAP de código de tempo \_ \_ lido para recuperar o código de tempo ou o valor Ed \_ DEVCAP \_ ATN \_ Read para recuperar o número de faixa absoluto.</span><span class="sxs-lookup"><span data-stu-id="a3811-108">Use the value ED\_DEVCAP\_TIMECODE\_READ to retrieve the timecode or the value ED\_DEVCAP\_ATN\_READ to retrieve the absolute track number.</span></span>

<span data-ttu-id="a3811-109">O membro de **código** de Code da estrutura de **\_ exemplo do código** de code é uma estrutura de código de um</span><span class="sxs-lookup"><span data-stu-id="a3811-109">The **timecode** member of the **TIMECODE\_SAMPLE** structure is a TIMECODE structure.</span></span> <span data-ttu-id="a3811-110">Quando o método retorna, o membro **dwFrames** da estrutura de código de tempo contém o código de tempo ou o número de faixa.</span><span class="sxs-lookup"><span data-stu-id="a3811-110">When the method returns, the **dwFrames** member of the TIMECODE structure contains the timecode or track number.</span></span> <span data-ttu-id="a3811-111">Para o código de tempo, as horas, os minutos, os segundos e os quadros são incluídos em um DWORD como valores de BCD (decimal codificado binário), com o formato *hhmmssff*.</span><span class="sxs-lookup"><span data-stu-id="a3811-111">For timecode, the hours, minutes, seconds, and frames are packed into a DWORD as binary coded decimal (BCD) values, with the format *hhmmssff*.</span></span> <span data-ttu-id="a3811-112">Use bitmasks para extrair os valores individuais.</span><span class="sxs-lookup"><span data-stu-id="a3811-112">Use bitmasks to extract the individual values.</span></span>

<span data-ttu-id="a3811-113">O exemplo a seguir recupera o código de tempo e o número de faixa.</span><span class="sxs-lookup"><span data-stu-id="a3811-113">The following example retrieves the timecode and track number.</span></span>


```C++
if (MyDevCap.bHasTimecode)
{
    TIMECODE_SAMPLE TimecodeSample;
    TimecodeSample.timecode.dwFrames = 0;
    char szBuf[32];

    TimecodeSample.dwFlags = ED_DEVCAP_TIMECODE_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample),  SUCCEEDED(hr)) 
    {
        DWORD dwTime = TimecodeSample.timecode.dwFrames; // Packed BCD value.
        int hour  = ((dwTime & 0x0F000000) >> 24) + 
                    (10 * ((dwTime & 0xF0000000) >> 28));
        int min   = ((dwTime & 0x0F0000) >> 16) + 
                    (10 * ((dwTime & 0xF00000) >> 20));
        int sec   = ((dwTime & 0x0F00) >> 8) + 
                    (10 * ((dwTime & 0xF000) >> 12));
        int frame = (dwTime & 0x0F) + 
                    (10 * ((dwTime & 0xF0) >> 4));
    }

    TimecodeSample.dwFlags = ED_DEVCAP_ATN_READ;
    if (hr = MyDevCap.pTimecode->GetTimecode(&TimecodeSample), SUCCEEDED(hr)) 
    {
        DWORD dwTrackNumber = TimecodeSample.timecode.dwFrames;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="a3811-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a3811-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3811-115">Controlando uma camcorder DV</span><span class="sxs-lookup"><span data-stu-id="a3811-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 
