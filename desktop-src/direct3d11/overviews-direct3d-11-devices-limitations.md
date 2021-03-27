---
title: Limitações ao criar dispositivos de referência e detorção
description: Existem algumas limitações para a criação de dispositivos WARP e de referência no Direct3D 10,1 e no Direct3D 11,0. Este tópico discute essas limitações.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e12540b1fdb8f2bc00ef2a0e596904e0b717bed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294080"
---
# <a name="limitations-creating-warp-and-reference-devices"></a>Limitações ao criar dispositivos de referência e detorção

Existem algumas limitações para a criação de dispositivos WARP e de referência no Direct3D 10,1 e no Direct3D 11,0. Este tópico discute essas limitações.

Os tipos de driver D3D10 \_ \_ \_ e \_ referência de tipo de driver d3d10 não têm \_ \_ suporte nos níveis de recurso D3D10 \_ \_ \_ de nível 9 \_ 1 a d3d10 \_ Feature \_ nível \_ 9 \_ 3 no Direct3D 10,1. Além disso, o tipo de driver de \_ Warp do tipo de driver D3D \_ \_ não tem suporte no \_ nível de recurso do D3D \_ \_ 11 \_ 0 no Direct3D 11,0. Ou seja, quando você chama [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para criar um dispositivo Direct3D 10,1 ou quando chama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para criar um dispositivo Direct3D 11,0, se você especificar uma combinação de um desses tipos de driver com um desses níveis de recurso na chamada, a chamada será inválida. Somente as seguintes combinações de níveis de recurso, tempos de execução e tipos de driver são válidas para dispositivos de detorção e referência:

-   \_Tipo de driver D3D \_ \_ Warp em todos os níveis de recurso no Direct3D 11,1, que o Windows 8 inclui

    \_ \_ \_ Referência de tipo de driver D3D em todos os níveis de recurso no Direct3D 11,1

    Quando você chamar [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para criar um dispositivo Direct3D 11,1, a chamada será válida se você especificar uma combinação de um desses tipos de driver com um desses níveis de recurso.

-   \_ \_ Tipo de driver D3D \_ Warp no \_ nível de recurso do D3D \_ \_ 9 \_ 1 por meio \_ \_ \_ \_ de níveis de recurso do nível de recurso do D3D 10 1 no Direct3D 11

    \_ \_ \_ Referência de tipo de driver D3D no nível de recurso do D3D \_ \_ \_ 9 \_ 1 por meio dos \_ \_ \_ \_ níveis de recurso do nível de recurso do D3D 11 0 no Direct3D 11

    Quando você chamar [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para criar um dispositivo Direct3D 11, a chamada será válida se você especificar uma combinação de um desses tipos de driver com um desses níveis de recurso.

-   D3D10 \_ tipo de driver \_ \_ dewarpe e \_ \_ \_ referência de tipo de driver d3d10 no nível de recurso d3d10 \_ \_ \_ \_ de 10 0 a D3D10 \_ \_ \_ de nível de recurso \_ de 10 1 no Direct3D 10,1

    Quando você chamar [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para criar um dispositivo Direct3D 10,1, a chamada será válida se você especificar uma combinação de um desses tipos de driver com um desses níveis de recurso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Introdução ao Direct3D 11 no hardware de nível inferior](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[Como: criar um dispositivo de detorção](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[Como: criar um dispositivo de referência](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[**\_Tipo de driver d3d10 \_**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[**\_LEVEL1 do recurso d3d10 \_**](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[**\_Tipo de driver do D3D \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[**\_Nível de recurso do D3D \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 