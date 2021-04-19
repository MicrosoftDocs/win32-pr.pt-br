---
title: Semântica
description: Uma semântica é uma cadeia de caracteres anexada a uma entrada ou saída do sombreador que transmite informações sobre o uso pretendido de um parâmetro.
ms.assetid: 6f5c504c-1940-4d1c-b594-a2132599376b
keywords:
- Binormal, semântica (DirectX HLSL)
- BLENDINDICES, semântica (DirectX HLSL)
- BLENDWEIGHT, semântica (DirectX HLSL)
- COR, semântica (DirectX HLSL)
- NEBLINA, semântica (DirectX HLSL)
- POSIÇÃOt, semântica (DirectX HLSL)
- PSIZE, semântica (DirectX HLSL)
- TANGENTE, semântica (DirectX HLSL)
- TESSFACTOR, semântica (DirectX HLSL)
- TEXCOORD, semântica (DirectX HLSL)
- VFACE, semântica (DirectX HLSL)
- VPOS, semântica (DirectX HLSL)
- Semântica de System-Value
- Semântica de valor do sistema
- ClipDistance, semântica (DirectX HLSL)
- Cobertura, semântica (DirectX HLSL)
- CullDistance, semântica (DirectX HLSL)
- Profundidade, semântica (DirectX HLSL)
- InstanceID, semântica (DirectX HLSL)
- IsFrontFace, semântica (DirectX HLSL)
- Posição, semântica (DirectX HLSL)
- Primitivaid, semântica (DirectX HLSL)
- RenderTargetArrayIndex, semântica (DirectX HLSL)
- Destino, semântica (DirectX HLSL)
- SampleIndex, semântica (DirectX HLSL)
- Vérticeid, semântica (DirectX HLSL)
- ViewportArrayIndex, semântica (DirectX HLSL)
- SV_ClipDistance, semântica (DirectX HLSL)
- SV_CullDistance, semântica (DirectX HLSL)
- SV_Depth, semântica (DirectX HLSL)
- SV_DepthGreaterEqual, semântica (DirectX HLSL)
- SV_DepthLessEqual, semântica (DirectX HLSL)
- SV_IsFrontFace, semântica (DirectX HLSL)
- SV_Position, semântica (DirectX HLSL)
- SV_RenderTargetArrayIndex, semântica (DirectX HLSL)
- SV_Target, semântica (DirectX HLSL)
- SV_ViewportArrayIndex, semântica (DirectX HLSL)
- SV_InstanceID, semântica (DirectX HLSL)
- SV_PrimitiveID, semântica (DirectX HLSL)
- SV_VertexID, semântica (DirectX HLSL)
- SV_Coverage, semântica (DirectX HLSL)
- SV_SampleIndex, semântica (DirectX HLSL)
- SV_InnerCoverage, semanitcs (DirectX HLSL)
- SV_StencilRef, semântica (DirectX HLSL)
- SV_GroupID, semântica (DirectX HLSL)
- SV_GroupThreadID, semântica (DirectX HLSL)
- Semântica de SV_DispatchThreadID (DirectX HLSL)
- SV_GroupIndex, semântica (DirectX HLSL)
- SV_OutputControlPointID, semântica (DirectX HLSL)
- SV_TessFactor, semântica (DirectX HLSL)
- SV_InsideTessFactor, semântica (DirectX HLSL)
- SV_DomainLocation, semântica (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e8979b4e4842a4c84317b456802ed8f1beefea35
ms.sourcegitcommit: 1d3c59a7066a75facc0565027251cad1ca1dd9c9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/18/2021
ms.locfileid: "107594161"
---
# <a name="semantics"></a>Semântica

Uma semântica é uma cadeia de caracteres anexada a uma entrada ou saída do sombreador que transmite informações sobre o uso pretendido de um parâmetro. A semântica é necessária em todas as variáveis passadas entre os estágios do sombreador. A sintaxe para adicionar uma semântica a uma variável de sombreador é mostrada aqui ([sintaxe de variável (DirectX HLSL)](dx-graphics-hlsl-variable-syntax.md)).

Em geral, os dados passados entre os estágios de pipeline são completamente genéricos e não são interpretados exclusivamente pelo sistema; semânticas arbitrárias são permitidas que não têm nenhum significado especial. Os parâmetros (no Direct3D 10 e posterior) que contêm essas semânticas especiais são chamados de [semântica de valor do sistema](#system-value-semantics).

## <a name="semantics-supported-in-direct3d-9-and-direct3d-10-and-later"></a>Semântica com suporte no Direct3D 9 e no Direct3D 10 e posterior

Os tipos de semântica a seguir têm suporte no Direct3D 9 e no Direct3D 10 e versões posteriores.

- [Semântica do sombreador de vértice](#vertex-shader-semantics)
- [Semântica do sombreador de pixel](#pixel-shader-semantics)

### <a name="vertex-shader-semantics"></a>Semântica do sombreador de vértice

Essas semânticas têm significado quando anexadas a um parâmetro Vertex-Shader. Essas semânticas têm suporte no Direct3D 9 e no Direct3D 10 e versões posteriores.

| Entrada | Descrição | Type |
|-|-|-|
| Binormal \[ n\] | Binormal | float4 |
| BLENDINDICES \[ n\] | Índices de mistura | uint |
| BLENDWEIGHT \[ n\] | Pesos de mistura | FLOAT |
| COR \[ n\] | Cor difusa e especular | float4 |
| NORMAL \[ n\] | Vetor normal | float4 |
| POSIÇÃO \[ n\] | Posição do vértice no espaço do objeto. | float4 |
| POSIÇÃO | Posição do vértice transformada. | float4 |
| PSIZE \[ n\] | Tamanho do ponto | FLOAT |
| TANGENTE \[ n\] | Tangente | float4 |
| TEXCOORD \[ n\] | Coordenadas de textura | float4 |

| Saída | Descrição | Type |
|-|-|-|
| COR \[ n\] | Cor difusa ou especular | float4 |
| NEBLINA | Neblina de vértice | FLOAT |
| POSIÇÃO \[ n\] | Posição de um vértice no espaço homogêneo. Posição de computação no espaço da tela dividindo (x, y, z) por w. Todo sombreador de vértice deve gravar um parâmetro com essa semântica. | float4 |
| PSIZE | Tamanho do ponto | FLOAT |
| TESSFACTOR \[ n\] | Fator de mosaico | FLOAT |

`n` é um inteiro opcional entre 0 e o número de recursos com suporte. Por exemplo, POSITION0, TEXCOORD1, etc.

### <a name="pixel-shader-semantics"></a>Semântica do sombreador de pixel

Essas semânticas têm significado quando anexadas a um parâmetro de entrada de sombreador de pixel. Essas semânticas têm suporte no Direct3D 9 e no Direct3D 10 e versões posteriores.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Entrada</th>
<th>Descrição</th>
<th>Type</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>COR [n]</td>
<td>Cor difusa ou especular.</td>
<td>float4</td>
</tr>
<tr class="even">
<td>TEXCOORD [n]</td>
<td>Coordenadas de textura</td>
<td>float4</td>
</tr>
<tr class="odd">
<td>VFACE</td>
<td>Escalar de ponto flutuante que indica um primitivo de volta. Um valor negativo é voltado para trás, enquanto um valor positivo é faces da câmera.
<blockquote>
[!Note]<br />
Essa semântica está disponível no <a href="dx-graphics-hlsl-sm3.md">modelo de sombreador do Direct3D 9 3,0</a>. Para o Direct3D 10 e posterior, use <a href="#semantics-supported-only-for-direct3d-10-and-newer">SV_IsFrontFace</a> em vez disso.
</blockquote>
<br/></td>
<td>FLOAT</td>
</tr>
<tr class="even">
<td>VPOS</td>
<td>O local do pixel (x, y) no espaço da tela. Para converter um sombreador do Direct3D 9 (que usa essa semântica) em um sombreador do Direct3D 10 e posterior, consulte o <a href="#direct3d-9-vpos-and-direct3d-10-sv_position">Direct3D 9 VPOS e o Direct3D 10 SV_Position</a>)</td>
<td>float2</td>
</tr>
</tbody>
</table>

<table>
<th>Saída</th>
<th>Descrição</th>
<th>Type</th>
</tr>
<td>COR [n]</td>
<td>Cor de saída</td>
<td>float4</td>
</tr>
<td>PROFUNDIDADE [n]</td>
<td>Profundidade de saída</td>
<td>FLOAT</td>
</tr>
</table>

`n` é um inteiro opcional entre 0 e o número de recursos com suporte. Por exemplo, PSIZE0, COLOR1, etc.

A semântica de cor só é válida no modo de compatibilidade de sombreador (ou seja, quando o sombreador é criado usando o \_ sombreador d3d10, \_ habilite a \_ compatibilidade com versões anteriores \_ ).

## <a name="semantics-supported-only-for-direct3d-10-and-newer"></a>Semântica suportada apenas para Direct3D 10 e mais recente.

Os seguintes tipos de semântica foram introduzidos recentemente para o Direct3D 10 e não estão disponíveis para o Direct3D 9.

- [Semântica de valor do sistema](#system-value-semantics)

### <a name="system-value-semantics"></a>Semântica de System-Value

A semântica de valor do sistema é nova no Direct3D 10. Todos os valores do sistema começam com um \_ prefixo de VA, um exemplo comum é a posição da VA \_ , que é interpretada pelo estágio do rasterizador. Os valores de sistema são válidos em outras partes do pipeline. Por exemplo, a \_ posição da VA pode ser especificada como uma entrada para um sombreador de vértice, bem como uma saída. Os sombreadores de pixel só podem gravar em parâmetros com a semântica de profundidade de VA \_ e de valor do \_ sistema de destino da VA.

Outros valores do sistema (ID de vértice da VA \_ , InstanceId da VA \_ , VA \_ IsFrontFace) só podem ser inseridos no primeiro sombreador ativo no pipeline que pode interpretar o valor específico; depois disso, a função de sombreador deve passar os valores para os estágios subsequentes.

A \_ primitiva de VA é uma exceção a essa regra de ser inserida apenas no primeiro sombreador ativo no pipeline que pode interpretar o valor específico; o hardware pode fornecer o mesmo valor de ID como entrada para o estágio envoltória-Shader, o estágio Domain-Shader e, depois disso, qualquer estágio é o primeiro habilitado: Geometry-Shader Stage ou o estágio pixel-sombreador.

Se o mosaico estiver habilitado, o estágio envoltória-Shader e o estágio Domain-Shader estarão presentes. Para um determinado patch, a mesma Primitivaid se aplica à invocação envoltória-shader do patch e a todas as invocações do sombreador do domínio mosaico. A mesma Primitivaid também se propaga para o próximo estágio ativo; Geometry-Shader Stage ou pixel-shader Stage se estiver habilitado.

Se o sombreador de geometria insere a \_ primitivaid de VA e porque pode gerar zero ou um ou mais primitivos por invocação, o sombreador deve programar sua própria escolha de valor de primitiva de VA \_ para cada primitiva de saída se um sombreador de pixel subsequente tiver entradas de VA \_ PrimtiveID.

Como outro exemplo, \_ a primitivaid de VA não pode ser interpretada pelo estágio Vertex-Shader porque um vértice pode ser um membro de vários primitivos.

Essas semânticas foram adicionadas ao Direct3D 10; Eles não estão disponíveis no Direct3D 9.

Semântica de valor do sistema para o estágio do rasterizador.

| Semântica de System-Value | Descrição | Type |
|-|-|-|
| VA \_ ClipDistance \[ n\] | Dados de distância do clipe. \_Os valores ClipDistance de VA são presumidos como uma distância assinada float32 para um plano. A configuração primitiva só invoca a rasterização em pixels para os quais as distâncias do plano interpolado são >= 0. Vários recortes de clipes podem ser implementados simultaneamente, declarando vários componentes de um ou mais elementos de vértice como o ClipDistance de VA \_ . Os valores de distância de clipe e de seleção combinados são no máximo o \# \_ clipe D3D ou os \_ \_ \_ \_ componentes de contagem de distância de seleção no \# \_ clipe D3D \_ ou registros de contagem de \_ elementos de distância de seleção \_ \_ \_ . Disponível para que todos os sombreadores sejam lidos ou gravados, exceto o sombreador de vértice, que pode gravar o valor, mas não levá-lo como entrada.<br/> O atributo **clipplanes** funciona como VA \_ ClipDistance, mas funciona em todo o [nível de recurso](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) de hardware 9 \_ x e superior. Para obter mais informações, consulte os [planos de corte do usuário no hardware nível 9 do recurso](./user-clip-planes-on-10level9.md).<br/> | FLOAT |
| VA \_ CullDistance \[ n\] | Dados de distância de seleção. Quando os componentes dos elementos de vértice recebem esse rótulo, esses valores são presumidos como uma distância assinada float32 para um plano. Os primitivos serão completamente descartados se as distâncias do plano para todos os vértices no primitivo forem < 0. Vários planos de seleção podem ser usados simultaneamente, declarando vários componentes de um ou mais elementos de vértice como o CullDistance de VA \_ . Os valores de distância de clipe e de seleção combinados são no máximo o \# \_ clipe D3D ou os \_ \_ \_ \_ componentes de contagem de distância de seleção no \# \_ clipe D3D \_ ou registros de contagem de \_ elementos de distância de seleção \_ \_ \_ . Disponível para que todos os sombreadores sejam lidos ou gravados, exceto o sombreador de vértice, que pode gravar o valor, mas não levá-lo como entrada.<br/> | FLOAT |
| Cobertura da VA \_ | Uma máscara que pode ser especificada na entrada, na saída ou em ambos os sombreadores de pixel. <br/> Para cobertura de VA \_ em um sombreador de pixel, a saída tem suporte no PS \_ 4 \_ 1 ou superior. <br/> Para cobertura de VA \_ em um sombreador de pixel, a entrada requer o PS \_ 5 \_ 0 ou superior. <br/> | uint |
| Profundidade da VA \_ | Dados de buffer de profundidade. Pode ser gravado pelo sombreador de pixel. | FLOAT |
| \_DEPTHGREATEREQUAL VA | Em um sombreador de pixel, permite a saída de profundidade, desde que seja maior ou igual ao valor determinado pelo rasterizador. Habilita o ajuste da profundidade sem desabilitar a Z inicial. | FLOAT |
| \_DEPTHLESSEQUAL VA | Em um sombreador de pixel, permite a saída de profundidade, desde que seja menor ou igual ao valor determinado pelo rasterizador. Habilita o ajuste da profundidade sem desabilitar a Z inicial. | FLOAT |
| [\_DISPATCHTHREADID VA](sv-dispatchthreadid.md) | Define o deslocamento de thread global dentro da chamada de expedição, por dimensão do grupo. Disponível como entrada para o sombreador de computação. (somente leitura) | uint3 |
| [\_DOMAINLOCATION VA](sv-domainlocation.md) | Define o local no envoltória do ponto de domínio atual que está sendo avaliado. Disponível como entrada para o sombreador de domínio. (somente leitura) | float2 \| 3 |
| [\_GroupId da VA](sv-groupid.md) | Define o deslocamento do grupo dentro de uma chamada de expedição, por dimensão da chamada de expedição. Disponível como entrada para o sombreador de computação. (somente leitura) | uint3 |
| [\_GROUPINDEX VA](sv-groupindex.md) | Fornece um índice achatado para um determinado thread dentro de um determinado grupo. Disponível como entrada para o sombreador de computação. (somente leitura) | uint |
| [\_GROUPTHREADID VA](sv-groupthreadid.md) | Define o deslocamento de thread dentro do grupo, por dimensão do grupo. Disponível como entrada para o sombreador de computação. (somente leitura) | uint3 |
| [\_GSINSTANCEID VA](sv-gsinstanceid.md) | Define a instância do sombreador de geometria. Disponível como entrada para o sombreador de geometria. A instância é necessária, pois um sombreador de geometria pode ser invocado até 32 vezes no mesmo primitivo de geometria. | uint |
| \_INNERCOVERAGE VA | Representa as informações de rasterização conservadora subestimadas (ou seja, se um pixel é garantido para ser totalmente coberto). Podem ser lidos ou gravados pelo sombreador de pixel. | |
| [\_INSIDETESSFACTOR VA](sv-insidetessfactor.md) | Define o valor de mosaico dentro de uma superfície de patch. Disponível no sombreador envoltória para gravação e disponível no sombreador de domínio para leitura. | float \| flutuante \[ 2\] |
| InstanceId da VA \_ | Identificador por instância gerado automaticamente pelo tempo de execução (consulte [usando valores de System-Generated (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Disponível para todos os sombreadores. | |
| \_ISFRONTFACE VA | Especifica se um triângulo é voltado para frente. Para linhas e pontos, IsFrontFace tem o valor true. A exceção são as linhas desenhadas fora dos triângulos (modo wireframe), que define IsFrontFace da mesma maneira como rasterizar o triângulo no modo sólido. Pode ser gravado pelo sombreador Geometry e lido pelo sombreador de pixel. | bool |
| [\_OUTPUTCONTROLPOINTID VA](sv-outputcontrolpointid.md) | Define o índice da ID do ponto de controle que está sendo operado por uma invocação do ponto de entrada principal do sombreador envoltória. Pode ser lido somente pelo sombreador envoltória. | uint |
| Posição da VA \_ | Quando \_ a posição da VA é declarada para entrada em um sombreador, ela pode ter um dos dois modos de interpolação especificados: linearNoPerspective ou linearNoPerspectiveCentroid, em que o último faz com que os valores de xyzw ajustados por centróide sejam fornecidos quando a suavização de multiamostrar. Quando usado em um sombreador, \_ a posição da VA descreve o local do pixel. Disponível em todos os sombreadores para obter o pixel Center com um deslocamento de 0,5. | float4 |
| \_Primitivaid de VA | Identificador por primitivo gerado automaticamente pelo tempo de execução (consulte [usando valores de System-Generated (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Pode ser gravado pelos sombreadores geometry ou pixel e lido pelos sombreadores Geometry, pixel, envoltória ou Domain. | uint |
| \_RENDERTARGETARRAYINDEX VA | Render-índice de matriz de destino. Aplicado à saída do sombreador de geometria e indica a fatia da matriz de destino de renderização para a qual o primitivo será desenhado pelo sombreador de pixel. \_O RENDERTARGETARRAYINDEX VA será válido somente se o destino de renderização for um recurso de matriz. Essa semântica se aplica somente a primitivos; se um primitivo tiver mais de um vértice, o valor do vértice à esquerda será usado. Esse valor também indica qual fatia de matriz de uma exibição de profundidade/estêncil é usada para fins de leitura/gravação.<br/> Pode ser gravado no sombreador de geometria e lido pelo sombreador de pixel.<br/> Se [D3D11_FEATURE_DATA_D3D11_OPTIONS3:: VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) for `true` , então \_ RenderTargetArrayIndex VA será aplicada a qualquer sombreador alimentando o rasterizador. | uint |
| \_SAMPLEINDEX VA | Dados de índice de frequência de exemplo. Disponível para leitura ou gravação somente pelo sombreador de pixel. | uint |
| \_STENCILREF VA | Representa o valor de referência do estêncil do sombreador de pixel atual. Pode ser gravado apenas pelo sombreador de pixel. | uint |
| \_Destino VA \[ n \] , em que 0 <= n <= 7 | O valor de saída que será armazenado em um destino de renderização. O índice indica para qual dos oito destinos de renderização associados você deve gravar. O valor está disponível para todos os sombreadores. | float \[ 2 \| 3 \| 4\] |
| [\_TESSFACTOR VA](sv-tessfactor.md) | Define o valor do mosaico em cada borda de um patch. Disponível para gravação no sombreador envoltória e leitura no sombreador de domínio. | float \[ 2 \| 3 \| 4\] |
| \_Vérticeid da VA | Identificador por vértice gerado automaticamente pelo tempo de execução (consulte [usando valores de System-Generated (Direct3D 10)](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-using.md)). Disponível apenas como a entrada para o sombreador de vértice. | uint |
| \_VIEWPORTARRAYINDEX VA | Índice de matriz do visor. Aplicado à saída do sombreador de geometria e indica qual visor usar para o primitivo que está sendo gravado no momento. Pode ser lido pelo sombreador de pixel. O primitivo será transformado e recortado em relação ao visor especificado pelo índice antes de ser passado para o rasterizador. Essa semântica se aplica somente a primitivos; se um primitivo tiver mais de um vértice, o valor do vértice à esquerda será usado. <br/> Se [D3D11_FEATURE_DATA_D3D11_OPTIONS3:: VPAndRTArrayIndexFromAnyShaderFeedingRasterizer](/windows/win32/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options3) for `true` , então \_ ViewportArrayIndex VA será aplicada a qualquer sombreador alimentando o rasterizador. | uint |
| \_SHADINGRATE VA | Define, através de [valores](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate)de taxa de sombreamento, o número de pixels gravados por uma invocação de sombreador de pixel para a [camada de taxa de sombreamento variável 2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) ou dispositivos superiores. Pode ser lido no sombreador de pixel. Pode ser gravado de um vértice ou sombreador de geometria. | uint |

### <a name="limitations-when-writing-sv_depth"></a>Limitações ao escrever a \_ profundidade da VA:

- Quando a multiamostragem (MultisampleEnable é **verdadeira** na [**d3d10 do \_ rasterizador \_ desc**](/windows/win32/api/d3d10/ns-d3d10-d3d10_rasterizer_desc)) e a gravação de um valor de profundidade (usando um sombreador de pixel), o valor único gravado também é usado no [teste de profundidade](../direct3d11/d3d10-graphics-programming-guide-depth-stencil.md); portanto, a capacidade de renderizar bordas primitivas em uma resolução mais alta é perdida quando a multiamostragem.
- Ao usar o controle de fluxo dinâmico, é impossível determinar no momento da compilação se um sombreador que grava a \_ profundidade da VA em alguns caminhos terá a garantia de gravar a \_ profundidade da VA em cada execução. Falha ao gravar a \_ profundidade da VA quando declarada resulta em um comportamento indefinido (que pode ou não incluir o descarte do pixel).
- Qualquer valor de float32 incluindo +/-INF e NaN pode ser gravado na \_ profundidade da SV.
- A gravação da profundidade da VA \_ ainda é válida ao executar a mesclagem de cores de fonte dupla.

## <a name="migration-from-direct3d-9-to-direct3d-10-and-later"></a>Migração do Direct3D 9 para o Direct3D 10 e posterior

Os seguintes problemas devem ser considerados ao migrar o código do Direct3D 9 para o Direct3D 10 e posteriores:

### <a name="mapping-to-direct3d-9-semantics"></a>Mapeando para a semântica do Direct3D 9

Algumas das semânticas do Direct3D 10 e posteriores são mapeadas diretamente para a semântica do Direct3D 9.

| Semântica do Direct3D 10 | Semântica equivalente do Direct3D 9 |
|-|-|
| Profundidade da VA \_ | DEPTH |
| Posição da VA \_ | PROPOSTAS |
| Destino da VA \_ | Cor |

> [!] Observação para desenvolvedores do Direct3D 9: para destinos do Direct3D 9, a semântica do sombreador deve mapear para uma semântica Direct3D 9 válida. Para POSITION0 de compatibilidade com versões anteriores (e seus nomes de variantes) são tratados como posição da VA \_ , a cor é tratada como destino da VA \_ .

- [Mapeando para a semântica do Direct3D 9](#mapping-to-direct3d-9-semantics)
- [Posição do Direct3D 9 VPOS e do Direct3D 10 VA \_](#direct3d-9-vpos-and-direct3d-10-sv_position)
- [Planos de corte do usuário no HLSL](#user-clip-planes-in-hlsl)

### <a name="direct3d-9-vpos-and-direct3d-10-sv_position"></a>Posição do Direct3D 9 VPOS e do Direct3D 10 VA \_

A posição da VA semântica D3D10 \_ fornece uma funcionalidade semelhante à semântica de VPOS do sombreador do Direct3D 9 do modelo 3. Por exemplo, no Direct3D 9, a sintaxe a seguir é usada para um sombreador de pixel usando coordenadas de espaço na tela:

```HLSL
float4 psMainD3D9( float4 screenSpace : VPOS ) : COLOR
{
    // code here 
}
```

VPOS foi adicionado para suporte ao modelo de sombreador 3, para especificar coordenadas de espaço na tela, pois a semântica de posição foi destinada a coordenadas de espaço de objeto.

No Direct3D 10 e posteriores, a \_ semântica da posição da VA (quando usada no contexto de um sombreador de pixel) especifica as coordenadas de espaço da tela (deslocamento por 0,5). Portanto, o sombreador do Direct3D 9 seria aproximadamente equivalente (sem a contabilidade do deslocamento 0,5) para o seguinte:

```HLSL
float4 psMainD3D10( float4 screenSpace : SV_Position ) : COLOR
{
    // code here
}
```

Ao migrar do Direct3D 9 para o Direct3D 10 e posterior, você precisará estar ciente disso ao traduzir seus sombreadores.

### <a name="user-clip-planes-in-hlsl"></a>Planos de corte do usuário no HLSL

A partir do Windows 8, você pode usar o atributo de função **clipplanes** em uma [declaração de função](dx-graphics-hlsl-function-syntax.md) HLSL em vez de VA \_ ClipDistance para fazer com que o sombreador funcione no nível de [recurso](../direct3d11/overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, bem como no nível de recurso 10 e superior. Para obter mais informações, consulte os [planos de corte do usuário no hardware nível 9 do recurso](./user-clip-planes-on-10level9.md).

## <a name="related-topics"></a>Tópicos relacionados

* [Sintaxe da linguagem](dx-graphics-hlsl-language-syntax.md)
* [Variáveis (DirectX HLSL)](dx-graphics-hlsl-variables.md)
