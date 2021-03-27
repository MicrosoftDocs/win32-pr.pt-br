---
title: Migrando para o Direct3D 11
description: Esta seção fornece informações para migrar para o Direct3D 11 de uma versão anterior do Direct3D.
ms.assetid: 3ec8b5c2-01e6-4fbe-ada7-43898db63bbe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ade0a0d32d3f8b5c07e6653955c0c407c8fa8f
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104294556"
---
# <a name="migrating-to-direct3d-11"></a>Migrando para o Direct3D 11

Esta seção fornece informações para migrar para o Direct3D 11 de uma versão anterior do Direct3D.

-   [Direct3D 9 para Direct3D 11](#direct3d-9-to-direct3d-11)
-   [Direct3D 10 para Direct3D 11](#direct3d-10-to-direct3d-11)
    -   [Enumerações e definições](#enumerations-and-defines)
    -   [Estruturas](#structures)
    -   [Interfaces](#interfaces)
    -   [Outras tecnologias relacionadas](#other-related-technologies)
-   [Direct3D 10,1 para Direct3D 11](#direct3d-101-to-direct3d-11)
    -   [Enumerações e definições](#enumerations-and-defines)
    -   [Estruturas](#structures)
    -   [Interfaces](#interfaces)
-   [Novos recursos para o Direct3D 11](#new-features-for-direct3d-11)
-   [Novos recursos para o DirectX 11,1](#new-features-for-directx-111)
-   [Novos recursos para o DirectX 11,2](#new-features-for-directx-112)
-   [Tópicos relacionados](#related-topics)

## <a name="direct3d-9-to-direct3d-11"></a>Direct3D 9 para Direct3D 11

A API do Direct3D 11 se baseia nos aprimoramentos do infraestrutura feitos no Direct3D 10 e no 10,1. Portar do Direct3D 9 para o Direct3D 11 é semelhante à mudança do Direct3D 9 para o Direct3D 10. A seguir estão os principais desafios desse esforço.

-   Remoção de todo o uso de pipeline de função fixa em favor de sombreadores programáveis criados exclusivamente em HLSL (compilados por meio de D3DCompiler em vez de D3DX9).
-   Gerenciamento de estado com base em objetos imutáveis em vez de alternâncias de estado individual.
-   Atualização para atender aos requisitos estritos de vinculação de layouts de entrada de buffer de vértice e assinaturas de sombreador.
-   Associando exibições de recursos do sombreador a todos os recursos de textura.
-   Mapear todo o conteúdo da imagem para um \_ formato dxgi, incluindo a remoção de todos os formatos de cor de 16 bits (5/5/5/1, 5/6/5, 4/4/4/4), remoção de todos os formatos de cor de 24 bits (8/8/8) e ordem de cores RGB estrita.
-   Dividir o uso de estado constante global em vários buffers de constantes pequenos e mais eficientes.

Para obter mais informações sobre como migrar do Direct3D 9 para o Direct3D 10, consulte [considerações do Direct3D 9 para o Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).

## <a name="direct3d-10-to-direct3d-11"></a>Direct3D 10 para Direct3D 11

A conversão de programas escritos para usar a API do Direct3D 10 ou 10,1 é um processo direto, pois o Direct3D 11 é uma extensão da API existente. Com apenas uma exceção secundária (anotada abaixo-filtragem de texto monocromático), todos os métodos e funcionalidades no Direct3D 10/10.1 estão disponíveis no Direct3D 11. A estrutura de tópicos a seguir descreve as diferenças entre as duas APIs para auxiliar na atualização do código existente. As principais diferenças aqui incluem:

-   As operações de renderização (empate, State etc.) não fazem mais parte da interface do dispositivo, mas, em vez disso, fazem parte da nova interface DeviceContext juntamente com os métodos de mapeamento/desmapeamento de recursos e de consulta de dispositivo.
-   O Direct3D 11 inclui todas as melhorias e alterações feitas entre o Direct3D 10,0 e o 10,1

### <a name="enumerations-and-defines"></a>Enumerações e definições



| Direct3D 10                            | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_formato dxgi                           | [**Dxgi \_ FORMATO**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)vários novos formatos dxgi foram definidos.<br/>                                                                                                                                                                                                                                                                                                                                |
| D3D10 \_ criar \_ \_ comutador \_ de dispositivo para \_ ref | [**D3D11 \_ CRIAR \_ \_ comutador de dispositivo \_ para \_ ref**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_create_device_flag)a funcionalidade de switch-to-ref não é suportada pelo Direct3D 11.<br/>                                                                                                                                                                                                                                                                        |
| \_Tipo de driver d3d10 \_                    | [**D3D \_ \_Tipo de driver**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type)Observe que os identificadores de enumeração no [**\_ \_ tipo de driver D3D**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) foram redefinidos dos identificadores no [**\_ \_ tipo de driver d3d10**](/windows/desktop/api/d3d10misc/ne-d3d10misc-d3d10_driver_type). Portanto, você deve ter certeza de usar os identificadores de enumeração em vez de números literais.<br/> [**D3D \_ O \_ tipo de driver**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_driver_type) é definido em D3Dcommon. h.<br/> |
| \_ \_ Sinalizador diverso de recurso d3d10 \_            | [**D3D11 \_ \_ \_ Sinalizador variado de recurso**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag)Observe que muitos desses sinalizadores foram redefinidos, portanto, certifique-se de usar identificadores de enumeração em vez de números literais.<br/>                                                                                                                                                                                                                                |
| Filtro de D3D10 \_                          | [**D3D11 \_ FILTRO**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_filter)Observe que a filtragem de texto d3d10 \_ filtro \_ \_ de texto 1BIT foi removida do Direct3D 11. Consulte DirectWrite.<br/>                                                                                                                                                                                                                                                                            |
| Contador de D3D11 \_                         | [**D3D11 \_ CONTADOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_counter)Observe que os contadores de fornecedor neutro foram removidos para o Direct3D 11, pois raramente eram compatíveis.<br/>                                                                                                                                                                                                                                                                          |
| D3D10 \_ x                               | D3D11 \_ x muitas enumerações e definições são as mesmas, têm limites maiores ou têm valores adicionais.<br/>                                                                                                                                                                                                                                                                                                               |



 

### <a name="structures"></a>Estruturas



| Direct3D 10                              | Direct3D 11                                                                                                                                                 |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ de \_ entrada de Declaração \_            | [**D3D11 \_ Portanto, a \_ \_ entrada de declaração**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_so_declaration_entry)adiciona o fluxo.<br/>                                                                  |
| D3D10 de \_ combinação \_ desc                       | [**D3D11 \_ BLEND \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)Observe que essa estrutura mudou significativamente de 10 para 10,1 para fornecer por estado de mesclagem de destino de renderização<br/> |
| D3D10 \_ buffer \_ desc                      | [**D3D11 \_ BUFFER \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc)adiciona um StructureByteStride para uso com recursos de sombreador de computação<br/>                                 |
| \_Exibição de recursos do sombreador d3d10 \_ \_ \_ desc      | [**D3D11 \_ Exibição de recursos do SOMBREAdor \_ \_ \_ desc**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)observação esta estrutura tinha membros de união adicionais adicionados para 10,1<br/>    |
| Exibição de estêncil de profundidade de D3D10 \_ \_ \_ \_ desc        | [**D3D11 \_ A \_ exibição de estêncil de profundidade \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc)tem um novo membro flags.<br/>                                                |
| \_Estatísticas de \_ pipeline de dados de consulta d3d10 \_ \_ | [**D3D11 \_ As \_ \_ \_ Estatísticas de pipeline de dados de consulta**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_query_data_pipeline_statistics)adicionam vários novos contadores de estágio de sombreador.<br/>                  |
| D3D10 \_ x                                 | D3D11 \_ x muitas estruturas são idênticas entre as duas APIs.<br/>                                                                                     |



 

### <a name="interfaces"></a>Interfaces



| Direct3D 10        | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device       | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> A interface do dispositivo foi dividida nessas duas partes. Para portabilidade rápida, você pode fazer uso de [**ID3D11Device:: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).<br/> Os métodos "ID3D10Device:: GetTextFilterSize" e "SetTextFilerSize" não existem mais. Consulte DirectWrite.<br/> Create \* Shader usa um parâmetro opcional adicional para [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage).<br/> \*Setshadr e \* Getshadr usam parâmetros opcionais adicionais para [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)(s).<br/> [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) usa uma matriz e uma contagem para vários avanços de fluxo de saída.<br/> O limite para o parâmetro NumEntries de [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) aumentou para D3D11 \_ , portanto a \_ contagem de fluxos \_ \* D3D11 \_ , portanto, a \_ contagem de \_ componentes de saída \_ no Direct3D 11.<br/> |
| ID3D10Buffer       | [**ID3D11Buffer**](/windows/desktop/api/D3D11/nn-d3d11-id3d11buffer)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10SwitchToRef  | [**ID3D11SwitchToRef**](/windows/desktop/api/D3D11SDKLayers/nn-d3d11sdklayers-id3d11switchtoref) Não há suporte para a funcionalidade switch-to-ref no Direct3D 11.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| ID3D10Texture1D    | [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture2D    | [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| ID3D10Texture3D    | [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) Os métodos Map e demapeamento foram movidos para [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext), e todos os métodos de mapa usam o [**\_ \_ subrecurso mapeado D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_mapped_subresource) em vez de um void \* \* .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ID3D10Asynchronous | [**ID3D11Asynchronous**](/windows/desktop/api/D3D11/nn-d3d11-id3d11asynchronous) Begin, end e GetData foram movidos para [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ID3D10x            | ID3D11x muitas interfaces são idênticas entre as duas APIs.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

### <a name="other-related-technologies"></a>Outras tecnologias relacionadas



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>solução 10/10.1</th>
<th>11 solução</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>APIs de HLSL (D3D10Compile *, D3DX10Compile*) e de reflexo de sombreador</td>
<td>D3DCompiler (consulte D3DCompiler. h)
<blockquote>
[!Note]<br />
Para aplicativos da Windows Store, as <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">APIs D3DCompiler</a> têm suporte apenas para desenvolvimento, não para implantação.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td>Efeitos 10</td>
<td>Os <a href="https://github.com/Microsoft/FX11">efeitos 11</a> estão disponíveis como fonte compartilhada online.
<blockquote>
[!Note]<br />
Esta solução não é adequada para aplicativos da Windows Store porque requer as <a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference">APIs D3DCompiler</a> em tempo de execução (implantação).
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>Matemática de D3DX9/D3DX10</td>
<td><a href="/windows/desktop/dxmath/directxmath-portal">DirectXMath</a></td>
</tr>
<tr class="even">
<td>D3DX10</td>
<td>D3DX11 no SDK do DirectX herdado <a href="https://github.com/Microsoft/DirectXTex">DirectXTex</a>, <a href="https://github.com/Microsoft/DirectXTK">DirectXTK</a>e <a href="https://github.com/Microsoft/DirectXMesh">DirectXMesh</a> oferecem alternativas para muitas tecnologias nas bibliotecas D3DX10 e D3DX11 herdadas.<br/> <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> e <a href="/windows/desktop/DirectWrite/direct-write-portal">DirectWrite</a> oferecem suporte de alta qualidade para a renderização de linhas e fontes com estilo.<br/></td>
</tr>
</tbody>
</table>



 

Para obter informações sobre o SDK do DirectX herdado, consulte [onde está o SDK do DirectX?](/windows/desktop/directx-sdk--august-2009-).

## <a name="direct3d-101-to-direct3d-11"></a>Direct3D 10,1 para Direct3D 11

O Direct3D 10,1 é uma extensão da interface do Direct3D 10, e todos os recursos do Direct3D 10,1 estão disponíveis no Direct3D 11. A maior parte da porta de 10,1 a 11 já foi abordada acima da mudança de 10 para 11.

### <a name="enumerations-and-defines"></a>Enumerações e definições



| Direct3D 10,1          | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_LEVEL1 do recurso d3d10 \_ | [**D3D \_ \_Nível de recurso**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level)idêntico, mas definido em D3DCommon. h, além da adição do nível de recurso do D3D \_ \_ \_ 11 \_ 0 para o hardware de 11 classes, juntamente com o nível de recurso do D3D \_ \_ \_ 9 \_ 1, nível de recurso do D3D \_ \_ \_ 9 \_ 2 e \_ nível de recurso do D3D \_ \_ 9 \_ 3 para 10level9<br/> (D3D10 \_ O \_ nível \_ de recurso 9 \_ 1, \_ nível de recurso d3d10 \_ \_ 9 \_ 2 e \_ nível de recurso d3d10 \_ \_ 9 \_ 3 também foram adicionados para 10,1 a d3d10 \_ 1. h)<br/> |



 

### <a name="structures"></a>Estruturas



| Direct3D 10,1                        | Direct3D 11                                                                                                                   |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| D3D10 \_ Blend \_ DESC1                  | [**D3D11 \_ BLEND \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)a versão 11 é idêntica a 10,1.<br/>                                 |
| \_DESC1 da \_ exibição de recursos do SOMBREAdor d3d10 \_ \_ | [**D3D11 \_ Exibição de recurso do SOMBREAdor \_ \_ \_ desc**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc)a versão 11 é idêntica a 10,1.<br/> |



 

### <a name="interfaces"></a>Interfaces



| Direct3D 10,1             | Direct3D 11                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID3D10Device1             | [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) e [ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)<br/> A interface do dispositivo foi dividida nessas duas partes. Para portabilidade rápida, você pode fazer uso de [**ID3D11Device:: GetImmediateContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-getimmediatecontext).<br/> Os métodos "ID3D10Device:: GetTextFilterSize" e "SetTextFilerSize" não existem mais. Consulte DirectWrite.<br/> Create \* Shader usa um parâmetro opcional adicional para [**ID3D11ClassLinkage**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classlinkage).<br/> \*Setshadr e \* Getshadr usam parâmetros opcionais adicionais para [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance)(s).<br/> [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) usa uma matriz e uma contagem para vários avanços de fluxo de saída.<br/> O limite para o parâmetro NumEntries de [**CreateGeometryShaderWithStreamOutput**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-creategeometryshaderwithstreamoutput) aumentou para D3D11 \_ , portanto a \_ contagem de fluxos \_ \* D3D11 \_ , portanto, a \_ contagem de \_ componentes de saída \_ no Direct3D 11.<br/> |
| ID3D10BlendState1         | [**ID3D11BlendState**](/windows/desktop/api/D3D11/nn-d3d11-id3d11blendstate)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| ID3D10ShaderResourceView1 | [**ID3D11ShaderResourceView**](/windows/desktop/api/D3D11/nn-d3d11-id3d11shaderresourceview)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

## <a name="new-features-for-direct3d-11"></a>Novos recursos para o Direct3D 11

Depois que o código for atualizado para usar a API do Direct3D 11, há inúmeros [novos recursos](direct3d-11-features.md) a serem considerados.

-   Processamento multithread por meio de listas de comandos e vários contextos
-   Implementando algoritmos avançados usando o sombreador de computação (usando perfis de sombreador 4,0, 4,1 ou 5,0)
-   Novos recursos de hardware de 11 classes:
    -   Modelo de sombreador HLSL 5,0
    -   Vinculação de sombreador dinâmico
    -   Mosaico por meio de envoltória e sombreadores de domínio
    -   Novos formatos de compactação de bloco: BC6H para imagens HDR, BC7 para imagens padrão de alta fidelidade
-   Utilizando a [tecnologia 10level9](overviews-direct3d-11-devices-downlevel.md) para renderização em vários dispositivos do shader Model 2,0 e do shader Model 3,0 por meio da API do DIrect3D 11 para suporte de hardware de vídeo de nível inferior no Windows Vista e no Windows 7.
-   Aproveitando o dispositivo de renderização de software WARP.

## <a name="new-features-for-directx-111"></a>Novos recursos para o DirectX 11,1

O Windows 8 inclui mais aprimoramentos de gráficos do DirectX a serem considerados ao implementar o código de gráficos do DirectX, que inclui [Direct3D 11,1](direct3d-11-features.md), [dxgi 1,2](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements), [Windows Display Driver Model (WDDM) 1,2](/windows-hardware/drivers/display/wddm-in-windows-8), hardware de [nível de recurso](overviews-direct3d-11-devices-downlevel-intro.md) 11,1, contextos de dispositivo Direct2D e outros aprimoramentos.

O suporte parcial para o [Direct3D 11,1](direct3d-11-features.md) está disponível no Windows 7 também por meio da [atualização de plataforma para o Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7), que está disponível por meio da [atualização de plataforma para o Windows 7](https://support.microsoft.com/kb/2670838).

## <a name="new-features-for-directx-112"></a>Novos recursos para o DirectX 11,2

O Windows 8.1 inclui [Direct3D 11,2](direct3d-11-2-features.md), [dxgi 1,3](/windows/desktop/direct3ddxgi/dxgi-1-3-improvements)e outros aprimoramentos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação para Direct3D 11](dx-graphics-overviews.md)
</dt> <dt>

[Efeitos (Direct3D 11)](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

