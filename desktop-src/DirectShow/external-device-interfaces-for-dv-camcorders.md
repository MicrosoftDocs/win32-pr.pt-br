---
description: Interfaces de dispositivo externo para camcorders DV
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Interfaces de dispositivo externo para camcorders DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e52b6d0fe00ff91ff87e9c810bbe7ecc319e9bfd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103826062"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a><span data-ttu-id="f4d31-103">Interfaces de dispositivo externo para camcorders DV</span><span class="sxs-lookup"><span data-stu-id="f4d31-103">External Device Interfaces for DV Camcorders</span></span>

<span data-ttu-id="f4d31-104">O filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) expõe três interfaces para controlar uma camcorder.</span><span class="sxs-lookup"><span data-stu-id="f4d31-104">The [WDM Video Capture](wdm-video-capture-filter.md) filter exposes three interfaces for controlling a camcorder.</span></span>



|                                                |                                                 |
|------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="f4d31-105">**IAMExtDevice**</span><span class="sxs-lookup"><span data-stu-id="f4d31-105">**IAMExtDevice**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | <span data-ttu-id="f4d31-106">A interface base para o controle de dispositivo externo.</span><span class="sxs-lookup"><span data-stu-id="f4d31-106">The base interface for external device control.</span></span> |
| [<span data-ttu-id="f4d31-107">**IAMExtTransport**</span><span class="sxs-lookup"><span data-stu-id="f4d31-107">**IAMExtTransport**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | <span data-ttu-id="f4d31-108">Controla as funções de VCR.</span><span class="sxs-lookup"><span data-stu-id="f4d31-108">Controls the VCR functions.</span></span>                     |
| [<span data-ttu-id="f4d31-109">**IAMTimecodeReader**</span><span class="sxs-lookup"><span data-stu-id="f4d31-109">**IAMTimecodeReader**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | <span data-ttu-id="f4d31-110">Lê o código de paread do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f4d31-110">Reads timecode from the device.</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="f4d31-111">Para usar essas interfaces com o driver camcorder MSDV, inclua o arquivo de cabeçalho XPrtDefs. h em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="f4d31-111">To use these interfaces with the MSDV camcorder driver, include the header file XPrtDefs.h in your project.</span></span>

 

<span data-ttu-id="f4d31-112">Depois de selecionar um dispositivo de captura e criar uma instância do filtro de captura, consulte o filtro para essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="f4d31-112">After you select a capture device and create an instance of the capture filter, query the filter for these interfaces.</span></span> <span data-ttu-id="f4d31-113">O exemplo a seguir declara uma estrutura personalizada que contém os ponteiros de interface, juntamente com os valores Boolianos que especificam a disponibilidade de cada interface:</span><span class="sxs-lookup"><span data-stu-id="f4d31-113">The following example declares a custom structure that holds the interface pointers, along with Boolean values that specify the availability of each interface:</span></span>


```C++
struct _MyDevCap
{
    IAMExtDevice       *pDevice;
    IAMExtTransport    *pTransport;
    IAMTimecodeReader  *pTimecode;
    BOOL                bHasDevice;
    BOOL                bHasTransport;
    BOOL                bHasTimecode;
} MyDevCap;

HRESULT hr;
IBaseFilter *pDVCam;  // Pointer to the capture filter.

// Create an instance of the capture filter (not shown).

hr = pDVCam->QueryInterface(IID_IAMExtDevice, (void **)&MyDevCap.pDevice);
MyDevCap.bHasDevice = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMExtTransport, (void **)&MyDevCap.pTransport);
MyDevCap.bHasTransport = (SUCCEEDED(hr));

hr = pDVCam->QueryInterface(IID_IAMTimecodeReader, (void **)&MyDevCap.pTimecode);
MyDevCap.bHasTimecode = (SUCCEEDED(hr));
```



## <a name="related-topics"></a><span data-ttu-id="f4d31-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4d31-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4d31-115">Controlando uma camcorder DV</span><span class="sxs-lookup"><span data-stu-id="f4d31-115">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



