---
description: Esta tabela lista os formatos Direct3D 9 que podem ser mapeados para um formato Direct3D 10.
ms.assetid: 07c9b827-6e2e-4599-b48a-f726484b643d
title: 'Formatos herdados: mapeie os formatos do Direct3D 9 para o Direct3D 10'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 230b8ed17984d47a3b57ce287aa9b434a2b92aae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760591"
---
# <a name="legacy-formats-map-direct3d-9-formats-to-direct3d-10"></a>Formatos herdados: mapeie os formatos do Direct3D 9 para o Direct3D 10

Esta tabela lista os formatos Direct3D 9 que podem ser mapeados para um formato Direct3D 10. Os formatos do Direct3D 10 divergiram dos formatos do Direct3D 9 para que os formatos de vértice e de textura possam ser mesclados para permitir aplicativos entre endian.



| Formato de textura/vértice/índice do Direct3D 9 | Formato do Direct3D 10 equivalente                                        |
|----------------------------------------|----------------------------------------------------------------------|
| D3DFMT \_ desconhecido                        | \_formato dxgi \_ desconhecido                                                |
| D3DFMT \_ R8G8B8                         | Não disponível                                                        |
| D3DFMT \_ A8R8G8B8                       | \_Formato dxgi \_ B8G8R8A8 \_ UNORM (dxgi 1,1)                             |
| D3DFMT \_ X8R8G8B8                       | \_Formato dxgi \_ B8G8R8X8 \_ UNORM (dxgi 1,1)                             |
| D3DFMT \_ R5G6B5                         | \_Formato dxgi \_ B5G6R5 \_ UNORM (dxgi 1,2)                               |
| D3DFMT \_ X1R5G5B5                       | Não disponível                                                        |
| D3DFMT \_ A1R5G5B5                       | \_Formato dxgi \_ B5G5R5A1 \_ UNORM (dxgi 1,2)                             |
| D3DFMT \_ A4R4G4B4                       | \_Formato dxgi \_ B4G4R4A4 \_ UNORM (dxgi 1,2)                             |
| D3DFMT \_ R3G3B2                         | Não disponível                                                        |
| D3DFMT \_ a8                             | \_Formato dxgi \_ a8 \_ UNORM                                              |
| D3DFMT \_ A8R3G3B2                       | Não disponível                                                        |
| D3DFMT \_ X4R4G4B4                       | Não disponível                                                        |
| D3DFMT \_ A2B10G10R10                    | \_R10G10B10A2 de formato dxgi \_                                            |
| D3DFMT \_ A8B8G8R8                       | Formato \_ dxgi \_ R8G8B8A8 \_ UNORM ou dxgi \_ \_ R8G8B8A8 \_ UNORM \_ sRGB |
| D3DFMT \_ X8B8G8R8                       | Não disponível                                                        |
| D3DFMT \_ G16R16                         | \_Formato dxgi \_ R16G16 \_ UNORM                                          |
| D3DFMT \_ A2R10G10B10                    | Não disponível                                                        |
| D3DFMT \_ A16B16G16R16                   | \_Formato dxgi \_ R16G16B16A16 \_ UNORM                                    |
| D3DFMT \_ A8P8                           | Não disponível                                                        |
| D3DFMT \_ P8                             | Não disponível                                                        |
| \_L8 D3DFMT                             | \_UNORM de R8 de formato dxgi \_ \_ ¹                                            |
| D3DFMT \_ A8L8                           | Não disponível                                                        |
| D3DFMT \_ A4L4                           | Não disponível                                                        |
| D3DFMT \_ V8U8                           | \_Formato dxgi \_ R8G8 \_ SNORM                                            |
| D3DFMT \_ L6V5U5                         | Não disponível                                                        |
| D3DFMT \_ X8L8V8U8                       | Não disponível                                                        |
| D3DFMT \_ Q8W8V8U8                       | \_Formato dxgi \_ R8G8B8A8 \_ SNORM                                        |
| D3DFMT \_ V16U16                         | \_Formato dxgi \_ R16G16 \_ SNORM                                          |
| D3DFMT \_ W11V11U10                      | Não disponível                                                        |
| D3DFMT \_ A2W10V10U10                    | Não disponível                                                        |
| D3DFMT \_ UYVY                           | Não disponível                                                        |
| D3DFMT \_ R8G8 \_ B8G8                     | \_Formato dxgi \_ G8R8 \_ G8B8 \_ UNORM ²                                    |
| D3DFMT \_ YUY2                           | Não disponível                                                        |
| D3DFMT \_ G8R8 \_ G8B8                     | \_Formato dxgi \_ R8G8 \_ B8G8 \_ UNORM ²                                    |
| D3DFMT \_ DXT1                           | Formato \_ dxgi \_ BC1 \_ UNORM ou dxgi \_ \_ BC1 \_ UNORM \_ sRGB           |
| D3DFMT \_ DXT2                           | Formato \_ dxgi \_ BC2 \_ UNORM ou dxgi \_ \_ BC2 \_ UNORM \_ sRGB ³         |
| D3DFMT \_ DXT3                           | Formato \_ dxgi \_ BC2 \_ UNORM ou dxgi \_ \_ BC2 \_ UNORM \_ sRGB           |
| D3DFMT \_ DXT4                           | Formato \_ dxgi \_ BC3 \_ UNORM ou dxgi \_ \_ BC3 \_ UNORM \_ sRGB ³         |
| D3DFMT \_ DXT5                           | Formato \_ dxgi \_ BC3 \_ UNORM ou dxgi \_ \_ BC3 \_ UNORM \_ sRGB           |
| D3DFMT \_ D16 e D3DFMT \_ D16 \_ bloqueáveis  | \_Formato dxgi \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32                            | Não disponível                                                        |
| D3DFMT \_ D15S1                          | Não disponível                                                        |
| D3DFMT \_ D24S8                          | Não disponível                                                        |
| D3DFMT \_ D24X8                          | Não disponível                                                        |
| D3DFMT \_ D24X4S4                        | Não disponível                                                        |
| D3DFMT \_ D16                            | \_Formato dxgi \_ D16 \_ UNORM                                             |
| D3DFMT \_ D32F \_ bloqueáveis                 | \_ \_ Float D32 de formato dxgi \_                                             |
| D3DFMT \_ D24FS8                         | Não disponível                                                        |
| D3DFMT \_ S1D15                          | Não disponível                                                        |
| D3DFMT \_ S8D24                          | \_Formato dxgi \_ D24 \_ UNORM \_ S8 \_ uint                                   |
| D3DFMT \_ X8D24                          | Não disponível                                                        |
| D3DFMT \_ X4S4D24                        | Não disponível                                                        |
| D3DFMT \_ L16                            | \_Formato dxgi \_ R16 \_ UNORM ¹                                           |
| D3DFMT \_ INDEX16                        | \_Formato dxgi \_ R16 \_ uint                                              |
| D3DFMT \_ INDEX32                        | \_Formato dxgi \_ R32 \_ uint                                              |
| D3DFMT \_ Q16W16V16U16                   | \_Formato dxgi \_ R16G16B16A16 \_ SNORM                                    |
| D3DFMT \_ Multi2 \_ ARGB8                  | Não disponível                                                        |
| D3DFMT \_ R16F                           | \_ \_ Float R16 de formato dxgi \_                                             |
| D3DFMT \_ G16R16F                        | \_ \_ Float R16G16 de formato dxgi \_                                          |
| D3DFMT \_ A16B16G16R16F                  | \_ \_ Float R16G16B16A16 de formato dxgi \_                                    |
| D3DFMT \_ R32F                           | \_ \_ Float R32 de formato dxgi \_                                             |
| D3DFMT \_ G32R32F                        | \_ \_ Float R32G32 de formato dxgi \_                                          |
| D3DFMT \_ A32B32G32R32F                  | \_ \_ Float R32G32B32A32 de formato dxgi \_                                    |
| D3DFMT \_ CxV8U8                         | Não disponível                                                        |
| D3DDECLTYPE \_ FLOAT1                    | \_ \_ Float R32 de formato dxgi \_                                             |
| D3DDECLTYPE \_ FLOAT2                    | \_ \_ Float R32G32 de formato dxgi \_                                          |
| D3DDECLTYPE \_ FLOAT3                    | \_ \_ Float R32G32B32 de formato dxgi \_                                       |
| D3DDECLTYPE \_ FLOAT4                    | \_ \_ Float R32G32B32A32 de formato dxgi \_                                    |
| D3DDECLTYPED3DCOLOR                    | Não disponível                                                        |
| D3DDECLTYPE \_ UBYTE4                    | \_Formato dxgi \_ R8G8B8A8 \_ uint ⁴                                       |
| D3DDECLTYPE \_ SHORT2                    | \_Formato dxgi \_ R16G16 \_ Santo                                           |
| D3DDECLTYPE \_ SHORT4                    | \_Formato dxgi \_ R16G16B16A16 \_ Santo                                     |
| D3DDECLTYPE \_ UBYTE4N                   | \_Formato dxgi \_ R8G8B8A8 \_ UNORM                                        |
| D3DDECLTYPE \_ SHORT2N                   | \_Formato dxgi \_ R16G16 \_ SNORM                                          |
| D3DDECLTYPE \_ SHORT4N                   | \_Formato dxgi \_ R16G16B16A16 \_ SNORM                                    |
| D3DDECLTYPE \_ USHORT2N                  | \_Formato dxgi \_ R16G16 \_ UNORM                                          |
| D3DDECLTYPE \_ USHORT4N                  | \_Formato dxgi \_ R16G16B16A16 \_ UNORM                                    |
| D3DDECLTYPE \_ UDEC3                     | Não disponível                                                        |
| D3DDECLTYPE \_ DEC3N                     | Não disponível                                                        |
| D3DDECLTYPE \_ FLOAT16 \_ 2                | \_ \_ Float R16G16 de formato dxgi \_                                          |
| D3DDECLTYPE \_ FLOAT16 \_ 4                | \_ \_ Float R16G16B16A16 de formato dxgi \_                                    |



 

1.  Use swizzle. r em um sombreador para duplicar vermelho para outros componentes para obter o comportamento do Direct3D 9.
2.  No Direct3D 9, os dados foram escalados verticalmente por 255.0 f, o que pode ser feito no código do sombreador.
3.  DXT2 e DXT3 são os mesmos de uma perspectiva de API; DXT4 e DXT5 são os mesmos de uma perspectiva de API. A única diferença foi contramultiplicada por alfa, que pode ser rastreada por um aplicativo e não precisa de um formato separado.
4.  Um sombreador obtém valores UINT, mas se o Direct3D 9 Style integral flutua (0,0 f, 1,0 f... 255. f) são necessários, UINT pode ser convertido em float32 em um sombreador.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 



