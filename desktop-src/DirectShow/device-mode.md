---
description: Modo de dispositivo
ms.assetid: d56021be-616b-41cd-8cf0-9e0d314f62cd
title: Modo de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4657fbb49e2619d75911c18185109805116b9647
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456870"
---
# <a name="device-mode"></a><span data-ttu-id="7d9c5-103">Modo de dispositivo</span><span class="sxs-lookup"><span data-stu-id="7d9c5-103">Device Mode</span></span>

<span data-ttu-id="7d9c5-104">As camcorders IEEE 1394 e USB podem alternar entre o modo de câmera e o modo VTR (gravador de fita de vídeo).</span><span class="sxs-lookup"><span data-stu-id="7d9c5-104">IEEE 1394 and USB camcorders can switch between camera mode and video tape recorder (VTR) mode.</span></span> <span data-ttu-id="7d9c5-105">Quando um modo de vídeo IEEE 1394 é comutado, o dispositivo é redefinido e o aplicativo deve enumerar novamente.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-105">When an IEEE 1394 camcorder switches modes, the device resets and the application must enumerate it again.</span></span> <span data-ttu-id="7d9c5-106">Não é possível que um aplicativo Alterne o modo programaticamente.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-106">There is no way for an application to switch the mode programmatically.</span></span> <span data-ttu-id="7d9c5-107">Câmeras de vídeo USB, por outro lado, podem alternar entre os modos de câmera e VTR sem redefinição, e o aplicativo pode alterar o modo.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-107">USB camcorders, on the other hand, can switch between camera and VTR modes without resetting, and the application can change the mode.</span></span>

<span data-ttu-id="7d9c5-108">**Driver MSDV**</span><span class="sxs-lookup"><span data-stu-id="7d9c5-108">**MSDV Driver**</span></span>

<span data-ttu-id="7d9c5-109">Para obter o modo atual em um dispositivo IEEE 1394, chame o método [**IAMExtDevice:: GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) com o valor \_ tipo de \_ dispositivo Ed DEVCAP \_ .</span><span class="sxs-lookup"><span data-stu-id="7d9c5-109">To get the current mode on an IEEE 1394 device, call the [**IAMExtDevice::GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) method with the value ED\_DEVCAP\_DEVICE\_TYPE.</span></span> <span data-ttu-id="7d9c5-110">Se o método retornar o valor ED \_ DEVTYPE \_ VCR, o dispositivo estará no modo VTR e terá funções como Pause, stop, Fast-Forward e retrocesso.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-110">If the method returns the value ED\_DEVTYPE\_VCR, the device is in VTR mode and has functions such as pause, stop, fast-forward, and rewind.</span></span> <span data-ttu-id="7d9c5-111">Caso contrário, se o método retornar \_ a \_ câmera Ed DEVTYPE, o dispositivo estará no modo de câmera.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-111">Otherwise, if the method returns ED\_DEVTYPE\_CAMERA, the device is in camera mode.</span></span> <span data-ttu-id="7d9c5-112">O exemplo de código a seguir mostra como consultar o tipo de dispositivo:</span><span class="sxs-lookup"><span data-stu-id="7d9c5-112">The following code example shows how to query the device type:</span></span>


```C++
if (MyDevCap.bHasDevice) 
{
    LONG lDeviceType = 0;
    MyDevCap.pDevice->GetCapability(ED_DEVCAP_DEVICE_TYPE, &lDeviceType, 0);

    if (lDeviceType == ED_DEVTYPE_VCR) 
    {
        // Device is a VTR. Enable all VTR functions.
    }
    else 
    {
        // Device is a camera. 
        // Enable record and record-pause; disable other functions.
    }
}
```



<span data-ttu-id="7d9c5-113">Se a camcorder ficar offline, você deverá consultá-la novamente quando ela ficar disponível.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-113">If the camcorder goes offline, you should query it again when it next becomes available.</span></span> <span data-ttu-id="7d9c5-114">O Gerenciador de gráficos de filtro posta um evento de [**\_ \_ perda de dispositivo EC**](ec-device-lost.md) quando o dispositivo é removido.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-114">The filter graph manager posts an [**EC\_DEVICE\_LOST**](ec-device-lost.md) event when the device is removed.</span></span>

<span data-ttu-id="7d9c5-115">**Driver UVC**</span><span class="sxs-lookup"><span data-stu-id="7d9c5-115">**UVC Driver**</span></span>

<span data-ttu-id="7d9c5-116">Como dispositivos de vídeo USB podem alternar modos sem redefinição, o código mostrado nos exemplos anteriores não é confiável para dispositivos USB.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-116">Because USB video devices can switch modes without resetting, the code shown in the previous examples is not reliable for USB devices.</span></span> <span data-ttu-id="7d9c5-117">Em vez disso, use a interface [**iseleger**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) para obter o modo atual.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-117">Instead, use the [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) interface to get the current mode.</span></span> <span data-ttu-id="7d9c5-118">Você também pode usar essa interface para alternar modos programaticamente se o dispositivo der suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="7d9c5-118">You can also use this interface to switch modes programmatically if the device supports it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d9c5-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7d9c5-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d9c5-120">Controlando uma camcorder DV</span><span class="sxs-lookup"><span data-stu-id="7d9c5-120">Controlling a DV Camcorder</span></span>](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



