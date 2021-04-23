---
description: Interfaces de dispositivo externo para camcorders DV
ms.assetid: 001321c5-70c7-4baa-ba5a-1e424ca0d647
title: Interfaces de dispositivo externo para camcorders DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5e7106ec6e9b744da0d1f71958aeb895ec8df1a
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909794"
---
# <a name="external-device-interfaces-for-dv-camcorders"></a><span data-ttu-id="87130-103">Interfaces de dispositivo externo para camcorders DV</span><span class="sxs-lookup"><span data-stu-id="87130-103">External Device Interfaces for DV Camcorders</span></span>

<span data-ttu-id="87130-104">O filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) expõe três interfaces para controlar uma camcorder.</span><span class="sxs-lookup"><span data-stu-id="87130-104">The [WDM Video Capture](wdm-video-capture-filter.md) filter exposes three interfaces for controlling a camcorder.</span></span>



| <span data-ttu-id="87130-105">Label</span><span class="sxs-lookup"><span data-stu-id="87130-105">Label</span></span> | <span data-ttu-id="87130-106">Valor</span><span class="sxs-lookup"><span data-stu-id="87130-106">Value</span></span> |
|------------------------------------------------|-------------------------------------------------|
| [<span data-ttu-id="87130-107">**IAMExtDevice**</span><span class="sxs-lookup"><span data-stu-id="87130-107">**IAMExtDevice**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | <span data-ttu-id="87130-108">A interface base para o controle de dispositivo externo.</span><span class="sxs-lookup"><span data-stu-id="87130-108">The base interface for external device control.</span></span> |
| [<span data-ttu-id="87130-109">**IAMExtTransport**</span><span class="sxs-lookup"><span data-stu-id="87130-109">**IAMExtTransport**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | <span data-ttu-id="87130-110">Controla as funções de VCR.</span><span class="sxs-lookup"><span data-stu-id="87130-110">Controls the VCR functions.</span></span>                     |
| [<span data-ttu-id="87130-111">**IAMTimecodeReader**</span><span class="sxs-lookup"><span data-stu-id="87130-111">**IAMTimecodeReader**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | <span data-ttu-id="87130-112">Lê o código de paread do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="87130-112">Reads timecode from the device.</span></span>                 |



 

> [!Note]  
> <span data-ttu-id="87130-113">Para usar essas interfaces com o driver camcorder MSDV, inclua o arquivo de cabeçalho XPrtDefs. h em seu projeto.</span><span class="sxs-lookup"><span data-stu-id="87130-113">To use these interfaces with the MSDV camcorder driver, include the header file XPrtDefs.h in your project.</span></span>

 

<span data-ttu-id="87130-114">Depois de selecionar um dispositivo de captura e criar uma instância do filtro de captura, consulte o filtro para essas interfaces.</span><span class="sxs-lookup"><span data-stu-id="87130-114">After you select a capture device and create an instance of the capture filter, query the filter for these interfaces.</span></span> <span data-ttu-id="87130-115">O exemplo a seguir declara uma estrutura personalizada que contém os ponteiros de interface, juntamente com os valores Boolianos que especificam a disponibilidade de cada interface:</span><span class="sxs-lookup"><span data-stu-id="87130-115">The following example declares a custom structure that holds the interface pointers, along with Boolean values that specify the availability of each interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="87130-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87130-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87130-117">Controlando uma camcorder DV</span><span class="sxs-lookup"><span data-stu-id="87130-117">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



