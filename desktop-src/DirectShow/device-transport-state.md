---
description: Estado de transporte do dispositivo
ms.assetid: 15edded0-207c-41e8-81fe-deb6335045eb
title: Estado de transporte do dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05f52ea846c79be6cb2d011b635da358f7ecd0a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370338"
---
# <a name="device-transport-state"></a>Estado de transporte do dispositivo

Para recuperar o estado atual do dispositivo, como reproduzir, pausar ou parar, chame o método de [**\_ modo IAMExtTransport:: Get**](/windows/desktop/api/Strmif/nf-strmif-iamexttransport-get_mode) . O método recupera uma constante que indica o estado do dispositivo:



| Valor                    | Estado do Dispositivo |
|--------------------------|--------------|
| \_reproduzir modo \_ Ed           | Reproduzir         |
| \_parada do modo Ed \_           | Stop         |
| \_congelamento do modo Ed \_         | Pausar        |
| \_modo Ed \_ FF             | Avanço rápido |
| \_modo Ed \_ Rebo            | Rewind       |
| \_registro de modo Ed \_         | Record       |
| \_congelamento de \_ registro do modo Ed \_ | Gravar-pausar |



 

O código a seguir verifica o estado do dispositivo:


```C++
LONG State;
hr = MyDevCap.pTransport->get_Mode(&State);
if (SUCCEEDED(hr))
{
    switch (State)
    {
        case ED_MODE_PLAY:
        // ... 
    }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Controlando uma camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



