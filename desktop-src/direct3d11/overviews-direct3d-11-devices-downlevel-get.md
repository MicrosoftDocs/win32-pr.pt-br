---
title: Como obter o nível de recurso do dispositivo
description: Este tópico mostra como obter o nível de recurso mais alto com suporte de um dispositivo.
ms.assetid: 5eb7dd5b-3be3-4b7f-bcc7-20027fdfe6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e587ad488a84641a92f0058d201014030e3467e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822910"
---
# <a name="how-to-get-the-device-feature-level"></a>Como: obter o nível de recurso do dispositivo

Este tópico mostra como obter o nível de [recurso](overviews-direct3d-11-devices-downlevel-intro.md) mais alto com suporte de um [dispositivo](overviews-direct3d-11-devices-intro.md). Os dispositivos do Direct3D 11 dão suporte a um conjunto fixo de níveis de recursos que são definidos na enumeração de [**\_ \_ nível de recurso do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) . Quando você souber o [nível de recurso](overviews-direct3d-11-devices-downlevel-intro.md) mais alto com suporte de um dispositivo, poderá executar caminhos de código apropriados para esse dispositivo.

**Para obter o nível de recurso do dispositivo**

1.  Chame a função [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) ou as funções [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) ao especificar **NULL** para o parâmetro *ppDevice* . Você pode fazer isso antes da criação do dispositivo.

    \- ou –

    Chame [**ID3D11Device:: GetFeatureLevel**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getfeaturelevel) após a criação do dispositivo.

2.  Examine o valor da enumeração de [**\_ \_ nível de recurso do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) retornado da última etapa para determinar o nível de recurso com suporte.

O exemplo de código a seguir demonstra como determinar o nível de recurso com suporte mais alto chamando a função [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) . O **D3D11CreateDevice** armazena o nível de recurso mais alto com suporte na variável nível. Você pode usar esse código para examinar o valor do tipo enumerado de [**\_ \_ nível de recurso do D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) que **D3D11CreateDevice** retorna. Observe que esse código lista todos os níveis de recursos explicitamente (para Direct3D 11,1 e Direct3D 11,2).

> [!Note]  
> Se o tempo de execução do Direct3D 11,1 estiver presente no computador e *pFeatureLevels* estiver definido como **NULL**, essa função não criará um dispositivo de nível de [**recurso do D3D \_ \_ \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) . Para criar um dispositivo de **nível de recurso do D3D \_ \_ \_ 11 \_ 1** , você deve fornecer explicitamente uma matriz de **nível de \_ recurso \_ do D3D** que inclua o **nível de recurso do D3D \_ \_ \_ 11 \_ 1**. Se você fornecer uma matriz de **\_ \_ nível de recurso do D3D** que contém o nível de recurso do **D3D \_ \_ \_ 11 \_ 1** em um computador que não tem o tempo de execução do Direct3D 11,1 instalado, essa função falhará imediatamente com E \_ INVALIDARG.

 


```C++
HRESULT hr = E_FAIL;
D3D_FEATURE_LEVEL MaxSupportedFeatureLevel = D3D_FEATURE_LEVEL_9_1;
D3D_FEATURE_LEVEL FeatureLevels[] = {
    D3D_FEATURE_LEVEL_11_1,
    D3D_FEATURE_LEVEL_11_0,
    D3D_FEATURE_LEVEL_10_1,
    D3D_FEATURE_LEVEL_10_0,
    D3D_FEATURE_LEVEL_9_3,
    D3D_FEATURE_LEVEL_9_2,
    D3D_FEATURE_LEVEL_9_1
    };

hr = D3D11CreateDevice(
    NULL,
    D3D_DRIVER_TYPE_HARDWARE,
    NULL, 
    0, 
    &FeatureLevels, 
    ARRAYSIZE(FeatureLevels), 
    D3D11_SDK_VERSION, 
    NULL, 
    &MaxSupportedFeatureLevel, 
    NULL 
    );

if(FAILED(hr))
{
    return hr;
}
```



A seção de [referência do 10Level9](d3d11-graphics-reference-10level9.md) lista as diferenças entre o comportamento de vários métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) em vários níveis de recursos do 10Level9.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Direct3D 11 em hardware de nível inferior](overviews-direct3d-11-devices-downlevel.md)
</dt> <dt>

[Como usar o Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




