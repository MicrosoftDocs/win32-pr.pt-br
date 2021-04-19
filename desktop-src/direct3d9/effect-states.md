---
description: Os Estados de efeito são usados para inicializar os Estados de pipeline na preparação para o processamento de vértice e pixel.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Estados de efeito (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e208c0c7c14564a9967562ff2fd04a400cb7901
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314759"
---
# <a name="effect-states-direct3d-9"></a>Estados de efeito (Direct3D 9)

Os Estados de efeito são usados para inicializar os Estados de pipeline na preparação para o processamento de vértice e pixel.


```
effect state [ [index] ] = expression;
```



Em que:

-   Estado de efeito – semelhante aos Estados de pipeline de função fixa tradicional. Uma lista completa de Estados é fornecida abaixo.
-   \[\[ \] índice \] do -Índice inteiro opcional. O índice identifica um estado específico dentro de uma matriz de Estados de efeito. Os colchetes externos indicam que um índice é opcional. Se um índice for usado, certifique-se de usar os colchetes internos.
-   Expression – expressão de atribuição de estado. Consulte [Expressions (Direct3D 9)](expressions.md).

Cada Estado tem um tipo de dados nativo. Esse é o tipo de dados em que o estado espera que os valores estejam quando o efeito os atribui. Os tipos de dados esperados por cada Estado estão listados abaixo.

Observe que a interface de efeito tentará converter valores para o tipo apropriado o mais cedo possível. Valores literais podem ser convertidos em tempo de compilação. Não literais (ou seja, variáveis regulares) precisam ser convertidas quando os métodos definidos apropriados são chamados. Por exemplo, a interface de efeito converterá valores definidos usando [**setbool**](id3dxbaseeffect--setbool.md), [**DefinirValor**](id3dxbaseeffect--setvalue.md)e outras funções semelhantes, se necessário. Para melhorar o desempenho, verifique se os valores passados para a interface de efeito já são do tipo correto e não precisarão de conversão. Se o tempo de execução não puder converter um valor, um erro será retornado.

Os Estados de efeito podem ser divididos nas seguintes categorias:

-   [Estados claros](#light-states)
-   [Estados de material](#material-states)
-   [Processar Estados](#render-states)
    -   [Estados de renderização de pipe de pixel](#pixel-pipe-render-states)
    -   [Estados de renderização de pipe de vértice](#vertex-pipe-render-states)
-   [Estados de amostra](#sampler-states)
-   [Estados de estágio de amostra](#sampler-stage-states)
-   [Estados do sombreador](#shader-states)
-   [Estados de constante do sombreador](#shader-constant-states)
-   [Estados de textura](#texture-states)
-   [Estados de estágio de textura](#texture-stage-states)
-   [Estados de transformação](#transform-states)

## <a name="light-states"></a>Estados claros

Para habilitar o melhor desempenho para a aplicação de um efeito, todos os componentes de uma luz ou um material devem ser especificados no arquivo de efeito. Declara que você não deve declarar está definido como um valor padrão porque não há como o Direct3D para definir os Estados de luz individualmente.



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| Estado claro            | Type   | Valores                                                                                                              |
| LightAmbient \[ n\]      | float4 | Consulte o membro de ambiente de [**D3DLIGHT9**](d3dlight9.md).                                                           |
| LightAttenuation0 \[ n\] | FLOAT  | Consulte o membro Attenuation0 de [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightAttenuation1 \[ n\] | FLOAT  | Consulte o membro Attenuation1 de [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightAttenuation2 \[ n\] | FLOAT  | Consulte o membro Attenuation2 de [**D3DLIGHT9**](d3dlight9.md).                                                      |
| LightDiffuse \[ n\]      | float4 | Consulte o membro difuso de [**D3DLIGHT9**](d3dlight9.md).                                                           |
| LightDirection \[ n\]    | float3 | Consulte o membro de direção de [**D3DLIGHT9**](d3dlight9.md).                                                         |
| N mais claro \[\]       | bool   | **True** ou **false**. Consulte o argumento bEnable em [**clarear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).            |
| LightFalloff \[ n\]      | FLOAT  | [**D3DCOLORVALUE**](d3dcolorvalue.md). Consulte o membro de queda de [**D3DLIGHT9**](d3dlight9.md).                   |
| LightPhi \[ n\]          | FLOAT  | Consulte o membro Phi de [**D3DLIGHT9**](d3dlight9.md).                                                               |
| LightPosition \[ n\]     | float3 | Consulte o membro position de [**D3DLIGHT9**](d3dlight9.md).                                                          |
| LightRange \[ n\]        | FLOAT  | Consulte o membro Range de [**D3DLIGHT9**](d3dlight9.md).                                                             |
| LightSpecular \[ n\]     | float4 | Consulte o membro especular de [**D3DLIGHT9**](d3dlight9.md).                                                          |
| LightTheta \[ n\]        | FLOAT  | Consulte o membro teta de [**D3DLIGHT9**](d3dlight9.md).                                                             |
| LightType \[ n\]         | DWORD  | Mesmo valor que a matriz de até n valores de [**D3DLIGHTTYPE**](./d3dlighttype.md) sem o \_ prefixo D3DLIGHT. |



 

Exemplo:


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



Isso habilitará a iluminação, tornará a iluminação do tipo, definirá a posição da luz como float3<10.0 f, 1,0 f, 23.0 f> e definirá a cor do ambiente como FLOAT4<0,7 f, 0,0 f, 0,0 f, 1.0>.

## <a name="material-states"></a>Estados de material

Declara que você não deve declarar está definido como um valor padrão porque não há como o Direct3D para definir os Estados de material individualmente.



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| Estado do material   | Type   | Valores                                         |
| MaterialAmbient  | float4 | Mesmo valor que o [ **ambiente**](d3dmaterial9.md)  |
| MaterialDiffuse  | float4 | Mesmo valor que [ **difusa**](d3dmaterial9.md)  |
| MaterialEmissive | float4 | Mesmo valor que [ **emissiva**](d3dmaterial9.md) |
| MaterialPower    | FLOAT  | Mesmo valor que a [ **energia**](d3dmaterial9.md)    |
| MaterialSpecular | float4 | Mesmo valor que [ **especular**](d3dmaterial9.md) |



 

Exemplo:


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



Isso definirá a cor difusa como FLOAT4<0,7 f, 0,0 f, 0,0 f, 1,0 f> e tornará o poder do material 3.0 f.

## <a name="render-states"></a>Processar Estados

Há dois tipos de Estados de renderização:

-   [Estados de renderização de pipe de pixel](#pixel-pipe-render-states)
-   [Estados de renderização de pipe de vértice](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a>Estados de renderização de pipe de pixel

Os Estados de renderização do arquivo de efeito têm nomes semelhantes aos Estados de pipeline de função fixa, geralmente com o prefixo removido.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Estado de renderização</td>
<td>Type</td>
<td>Valores</td>
</tr>
<tr class="even">
<td>AlphaBlendEnable</td>
<td>bool</td>
<td>Verdadeiro ou falso. Os mesmos valores que D3DRS_ALPHABLENDENABLE em <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</td>
</tr>
<tr class="odd">
<td>AlphaFunc</td>
<td>DWORD</td>
<td>Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sem o prefixo D3DCMP_. Consulte D3DRS_ALPHAFUNC.</td>
</tr>
<tr class="even">
<td>AlphaRef</td>
<td>DWORD</td>
<td>Mesmos valores que D3DRS_ALPHAREF.</td>
</tr>
<tr class="odd">
<td>AlphaTestEnable</td>
<td>DWORD</td>
<td>Verdadeiro ou falso. Consulte D3DRS_ALPHATESTENABLE.</td>
</tr>
<tr class="even">
<td>BlendOp</td>
<td>DWORD</td>
<td>Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> sem o prefixo D3DBLENDOP_.</td>
</tr>
<tr class="odd">
<td>ColorWriteEnable</td>
<td>DWORD</td>
<td>Combinação de bits de vermelho | VERDE | AZUL | Alfa. Consulte D3DRS_COLORWRITEENABLE.</td>
</tr>
<tr class="even">
<td>DepthBias</td>
<td>FLOAT</td>
<td>Mesmos valores que D3DRS_DEPTHBIAS.</td>
</tr>
<tr class="odd">
<td>DestBlend</td>
<td>DWORD</td>
<td>Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sem o prefixo D3DBLEND_.</td>
</tr>
<tr class="even">
<td>DitherEnable</td>
<td>bool</td>
<td>Verdadeiro ou falso. Mesmos valores que D3DRS_DITHERENABLE.</td>
</tr>
<tr class="odd">
<td>FillMode</td>
<td>DWORD</td>
<td>Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> sem o prefixo D3DFILL_.</td>
</tr>
<tr class="even">
<td>LastPixel</td>
<td>DWORD</td>
<td>Verdadeiro ou falso. Consulte D3DRS_LASTPIXEL.</td>
</tr>
<tr class="odd">
<td>Shadmode</td>
<td>DWORD</td>
<td>Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> sem o prefixo D3DSHADE_.</td>
</tr>
<tr class="even">
<td>SlopeScaleDepthBias</td>
<td>FLOAT</td>
<td>Mesmos valores que D3DRS_SLOPESCALEDEPTHBIAS.</td>
</tr>
<tr class="odd">
<td>SrcBlend</td>
<td>DWORD</td>
<td>Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> sem o prefixo D3DBLEND_.</td>
</tr>
<tr class="even">
<td>SRGBWriteEnable</td>
<td>bool</td>
<td>Verdadeiro ou falso. Mesmos valores que D3DRS_SRGBWRITEENABLE.</td>
</tr>
<tr class="odd">
<td>StencilEnable</td>
<td>bool</td>
<td>Verdadeiro ou falso. Mesmos valores que D3DRS_STENCILENABLE.</td>
</tr>
<tr class="even">
<td>StencilFail</td>
<td>DWORD</td>
<td>Os mesmos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sem o prefixo D3DSTENCILCAP_. Consulte D3DRS_STENCILFAIL.</td>
</tr>
<tr class="odd">
<td>StencilFunc</td>
<td>DWORD</td>
<td>Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sem o prefixo D3DCMP_. Consulte D3DRS_STENCILFUNC.</td>
</tr>
<tr class="even">
<td>StencilMask</td>
<td>DWORD</td>
<td>Mesmos valores que D3DRS_STENCILMASK.</td>
</tr>
<tr class="odd">
<td>StencilPass</td>
<td>DWORD</td>
<td>Os mesmos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sem o prefixo D3DSTENCILCAP_. Consulte D3DRS_STENCILPASS.</td>
</tr>
<tr class="even">
<td>StencilRef</td>
<td>INT</td>
<td>Mesmos valores que D3DRS_STENCILREF.</td>
</tr>
<tr class="odd">
<td>StencilWriteMask</td>
<td>DWORD</td>
<td>Mesmos valores que D3DRS_STENCILWRITEMASK.</td>
</tr>
<tr class="even">
<td>StencilZFail</td>
<td>DWORD</td>
<td>Os mesmos valores que <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> sem o prefixo D3DSTENCILCAP_. Consulte D3DRS_STENCILZFAIL.</td>
</tr>
<tr class="odd">
<td>TextureFactor</td>
<td>DWORD</td>
<td>Mesmos valores que <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>. Mesmos valores que D3DRS_TEXTUREFACTOR.</td>
</tr>
<tr class="even">
<td>Wrap0 - Wrap15</td>
<td>DWORD</td>
<td>Os valores são os mesmos que os valores usados pelo D3DRS_WRAP0. Os valores válidos são:
<ul>
<li>COORD0 (que corresponde a D3DWRAPCOORD_0)</li>
<li>COORD1 (que corresponde a D3DWRAPCOORD_1)</li>
<li>COORD2 (que corresponde a D3DWRAPCOORD_2)</li>
<li>COORD3 (que corresponde a D3DWRAPCOORD_3)</li>
<li>U (que corresponde a D3DWRAP_U)</li>
<li>V (que corresponde a D3DWRAP_V)</li>
<li>W (que corresponde a D3DWRAP_W)</li>
</ul></td>
</tr>
<tr class="odd">
<td>ZEnable</td>
<td>DWORD</td>
<td>Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> sem o prefixo D3DZB_.</td>
</tr>
<tr class="even">
<td>ZFunc</td>
<td>DWORD</td>
<td>Os mesmos valores que <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> sem o prefixo D3DCMP_. Consulte D3DRS_ZFUNC.</td>
</tr>
<tr class="odd">
<td>ZWriteEnable</td>
<td>bool</td>
<td>Verdadeiro ou falso. Consulte D3DRS_ZWRITEENABLE.</td>
</tr>
</tbody>
</table>



 

Exemplo:


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



Isso habilitará a mistura alfa e fará com que todas as geometrias sejam renderizadas em wireframe.

### <a name="vertex-pipe-render-states"></a>Estados de renderização de pipe de vértice

Os Estados de renderização do arquivo de efeito têm nomes semelhantes aos Estados de pipeline de função fixa, geralmente com o prefixo removido.



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| Estado de renderização             | Type   | Valores                                                                                                                                        |
| Ambiente                  | float4 | Mesmos valores que D3DRS \_ ambiente.                                                                                                                |
| AmbientMaterialSource    | DWORD  | Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS. Consulte D3DRS \_ AMBIENTMATERIALSOURCE.  |
| Recortando                 | bool   | Verdadeiro ou falso. Mesmos valores que o \_ recorte de D3DRS.                                                                                                |
| ClipPlaneEnable          | DWORD  | Combinação de bits de D3DCLIPPLANE0-D3DCLIPPLANE5. Consulte [**D3DCLIPPLANEn**](d3dclipplanen.md) e D3DRS \_ CLIPPLANEENABLE.           |
| ColorVertex              | bool   | Verdadeiro ou falso. Mesmos valores que D3DRS \_ COLORVERTEX.                                                                                             |
| De seleção                 | DWORD  | Mesmos valores que [**D3DCULL**](./d3dcull.md) sem o \_ prefixo D3DCULL.                                                                 |
| DiffuseMaterialSource    | DWORD  | Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS. Consulte D3DRS \_ DiffuseMaterialSource.  |
| EmissiveMaterialSource   | DWORD  | Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS. Consulte D3DRS \_ EMISSIVEMATERIALSOURCE. |
| FogColor                 | DWORD  | Mesmos valores que [**D3DCOLOR**](d3dcolor.md). Consulte D3DRS \_ FOGCOLOR.                                                                             |
| FogDensity               | FLOAT  | Mesmos valores que D3DRS \_ FOGDENSITY.                                                                                                             |
| FogEnable                | bool   | Verdadeiro ou falso. Mesmos valores que D3DRS \_ FOGENABLE.                                                                                               |
| FogEnd                   | FLOAT  | Mesmos valores que D3DRS \_ FOGEND.                                                                                                                 |
| FogStart                 | FLOAT  | Mesmos valores que D3DRS \_ FOGSTART.                                                                                                               |
| FogTableMode             | DWORD  | Mesmos valores que [**D3DFOGMODE**](./d3dfogmode.md). Consulte D3DRS \_ FOGTABLEMODE no [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).     |
| FogVertexMode            | DWORD  | Mesmos valores que [**D3DFOGMODE**](./d3dfogmode.md) sem o \_ prefixo D3DFOG.                                                            |
| IndexedVertexBlendEnable | bool   | Verdadeiro ou falso. Mesmos valores que D3DRS \_ INDEXEDVERTEXBLENDENABLE.                                                                                |
| Iluminação                 | bool   | Verdadeiro ou falso. Mesmos valores que a \_ iluminação D3DRS.                                                                                                |
| LocalViewer              | bool   | Verdadeiro ou falso. Mesmos valores que D3DRS \_ LOCALVIEWER.                                                                                             |
| MultiSampleAntialias     | bool   | Mesmos valores que D3DRS \_ MULTISAMPLEANTIALIAS.                                                                                                   |
| MultiSampleMask          | DWORD  | Mesmos valores que D3DRS \_ MULTISAMPLEMASK.                                                                                                        |
| NormalizeNormals         | bool   | Verdadeiro ou falso. Mesmos valores que D3DRS \_ NORMALIZENORMALS.                                                                                        |
| PatchSegments            | FLOAT  | Mesmos valores que nSegments em [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).                                                         |
| PointScale \_ A            | FLOAT  | Os mesmos valores que D3DRS \_ POINTSCALE \_ A.                                                                                                          |
| PointScale \_ B            | FLOAT  | Os mesmos valores que D3DRS \_ POINTSCALE \_ B.                                                                                                          |
| PointScale \_ C            | FLOAT  | Os mesmos valores que D3DRS \_ POINTSCALE \_ C.                                                                                                          |
| PointScaleEnable         | bool   | Mesmos valores que D3DRS \_ POINTSCALEENABLE.                                                                                                       |
| Pontos                | FLOAT  | Os mesmos valores que D3DRS \_ apontam.                                                                                                              |
| Pontos \_ mínimos           | FLOAT  | Os mesmos valores que D3DRS \_ apontam \_ mín.                                                                                                         |
| Pontos \_ máximos           | FLOAT  | Os mesmos valores que D3DRS \_ aponta para \_ Max sem o \_ prefixo D3DRS.                                                                              |
| PointSpriteEnable        | bool   | Verdadeiro ou falso. Mesmos valores que D3DRS \_ POINTSPRITEENABLE.                                                                                       |
| RangeFogEnable           | bool   | Verdadeiro ou falso. Mesmos valores que D3DRS \_ RANGEFOGENABLE.                                                                                          |
| SpecularEnable           | bool   | Verdadeiro ou falso. Mesmos valores que D3DRS \_ SPECULARENABLE.                                                                                          |
| SpecularMaterialSource   | DWORD  | Mesmos valores que [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) sem o \_ prefixo D3DMCS. Consulte D3DRS \_ SPECULARMATERIALSOURCE. |
| TweenFactor              | FLOAT  | Mesmos valores que D3DRS \_ TWEENFACTOR.                                                                                                            |
| VertexBlend              | DWORD  | Mesmos valores que [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) sem o \_ prefixo D3DVBF. Consulte D3DRS \_ VERTEXBLEND.                  |



 

Exemplo:


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



Isso fará com que a cor do ambiente FLOAT4<0,7 f, 0,0 f, 0,0 f, 1,0 f>, defina o modo de remoção do backface como contador no sentido anti-horário e defina a cor da neblina como vermelha.

## <a name="sampler-states"></a>Estados de amostra

Um estado de amostra representa um objeto de amostra.



|         |         |                                     |
|---------|---------|-------------------------------------|
| Estado   | Type    | Valores                              |
| Exemplo | cores | **NULL** ou um bloco de estado de amostra. |



 

## <a name="sampler-stage-states"></a>Estados de estágio de amostra

Os Estados de estágio de amostra são usados para amostras de texturas. O estado de amostra determina os tipos de filtragem e os modos de endereçamento de textura.



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| Estado do classificador       | Type                         | Valores                                                                                                                            |
| Endereço de \[ 16\]      | DWORD                        | Mesmos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sem o \_ prefixo D3DTADDRESS. Consulte D3DSAMP \_ AddressU.      |
| AddressV \[ 16\]      | DWORD                        | Mesmos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sem o \_ prefixo D3DTADDRESS. Consulte D3DSAMP \_ ADDRESSV.      |
| AddressW \[ 16\]      | DWORD                        | Mesmos valores que [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) sem o \_ prefixo D3DTADDRESS. Consulte D3DSAMP \_ ADDRESSW.      |
| BorderColor \[ 16\]   | [**D3DCOLOR**](d3dcolor.md) | Mesmos valores que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sem o \_ prefixo D3DTEXF. Consulte D3DSAMP \_ BORDERCOLOR. |
| MagFilter \[ 16\]     | DWORD                        | Mesmos valores que [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) sem o \_ prefixo D3DTEXF. Consulte D3DSAMP \_ MAGFILTER.   |
| MaxAnisotropy \[ 16\] | DWORD                        | Os mesmos valores que D3DSAMP \_ MAXANISOTROPY sem o \_ prefixo D3DSAMP.                                                               |
| MaxMipLevel \[ 16\]   | INT                          | Os mesmos valores que D3DSAMP \_ MAXMIPLEVEL sem o \_ prefixo D3DSAMP.                                                                 |
| MinFilter \[ 16\]     | DWORD                        | Os mesmos valores que D3DSAMP \_ MINFILTER sem o \_ prefixo D3DSAMP.                                                                   |
| MipFilter \[ 16\]     | DWORD                        | Os mesmos valores que D3DSAMP \_ MIPFILTER sem o \_ prefixo D3DSAMP.                                                                   |
| MipMapLodBias \[ 16\] | FLOAT                        | Os mesmos valores que D3DSAMP \_ MIPMAPLODBIAS sem o \_ prefixo D3DSAMP.                                                               |
| SRGBTexture         | bool                         | Mesmo valor que D3DSAMP \_ SRGBTEXTURE sem o \_ prefixo D3DSAMP.                                                                   |



 

Exemplo:


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



Isso coloca UVW valores entre 0 e 1.

## <a name="shader-states"></a>Estados do sombreador

Há apenas dois Estados de sombreador de efeito: um associado a um objeto de sombreador de vértice e o outro associado a um objeto de sombreador de pixel.



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| Estado do sombreador | Type         | Valores                                                                      |
| PixelShader  | PixelShader  | **NULL**, um bloco de assembly, um destino de compilação ou um parâmetro de sombreador de pixel. |
| VertexShader | vertexshader | **NULL**, um bloco de assembly, um destino de compilação ou um parâmetro de sombreador de pixel. |



 

Exemplo:


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



Isso compilará VSTexture, um sombreador de vértice definido anteriormente no arquivo. FX, para o vertex shader versão 1,1 e, em seguida, definirá esse sombreador compilado como o sombreador de vértice. O sombreador de pixel é atribuído a **NULL**.

## <a name="shader-constant-states"></a>Estados de constante do sombreador

Os Estados de constante do sombreador são usados para acessar parâmetros de constante de sombreador.



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| Estado de constante do sombreador | Type            | Valores                                       |
| PixelShaderConstant   | float \[ m \[ n\]\] | matriz m x n de floats; m e n são opcionais. |
| PixelShaderConstant1  | float4          | Um 4D flutuante.                                |
| PixelShaderConstant2  | float4x2        | Dois 4D flutuantes.                               |
| PixelShaderConstant3  | float4x3        | Três o 4D floats.                             |
| PixelShaderConstant4  | float4x4        | Quatro o 4D flutua.                              |
| PixelShaderConstantB  | bool \[ m \[ n\]\]  | matriz m x n de BOOLs; m e n são opcionais.  |
| PixelShaderConstantI  | int \[ m \[ n\]\]   | matriz m x n de ints. m e n são opcionais.   |
| PixelShaderConstantF  | float \[ m \[ n\]\] | matriz m x n de floats. m e n são opcionais. |
| VertexShaderConstant  | float \[ m \[ n\]\] | matriz m x n de floats. m e n são opcionais. |
| VertexShaderConstant1 | float4          | Um 4D flutuante.                                |
| VertexShaderConstant2 | float4x2        | Dois 4D flutuantes.                               |
| VertexShaderConstant3 | float4x3        | Três o 4D floats.                             |
| VertexShaderConstant4 | float4x4        | Quatro o 4D flutua.                              |
| VertexShaderConstantB | bool \[ m \[ n\]\]  | matriz m x n de BOOLs. m e n são opcionais.  |
| VertexShaderConstantI | int \[ m \[ n\]\]   | matriz m x n de ints. m e n são opcionais.   |
| VertexShaderConstantF | float \[ m \[ n\]\] | matriz m x n de floats. m e n são opcionais. |



 

## <a name="texture-states"></a>Estados de textura

Os Estados de textura inicializam texturas usadas pelo misturador multitextura.



|               |         |                                   |
|---------------|---------|-----------------------------------|
| Estado de textura | Type    | Valores                            |
| Textura \[ 8\]  | textura | **NULL** ou um parâmetro de textura. |



 

## <a name="texture-stage-states"></a>Estados de estágio de textura

Estados de estágio de textura configuram texturas e os estágios de textura no misturador multitextura.



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Estado do estágio de textura        | Type  | Valores                                                                                                                                                    |
| AlphaOp \[ 8\]               | DWORD | O mesmo que [**D3DTEXTUREOP**](./d3dtextureop.md) sem o \_ prefixo D3DTOP. Consulte D3DTSS \_ ALPHAOP.                                                      |
| AlphaArg0 \[ 8\]             | DWORD | O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA. Consulte D3DTSS \_ ALPHAARG0.                                                                             |
| AlphaArg1 \[ 8\]             | DWORD | O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA. Consulte D3DTSS \_ ALPHAARG1.                                                                             |
| AlphaArg2 \[ 8\]             | DWORD | O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA. Consulte D3DTSS \_ ALPHAARG2.                                                                             |
| ColorArg0 \[ 8\]             | DWORD | O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA. Consulte D3DTSS \_ COLORARG0.                                                                             |
| ColorArg1 \[ 8\]             | DWORD | O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA. Consulte D3DTSS \_ COLORARG1.                                                                             |
| ColorArg2 \[ 8\]             | DWORD | O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA. Consulte D3DTSS \_ COLORARG2.                                                                             |
| ColorOp \[ 8\]               | DWORD | O mesmo que [**D3DTEXTUREOP**](./d3dtextureop.md) sem o \_ prefixo D3DTOP. Consulte D3DTSS \_ COLOROP.                                                      |
| BumpEnvLScale \[ 8\]         | FLOAT | Os mesmos valores que D3DTSS \_ BUMPENVLSCALE sem o \_ prefixo D3DTSS TCI.                                                                                      |
| BumpEnvLOffset \[ 8\]        | FLOAT | Os mesmos valores que D3DTSS \_ BUMPENVLOFFSET sem o \_ prefixo D3DTSS TCI.                                                                                     |
| BumpEnvMat00 \[ 8\]          | FLOAT | Mesmos valores que D3DTSS \_ BUMPENVMAT00.                                                                                                                      |
| BumpEnvMat01 \[ 8\]          | FLOAT | Mesmos valores que D3DTSS \_ BUMPENVMAT01.                                                                                                                      |
| BumpEnvMat10 \[ 8\]          | FLOAT | Mesmos valores que D3DTSS \_ BUMPENVMAT10.                                                                                                                      |
| BumpEnvMat11 \[ 8\]          | FLOAT | Mesmos valores que D3DTSS \_ BUMPENVMAT11.                                                                                                                      |
| ResultArg \[ 8\]             | DWORD | O mesmo que [D3DTA](d3dta.md) sem o \_ prefixo D3DTA. Consulte D3DTSS \_ RESULTARG.                                                                             |
| TexCoordIndex \[ 8\]         | DWORD | Os mesmos valores que D3DTSS \_ TEXCOORDINDEX sem o \_ prefixo D3DTSS TCI.                                                                                      |
| TextureTransformFlags \[ 8\] | DWORD | Mesmos valores que [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) valores sem o \_ prefixo D3DTTFF. Consulte D3DTSS \_ TEXTURETRANSFORMFLAGS. |



 

## <a name="transform-states"></a>Estados de transformação

Defina Estados de transformação para inicializar matrizes de transformação. Os efeitos usam matrizes transpostas para obter eficiência. Você pode fornecer matrizes transpostas a um efeito, ou um efeito irá transpor automaticamente as matrizes antes de usá-las.



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| Estado de transformação       | Type     | Valores                                                                                                                          |
| ProjectionTransform   | float4x4 | Uma matriz 4x4 de floats. Mesmos valores que D3DTS \_ projeção sem o \_ prefixo D3DTS.                                            |
| TextureTransform \[ 8\] | float4x4 | Uma matriz 4x4 de floats. Mesmos valores que [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) sem o \_ prefixo D3DTS. |
| ViewTransform         | float4x4 | Uma matriz 4x4 de floats. Mesmos valores que D3DTS \_ exibição sem o \_ prefixo D3DTS.                                                  |
| WorldTransform        | float4x4 | Uma matriz 4x4 de floats.                                                                                                         |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Formato do efeito](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
