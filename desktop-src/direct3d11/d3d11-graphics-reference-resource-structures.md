---
title: Estruturas de recursos (gráficos do Direct3D 11)
description: Estruturas são usadas para criar e usar recursos.
ms.assetid: a29e01ac-8aa1-4a40-ad4d-3b738e129436
keywords:
- estruturas, recurso do Direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5020792e1fb56a52e7a4354964c45bb5d65bbba4
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103824126"
---
# <a name="resource-structures-direct3d-11-graphics"></a>Estruturas de recursos (gráficos do Direct3D 11)

Estruturas são usadas para criar e usar recursos.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                         | Descrição                                                                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**D3D11 \_ buffer \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)<br/>                                   | Descreve um recurso de buffer.<br/>                                                                           |
| [**D3D11 \_ buffer \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_rtv)<br/>                                     | Especifica os elementos em um recurso de buffer para usar em uma exibição de destino de renderização.<br/>                            |
| [**D3D11 do \_ buffer do \_ servidor**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_srv)<br/>                                     | Especifica os elementos em um recurso de buffer a ser usado em uma exibição de recurso de sombreador.<br/>                          |
| [**D3D11 \_ buffer \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav)<br/>                                     | Descreve os elementos em um buffer para usar em uma exibição de acesso não ordenado.<br/>                                  |
| [**D3D11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv)<br/>                                 | Descreve os elementos em um recurso de buffer bruto para usar em uma exibição de recurso de sombreador.<br/>                      |
| [**Exibição de estêncil de profundidade de D3D11 \_ \_ \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)<br/>         | Especifica os subrecursos de uma textura que são acessíveis a partir de uma exibição de estêncil de profundidade.<br/>                 |
| [**\_Subrecurso MAPEADO D3D11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource)<br/>                     | Fornece acesso a dados de subrecurso.<br/>                                                                   |
| [**D3D11 de \_ MIP embalado empacotado \_ \_**](/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_packed_mip_desc)<br/>                          | Descreve a estrutura lado a lado de um recurso de mosaico com mipmaps. <br/>                                        |
| [**D3D11 \_ de \_ exibição de destino de renderização \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc)<br/>         | Especifica os subrecursos de um recurso que são acessíveis usando uma exibição de destino de renderização.<br/>             |
| [**D3D11 \_ de \_ exibição de destino de renderização \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_render_target_view_desc1)<br/>       | Descreve os subrecursos de um recurso que são acessíveis usando uma exibição de destino de renderização.<br/>             |
| [**\_Exibição de recursos do sombreador D3D11 \_ \_ \_ desc**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)<br/>     | Descreve uma exibição de recurso de sombreador.<br/>                                                                      |
| [**\_DESC1 da \_ exibição de recursos do SOMBREAdor D3D11 \_ \_**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_shader_resource_view_desc1)<br/>   | Descreve uma exibição de recurso de sombreador.<br/>                                                                      |
| [**\_Dados de SUBrecurso do D3D11 \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)<br/>                         | Especifica os dados para inicializar um subrecurso.<br/>                                                         |
| [**SubD3D11 de \_ SUBrecurso \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_subresource_tiling)<br/>                     | Descreve um volume de subrecurso em ladrilho.<br/>                                                                  |
| [**\_DSV de \_ matriz D3D11 TEX1D \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_dsv)<br/>                          | Especifica os subrecursos de uma matriz de texturas 1D a serem usadas em uma exibição de estêncil de profundidade.<br/>                |
| [**\_Matriz D3D11 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_rtv)<br/>                          | Especifica os subrecursos de uma matriz de texturas 1D a serem usadas em uma exibição de destino de renderização.<br/>                |
| [**D3D11 \_ TEX1D \_ matriz \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_srv)<br/>                          | Especifica os subrecursos de uma matriz de texturas 1D a serem usadas em uma exibição de recurso de sombreador.<br/>              |
| [**\_Matriz D3D11 \_ TEX1D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_uav)<br/>                          | Descreve uma matriz de recursos de textura de 1D de acesso não ordenado.<br/>                                           |
| [**\_DSV D3D11 TEX1D \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_dsv)<br/>                                       | Especifica o subrecurso de uma textura 1D que é acessível para uma exibição de estêncil de profundidade.<br/>                |
| [**D3D11 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_rtv)<br/>                                       | Especifica o subrecurso de uma textura 1D para usar em uma exibição de destino de renderização.<br/>                            |
| [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)<br/>                                       | Especifica o subrecurso de uma textura 1D para usar em um modo de exibição de recurso de sombreador.<br/>                          |
| [**D3D11 \_ TEX1D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_uav)<br/>                                       | Descreve um recurso de textura de 1D de acesso não ordenado.<br/>                                                      |
| [**\_DSV de \_ matriz D3D11 TEX2D \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv)<br/>                          | Especifica os subrecursos de texturas 2D de matriz que são acessíveis a uma exibição de estêncil de profundidade.<br/>      |
| [**\_Matriz D3D11 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_rtv)<br/>                          | Especifica os subrecursos de uma matriz de texturas 2D a serem usadas em uma exibição de destino de renderização.<br/>                |
| [**\_Matriz D3D11 \_ TEX2D \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_rtv1)<br/>                        | Descreve os subrecursos de uma matriz de texturas 2D para usar em uma exibição de destino de renderização.<br/>                |
| [**D3D11 \_ TEX2D \_ matriz \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_srv)<br/>                          | Especifica os subrecursos de uma matriz de texturas 2D a serem usadas em uma exibição de recurso de sombreador.<br/>              |
| [**D3D11 \_ TEX2D \_ array \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_srv1)<br/>                        | Descreve os subrecursos de uma matriz de texturas 2D para usar em uma exibição de recurso de sombreador.<br/>              |
| [**\_Matriz D3D11 \_ TEX2D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_uav)<br/>                          | Descreve uma matriz de recursos de textura 2D de acesso não ordenado.<br/>                                           |
| [**\_Matriz D3D11 \_ TEX2D \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_uav1)<br/>                        | Descreve uma matriz de recursos de textura 2D de acesso não ordenado.<br/>                                           |
| [**\_DSV D3D11 TEX2D \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_dsv)<br/>                                       | Especifica o subrecurso de uma textura 2D que é acessível para uma exibição de estêncil de profundidade.<br/>                |
| [**D3D11 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_rtv)<br/>                                       | Especifica o subrecurso de uma textura 2D a ser usado em uma exibição de destino de renderização.<br/>                            |
| [**D3D11 \_ TEX2D \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_rtv1)<br/>                                     | Descreve o subrecurso de uma textura 2D para usar em uma exibição de destino de renderização.<br/>                            |
| [**D3D11 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_srv)<br/>                                       | Especifica o subrecurso de uma textura 2D a ser usado em um modo de exibição de recurso de sombreador.<br/>                          |
| [**D3D11 \_ TEX2D \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_srv1)<br/>                                     | Descreve o subrecurso de uma textura 2D para usar em uma exibição de recurso de sombreador.<br/>                          |
| [**D3D11 \_ TEX2D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_uav)<br/>                                       | Descreve um recurso de textura 2D de acesso não ordenado.<br/>                                                      |
| [**D3D11 \_ TEX2D \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_uav1)<br/>                                     | Descreve um recurso de textura 2D de acesso não ordenado.<br/>                                                      |
| [**\_DSV de \_ matriz D3D11 TEX2DMS \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_dsv)<br/>                      | Especifica os subrecursos de uma matriz de texturas 2D de uma amostra para uma exibição de estêncil de profundidade.<br/>         |
| [**\_Matriz D3D11 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_rtv)<br/>                      | Especifica os subrecursos de uma matriz de texturas 2D de amostra para usar em uma exibição de destino de renderização.<br/> |
| [**D3D11 \_ TEX2DMS \_ matriz \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_srv)<br/>                      | Especifica os subrecursos de uma matriz de texturas 2D de amostra para usar em uma exibição de recurso de sombreador.<br/> |
| [**\_DSV D3D11 TEX2DMS \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_dsv)<br/>                                   | Especifica o subrecurso de uma textura 2D de amostra que é acessível para uma exibição de estêncil de profundidade.<br/>   |
| [**D3D11 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_rtv)<br/>                                   | Especifica o subrecurso de uma textura 2D com uma amostra a ser usada em uma exibição de destino de renderização.<br/>               |
| [**D3D11 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_srv)<br/>                                   | Especifica os subrecursos de uma textura 2D de amostra para usar em uma exibição de recurso de sombreador.<br/>            |
| [**D3D11 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_rtv)<br/>                                       | Especifica os subrecursos de uma textura 3D para usar em uma exibição de destino de renderização.<br/>                           |
| [**D3D11 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_srv)<br/>                                       | Especifica os subrecursos de uma textura 3D para usar em uma exibição de recurso de sombreador.<br/>                         |
| [**D3D11 \_ TEX3D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_uav)<br/>                                       | Descreve um recurso de textura 3D de acesso não ordenado.<br/>                                                      |
| [**D3D11 \_ TEXCUBE \_ matriz \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_array_srv)<br/>                      | Especifica os subrecursos de uma matriz de texturas de cubo a ser usada em uma exibição de recurso de sombreador.<br/>            |
| [**D3D11 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_srv)<br/>                                   | Especifica o subrecurso de uma textura de cubo a ser usada em uma exibição de recurso de sombreador.<br/>                        |
| [**D3D11 \_ TEXTURE1D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture1d_desc)<br/>                             | Descreve uma textura 1D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)<br/>                             | Descreve uma textura 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1)<br/>                           | Descreve uma textura 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture3d_desc)<br/>                             | Descreve uma textura 3D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1)<br/>                           | Descreve uma textura 3D.<br/>                                                                                |
| [**\_Tamanho da \_ região do bloco D3D11 \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size)<br/>                        | Descreve o tamanho de uma região em ladrilho.<br/>                                                                  |
| [**\_ \_ Coordenada de recurso de lado D3D11 \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate)<br/>      | Descreve as coordenadas de um recurso em ladrilho.<br/>                                                         |
| [**\_Forma do bloco D3D11 \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape)<br/>                                     | Descreve a forma de um bloco especificando suas dimensões.<br/>                                            |
| [**\_Modo de exibição de acesso não ordenado D3D11 \_ \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc)<br/>   | Especifica os subrecursos de um recurso que são acessíveis usando uma exibição de acesso não ordenado.<br/>         |
| [**D3D11 \_ modo de exibição de acesso não ordenado \_ \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_unordered_access_view_desc1)<br/> | Descreve os subrecursos de um recurso que são acessíveis usando uma exibição de acesso não ordenado.<br/>         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de recurso](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





