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
# <a name="external-device-interfaces-for-dv-camcorders"></a>Interfaces de dispositivo externo para camcorders DV

O filtro de [captura de vídeo WDM](wdm-video-capture-filter.md) expõe três interfaces para controlar uma camcorder.



|                                                |                                                 |
|------------------------------------------------|-------------------------------------------------|
| [**IAMExtDevice**](/windows/desktop/api/Strmif/nn-strmif-iamextdevice)           | A interface base para o controle de dispositivo externo. |
| [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport)     | Controla as funções de VCR.                     |
| [**IAMTimecodeReader**](/windows/desktop/api/Strmif/nn-strmif-iamtimecodereader) | Lê o código de paread do dispositivo.                 |



 

> [!Note]  
> Para usar essas interfaces com o driver camcorder MSDV, inclua o arquivo de cabeçalho XPrtDefs. h em seu projeto.

 

Depois de selecionar um dispositivo de captura e criar uma instância do filtro de captura, consulte o filtro para essas interfaces. O exemplo a seguir declara uma estrutura personalizada que contém os ponteiros de interface, juntamente com os valores Boolianos que especificam a disponibilidade de cada interface:


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando uma camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



