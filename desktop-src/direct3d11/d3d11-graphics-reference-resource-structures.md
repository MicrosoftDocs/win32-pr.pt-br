---
title: Estruturas de recursos (elementos gráficos do Direct3D 11)
description: Estruturas são usadas para criar e usar recursos.
ms.assetid: a29e01ac-8aa1-4a40-ad4d-3b738e129436
keywords:
- estruturas, recurso direct3D 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acff7e10538910082dcd15220cb41a2ec360c24472837a569530f0b306313db3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119125120"
---
# <a name="resource-structures-direct3d-11-graphics"></a>Estruturas de recursos (elementos gráficos do Direct3D 11)

Estruturas são usadas para criar e usar recursos.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                         | Descrição                                                                                                       |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**D3D11 \_ BUFFER \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)<br/>                                   | Descreve um recurso de buffer.<br/>                                                                           |
| [**D3D11 \_ BUFFER \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_rtv)<br/>                                     | Especifica os elementos em um recurso de buffer a ser usado em uma exibição de destino de renderização.<br/>                            |
| [**SRV do BUFFER D3D11 \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_srv)<br/>                                     | Especifica os elementos em um recurso de buffer a ser usado em uma exibição sombreador-recurso.<br/>                          |
| [**UAV DO BUFFER D3D11 \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_uav)<br/>                                     | Descreve os elementos em um buffer a ser usado em uma exibição de acesso não organizado.<br/>                                  |
| [**D3D11 \_ BUFFEREX \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_bufferex_srv)<br/>                                 | Descreve os elementos em um recurso de buffer bruto a ser usado em uma exibição sombreador-recurso.<br/>                      |
| [**D3D11 \_ \_ DESC DE EXIBIÇÃO DE ESTÊNCIL \_ DE \_ PROFUNDIDADE**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)<br/>         | Especifica as sub-recursos de uma textura que podem ser acessadas de uma exibição de estêncil de profundidade.<br/>                 |
| [**D3D11 \_ \_ SUBRESOURCE MAPEADA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource)<br/>                     | Fornece acesso a dados de sub-fonte.<br/>                                                                   |
| [**D3D11 \_ \_ MIP \_ DESC EMPACOTADO**](/windows/desktop/api/d3d11_2/ns-d3d11_2-d3d11_packed_mip_desc)<br/>                          | Descreve a estrutura de bloco de um recurso lado a lado com mipmaps. <br/>                                        |
| [**D3D11 \_ \_ RENDERIZAR EXIBIÇÃO \_ DE DESTINO \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_render_target_view_desc)<br/>         | Especifica as sub-fontes de um recurso que podem ser acessadas usando uma exibição de destino de renderização.<br/>             |
| [**D3D11 \_ \_ RENDERIZAR EXIBIÇÃO \_ DE DESTINO \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_render_target_view_desc1)<br/>       | Descreve as sub-fontes de um recurso que podem ser acessadas usando uma exibição de destino de renderização.<br/>             |
| [**D3D11 \_ DESC DE EXIBIÇÃO DE \_ RECURSOS DO \_ \_ SOMBREADOR**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)<br/>     | Descreve uma exibição sombreador-recurso.<br/>                                                                      |
| [**D3D11 \_ SHADER \_ RESOURCE \_ VIEW \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_shader_resource_view_desc1)<br/>   | Descreve uma exibição sombreador-recurso.<br/>                                                                      |
| [**D3D11 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_subresource_data)<br/>                         | Especifica dados para inicializar uma sub-fonte.<br/>                                                         |
| [**BLOCO D3D11 \_ SUBRESOURCE \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_subresource_tiling)<br/>                     | Descreve um volume de sub-fonte lado a lado.<br/>                                                                  |
| [**D3D11 \_ TEX1D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_dsv)<br/>                          | Especifica as sub-recursos de uma matriz de texturas 1D a ser usada em uma exibição de estêncil de profundidade.<br/>                |
| [**D3D11 \_ TEX1D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_rtv)<br/>                          | Especifica as sub-recursos de uma matriz de texturas 1D a ser usada em uma exibição de destino de renderização.<br/>                |
| [**D3D11 \_ TEX1D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_srv)<br/>                          | Especifica as sub-fontes de uma matriz de texturas 1D a ser usada em uma exibição de sombreador-recurso.<br/>              |
| [**D3D11 \_ TEX1D \_ ARRAY \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_array_uav)<br/>                          | Descreve uma matriz de recursos de textura 1D de acesso não organizado.<br/>                                           |
| [**D3D11 \_ TEX1D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_dsv)<br/>                                       | Especifica a sub-fonte de uma textura 1D acessível a uma exibição de estêncil de profundidade.<br/>                |
| [**D3D11 \_ TEX1D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_rtv)<br/>                                       | Especifica a sub-fonte de uma textura 1D a ser usada em uma exibição de destino de renderização.<br/>                            |
| [**D3D11 \_ TEX1D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_srv)<br/>                                       | Especifica a sub-fonte de uma textura 1D a ser usada em uma exibição sombreador-recurso.<br/>                          |
| [**D3D11 \_ TEX1D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex1d_uav)<br/>                                       | Descreve um recurso de textura 1D de acesso não organizado.<br/>                                                      |
| [**D3D11 \_ TEX2D \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_dsv)<br/>                          | Especifica as sub-recursos de uma matriz de texturas 2D acessíveis a uma exibição de estêncil de profundidade.<br/>      |
| [**D3D11 \_ TEX2D \_ ARRAY \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_rtv)<br/>                          | Especifica as sub-recursos de uma matriz de texturas 2D a ser usada em uma exibição de destino de renderização.<br/>                |
| [**D3D11 \_ TEX2D \_ ARRAY \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_rtv1)<br/>                        | Descreve as sub-recursos de uma matriz de texturas 2D a ser usada em uma exibição de destino de renderização.<br/>                |
| [**D3D11 \_ TEX2D \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_srv)<br/>                          | Especifica as sub-fontes de uma matriz de texturas 2D a ser usada em uma exibição de sombreador-recurso.<br/>              |
| [**D3D11 \_ TEX2D \_ ARRAY \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_srv1)<br/>                        | Descreve as sub-fontes de uma matriz de texturas 2D a ser usada em uma exibição de sombreador-recurso.<br/>              |
| [**D3D11 \_ TEX2D \_ ARRAY \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_array_uav)<br/>                          | Descreve uma matriz de recursos de textura 2D de acesso não organizado.<br/>                                           |
| [**D3D11 \_ TEX2D \_ ARRAY \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_array_uav1)<br/>                        | Descreve uma matriz de recursos de textura 2D de acesso não organizado.<br/>                                           |
| [**D3D11 \_ TEX2D \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_dsv)<br/>                                       | Especifica a sub-fonte de uma textura 2D acessível a uma exibição de estêncil de profundidade.<br/>                |
| [**D3D11 \_ TEX2D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_rtv)<br/>                                       | Especifica a sub-fonte de uma textura 2D a ser usada em uma exibição de destino de renderização.<br/>                            |
| [**D3D11 \_ TEX2D \_ RTV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_rtv1)<br/>                                     | Descreve a sub-fonte de uma textura 2D a ser usada em uma exibição de destino de renderização.<br/>                            |
| [**D3D11 \_ TEX2D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_srv)<br/>                                       | Especifica a sub-fonte de uma textura 2D a ser usada em uma exibição de sombreador-recurso.<br/>                          |
| [**D3D11 \_ TEX2D \_ SRV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_srv1)<br/>                                     | Descreve a sub-fonte de uma textura 2D a ser usada em uma exibição sombreador-recurso.<br/>                          |
| [**D3D11 \_ TEXAS2D \_ UAV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2d_uav)<br/>                                       | Descreve um recurso de textura 2D de acesso não organizado.<br/>                                                      |
| [**D3D11 \_ TEX2D \_ UAV1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-d3d11_tex2d_uav1)<br/>                                     | Descreve um recurso de textura 2D de acesso não organizado.<br/>                                                      |
| [**D3D11 \_ TEX2DMS \_ ARRAY \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_dsv)<br/>                      | Especifica as sub-recursos de uma matriz de texturas 2D multisampled para uma exibição de estêncil de profundidade.<br/>         |
| [**D3D11 \_ TEX2DMS \_ ARRAY \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_rtv)<br/>                      | Especifica as sub-recursos de uma matriz de texturas 2D multisampled a ser usada em uma exibição de destino de renderização.<br/> |
| [**D3D11 \_ TEX2DMS \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_array_srv)<br/>                      | Especifica as sub-fontes de uma matriz de texturas 2D multisampled a ser usada em uma exibição sombreador-recurso.<br/> |
| [**D3D11 \_ TEX2DMS \_ DSV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_dsv)<br/>                                   | Especifica a sub-fonte de uma textura 2D multisampled que é acessível a uma exibição de estêncil de profundidade.<br/>   |
| [**D3D11 \_ TEX2DMS \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_rtv)<br/>                                   | Especifica a sub-fonte de uma textura 2D multisampled a ser usada em uma exibição de destino de renderização.<br/>               |
| [**D3D11 \_ TEX2DMS \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex2dms_srv)<br/>                                   | Especifica as sub-fontes de uma textura 2D multisampled a ser usada em uma exibição de sombreador-recurso.<br/>            |
| [**D3D11 \_ TEX3D \_ RTV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_rtv)<br/>                                       | Especifica as sub-recursos de uma textura 3D a ser usada em uma exibição de destino de renderização.<br/>                           |
| [**D3D11 \_ TEX3D \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_srv)<br/>                                       | Especifica as sub-fontes de uma textura 3D a ser usada em uma exibição de sombreador-recurso.<br/>                         |
| [**D3D11 \_ UAV DO TEX3D \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_tex3d_uav)<br/>                                       | Descreve um recurso de textura 3D de acesso não organizado.<br/>                                                      |
| [**D3D11 \_ TEXCUBE \_ ARRAY \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_array_srv)<br/>                      | Especifica as sub-fontes de uma matriz de texturas de cubo a ser usada em uma exibição de sombreador-recurso.<br/>            |
| [**D3D11 \_ TEXCUBE \_ SRV**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texcube_srv)<br/>                                   | Especifica a sub-fonte de uma textura de cubo a ser usada em uma exibição sombreador-recurso.<br/>                        |
| [**D3D11 \_ TEXTURE1D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture1d_desc)<br/>                             | Descreve uma textura 1D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture2d_desc)<br/>                             | Descreve uma textura 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE2D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture2d_desc1)<br/>                           | Descreve uma textura 2D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_texture3d_desc)<br/>                             | Descreve uma textura 3D.<br/>                                                                                |
| [**D3D11 \_ TEXTURE3D \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_texture3d_desc1)<br/>                           | Descreve uma textura 3D.<br/>                                                                                |
| [**TAMANHO DA REGIÃO DO TILE D3D11 \_ \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_region_size)<br/>                        | Descreve o tamanho de uma região lado a lado.<br/>                                                                  |
| [**D3D11 \_ COORDENADA DE RECURSO LADO A \_ \_ LADO**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tiled_resource_coordinate)<br/>      | Descreve as coordenadas de um recurso lado a lado.<br/>                                                         |
| [**FORMA DO TILE D3D11 \_ \_**](/windows/desktop/api/D3D11_2/ns-d3d11_2-d3d11_tile_shape)<br/>                                     | Descreve a forma de um lado especificando suas dimensões.<br/>                                            |
| [**D3D11 \_ DESC DE EXIBIÇÃO DE \_ ACESSO NÃO \_ \_ ORGANIZADO**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_unordered_access_view_desc)<br/>   | Especifica as sub-fontes de um recurso que podem ser acessadas usando uma exibição de acesso não organizado.<br/>         |
| [**D3D11 EXIBIÇÃO DE ACESSO NÃO \_ \_ ORGANIZADO \_ \_ DESC1**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_unordered_access_view_desc1)<br/> | Descreve as sub-fontes de um recurso que podem ser acessadas usando uma exibição de acesso não organizado.<br/>         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de recursos](d3d11-graphics-reference-resource.md)
</dt> </dl>

 

 





