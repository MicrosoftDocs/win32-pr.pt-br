---
description: Formato de sinal
ms.assetid: 8684972c-3233-49bf-8c34-ca644aca432a
title: Formato de sinal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb6983328729e0dc72d93c0e00a74e7e65a7f237
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825828"
---
# <a name="signal-format"></a><span data-ttu-id="57788-103">Formato de sinal</span><span class="sxs-lookup"><span data-stu-id="57788-103">Signal Format</span></span>

<span data-ttu-id="57788-104">O formato de sinal de camcorder DV pode ser NTSC ou PAL, Standard ou de execução longa.</span><span class="sxs-lookup"><span data-stu-id="57788-104">A DV camcorder's signal format can be NTSC or PAL, standard or long-play.</span></span>

<span data-ttu-id="57788-105">**Driver MSDV**</span><span class="sxs-lookup"><span data-stu-id="57788-105">**MSDV Driver**</span></span>

<span data-ttu-id="57788-106">Para obter o formato de sinal de entrada do driver MSDV, chame o método [**IAMExtTransport:: GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) e passe o sinalizador de sinal de entrada do Ed \_ transbasic \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="57788-106">To get the input signal format from the MSDV driver, call the [**IAMExtTransport::GetTransportBasicParameters**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-gettransportbasicparameters) method and pass in the ED\_TRANSBASIC\_INPUT\_SIGNAL flag.</span></span> <span data-ttu-id="57788-107">O método retorna uma constante definida, indicando o formato.</span><span class="sxs-lookup"><span data-stu-id="57788-107">The method returns a defined constant, indicating the format.</span></span>

<span data-ttu-id="57788-108">O código a seguir verifica o formato de sinal e usa esse valor para calcular o tempo médio por quadro.</span><span class="sxs-lookup"><span data-stu-id="57788-108">The following code checks the signal format, and uses this value to calculates the average time per frame.</span></span> <span data-ttu-id="57788-109">O modo de variável recebe a constante de formato de sinal.</span><span class="sxs-lookup"><span data-stu-id="57788-109">The variable Mode receives the signal-format constant.</span></span>


```C++
LONG Mode, AvgTimePerFrame;
hr = MyDevCap.pTransport->GetTransportBasicParameters(
        ED_TRANSBASIC_INPUT_SIGNAL, &Mode, NULL);
if (SUCCEEDED(hr))
{
    switch (Mode)
    {
    case ED_TRANSBASIC_SIGNAL_525_60_SD: // NTSC SD
        AvgTimePerFrame = 33;  // 33 msec (29.97 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_525_60_SDL: // NTSC SDL
        AvgTimePerFrame = 33;  
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SD: // PAL SD
        AvgTimePerFrame = 40;  // 40 msec (25 FPS)
        break;
    case ED_TRANSBASIC_SIGNAL_625_50_SDL: // PAL SDL
        AvgTimePerFrame = 40;  
        break;
    default: 
        // Unknown type
        AvgTimePerFrame = 33; // Default
        break;
    }
}
```



<span data-ttu-id="57788-110">Para obter o formato de sinal de saída, chame o mesmo método com o \_ sinalizador de sinal de saída Ed transbasic \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="57788-110">To get the output signal format, call the same method with the ED\_TRANSBASIC\_OUTPUT\_SIGNAL flag.</span></span>

<span data-ttu-id="57788-111">**Driver UVC**</span><span class="sxs-lookup"><span data-stu-id="57788-111">**UVC Driver**</span></span>

<span data-ttu-id="57788-112">Para obter o formato de sinal de entrada ou saída do driver UVC, chame [**IAMStreamConfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) no PIN e examine o bloco de formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="57788-112">To get the input or output signal format from the UVC driver, call [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) on the pin and examine the video format block.</span></span> <span data-ttu-id="57788-113">(Para dispositivos UVC, o código mostrado no exemplo anterior geralmente retorna ED \_ \_Sinal transbasic \_ desconhecido, portanto, não é confiável.)</span><span class="sxs-lookup"><span data-stu-id="57788-113">(For UVC devices, the code shown in the previous example usually returns ED\_TRANSBASIC\_SIGNAL\_UNKNOWN, so it is not reliable.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="57788-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="57788-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57788-115">Controlando uma camcorder DV</span><span class="sxs-lookup"><span data-stu-id="57788-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



