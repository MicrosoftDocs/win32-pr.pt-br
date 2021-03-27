---
title: Grupos de estado de efeito (Direct3D 11)
description: Os Estados de efeito são pares de valor de nome na forma de uma expressão.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- efeito, grupos de estado (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58def71b6362706eb831129b1d222ef3d1cc9341
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917331"
---
# <a name="effect-state-groups-direct3d-11"></a>Grupos de estado de efeito (Direct3D 11)

Os Estados de efeito são pares de valor de nome na forma de uma expressão.

-   [Estado do Blend](#blend-state)
-   [Profundidade e estado do estêncil](#depth-and-stencil-state)
-   [Estado do rasterizador](#rasterizer-state)
-   [Estado do classificador](#sampler-state)
-   [Estado do objeto de efeito](#effect-object-state)
-   [Definindo e usando objetos de estado](#defining-and-using-state-objects)
-   [Tópicos relacionados](#related-topics)

## <a name="blend-state"></a>Estado de mesclagem



|                                                                                                                       |                                                           |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK | Membros de [ **D3D11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) |



 

## <a name="depth-and-stencil-state"></a>Profundidade e estado do estêncil



|                                                                                                                                                                |                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK                                                                                 | Membros do [ **\_ estêncil de profundidade D3D11 \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)    |
| FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC | Membro de [ **D3D11 \_ profundidade \_ STENCILOP \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc) |



 

## <a name="rasterizer-state"></a>Estado do rasterizador



|                                                                                                                                 |                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| FILLMODE                                                                                                                        | [**\_Modo de preenchimento D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| De seleção                                                                                                                        | [**\_Modo de seleção de D3D11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE | Membros do [ **\_ rasterizador D3D11 \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc) |



 

## <a name="sampler-state"></a>Estado do classificador



|                                                                                                     |                                                               |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| Filter endereçou AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD | Membros de [ **amostra de D3D11 \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc) |



 

Consulte [tipo de amostra (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) para obter exemplos.

## <a name="effect-object-state"></a>Estado do objeto de efeito



| Este objeto de efeito                          | É mapeada para                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| RASTERIZERSTATE                             | Um objeto de estado de [estado do rasterizador](#rasterizer-state) .               |
| DEPTHSTENCILSTATE                           | Um objeto de estado de [estado de profundidade e de estêncil](#depth-and-stencil-state) . |
| BLENDstate                                  | Um objeto de estado de [estado de mistura](#blend-state) .                         |
| VERTEXSHADER                                | Um objeto de sombreador de vértice compilado.                                    |
| PIXELSHADER                                 | Um objeto de sombreador de pixel compilado.                                     |
| GEOMETRYSHADER                              | Um objeto de sombreador Geometry compilado.                                  |
| \_SAMPLEMASK DS STENCILREFAB \_ BLENDFACTORAB \_ | Membros de [**D3DX11 \_ Pass \_ desc**](d3dx11-pass-desc.md).          |



 

## <a name="defining-and-using-state-objects"></a>Definindo e usando objetos de estado

Os objetos de estado são declarados em arquivos FX no formato a seguir. StateObjectType é um dos Estados listados acima e MemberName é o nome de qualquer membro que terá um valor não padrão.


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



Por exemplo, para configurar um objeto de estado de mistura com AlphaToCoverageEnable e BlendEnable \[ 0 \] definido como **false** , o código a seguir seria usado.


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



O objeto de estado é aplicado a uma passagem de técnica usando uma das funções de FileState, descritas na [sintaxe de técnica de efeito (Direct3D 11)](d3d11-effect-technique-syntax.md). Por exemplo, para aplicar o objeto Blendstate descrito acima, o código a seguir seria usado.


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe da técnica de efeito](d3d11-effect-technique-syntax.md)
</dt> <dt>

[Formato de efeito (Direct3D 11)](d3d11-effect-format.md)
</dt> </dl>

 

 