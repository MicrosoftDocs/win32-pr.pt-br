---
title: Limitações ao criar dispositivos DE DISTORÇÃO e referência
description: Existem algumas limitações para a criação de dispositivos DE DISTORÇÃO e Referência no Direct3D 10.1 e direct3D 11.0. Este tópico discute essas limitações.
ms.assetid: 7e022e5d-daa3-48fa-b9fe-4b569220e55e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0483ed6d5fd7348df39a4f3064f377845d6bfae1fe46abc47be5acd99e191c29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608606"
---
# <a name="limitations-creating-warp-and-reference-devices"></a>Limitações ao criar dispositivos DE DISTORÇÃO e referência

Existem algumas limitações para a criação de dispositivos DE DISTORÇÃO e Referência no Direct3D 10.1 e direct3D 11.0. Este tópico discute essas limitações.

Os tipos de driver D3D10 DRIVER TYPE WARP e D3D10 DRIVER TYPE REFERENCE não têm suporte nos níveis de recurso \_ \_ \_ \_ \_ \_ D3D10 \_ FEATURE \_ LEVEL \_ 9 \_ 1 a D3D10 \_ FEATURE LEVEL \_ \_ 9 3 no \_ Direct3D 10.1. Além disso, o tipo de driver D3D DRIVER TYPE WARP não tem suporte no \_ \_ \_ D3D \_ FEATURE \_ LEVEL \_ 11 \_ 0 no Direct3D 11.0. Ou seja, quando você chama [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para criar um dispositivo Direct3D 10.1 ou quando chama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para criar um dispositivo Direct3D 11.0, se você especificar uma combinação de um desses tipos de driver com um desses níveis de recurso na chamada, a chamada será inválida. Somente as seguintes combinações de níveis de recurso, runtimes e tipos de driver são válidas para dispositivos DE DISTORÇÃO e Referência:

-   D3D DRIVER TYPE WARP em todos os níveis de recursos no \_ \_ \_ Direct3D 11.1, que Windows 8 inclui

    REFERÊNCIA DE TIPO DE DRIVER D3D \_ em todos os níveis de recurso no \_ \_ Direct3D 11.1

    Quando você chama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para criar um dispositivo Direct3D 11.1, a chamada é válida se você especificar uma combinação de um desses tipos de driver com um desses níveis de recurso.

-   D3D DRIVER TYPE WARP nos níveis de recurso \_ \_ \_ D3D \_ FEATURE \_ LEVEL \_ \_ 9 1 a D3D \_ FEATURE LEVEL \_ \_ 10 \_ 1 no Direct3D 11

    REFERÊNCIA DE TIPO DE DRIVER D3D nos níveis de recurso \_ \_ \_ D3D \_ FEATURE \_ LEVEL \_ \_ 9 1 a D3D \_ FEATURE LEVEL \_ \_ 11 \_ 0 no Direct3D 11

    Quando você chama [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) para criar um dispositivo Direct3D 11, a chamada é válida se você especificar uma combinação de um desses tipos de driver com um desses níveis de recurso.

-   REFERÊNCIA DO TIPO DE DRIVER D3D10 WARP e \_ \_ \_ D3D10 \_ DRIVER \_ NO \_ D3D10 \_ FEATURE LEVEL \_ \_ 10 0 até \_ D3D10 \_ FEATURE LEVEL \_ \_ 10 1 feature levels in \_ Direct3D 10.1

    Quando você chama [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) para criar um dispositivo Direct3D 10.1, a chamada é válida se você especificar uma combinação de um desses tipos de driver com um desses níveis de recurso.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Dispositivos](overviews-direct3d-11-devices.md)
</dt> <dt>

[Introdução ao Direct3D 11 em hardware de nível baixo](overviews-direct3d-11-devices-downlevel-intro.md)
</dt> <dt>

[Como criar um dispositivo WARP](overviews-direct3d-11-devices-create-warp.md)
</dt> <dt>

[Como criar um dispositivo de referência](overviews-direct3d-11-devices-create-ref.md)
</dt> <dt>

[**TIPO DE DRIVER D3D10 \_ \_**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type)
</dt> <dt>

[**D3D10 \_ FEATURE \_ LEVEL1**](/windows/desktop/api/d3d10_1/ne-d3d10_1-d3d10_feature_level1)
</dt> <dt>

[**TIPO DE DRIVER D3D \_ \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)
</dt> <dt>

[**NÍVEL DE \_ RECURSO D3D \_**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)
</dt> </dl>

 

 