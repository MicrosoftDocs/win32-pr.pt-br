---
description: Este tópico descreve como um aplicativo pode alterar programaticamente as configurações de imagem e câmera em um dispositivo de captura de vídeo.
ms.assetid: f789db78-292e-4092-a5dc-1906845fb1dd
title: Configurar a qualidade do vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5987352eb329410efd3fc74d6bf12539e968da8e24d2f0a65af9c9ac7b5cb85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871766"
---
# <a name="configure-the-video-quality"></a>Configurar a qualidade do vídeo

Este tópico descreve como um aplicativo pode alterar programaticamente as configurações de imagem e câmera em um dispositivo de captura de vídeo.

-   [Configurações procamp](#procamp-settings)
-   [Camera Settings](#camera-settings)
-   [Tópicos relacionados](#related-topics)

## <a name="procamp-settings"></a>Configurações procamp

Windows As câmeras de vídeo do modelo de driver (WDM) podem dar suporte a propriedades que controlam a qualidade da imagem:

-   Compensação de luz
-   Brightness
-   Contraste
-   Conheça
-   Gama
-   Matiz
-   Saturação
-   Nitidez
-   Proporção de branco

Essas propriedades são controladas por meio da interface [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) . Use esta interface da seguinte maneira:

1.  Chame [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no filtro de captura para a interface [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) .
2.  Para cada propriedade que você deseja definir, chame o método [**IAMVideoProcAmp:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) . As propriedades são especificadas pela enumeração [**VideoProcAmpProperty**](/windows/win32/api/strmif/ne-strmif-videoprocampproperty) . Se o método **GetRange** falhar, isso significa que a câmera não oferece suporte a essa propriedade específica.
3.  Se [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) tiver sucesso, ele retornará o intervalo de valores com suporte para a propriedade, o valor padrão e o incremento mínimo.
4.  Para obter o valor atual de uma propriedade, chame [**IAMVideoProcAmp:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-get).
5.  Para definir uma propriedade, chame o método [**IAMVideoProcAmp:: Set**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-set) . Para restaurar uma propriedade para seu valor padrão, chame [**GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamvideoprocamp-getrange) para localizar o padrão e passar esse valor para o método **set** .

Você não precisa interromper o gráfico de filtro ao definir as propriedades.

O código a seguir configura um controle TrackBar para que ele possa ser usado para definir o brilho. O intervalo de TrackBar corresponde ao intervalo de brilho que o dispositivo dá suporte e a posição de TrackBar corresponde à configuração de brilho inicial do dispositivo.


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



## <a name="camera-settings"></a>Camera Settings

A interface [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) é semelhante a [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp), mas controla várias configurações na própria câmera:

-   Exposição
-   Foco
-   Iris
-   Panorâmica
-   Roll
-   Inclinação
-   Zoom

Para usar essa interface, siga as mesmas etapas usadas para [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp):

1.  Consulte o filtro de captura para o [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol).
2.  Chame [**IAMCameraControl:: GetRange**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-getrange) para localizar quais configurações têm suporte e o intervalo possível para cada configuração.
3.  Chame [**IAMCameraControl:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-get) para obter o valor atual de uma configuração.
4.  Chame [**IAMCameraControl:: Set**](/windows/desktop/api/Strmif/nf-strmif-iamcameracontrol-set) para definir o valor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Configurando um dispositivo de captura de vídeo](configuring-a-video-capture-device.md)
</dt> </dl>

 

 
