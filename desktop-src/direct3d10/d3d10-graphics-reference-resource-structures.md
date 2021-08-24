---
description: Estruturas usadas para criar e usar recursos.
ms.assetid: d8fe2ebe-349a-456e-9a5a-16f2d3419800
title: Estruturas de recursos (elementos gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb45ff5d77d7bb0417b54b88a4014e2a96f522d2e026c778efcd05d23f624bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635016"
---
# <a name="resource-structures-direct3d-10-graphics"></a>Estruturas de recursos (elementos gráficos do Direct3D 10)

Estruturas usadas para criar e usar [recursos](d3d10-graphics-programming-guide-resources-types.md).



| Estruturas                                                                 | Descrição                                                                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D10 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)                           | Descrição de um [recurso de buffer.](d3d10-graphics-programming-guide-resources-types.md)                                                                     |
| [**D3D10 \_ BUFFER \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_rtv)                             | Descreve os elementos em um [buffer](d3d10-graphics-programming-guide-resources-types.md) a serem usados em uma exibição de destino de renderização.                                |
| [**SRV do BUFFER D3D10 \_ \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_srv)                             | Descreve os elementos em um recurso [de buffer](d3d10-graphics-programming-guide-resources-types.md) a ser usado em uma exibição sombreador-recurso.                         |
| [**D3D10 \_ \_ DESC DE EXIBIÇÃO DE ESTÊNCIL \_ DE \_ PROFUNDIDADE**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_view_desc) | Descreve uma exibição de estêncil de profundidade.                                                                                                                               |
| [**D3D10 \_ TEXTURA \_ MAPEADA2D**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture2d)                 | Fornece acesso a dados de sub-fonte em uma [textura 2D.](d3d10-graphics-programming-guide-resources-types.md)                                                  |
| [**D3D10 \_ TEXTURA \_ MAPEADA3D**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture3d)                 | Fornece acesso a dados de sub-fonte em uma [textura 3D.](d3d10-graphics-programming-guide-resources-types.md)                                                  |
| [**D3D10 \_ \_ RENDERIZAR EXIBIÇÃO \_ DE DESTINO \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_render_target_view_desc) | Descreve uma exibição de destino de renderização.                                                                                                                               |
| [**D3D10 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)                 | Especifica dados para inicializar um recurso.                                                                                                                   |
| [**D3D10 \_ TEX1D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_dsv)                  | Especifica qual nível de mipmap e texturas em uma matriz de textura [1D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de estêncil de profundidade.       |
| [**D3D10 \_ TEX1D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_rtv)                  | Especifica as sub-recursos de uma matriz de [texturas 1D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de destino de renderização.             |
| [**D3D10 \_ TEX1D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_srv)                  | Especifica os níveis de mipmap e texturas em uma matriz de textura [1D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de sombreador-recurso.      |
| [**D3D10 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_dsv)                               | Especifica as sub-recursos de uma textura [1D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de estêncil de profundidade.                        |
| [**D3D10 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_rtv)                               | Especifica as sub-recursos de uma textura [1D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de destino de renderização.                        |
| [**D3D10 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_srv)                               | Especifica as sub-fontes de uma textura [1D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de sombreador-recurso.                      |
| [**D3D10 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)                  | Especifica qual nível de mipmap e quais texturas em uma matriz de textura [2D](d3d10-graphics-programming-guide-resources-types.md) usar em uma exibição de estêncil de profundidade. |
| [**D3D10 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_rtv)                  | Especifica qual nível de mipmap e quais texturas em uma matriz de textura [2D](d3d10-graphics-programming-guide-resources-types.md) usar em uma exibição de destino de renderização. |
| [**D3D10 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_srv)                  | Especifica as sub-fontes de uma matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de sombreador-recurso.           |
| [**D3D10 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_dsv)                               | Especifica as sub-recursos de uma textura [2D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de estêncil de profundidade.                        |
| [**D3D10 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_rtv)                               | Especifica as sub-recursos de uma textura [2D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de destino de renderização.                        |
| [**D3D10 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_srv)                               | Especifica as sub-fontes de uma textura [2D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de sombreador-recurso.                      |
| [**D3D10 \_ TEX2DMS \_ ARRAY \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_dsv)              | Especifica as sub-recursos de uma matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de estêncil de profundidade.             |
| [**D3D10 \_ TEX2DMS \_ ARRAY \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_rtv)              | Especifica as sub-recursos de uma matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de destino de renderização.             |
| [**D3D10 \_ TEX2DMS \_ ARRAY \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_srv)              | Especifica as sub-fontes de uma matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de sombreador-recurso.           |
| [**D3D10 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_dsv)                           | Especifica as sub-recursos de uma textura [2D](d3d10-graphics-programming-guide-resources-types.md) multisampled a ser usada em uma exibição de estêncil de profundidade.           |
| [**D3D10 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_rtv)                           | Especifica as sub-recursos de uma textura [2D](d3d10-graphics-programming-guide-resources-types.md) multisampled a ser usada em uma exibição de destino de renderização.           |
| [**D3D10 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_srv)                           | Especifica as sub-fontes de uma textura [2D](d3d10-graphics-programming-guide-resources-types.md) multisampled a ser usada em uma exibição de sombreador-recurso.         |
| [**D3D10 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_rtv)                               | Especifica as sub-recursos de uma textura [3D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de destino de renderização.                        |
| [**D3D10 \_ SRV DO TEX3D \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_srv)                               | Especifica as sub-fontes de uma textura [3D](d3d10-graphics-programming-guide-resources-types.md) a ser usada em uma exibição de sombreador-recurso.                      |
| [**D3D10 \_ TEXCUBE \_ ARRAY \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)            | Especifica as sub-fontes de uma textura de cubo [a](d3d10-graphics-programming-guide-resources-types.md) ser usada em uma exibição sombreador-recurso.                    |
| [**D3D10 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_texcube_srv)                           | Especifica as sub-fontes de uma textura de cubo [a](d3d10-graphics-programming-guide-resources-types.md) ser usada em uma exibição sombreador-recurso.                    |
| [**D3D10 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture1d_desc)                     | Descreve um recurso [de textura 1D.](d3d10-graphics-programming-guide-resources-types.md)                                                                      |
| [**D3D10 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture2d_desc)                     | Descreve um recurso [de textura 2D.](d3d10-graphics-programming-guide-resources-types.md)                                                                      |
| [**D3D10 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture3d_desc)                     | Descreve um recurso [de textura 3D.](d3d10-graphics-programming-guide-resources-types.md)                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de recursos](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



