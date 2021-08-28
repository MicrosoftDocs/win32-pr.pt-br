---
title: 10Level9 ID3D11Device Methods
description: Esta seção lista as diferenças entre cada nível de recurso 10Level9 e o nível de recurso D3D FEATURE LEVEL 11 0 e superior para os métodos \_ \_ \_ \_ ID3D11Device.
ms.assetid: c3bc32a9-8d97-430b-be6a-b4935d7ac56c
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f467e47d7ba623f1c28111cf3bf7cc6a07da8317
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475782"
---
# <a name="10level9-id3d11device-methods"></a>10Level9 ID3D11Device Methods

Esta seção lista as diferenças entre cada nível de recurso 10Level9 e o nível de recurso D3D FEATURE LEVEL 11 0 e superior para os métodos \_ \_ \_ \_ [**ID3D11Device.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device)

-   [ID3D11Device::CheckCounter](#id3d11devicecheckcounter)
-   [ID3D11Device::CheckFormatSupport](#id3d11devicecheckformatsupport)
-   [ID3D11Device::CheckMultisampleQualityLevels](#id3d11devicecheckmultisamplequalitylevels)
-   [ID3D11Device::CreateBlendState](#id3d11devicecreateblendstate)
-   [ID3D11Device::CreateBlendState1](#id3d11devicecreateblendstate1)
-   [ID3D11Device::CreateBuffer](#id3d11devicecreatebuffer)
-   [ID3D11Device::CreateCounter](#id3d11devicecreatecounter)
-   [ID3D11Device::CreateDepthStencilView](#id3d11devicecreatedepthstencilview)
-   [ID3D11Device::CreateDomainShader](#id3d11devicecreatedomainshader)
-   [ID3D11Device::CreateGeometryShader](#id3d11devicecreategeometryshader)
-   [ID3D11Device::CreateGeometryShaderWithStreamOutput](#id3d11devicecreategeometryshaderwithstreamoutput)
-   [ID3D11Device::CreateHullShader](#id3d11devicecreatehullshader)
-   [ID3D11Device::CreateInputLayout](#id3d11devicecreateinputlayout)
-   [ID3D11Device::CreatePixelShader](#id3d11devicecreatepixelshader)
-   [ID3D11Device::CreatePredicate](#id3d11devicecreatepredicate)
-   [ID3D11Device::CreateQuery](#id3d11devicecreatequery)
-   [ID3D11Device::CreateRasterizerState](#id3d11devicecreaterasterizerstate)
-   [ID3D11Device::CreateRenderTargetView](#id3d11devicecreaterendertargetview)
-   [ID3D11Device::CreateSamplerState](#id3d11devicecreatesamplerstate)
-   [ID3D11Device::CreateShaderResourceView](#id3d11devicecreateshaderresourceview)
-   [ID3D11Device::CreateTexture1D](#id3d11devicecreatetexture1d)
-   [ID3D11Device::CreateTexture2D](#id3d11devicecreatetexture2d)
-   [ID3D11Device::CreateTexture3D](#id3d11devicecreatetexture3d)
-   [ID3D11Device::CreateUnorderedAccessView](#id3d11devicecreateunorderedaccessview)
-   [ID3D11Device::CreateVertexShader](#id3d11devicecreatevertexshader)
-   [ID3D11Device::OpenSharedResource](#id3d11deviceopensharedresource)
-   [Tópicos relacionados](#related-topics)

## <a name="id3d11devicecheckcounter"></a>ID3D11Device::CheckCounter




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Opcionalmente, há suporte para contadores dependentes do dispositivo. Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkcounterinfo"><strong>ID3D11Device::CheckCounterInfo</strong></a> para determinar support.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecheckformatsupport"></a>ID3D11Device::CheckFormatSupport




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Confira o suporte ao formato <a href="overviews-direct3d-11-devices-downlevel-intro.md">por nível de recurso</a>${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecheckmultisamplequalitylevels"></a>ID3D11Device::CheckMultisampleQualityLevels




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Os níveis de recurso não garantem o suporte à MSAA.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreateblendstate"></a>ID3D11Device::CreateBlendState



| Nível de recursos              | Diferenças de comportamento                                                                                                                                                                                                                                                                                                                                             |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1  | AlphaToCoverageEnable deve ser **FALSE.**<br/> Os quatro primeiros BlendEnables devem ter o mesmo valor.<br/> Não há suporte para \_ O \_ ALPHASAT do BLEND SRC \_ D3D11.<br/> Não há suporte para a combinação de cores de origem dupla (qualquer SrcBlend ou DestBlend com SRC1 no nome)<br/>                                                                                |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2  | AlphaToCoverageEnable deve ser **FALSE.**<br/> Os quatro primeiros BlendEnables devem ter o mesmo valor.<br/> Os quatro primeiros RenderTargetWriteMasks devem ter o mesmo valor.<br/> Não há suporte para \_ O \_ ALPHASAT do BLEND SRC \_ D3D11.<br/> Não há suporte para a combinação de cores de origem dupla (qualquer SrcBlend ou DestBlend com SRC1 no nome)<br/> |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3  | AlphaToCoverageEnable deve ser **FALSE.**<br/> Os quatro primeiros BlendEnables devem ter o mesmo valor.<br/> Não há suporte para \_ O \_ ALPHASAT do BLEND SRC \_ D3D11.<br/> Não há suporte para a combinação de cores de origem dupla (qualquer SrcBlend ou DestBlend com SRC1 no nome)<br/>                                                                                |
| D3D \_ FEATURE \_ LEVEL \_ 10 \_ 0 | Adiciona alfa à cobertura                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="id3d11devicecreateblendstate1"></a>ID3D11Device::CreateBlendState1



| Nível de recursos              | Diferenças de comportamento                                                                                                                                                                                                                                                                                                                                         |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1  | Sem suporte<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2  | Sem suporte<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3  | Sem suporte<br/>                                                                                                                                                                                                                                                                                                                                       |
| D3D \_ FEATURE \_ LEVEL \_ 10 \_ 0 | O membro *OutputMergerLogicOp* foi adicionado a [**D3D11 \_ FEATURE DATA \_ \_ D3D11 \_ OPTIONS**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options), para determinar o suporte para operações lógicas (operações lógicas bit a bit entre a saída do sombreador de pixel e o conteúdo de destino de renderização, consulte [**D3D11 \_ RENDER TARGET BLEND \_ \_ \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-d3d11_render_target_blend_desc1)). |



 

## <a name="id3d11devicecreatebuffer"></a>ID3D11Device::CreateBuffer




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Buffers não podem ter exibições de destino de renderização.<br /> Os buffers devem ter exatamente um dos D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER ou D3D11_BIND_CONSTANT_BUFFER.<br /> Permite apenas buffers de índice com o DXGI_FORMAT_R16_UINT formato. <br /> | 
| D3D_FEATURE_LEVEL_9_2 |  Buffers não podem ter exibições de destino de renderização.<br /> Os buffers devem ter exatamente um dos D3D11_BIND_VERTEX_BUFFER, D3D11_BIND_INDEX_BUFFER ou D3D11_BIND_CONSTANT_BUFFER.<br /> Permite buffers de índice com os formatos DXGI_FORMAT_R16_UINT e DXGI_FORMAT_R32_UINT como D3D_FEATURE_LEVEL_10_0 e superior. <br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatecounter"></a>ID3D11Device::CreateCounter




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatedepthstencilview"></a>ID3D11Device::CreateDepthStencilView




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Não dá suporte a estêncil de dois lados.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatedomainshader"></a>ID3D11Device::CreateDomainShader




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Não há suporte para qualquer nível de recurso 9.* ou 10.*. ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecreategeometryshader"></a>ID3D11Device::CreateGeometryShader




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreategeometryshaderwithstreamoutput"></a>ID3D11Device::CreateGeometryShaderWithStreamOutput




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatehullshader"></a>ID3D11Device::CreateHullShader




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Sem suporte em nenhum nível de recurso 9.* ou 10.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 
| D3D_FEATURE_LEVEL_10_0 | 
| D3D_FEATURE_LEVEL_10_1 | 




 

## <a name="id3d11devicecreateinputlayout"></a>ID3D11Device::CreateInputLayout



| Nível de recursos             | Diferenças de comportamento                                                                                              |
|---------------------------|-------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Não dá suporte a DADOS DE ENTRADA POR \_ \_ \_ \_ INSTÂNCIA D3D11                                                                |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Não dá suporte a DADOS DE ENTRADA POR \_ \_ \_ \_ INSTÂNCIA D3D11                                                                |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | O fluxo de vértice zero deve ter DADOS DE ENTRADA POR VÉRTICE D3D11, se algum fluxo tiver \_ DADOS DE ENTRADA POR \_ \_ \_ \_ \_ \_ \_ VÉRTICE D3D11 |



 

Consulte o gráfico de formato de suporte [por nível](overviews-direct3d-11-devices-downlevel-intro.md) de recurso para obter detalhes sobre quais formatos podem ser usados para dados de vértice em cada nível de recurso.

## <a name="id3d11devicecreatepixelshader"></a>ID3D11Device::CreatePixelShader



| Nível de recursos             | Diferenças de comportamento                                    |
|---------------------------|---------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Deve usar ps \_ 4 \_ 0 \_ nível \_ 9 \_ 1                          |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Deve usar ps \_ 4 \_ 0 \_ nível \_ 9 \_ 1                          |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Deve usar ps \_ 4 \_ 0 \_ nível \_ 9 \_ 3 ou ps \_ 4 \_ 0 \_ nível \_ 9 \_ 1 |



 

## <a name="id3d11devicecreatepredicate"></a>ID3D11Device::CreatePredicate




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatequery"></a>ID3D11Device::CreateQuery



| Nível de recursos             | Diferenças de comportamento                                                                                                                                  |
|---------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Há suporte para consultas de eventos. As consultas de data/hora são opcionais: chame [**CreateQuery para**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) determinar o suporte.               |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Há suporte para consultas de evento e oclusão. As consultas de data/hora são opcionais: chame [**CreateQuery para**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) determinar o suporte. |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Há suporte para consultas de evento e oclusão. As consultas de data/hora são opcionais: chame [**CreateQuery para**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createquery) determinar o suporte. |



 

## <a name="id3d11devicecreaterasterizerstate"></a>ID3D11Device::CreateRasterizerState




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | DepthClipEnable deve ser <strong>TRUE.</strong> DepthBiasClamp deve ser definido como 0.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreaterendertargetview"></a>ID3D11Device::CreateRenderTargetView




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Só é possível dar suporte a exibições de destino de renderização de objetos Texture2D.${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatesamplerstate"></a>ID3D11Device::CreateSamplerState




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Não há suporte para filtro de comparação.<br /> A cor da borda deve estar dentro de [0,1]<br /> A LOD mínima não pode ser fracionada<br /> O LOD máximo deve ser FLT_MAX<br /> A anisopatia máxima é 2.<br /> D3D11_TEXTURE_ADDRESS_MIRRORONCE há suporte.<br /> | 
| D3D_FEATURE_LEVEL_9_2 |  Não há suporte para filtro de comparação.<br /> A cor da borda deve estar dentro de [0,1]<br /> A LOD mínima não pode ser fracionada<br /> O LOD máximo deve ser FLT_MAX<br /> O máximo de anisomose é 16.<br /> ${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreateshaderresourceview"></a>ID3D11Device::CreateShaderResourceView



| Nível de recursos             | MostDetailedMip mais MipLevels devem incluir a menor LOD (menor sub-fonte | A exibição deve incluir todos os elementos da matriz de recursos |
|---------------------------|------------------------------------------------------------------------------|-----------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Sim                                                                          | sim                                           |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Sim                                                                          | Sim                                           |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Sim                                                                          | Sim                                           |



 

## <a name="id3d11devicecreatetexture1d"></a>ID3D11Device::CreateTexture1D




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatetexture2d"></a>ID3D11Device::CreateTexture2D

Os recursos Texture2D têm limites em sua largura e altura que diferem entre os [níveis de recurso](overviews-direct3d-11-devices-downlevel-intro.md). Nos níveis de recurso 9 3, os seguintes minima são \_ garantidos e implementações individuais podem exceder os requisitos.



| Nível de recursos             | Se O MipCount > 1, as dimensões deverão ser uma potência integral de dois | Dimensão de textura mínima com suporte | Dimensões de texturas de cubo devem ter potência de dois | Se MISC \_ TEXTURECUBE estiver definido, ArraySize será: | Se MISC \_ TEXTURECUBE não estiver definido, ArraySize será. |
|---------------------------|--------------------------------------------------------------|-------------------------------------|-----------------------------------------------|------------------------------------------------|----------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Sim                                                          | 2.048                                | Sim                                           | 6                                              | 1                                                  |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Sim                                                          | 2.048                                | Sim                                           | 6                                              | 1                                                  |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Sim                                                          | 4096                                | Sim                                           | 6                                              | 1                                                  |



 

Na tabela anterior, o nome completo **de MISC \_ TEXTURECUBE** é [**D3D11 \_ RESOURCE \_ MISC \_ TEXTURECUBE**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag).

Os seguintes são verdadeiros para todos os 9 níveis \_ \* [de recurso:](overviews-direct3d-11-devices-downlevel-intro.md)

-   Ao usar D3D11 \_ USAGE \_ DEFAULT ou D3D11 \_ USAGE \_ IMMUTABLE, BindFlags não pode ser zero.
-   Ao usar D3D11 \_ BIND \_ DEPTH \_ STENCIL, MipLevels deve ser 1.
-   Ao usar D3D11 \_ BIND \_ SHADER \_ RESOURCE, SampleDesc.Count deve ser 1.
-   Ao usar D3D11 \_ BIND \_ PRESENT, o recurso não pode ter O RECURSO DE SOMBREADOR BIND D3D11. \_ \_ \_
-   Ao usar D3D10 DDI RESOURCE MISC SHARED, Format não pode ser \_ \_ \_ \_ DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM ou DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM \_ SRGB.

## <a name="id3d11devicecreatetexture3d"></a>ID3D11Device::CreateTexture3D



| Nível de recursos             | Dimensão Máxima (qualquer eixo) | As dimensões devem ter potência de dois |
|---------------------------|------------------------------|---------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | 256                          | Sim                             |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | 512                          | Sim                             |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | 512                          | Sim                             |



 

Se o recurso for D3D11 \_ USAGE \_ DEFAULT ou D3D11 \_ USAGE \_ IMMUTABLE, BindFlags não poderá ser zero.

## <a name="id3d11devicecreateunorderedaccessview"></a>ID3D11Device::CreateUnorderedAccessView




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 | Não há suporte para nenhum nível de recurso 9.* .${REMOVE}$<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="id3d11devicecreatevertexshader"></a>ID3D11Device::CreateVertexShader



| Nível de recursos             | Diferenças de comportamento                                    |
|---------------------------|---------------------------------------------------------|
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 1 | Deve usar vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1                          |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 2 | Deve usar vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1                          |
| D3D \_ FEATURE \_ LEVEL \_ 9 \_ 3 | Deve usar vs \_ 4 \_ 0 \_ nível \_ 9 \_ 3 ou \_ vs 4 \_ 0 nível \_ \_ 9 \_ 1 |



 

## <a name="id3d11deviceopensharedresource"></a>ID3D11Device::OpenSharedResource




| Nível de recursos | Diferenças de comportamento | 
|---------------|----------------------|
| D3D_FEATURE_LEVEL_9_1 |  Use <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport"><strong>ID3D11Device:: CheckFeatureSupport</strong></a> com o valor <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_feature"><strong>D3D11_FEATURE_FORMAT_SUPPORT2</strong></a> e a estrutura <a href="/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_format_support2"><strong>D3D11_FEATURE_DATA_FORMAT_SUPPORT2</strong></a> para determinar se um formato pode ser compartilhado. Se o formato puder ser compartilhado, <strong>CheckFeatureSupport</strong> retornará o sinalizador <a href="/windows/desktop/api/D3D11/ne-d3d11-d3d11_format_support2"><strong>D3D11_FORMAT_SUPPORT2_SHAREABLE</strong></a> .<br /><blockquote>[!Note]<br />[<strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong>](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) e <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> nunca são compartilháveis ao usar o nível de recurso 9, mesmo que o dispositivo indique suporte a recursos opcionais para <strong>D3D11_FORMAT_SUPPORT_SHAREABLE</strong>. A tentativa de criar recursos compartilhados com formatos DXGI <strong>DXGI_FORMAT_R8G8B8A8_UNORM</strong> e <strong>DXGI_FORMAT_R8G8B8A8_UNORM_SRGB</strong> sempre falhará, a menos que o nível de recurso seja 10_0 ou superior.</blockquote><br /> $ {REMOVER} $<br /> | 
| D3D_FEATURE_LEVEL_9_2 | 
| D3D_FEATURE_LEVEL_9_3 | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

