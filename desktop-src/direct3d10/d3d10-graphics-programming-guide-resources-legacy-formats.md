---
description: Esta tabela lista os formatos direct3D 9 que podem ser mapeados para um formato Direct3D 10.
ms.assetid: 07c9b827-6e2e-4599-b48a-f726484b643d
title: 'Formatos herdados: mapear formatos direct3D 9 para o Direct3D 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c40a437ef42b4ce24b468c39d169b39db7fb9cb7951c825da38bb63f85b9dba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895296"
---
# <a name="legacy-formats-map-direct3d-9-formats-to-direct3d-10"></a>Formatos herdados: mapear formatos direct3D 9 para o Direct3D 10

Esta tabela lista os formatos direct3D 9 que podem ser mapeados para um formato Direct3D 10. Os formatos direct3D 10 divergem dos formatos Direct3D 9 para que os formatos de vértice e textura possam ser mesclados para habilitar aplicativos entre extremidades.



| Formato de textura/vértice/índice direct3D 9 | Formato equivalente do Direct3D 10                                        |
|----------------------------------------|----------------------------------------------------------------------|
| D3DFMT \_ UNKNOWN                        | FORMATO DXGI \_ \_ DESCONHECIDO                                                |
| D3DFMT \_ R8G8B8                         | Não disponível                                                        |
| D3DFMT \_ A8R8G8B8                       | DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM (DXGI 1.1)                             |
| D3DFMT \_ X8R8G8B8                       | DXGI \_ FORMAT \_ B8G8R8X8 \_ UNORM (DXGI 1.1)                             |
| D3DFMT \_ R5G6B5                         | FORMATO DXGI \_ \_ B5G6R5 \_ UNORM (DXGI 1.2)                               |
| D3DFMT \_ X1R5G5B5                       | Não disponível                                                        |
| D3DFMT \_ A1R5G5B5                       | DXGI \_ FORMAT \_ B5G5R5A1 \_ UNORM (DXGI 1.2)                             |
| D3DFMT \_ A4R4G4B4                       | DXGI \_ FORMAT \_ B4G4R4A4 \_ UNORM (DXGI 1.2)                             |
| D3DFMT \_ R3G3B2                         | Não disponível                                                        |
| D3DFMT \_ A8                             | FORMATO DXGI \_ \_ A8 \_ UNORM                                              |
| D3DFMT \_ A8R3G3B2                       | Não disponível                                                        |
| D3DFMT \_ X4R4G4B4                       | Não disponível                                                        |
| D3DFMT \_ A2B10G10R10                    | FORMATO DXGI \_ \_ R10G10B10A2                                            |
| D3DFMT \_ A8B8G8R8                       | FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM ou FORMATO DXGI \_ \_ R8G8B8A8 \_ UNORM \_ SRGB |
| D3DFMT \_ X8B8G8R8                       | Não disponível                                                        |
| D3DFMT \_ G16R16                         | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                          |
| D3DFMT \_ A2R10G10B10                    | Não disponível                                                        |
| D3DFMT \_ A16B16G16R16                   | DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM                                    |
| D3DFMT \_ A8P8                           | Não disponível                                                        |
| D3DFMT \_ P8                             | Não disponível                                                        |
| D3DFMT \_ L8                             | FORMATO DXGI \_ \_ R8 \_ UNORM 2                                            |
| D3DFMT \_ A8L8                           | Não disponível                                                        |
| D3DFMT \_ A4L4                           | Não disponível                                                        |
| D3DFMT \_ V8U8                           | FORMATO DXGI \_ \_ R8G8 \_ SNORM                                            |
| D3DFMT \_ L6V5U5                         | Não disponível                                                        |
| D3DFMT \_ X8L8V8U8                       | Não disponível                                                        |
| D3DFMT \_ Q8W8V8U8                       | FORMATO DXGI \_ \_ R8G8B8A8 \_ SNORM                                        |
| D3DFMT \_ V16U16                         | FORMATO DXGI \_ \_ R16G16 \_ SNORM                                          |
| D3DFMT \_ W11V11U10                      | Não disponível                                                        |
| D3DFMT \_ A2W10V10U10                    | Não disponível                                                        |
| D3DFMT \_ UYVY                           | Não disponível                                                        |
| D3DFMT \_ R8G8 \_ B8G8                     | FORMATO DXGI \_ \_ G8R8 \_ G8B8 \_ UNORM 2                                    |
| D3DFMT \_ YUY2                           | Não disponível                                                        |
| D3DFMT \_ G8R8 \_ G8B8                     | FORMATO DXGI \_ \_ R8G8 \_ B8G8 \_ UNORM 2                                    |
| D3DFMT \_ DXT1                           | FORMATO DXGI \_ \_ BC1 \_ UNORM ou FORMATO DXGI \_ \_ BC1 \_ UNORM \_ SRGB           |
| D3DFMT \_ DXT2                           | FORMATO DXGI \_ \_ BC2 \_ UNORM ou FORMATO DXGI \_ \_ BC2 \_ UNORM \_ SRGB 2         |
| D3DFMT \_ DXT3                           | FORMATO DXGI \_ \_ BC2 \_ UNORM ou FORMATO DXGI \_ \_ BC2 \_ UNORM \_ SRGB           |
| D3DFMT \_ DXT4                           | FORMATO DXGI \_ \_ BC3 \_ UNORM ou FORMATO DXGI \_ \_ BC3 \_ UNORM \_ SRGB 2         |
| D3DFMT \_ DXT5                           | FORMATO DXGI \_ \_ BC3 \_ UNORM ou FORMATO DXGI \_ \_ BC3 \_ UNORM \_ SRGB           |
| D3DFMT \_ D16 e D3DFMT \_ D16 \_ LOCKABLE  | FORMATO DXGI \_ \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32                            | Não disponível                                                        |
| D3DFMT \_ D15S1                          | Não disponível                                                        |
| D3DFMT \_ D24S8                          | Não disponível                                                        |
| D3DFMT \_ D24X8                          | Não disponível                                                        |
| D3DFMT \_ D24X4S4                        | Não disponível                                                        |
| D3DFMT \_ D16                            | FORMATO DXGI \_ \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32F \_ LOCKABLE                 | DXGI \_ FORMAT \_ D32 \_ FLOAT                                             |
| D3DFMT \_ D24FS8                         | Não disponível                                                        |
| D3DFMT \_ S1D15                          | Não disponível                                                        |
| D3DFMT \_ S8D24                          | FORMATO DXGI \_ \_ D24 \_ UNORM \_ S8 \_ UINT                                   |
| D3DFMT \_ X8D24                          | Não disponível                                                        |
| D3DFMT \_ X4S4D24                        | Não disponível                                                        |
| D3DFMT \_ L16                            | FORMATO DXGI \_ \_ R16 \_ UNORM 2                                           |
| D3DFMT \_ INDEX16                        | FORMATO DXGI \_ \_ R16 \_ UINT                                              |
| D3DFMT \_ INDEX32                        | FORMATO DXGI \_ \_ R32 \_ UINT                                              |
| D3DFMT \_ Q16W16V16U16                   | FORMATO DXGI \_ \_ R16G16B16A16 \_ SNORM                                    |
| D3DFMT \_ MULTI2 \_ ARGB8                  | Não disponível                                                        |
| D3DFMT \_ R16F                           | DXGI \_ FORMAT \_ R16 \_ FLOAT                                             |
| D3DFMT \_ G16R16F                        | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                          |
| D3DFMT \_ A16B16G16R16F                  | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                    |
| D3DFMT \_ R32F                           | DXGI \_ FORMAT \_ R32 \_ FLOAT                                             |
| D3DFMT \_ G32R32F                        | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                          |
| D3DFMT \_ A32B32G32R32F                  | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                    |
| D3DFMT \_ CxV8U8                         | Não disponível                                                        |
| D3DDECLTYPE \_ FLOAT1                    | DXGI \_ FORMAT \_ R32 \_ FLOAT                                             |
| D3DDECLTYPE \_ FLOAT2                    | DXGI \_ FORMAT \_ R32G32 \_ FLOAT                                          |
| D3DDECLTYPE \_ FLOAT3                    | DXGI \_ FORMAT \_ R32G32B32 \_ FLOAT                                       |
| D3DDECLTYPE \_ FLOAT4                    | DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT                                    |
| D3DDECLTYPED3DCOLOR                    | Não disponível                                                        |
| D3DDECLTYPE \_ UBYTE4                    | FORMATO DXGI \_ \_ R8G8B8A8 \_ UINT                                       |
| D3DDECLTYPE \_ SHORT2                    | DXGI \_ FORMAT \_ R16G16 \_ SINT                                           |
| D3DDECLTYPE \_ SHORT4                    | DXGI \_ FORMAT \_ R16G16B16A16 \_ SINT                                     |
| D3DDECLTYPE \_ UBYTE4N                   | DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM                                        |
| D3DDECLTYPE \_ SHORT2N                   | FORMATO DXGI \_ \_ R16G16 \_ SNORM                                          |
| D3DDECLTYPE \_ SHORT4N                   | FORMATO DXGI \_ \_ R16G16B16A16 \_ SNORM                                    |
| D3DDECLTYPE \_ USHORT2N                  | DXGI \_ FORMAT \_ R16G16 \_ UNORM                                          |
| D3DDECLTYPE \_ USHORT4N                  | DXGI \_ FORMAT \_ R16G16B16A16 \_ UNORM                                    |
| D3DDECLTYPE \_ UDEC3                     | Não disponível                                                        |
| D3DDECLTYPE \_ DEC3N                     | Não disponível                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2                | DXGI \_ FORMAT \_ R16G16 \_ FLOAT                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4                | DXGI \_ FORMAT \_ R16G16B16A16 \_ FLOAT                                    |



 

1.  Use .r swizzle em um sombreador para duplicar vermelho para outros componentes para obter o comportamento do Direct3D 9.
2.  No Direct3D 9, os dados foram dimensionados em 255,0f, o que pode ser feito no código do sombreador.
3.  DXT2 e DXT3 são os mesmos de uma perspectiva de API; DXT4 e DXT5 são os mesmos da perspectiva da API. A única diferença foi alfa pré-ultado, que pode ser acompanhado por um aplicativo e não precisa de um formato separado.
4.  Um sombreador obtém valores UINT, mas se o estilo integral do Direct3D 9 flutua (0,0f, 1,0f... 255.f) são necessários, o UINT pode ser convertido em float32 em um sombreador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



