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
# <a name="device-mode"></a>Modo de dispositivo

As camcorders IEEE 1394 e USB podem alternar entre o modo de câmera e o modo VTR (gravador de fita de vídeo). Quando um modo de vídeo IEEE 1394 é comutado, o dispositivo é redefinido e o aplicativo deve enumerar novamente. Não é possível que um aplicativo Alterne o modo programaticamente. Câmeras de vídeo USB, por outro lado, podem alternar entre os modos de câmera e VTR sem redefinição, e o aplicativo pode alterar o modo.

**Driver MSDV**

Para obter o modo atual em um dispositivo IEEE 1394, chame o método [**IAMExtDevice:: GetCapability**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-getcapability) com o valor \_ tipo de \_ dispositivo Ed DEVCAP \_ . Se o método retornar o valor ED \_ DEVTYPE \_ VCR, o dispositivo estará no modo VTR e terá funções como Pause, stop, Fast-Forward e retrocesso. Caso contrário, se o método retornar \_ a \_ câmera Ed DEVTYPE, o dispositivo estará no modo de câmera. O exemplo de código a seguir mostra como consultar o tipo de dispositivo:


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



Se a camcorder ficar offline, você deverá consultá-la novamente quando ela ficar disponível. O Gerenciador de gráficos de filtro posta um evento de [**\_ \_ perda de dispositivo EC**](ec-device-lost.md) quando o dispositivo é removido.

**Driver UVC**

Como dispositivos de vídeo USB podem alternar modos sem redefinição, o código mostrado nos exemplos anteriores não é confiável para dispositivos USB. Em vez disso, use a interface [**iseleger**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) para obter o modo atual. Você também pode usar essa interface para alternar modos programaticamente se o dispositivo der suporte a ele.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando uma camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



