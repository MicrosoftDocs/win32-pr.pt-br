---
description: Estados de efeito são pares nome-valor na forma de uma expressão.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Grupos de estado de efeito (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4617f786b984c96b271600e05b3ea8da9b5701fd
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335560"
---
# <a name="effect-state-groups-direct3d-10"></a>Grupos de estado de efeito (Direct3D 10)

Estados de efeito são pares nome-valor na forma de uma expressão.

## <a name="blend-state"></a>Estado do Blend

| Estado do efeito | Grupo |
|-|-|
| **ALPHATOCOVERAGEENABLE,** **BLENDENABLE,** **SRCBLEND,** **DESTBLEND,** **BLENDOP,** **SRCBLENDALPHA,** **DESTBLENDALPHA,** **BLENDOPALPHA,** **RENDERTARGETWRITEMASK** | Membros do [ **D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc) |

## <a name="depth-and-stencil-state"></a>Profundidade e estado de estêncil

| Estado do efeito| Grupo |
|-|-|
| **DEPTHENABLE,** **DEPTHWRITEMASK,** **DEPTHFUNC,NCILENABLE,** **STENCILREADMASK,** **STENCILWRITEMASK**  | Membros do [ **D3D10 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc) |
| **FRONTFACESTENCILFAIL**, **FRONTFACESTENCILZFAIL,** **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC** | Membro do [ **D3D10 \_ DEPTH \_ \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc) |

## <a name="rasterizer-state"></a>Estado do rasterizador

| Estado do efeito| Grupo |
|-|-|
| Fillmode | [**MODO DE PREENCHIMENTO D3D10 \_ \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| MODELO DE RESLÚSCULO | [**MODO DE \_ RESSUÇÃO D3D10 \_**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| **FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP,** **SLOPESCALEDDEPTHBIAS,** **ZCLIPENABLE,** **SCISSORENABLE,** **MULTISAMPLEENABLE,** **ANTIALIASEDLINEENABLE** | Membros do [ **D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc) |

## <a name="sampler-state"></a>Estado de amostra

| Estado do efeito | Grupo |
|-|-|
| **Filtro**, **endereçou**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD** | Membros de [ **amostra de d3d10 \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc) |

Consulte [tipo de amostra (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) para obter exemplos.

## <a name="effect-object-state"></a>Estado do objeto de efeito

| Este objeto de efeito | É mapeada para |
|-|-|
| RASTERIZERSTATE | Um objeto de estado de [estado do rasterizador](#rasterizer-state) . |
| DEPTHSTENCILSTATE | Um objeto de estado de [estado de profundidade e de estêncil](#depth-and-stencil-state) . |
| BLENDstate | Um objeto de estado de [estado de mistura](#blend-state) . |
| VERTEXSHADER | Um objeto de sombreador de vértice compilado. |
| PIXELSHADER | Um objeto de sombreador de pixel compilado. |
| GEOMETRYSHADER | Um objeto de sombreador Geometry compilado. |
| DS \_ STENCILREF AB \_ BLENDFACTOR AB \_ SAMPLEMASK | Membros de [**d3d10 \_ Pass \_ desc**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc). |

## <a name="defining-and-using-state-objects"></a>Definindo e usando objetos de estado

Os objetos de estado são declarados em arquivos FX no formato a seguir. *StateObjectType* é um dos Estados listados acima e *MemberName* é o nome de qualquer membro que terá um valor não padrão.

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

Por exemplo, para configurar um objeto de estado de mistura com AlphaToCoverageEnable e BlendEnable \[ 0 \] definido como **false**, o código a seguir seria usado.

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

O objeto de estado é aplicado a uma passagem de técnica usando uma das funções de FileState, descritas na [sintaxe de técnica de efeito (Direct3D 10)](d3d10-effect-technique-syntax.md). Por exemplo, para aplicar o objeto Blendstate descrito acima, o código a seguir seria usado.

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

Para obter um tutorial que descreve o uso de Estados, consulte [Gerenciamento de estado](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).

## <a name="related-topics"></a>Tópicos relacionados

* [Sintaxe da técnica de efeito](d3d10-effect-technique-syntax.md)
* [Formato de efeito (Direct3D 10)](d3d10-effect-format.md)
