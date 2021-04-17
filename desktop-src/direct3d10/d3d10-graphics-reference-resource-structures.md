---
description: Estruturas usadas para criar e usar recursos.
ms.assetid: d8fe2ebe-349a-456e-9a5a-16f2d3419800
title: Estruturas de recursos (gráficos do Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4da964bf19c1ce5e1e5c4dfd0685df79b28ac5e3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798375"
---
# <a name="resource-structures-direct3d-10-graphics"></a>Estruturas de recursos (gráficos do Direct3D 10)

Estruturas usadas para criar e usar [recursos](d3d10-graphics-programming-guide-resources-types.md).



| Estruturas                                                                 | Descrição                                                                                                                                                   |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**D3D10 \_ buffer \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_buffer_desc)                           | Descrição de um recurso de [buffer](d3d10-graphics-programming-guide-resources-types.md) .                                                                     |
| [**D3D10 \_ buffer \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_rtv)                             | Descreve os elementos em um [buffer](d3d10-graphics-programming-guide-resources-types.md) a ser usado em uma exibição de destino de renderização.                                |
| [**D3D10 do \_ buffer do \_ servidor**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_buffer_srv)                             | Descreve os elementos em um recurso de [buffer](d3d10-graphics-programming-guide-resources-types.md) para usar em uma exibição de recurso de sombreador.                         |
| [**Exibição de estêncil de profundidade de D3D10 \_ \_ \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_view_desc) | Descreve uma exibição de estêncil de profundidade.                                                                                                                               |
| [**\_TEXTURE2D d3d10 mapeado \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture2d)                 | Fornece acesso a dados de subrecurso em uma [textura 2D](d3d10-graphics-programming-guide-resources-types.md).                                                  |
| [**\_TEXTURE3D d3d10 mapeado \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_mapped_texture3d)                 | Fornece acesso a dados de subrecurso em uma [textura 3D](d3d10-graphics-programming-guide-resources-types.md).                                                  |
| [**D3D10 \_ de \_ exibição de destino de renderização \_ \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_render_target_view_desc) | Descreve uma exibição de destino de renderização.                                                                                                                               |
| [**\_Dados de SUBrecurso do d3d10 \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_subresource_data)                 | Especifica os dados para inicializar um recurso.                                                                                                                   |
| [**\_DSV de \_ matriz d3d10 TEX1D \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_dsv)                  | Especifica qual nível de mipmap e texturas em uma [matriz de textura 1D](d3d10-graphics-programming-guide-resources-types.md) usar em uma exibição de estêncil de profundidade.       |
| [**\_Matriz d3d10 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_rtv)                  | Especifica os subrecursos de uma matriz de [texturas 1D](d3d10-graphics-programming-guide-resources-types.md) a serem usadas em uma exibição de destino de renderização.             |
| [**D3D10 \_ TEX1D \_ matriz \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_array_srv)                  | Especifica os níveis de mipmap e texturas em uma [matriz de textura 1D](d3d10-graphics-programming-guide-resources-types.md) para usar em uma exibição de recurso de sombreador.      |
| [**\_DSV d3d10 TEX1D \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_dsv)                               | Especifica os subrecursos de uma [textura 1D](d3d10-graphics-programming-guide-resources-types.md) para usar em uma exibição de estêncil de profundidade.                        |
| [**D3D10 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_rtv)                               | Especifica os subrecursos de uma [textura 1D](d3d10-graphics-programming-guide-resources-types.md) para usar em uma exibição de destino de renderização.                        |
| [**D3D10 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex1d_srv)                               | Especifica os subrecursos de uma [textura 1D](d3d10-graphics-programming-guide-resources-types.md) para usar em uma exibição de recurso de sombreador.                      |
| [**\_DSV de \_ matriz d3d10 TEX2D \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)                  | Especifica qual nível de mipmap e quais texturas em uma [matriz de textura 2D](d3d10-graphics-programming-guide-resources-types.md) usar em uma exibição de estêncil de profundidade. |
| [**\_Matriz d3d10 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_rtv)                  | Especifica qual nível de mipmap e quais texturas em uma [matriz de textura 2D](d3d10-graphics-programming-guide-resources-types.md) usar em uma exibição de destino de renderização. |
| [**D3D10 \_ TEX2D \_ matriz \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_srv)                  | Especifica os subrecursos de uma matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) a serem usadas em uma exibição de recurso de sombreador.           |
| [**\_DSV d3d10 TEX2D \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_dsv)                               | Especifica os subrecursos de uma [textura 2D](d3d10-graphics-programming-guide-resources-types.md) para usar em uma exibição de estêncil de profundidade.                        |
| [**D3D10 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_rtv)                               | Especifica os subrecursos de uma [textura 2D](d3d10-graphics-programming-guide-resources-types.md) para usar em uma exibição de destino de renderização.                        |
| [**D3D10 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_srv)                               | Especifica os subrecursos de uma [textura 2D](d3d10-graphics-programming-guide-resources-types.md) para usar em uma exibição de recurso de sombreador.                      |
| [**\_DSV de \_ matriz d3d10 TEX2DMS \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_dsv)              | Especifica os subrecursos de uma matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) a serem usadas em uma exibição de estêncil de profundidade.             |
| [**\_Matriz d3d10 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_rtv)              | Especifica os subrecursos de uma matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) para usar em uma exibição de destino de renderização.             |
| [**D3D10 \_ TEX2DMS \_ matriz \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_array_srv)              | Especifica os subrecursos de uma matriz de [texturas 2D](d3d10-graphics-programming-guide-resources-types.md) a serem usadas em uma exibição de recurso de sombreador.           |
| [**\_DSV d3d10 TEX2DMS \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_dsv)                           | Especifica os subrecursos de uma [textura 2D](d3d10-graphics-programming-guide-resources-types.md) de uma amostra a ser usada em uma exibição de estêncil de profundidade.           |
| [**D3D10 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_rtv)                           | Especifica os subrecursos de uma [textura 2D](d3d10-graphics-programming-guide-resources-types.md) de uma amostra a ser usada em uma exibição de destino de renderização.           |
| [**D3D10 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2dms_srv)                           | Especifica os subrecursos de uma [textura 2D](d3d10-graphics-programming-guide-resources-types.md) de uma amostra a ser usada em uma exibição de recurso de sombreador.         |
| [**D3D10 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_rtv)                               | Especifica os subrecursos de uma [textura 3D](d3d10-graphics-programming-guide-resources-types.md) para usar em uma exibição de destino de renderização.                        |
| [**D3D10 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex3d_srv)                               | Especifica os subrecursos de uma [textura 3D](d3d10-graphics-programming-guide-resources-types.md) para usar em uma exibição de recurso de sombreador.                      |
| [**D3D10 \_ TEXCUBE \_ array \_ SRV1**](/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_texcube_array_srv1)            | Especifica os subrecursos de uma textura de [cubo](d3d10-graphics-programming-guide-resources-types.md) a ser usado em uma exibição de recurso de sombreador.                    |
| [**D3D10 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_texcube_srv)                           | Especifica os subrecursos de uma textura de [cubo](d3d10-graphics-programming-guide-resources-types.md) a ser usado em uma exibição de recurso de sombreador.                    |
| [**D3D10 \_ TEXTURE1D \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture1d_desc)                     | Descreve um recurso de [textura 1D](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |
| [**D3D10 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture2d_desc)                     | Descreve um recurso de [textura 2D](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |
| [**D3D10 \_ TEXTURE3D \_ desc**](/windows/desktop/api/D3D10/ns-d3d10-cd3d10_texture3d_desc)                     | Descreve um recurso de [textura 3D](d3d10-graphics-programming-guide-resources-types.md) .                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de recurso](d3d10-graphics-reference-resource.md)
</dt> </dl>

 

 



