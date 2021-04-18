---
description: O Direct3D fornece as seguintes funções para determinar o suporte de hardware.
ms.assetid: 63afa799-2c2c-432c-993e-dca8f7433d59
title: Determinando o suporte de hardware (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc4fbc04343ede671d009054ac3782bbf2563109
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105808337"
---
# <a name="determining-hardware-support-direct3d-9"></a>Determinando o suporte de hardware (Direct3D 9)

O Direct3D fornece as seguintes funções para determinar o suporte de hardware.

-   [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat)

    Usado para verificar se um formato de superfície pode ser usado como uma textura, se um formato de superfície pode ser usado como uma textura e um destino de renderização, ou se um formato de superfície pode ser usado como um buffer de estêncil de profundidade. Além disso, esse método é usado para verificar o suporte ao formato do buffer de profundidade e o suporte ao formato de buffer de estêncil de profundidade.

-   [**IDirect3D9::CheckDeviceType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicetype)

    Usado para verificar a capacidade de um dispositivo de executar aceleração de hardware, a capacidade de um dispositivo de criar uma cadeia de permuta para apresentação ou a capacidade de um dispositivo de renderizar para o formato de exibição atual.

-   [**IDirect3D9::CheckDepthStencilMatch**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdepthstencilmatch)

    Usado para verificar se um formato de buffer de profundidade/estêncil é compatível com um formato de destino de renderização. Observe que, antes de chamar esse método, o aplicativo deve chamar [**IDirect3D9:: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) nos formatos de profundidade e de destino de renderização.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
