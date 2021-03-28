---
title: Métodos 10Level9 ID3D11Device
description: Esta seção lista as diferenças entre cada nível de recurso 10Level9 e o nível de recurso do D3D \_ \_ \_ 11 \_ 0 e superior para os métodos ID3D11Device.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 400c7f321981f13b3e184a25139782c8a9d9a2ba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366455"
---
# <a name="10level9-id3d11device-methods"></a>Métodos 10Level9 ID3D11Device

Esta seção lista as diferenças entre cada nível de recurso 10Level9 e o nível de recurso do D3D \_ \_ \_ 11 \_ 0 e superior para os métodos [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) .

-   [ID3D11Device::CheckCounter](#id3d11devicecheckcounter)
-   [ID3D11Device::CheckFormatSupport](#id3d11devicecheckformatsupport)
-   [ID3D11Device::CheckMultisampleQualityLevels](#id3d11devicecheckmultisamplequalitylevels)
-   [ID3D11Device:: createblendstate](#id3d11devicecreateblendstate)
-   [ID3D11Device::CreateBlendState1](#id3d11devicecreateblendstate1)
-   [ID3D11Device:: CreateBuffer](#id3d11devicecreatebuffer)
-   [ID3D11Device:: createcounterer](#id3d11devicecreatecounter)
-   [ID3D11Device::CreateDepthStencilView](#id3d11devicecreatedepthstencilview)
-   [ID3D11Device::CreateDomainShader](#id3d11devicecreatedomainshader)
-   [ID3D11Device::CreateGeometryShader](#id3d11devicecreategeometryshader)
-   [ID3D11Device::CreateGeometryShaderWithStreamOutput](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [ID3D11Device::CreateHullShader](#id3d11devicecreatehullshader)
-   [ID3D11Device::CreateInputLayout](#id3d11devicecreateinputlayout)
-   [ID3D11Device::CreatePixelShader](#id3d11devicecreatepixelshader)
-   [ID3D11Device:: predicado](#id3d11devicecreatepredicate)
-   [ID3D11Device:: CreateQuery](#id3d11devicecreatequery)
-   [ID3D11Device::CreateRasterizerState](#id3d11devicecreaterasterizerstate)
-   [ID3D11Device::CreateRenderTargetView](#id3d11devicecreaterendertargetview)
-   [ID3D11Device:: createsamplestate](#id3d11devicecreatesamplerstate)
-   [ID3D11Device::CreateShaderResourceView](#id3d11devicecreateshaderresourceview)
-   [ID3D11Device::CreateTexture1D](#id3d11devicecreatetexture1d)
-   [ID3D11Device::CreateTexture2D](#id3d11devicecreatetexture2d)
-   [ID3D11Device::CreateTexture3D](#id3d11devicecreatetexture3d)
-   [ID3D11Device::CreateUnorderedAccessView](#id3d11devicecreateunorderedaccessview)
-   [ID3D11Device::CreateVertexShader](#id3d11devicecreatevertexshader)
-   [ID3D11Device::OpenSharedResource](#id3d11deviceopensharedresource)
-   [Tópicos relacionados](#related-topics)

## <a name="id3d11devicecheckcounter"></a>ID3D11Device::CheckCounter



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Os contadores dependentes do dispositivo têm suporte opcional. Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device:: CheckCounterInfo</strong></a> para determinar o suporte. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckformatsupport"></a>ID3D11Device::CheckFormatSupport



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Consulte suporte de formato por <a href="overviews-direct3d-11-devices-downlevel-intro.md">nível de recurso</a>$ {remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a>ID3D11Device::CheckMultisampleQualityLevels



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Os níveis de recurso não oferecem nenhuma garantia relativa ao suporte a MSAA. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateblendstate"></a>ID3D11Device:: createblendstate



| Nível de recursos              | Diferenças de comportamento                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nível de recurso do D3D \_ \_ \_ 9 \_ 1  | AlphaToCoverageEnable deve ser **false**.<br/> Os primeiros quatro BlendEnables devem ter o mesmo valor.<br/> D3D11 \_ Blend \_ src \_ ALPHASAT não tem suporte.<br/> Mistura de cores de fonte dupla sem suporte (qualquer SrcBlend ou DestBlend com SRC1 no nome)<br/>                                                                                |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 2  | AlphaToCoverageEnable deve ser **false**.<br/> Os primeiros quatro BlendEnables devem ter o mesmo valor.<br/> Os primeiros quatro RenderTargetWriteMasks devem ter o mesmo valor.<br/> D3D11 \_ Blend \_ src \_ ALPHASAT não tem suporte.<br/> Mistura de cores de fonte dupla sem suporte (qualquer SrcBlend ou DestBlend com SRC1 no nome)<br/> |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 3  | AlphaToCoverageEnable deve ser **false**.<br/> Os primeiros quatro BlendEnables devem ter o mesmo valor.<br/> D3D11 \_ Blend \_ src \_ ALPHASAT não tem suporte.<br/> Mistura de cores de fonte dupla sem suporte (qualquer SrcBlend ou DestBlend com SRC1 no nome)<br/>                                                                                |
| Nível de recurso do D3D \_ \_ \_ 10 \_ 0 | Adiciona alfa para cobertura                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a>ID3D11Device::CreateBlendState1



| Nível de recursos              | Diferenças de comportamento                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nível de recurso do D3D \_ \_ \_ 9 \_ 1  | Sem suporte<br/>                                                                                                                                                                                                                                                                                                                                       |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 2  | Sem suporte<br/>                                                                                                                                                                                                                                                                                                                                       |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 3  | Sem suporte<br/>                                                                                                                                                                                                                                                                                                                                       |
| Nível de recurso do D3D \_ \_ \_ 10 \_ 0 | O membro *OutputMergerLogicOp* foi adicionado às opções de D3D11 de dados de recurso do D3D11, para determinar o suporte para operações lógicas (operações lógicas de bits de saída entre o sombreador de pixel e o conteúdo de destino de renderização, consulte [**D3D11 \_ renderizar \_ \_ \_ DESC1 Blend de destino**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)). [**\_ \_ \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options) |



 

## <a name="id3d11devicecreatebuffer"></a>ID3D11Device:: CreateBuffer



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>Buffers não podem ter exibições de destino de renderização.<br/> Os buffers devem ter exatamente um dos D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER ou D3D11_BIND_CONSTANT_BUFFER.<br/> Permite apenas buffers de índice com o formato DXGI_FORMAT_R16_UINT. <br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> Buffers não podem ter exibições de destino de renderização.<br/> Os buffers devem ter exatamente um dos D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER ou D3D11_BIND_CONSTANT_BUFFER.<br/> Permite buffers de índice com os formatos DXGI_FORMAT_R16_UINT e DXGI_FORMAT_R32_UINT como D3D_FEATURE_LEVEL_10_0 e superior. <br/> $ {REMOVER} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatecounter"></a>ID3D11Device:: createcounterer



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedepthstencilview"></a>ID3D11Device::CreateDepthStencilView



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Não dá suporte a estêncil de dois lados. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatedomainshader"></a>ID3D11Device::CreateDomainShader



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Sem suporte em nenhum nível de recurso 9. * ou 10. *. $ {REMOVER} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshader"></a>ID3D11Device::CreateGeometryShader



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a>ID3D11Device::CreateGeometryShaderWithStreamOutput



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatehullshader"></a>ID3D11Device::CreateHullShader



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Sem suporte em qualquer nível de recurso 9. * ou 10. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateinputlayout"></a>ID3D11Device::CreateInputLayout



| Nível de recursos             | Diferenças de comportamento                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| Nível de recurso do D3D \_ \_ \_ 9 \_ 1 | Não dá suporte à \_ entrada \_ D3D11 \_ por \_ dados de instância                                                                |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 2 | Não dá suporte à \_ entrada \_ D3D11 \_ por \_ dados de instância                                                                |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 3 | O fluxo de vértice zero deve ter \_ entrada D3D11 \_ por \_ \_ dados de vértice, se qualquer fluxo tiver \_ dados de entrada D3D11 \_ por \_ vértice \_ |



 

Consulte o gráfico suporte de formato por [nível de recurso](overviews-direct3d-11-devices-downlevel-intro.md) para obter detalhes sobre quais formatos podem ser usados para dados de vértice em cada nível de recurso.

## <a name="id3d11devicecreatepixelshader"></a>ID3D11Device::CreatePixelShader



| Nível de recursos             | Diferenças de comportamento                                    |
|---------------------------|---------------------------------------------------------|
| Nível de recurso do D3D \_ \_ \_ 9 \_ 1 | Deve usar o PS \_ 4 \_ 0 \_ nível \_ 9 \_ 1                          |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 2 | Deve usar o PS \_ 4 \_ 0 \_ nível \_ 9 \_ 1                          |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 3 | Deve usar PS \_ 4 \_ 0 \_ nível \_ 9 \_ 3 ou PS \_ 4 \_ 0 \_ nível \_ 9 \_ 1 |



 

## <a name="id3d11devicecreatepredicate"></a>ID3D11Device:: predicado



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatequery"></a>ID3D11Device:: CreateQuery



| Nível de recursos             | Diferenças de comportamento                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nível de recurso do D3D \_ \_ \_ 9 \_ 1 | Há suporte para consultas de evento. As consultas de carimbo de data/hora são opcionais: chame [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar o suporte.               |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 2 | Há suporte para consultas de evento e oclusão. As consultas de carimbo de data/hora são opcionais: chame [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar o suporte. |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 3 | Há suporte para consultas de evento e oclusão. As consultas de carimbo de data/hora são opcionais: chame [**CreateQuery**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) para determinar o suporte. |



 

## <a name="id3d11devicecreaterasterizerstate"></a>ID3D11Device::CreateRasterizerState



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">DepthClipEnable deve ser <strong>true</strong>. DepthBiasClamp deve ser definido como 0. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreaterendertargetview"></a>ID3D11Device::CreateRenderTargetView



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Só pode dar suporte a exibições de destino de renderização de objetos Texture2D. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatesamplerstate"></a>ID3D11Device:: createsamplestate



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>Não há suporte para o filtro de comparação.<br/> A cor da borda deve estar entre [0, 1]<br/> Min LOD não pode ser fracionário<br/> O LOD máximo deve ser FLT_MAX<br/> O máximo de anisotropy é 2.<br/> Não há suporte para D3D11_TEXTURE_ADDRESS_MIRRORONCE.<br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> Não há suporte para o filtro de comparação.<br/> A cor da borda deve estar entre [0, 1]<br/> Min LOD não pode ser fracionário<br/> O LOD máximo deve ser FLT_MAX<br/> O máximo de anisotropy é 16.<br/> $ {REMOVER} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreateshaderresourceview"></a>ID3D11Device::CreateShaderResourceView



| Nível de recursos             | MostDetailedMip Plus MipLevels deve incluir o menor LOD (menor subrecurso | A exibição deve incluir todos os elementos da matriz de recursos |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| Nível de recurso do D3D \_ \_ \_ 9 \_ 1 | Yes                                                                          | sim                                           |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 2 | Sim                                                                          | Sim                                           |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 3 | Sim                                                                          | Sim                                           |



 

## <a name="id3d11devicecreatetexture1d"></a>ID3D11Device::CreateTexture1D



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatetexture2d"></a>ID3D11Device::CreateTexture2D

Os recursos Texture2D têm limites de largura e altura que diferem nos [níveis de recursos](overviews-direct3d-11-devices-downlevel-intro.md). Nos níveis de recurso 9 \_ 3, os seguintes são mínimo garantidos, e implementações individuais podem exceder os requisitos.



| Nível de recursos             | Se MipCount > 1, as dimensões devem ser uma potência integral de dois | Dimensão de textura mínima com suporte | As dimensões de texturas de cubo devem ser a potência de dois | Se \_ TEXTURECUBE for definido, as matrizes serão: | Se MISC \_ TEXTURECUBE não for definido, o arrays será. |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| Nível de recurso do D3D \_ \_ \_ 9 \_ 1 | Yes                                                          | 2.048                                | Yes                                           | 6                                              | 1                                                  |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 2 | Yes                                                          | 2.048                                | Yes                                           | 6                                              | 1                                                  |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 3 | Yes                                                          | 4096                                | Yes                                           | 6                                              | 1                                                  |



 

Na tabela anterior, o nome completo de **misc \_ TEXTURECUBE** é [**D3D11 do \_ recurso \_ misc \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).

Os itens a seguir são verdadeiros para todos os 9 \_ \* [níveis de recursos](overviews-direct3d-11-devices-downlevel-intro.md):

-   Ao usar o \_ \_ padrão de uso D3D11 ou o uso de D3D11 \_ \_ imutável, BindFlags não pode ser zero.
-   Ao usar o \_ \_ \_ estêncil de profundidade de D3D11 BIND, MipLevels deve ser 1.
-   Ao usar o \_ recurso D3D11 BIND \_ Shader \_ , o SampleDesc. Count deve ser 1.
-   Ao usar a \_ Associação D3D11 \_ presente, o recurso não pode ter o \_ recurso D3D11 BIND \_ Shader \_ .
-   Ao usar o \_ \_ recurso de DDI d3d10 \_ misc \_ compartilhado, o formato não pode ser o \_ formato dxgi \_ R8G8B8A8 \_ UNORM ou o \_ formato dxgi \_ R8G8B8A8 \_ UNORM \_ sRGB.

## <a name="id3d11devicecreatetexture3d"></a>ID3D11Device::CreateTexture3D



| Nível de recursos             | Dimensão máxima (qualquer eixo) | As dimensões devem ser forçadas de dois |
|---------------------------|------------------------------|---------------------------------|
| Nível de recurso do D3D \_ \_ \_ 9 \_ 1 | 256                          | Yes                             |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 2 | 512                          | Yes                             |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 3 | 512                          | Yes                             |



 

Se o recurso for D3D11 \_ uso \_ padrão ou o uso de D3D11 \_ \_ imutável, BindFlags não poderá ser zero.

## <a name="id3d11devicecreateunorderedaccessview"></a>ID3D11Device::CreateUnorderedAccessView



<table>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Sem suporte em nenhum nível de recurso de 9. *. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecreatevertexshader"></a>ID3D11Device::CreateVertexShader



| Nível de recursos             | Diferenças de comportamento                                    |
|---------------------------|---------------------------------------------------------|
| Nível de recurso do D3D \_ \_ \_ 9 \_ 1 | Deve usar vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1                          |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 2 | Deve usar vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1                          |
| Nível de recurso do D3D \_ \_ \_ 9 \_ 3 | Deve usar vs \_ 4 \_ 0 \_ nível \_ 9 \_ 3 ou vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1 |



 

## <a name="id3d11deviceopensharedresource"></a>ID3D11Device::OpenSharedResource



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Nível de recursos</th>
<th>Diferenças de comportamento</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: CheckFeatureSupport</strong></a> com o valor <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> e a estrutura <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> para determinar se um formato pode ser compartilhado. Se o formato puder ser compartilhado, <strong>CheckFeatureSupport</strong> retornará o sinalizador <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> .<br/>
<blockquote>
[!Note]<br />
[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>] (/Windows/Desktop/API/dxgiformat/ne-dxgiformat-dxgi_format) e <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> nunca podem ser compartilhados ao usar o nível de recurso 9, mesmo que o dispositivo indique suporte a recursos opcionais para <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>. A tentativa de criar recursos compartilhados com formatos DXGI <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> e <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> sempre falhará, a menos que o nível de recurso seja 10_0 ou superior.
</blockquote>
<br/> $ {REMOVER} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

