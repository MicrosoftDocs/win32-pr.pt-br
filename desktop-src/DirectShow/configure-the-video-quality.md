---
description: Este tópico descreve como um aplicativo pode alterar programaticamente as configurações de imagem e câmera em um dispositivo de captura de vídeo.
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: Configurar a qualidade do vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cb8d2d28e39f0083aac521f1953ebbb1ca8d5b6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645788"
---
# <a name="configure-the-video-quality"></a><span data-ttu-id="ff995-103">Configurar a qualidade do vídeo</span><span class="sxs-lookup"><span data-stu-id="ff995-103">Configure the Video Quality</span></span>

<span data-ttu-id="ff995-104">Este tópico descreve como um aplicativo pode alterar programaticamente as configurações de imagem e câmera em um dispositivo de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ff995-104">This topic describes how an application can programmatically change the image and camera settings on a video capture device.</span></span>

-   [<span data-ttu-id="ff995-105">Configurações do Procamp</span><span class="sxs-lookup"><span data-stu-id="ff995-105">ProcAmp Settings</span></span>](#procamp-settings)
-   [<span data-ttu-id="ff995-106">Camera Settings</span><span class="sxs-lookup"><span data-stu-id="ff995-106">Camera Settings</span></span>](#camera-settings)
-   [<span data-ttu-id="ff995-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff995-107">Related topics</span></span>](#related-topics)

## <a name="procamp-settings"></a><span data-ttu-id="ff995-108">Configurações do Procamp</span><span class="sxs-lookup"><span data-stu-id="ff995-108">ProcAmp Settings</span></span>

<span data-ttu-id="ff995-109">As câmeras de vídeo Windows Driver Model (WDM) podem dar suporte a propriedades que controlam a qualidade da imagem:</span><span class="sxs-lookup"><span data-stu-id="ff995-109">Windows Driver Model (WDM) video cameras can support properties that control the quality of the image:</span></span>

-   <span data-ttu-id="ff995-110">Compensação de luz</span><span class="sxs-lookup"><span data-stu-id="ff995-110">Backlight compensation</span></span>
-   <span data-ttu-id="ff995-111">Brightness</span><span class="sxs-lookup"><span data-stu-id="ff995-111">Brightness</span></span>
-   <span data-ttu-id="ff995-112">Contraste</span><span class="sxs-lookup"><span data-stu-id="ff995-112">Contrast</span></span>
-   <span data-ttu-id="ff995-113">Conheça</span><span class="sxs-lookup"><span data-stu-id="ff995-113">Gain</span></span>
-   <span data-ttu-id="ff995-114">Gama</span><span class="sxs-lookup"><span data-stu-id="ff995-114">Gamma</span></span>
-   <span data-ttu-id="ff995-115">Matiz</span><span class="sxs-lookup"><span data-stu-id="ff995-115">Hue</span></span>
-   <span data-ttu-id="ff995-116">Saturação</span><span class="sxs-lookup"><span data-stu-id="ff995-116">Saturation</span></span>
-   <span data-ttu-id="ff995-117">Nitidez</span><span class="sxs-lookup"><span data-stu-id="ff995-117">Sharpness</span></span>
-   <span data-ttu-id="ff995-118">Proporção de branco</span><span class="sxs-lookup"><span data-stu-id="ff995-118">White balance</span></span>

<span data-ttu-id="ff995-119">Essas propriedades são controladas por meio da interface [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .</span><span class="sxs-lookup"><span data-stu-id="ff995-119">These properties are controlled through the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span> <span data-ttu-id="ff995-120">Use esta interface da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="ff995-120">Use this interface as follows:</span></span>

1.  <span data-ttu-id="ff995-121">Chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no filtro de captura para a interface [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .</span><span class="sxs-lookup"><span data-stu-id="ff995-121">Call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the capture filter for the [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) interface.</span></span>
2.  <span data-ttu-id="ff995-122">Para cada propriedade que você deseja definir, chame o método [**IAMVideoProcAmp:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) .</span><span class="sxs-lookup"><span data-stu-id="ff995-122">For each property that you want to set, call the [**IAMVideoProcAmp::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) method.</span></span> <span data-ttu-id="ff995-123">As propriedades são especificadas pela enumeração [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) .</span><span class="sxs-lookup"><span data-stu-id="ff995-123">Properties are specified by the [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) enumeration.</span></span> <span data-ttu-id="ff995-124">Se o método **GetRange** falhar, isso significa que a câmera não oferece suporte a essa propriedade específica.</span><span class="sxs-lookup"><span data-stu-id="ff995-124">If the **GetRange** method fails, it means the camera does not support that particular property.</span></span>
3.  <span data-ttu-id="ff995-125">Se [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) tiver sucesso, ele retornará o intervalo de valores com suporte para a propriedade, o valor padrão e o incremento mínimo.</span><span class="sxs-lookup"><span data-stu-id="ff995-125">If [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) succeeds, it returns the range of supported values for the property, the default value, and the minimum increment.</span></span>
4.  <span data-ttu-id="ff995-126">Para obter o valor atual de uma propriedade, chame [**IAMVideoProcAmp:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).</span><span class="sxs-lookup"><span data-stu-id="ff995-126">To get the current value of a property, call [**IAMVideoProcAmp::Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).</span></span>
5.  <span data-ttu-id="ff995-127">Para definir uma propriedade, chame o método [**IAMVideoProcAmp:: Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) .</span><span class="sxs-lookup"><span data-stu-id="ff995-127">To set a property, call the [**IAMVideoProcAmp::Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) method.</span></span> <span data-ttu-id="ff995-128">Para restaurar uma propriedade para seu valor padrão, chame [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) para localizar o padrão e passar esse valor para o método **set** .</span><span class="sxs-lookup"><span data-stu-id="ff995-128">To restore a property to its default value, call [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) to find the default and pass that value to the **Set** method.</span></span>

<span data-ttu-id="ff995-129">Você não precisa interromper o gráfico de filtro ao definir as propriedades.</span><span class="sxs-lookup"><span data-stu-id="ff995-129">You do not have to stop the filter graph when you set the properties.</span></span>

<span data-ttu-id="ff995-130">O código a seguir configura um controle TrackBar para que ele possa ser usado para definir o brilho.</span><span class="sxs-lookup"><span data-stu-id="ff995-130">The following code configures a trackbar control so that it can be used to set the brightness.</span></span> <span data-ttu-id="ff995-131">O intervalo de TrackBar corresponde ao intervalo de brilho que o dispositivo dá suporte e a posição de TrackBar corresponde à configuração de brilho inicial do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ff995-131">The range of the trackbar corresponds to the brightness range that the device supports, and position of the trackbar corresponds to the device's initial brightness setting.</span></span>


```C++
HWND hTrackbar; // Handle to the trackbar control. 
// Initialize hTrackbar (not shown).

// Query the capture filter for the IAMVideoProcAmp interface.
IAMVideoProcAmp *pProcAmp = 0;
hr = pCap->QueryInterface(IID_IAMVideoProcAmp, (void**)&pProcAmp);
if (FAILED(hr))
{
    // The device does not support IAMVideoProcAmp, so disable the control.
    EnableWindow(hTrackbar, FALSE);
}
else
{
    long Min, Max, Step, Default, Flags, Val;

    // Get the range and default value. 
    hr = m_pProcAmp->GetRange(VideoProcAmp_Brightness, &Min, &Max, &Step,
        &Default, &Flags);
    if (SUCCEEDED(hr))
    {
        // Get the current value.
        hr = m_pProcAmp->Get(VideoProcAmp_Brightness, &Val, &Flags);
    }
    if (SUCCEEDED(hr))
    {
        // Set the trackbar range and position.
        SendMessage(hTrackbar, TBM_SETRANGE, TRUE, MAKELONG(Min, Max));
        SendMessage(hTrackbar, TBM_SETPOS, TRUE, Val);
        EnableWindow(hTrackbar, TRUE);
    }
    else
    {
        // This property is not supported, so disable the control.
        EnableWindow(hTrackbar, FALSE);
    }
}
```



## <a name="camera-settings"></a><span data-ttu-id="ff995-132">Camera Settings</span><span class="sxs-lookup"><span data-stu-id="ff995-132">Camera Settings</span></span>

<span data-ttu-id="ff995-133">A interface [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) é semelhante a [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), mas controla várias configurações na própria câmera:</span><span class="sxs-lookup"><span data-stu-id="ff995-133">The [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) interface is similar to [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), but controls various setttings on the camera itself:</span></span>

-   <span data-ttu-id="ff995-134">Exposição</span><span class="sxs-lookup"><span data-stu-id="ff995-134">Exposure</span></span>
-   <span data-ttu-id="ff995-135">Foco</span><span class="sxs-lookup"><span data-stu-id="ff995-135">Focus</span></span>
-   <span data-ttu-id="ff995-136">Íris</span><span class="sxs-lookup"><span data-stu-id="ff995-136">Iris</span></span>
-   <span data-ttu-id="ff995-137">Panorâmica</span><span class="sxs-lookup"><span data-stu-id="ff995-137">Pan</span></span>
-   <span data-ttu-id="ff995-138">Roll</span><span class="sxs-lookup"><span data-stu-id="ff995-138">Roll</span></span>
-   <span data-ttu-id="ff995-139">Inclinação</span><span class="sxs-lookup"><span data-stu-id="ff995-139">Tilt</span></span>
-   <span data-ttu-id="ff995-140">Zoom</span><span class="sxs-lookup"><span data-stu-id="ff995-140">Zoom</span></span>

<span data-ttu-id="ff995-141">Para usar essa interface, siga as mesmas etapas usadas para [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):</span><span class="sxs-lookup"><span data-stu-id="ff995-141">To use this interface, follow the same steps used for [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):</span></span>

1.  <span data-ttu-id="ff995-142">Consulte o filtro de captura para o [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).</span><span class="sxs-lookup"><span data-stu-id="ff995-142">Query the capture filter for the [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).</span></span>
2.  <span data-ttu-id="ff995-143">Chame [**IAMCameraControl:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) para localizar quais configurações têm suporte e o intervalo possível para cada configuração.</span><span class="sxs-lookup"><span data-stu-id="ff995-143">Call [**IAMCameraControl::GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) to find which settings are supported, and the possible range for each settings.</span></span>
3.  <span data-ttu-id="ff995-144">Chame [**IAMCameraControl:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) para obter o valor atual de uma configuração.</span><span class="sxs-lookup"><span data-stu-id="ff995-144">Call [**IAMCameraControl::Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) to get the current value of a setting.</span></span>
4.  <span data-ttu-id="ff995-145">Chame [**IAMCameraControl:: Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) para definir o valor.</span><span class="sxs-lookup"><span data-stu-id="ff995-145">Call [**IAMCameraControl::Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) to set the value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff995-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ff995-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff995-147">Configurando um dispositivo de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ff995-147">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
