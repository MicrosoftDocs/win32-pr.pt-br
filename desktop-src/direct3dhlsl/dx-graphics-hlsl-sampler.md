---
title: Tipo de amostra
description: Use a sintaxe a seguir para declarar o estado de amostra, bem como o estado de comparação de amostra.
ms.assetid: 6534d343-d724-46e5-b300-2a29124a1a28
keywords:
- Tipo de amostra HLSL
topic_type:
- apiref
api_name:
- Sampler Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0206f7030d3b3a05570e74273d9510bb9c2592c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119571"
---
# <a name="sampler-type"></a>Tipo de amostra

Use a sintaxe a seguir para declarar o estado de amostra, bem como o estado de comparação de amostra.



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 10 e posterior:<br/> Aqui está a sintaxe de uma amostra no Direct3D 9.<br/> 
<table>
<tbody>
<tr class="odd">
<td><em>nome</em>do classificador  =  <em>SampleType</em>{Texture = <<em>texture_variable</em> > ;   [<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p>
<p>A sintaxe de uma amostra no Direct3D 10 e posterior é ligeiramente alterada para dar suporte a objetos de textura e matrizes de amostra.</p>

<table>
<tbody>
<tr class="odd">
<td><em>Nome do classificador [índice]</em>{[<em>state_name = state_value;</em>]   ... };</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="sampler"></span><span id="SAMPLER"></span>cores
</dt> <dd>

Somente Direct3D 9. Palavra-chave required.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*
</dt> <dd>

Cadeia de caracteres ASCII que identifica exclusivamente o nome da variável de amostra.

</dd> <dt>

<span id="_Index_"></span><span id="_index_"></span><span id="_INDEX_"></span>*\[Index\]*
</dt> <dd>

Direct3D 10 e posterior somente. Tamanho opcional da matriz; um inteiro positivo maior ou igual a 1.

</dd> <dt>

<span id="SamplerType"></span><span id="samplertype"></span><span id="SAMPLERTYPE"></span>*SampleType*
</dt> <dd>

\[no \] tipo de amostra, que é um dos seguintes: *amostra*, *sampler1D*, *sampler2D*, *sampler3D*, *samplerCUBE*, *\_ estado de amostra*, *samplestate*.

Diferenças entre o Direct3D 9 e o Direct3D 10 e posterior:

- O Direct3D 10 e posterior dá suporte a um tipo de amostra adicional: *SamplerComparisonState*.



 

</dd> <dt>

<span id="Texture____texture_variable__"></span><span id="texture____texture_variable__"></span><span id="TEXTURE____TEXTURE_VARIABLE__"></span>*Texture* = <*\_ variável de textura*>;
</dt> <dd>

Somente Direct3D 9. Uma variável de textura. A palavra-chave *Texture* é necessária no lado esquerdo; o nome da variável pertence ao lado direito da expressão dentro dos colchetes angulares.

</dd> <dt>

<span id="state_name___state_value"></span><span id="STATE_NAME___STATE_VALUE"></span>*nome do estado \_ = \_ valor do estado*
</dt> <dd>

\[na \] (s) atribuição (ões) de estado opcional. O lado esquerdo de uma atribuição é um nome de estado, o lado direito é o valor de estado. Todas as atribuições de estado devem aparecer dentro de um bloco de instruções (entre chaves). Cada instrução é separada com um ponto e vírgula. A tabela a seguir lista os possíveis nomes de estado.


```
// sampler state
AddressU
AddressV
AddressW
BorderColor
Filter
MaxAnisotropy
MaxLOD
MinLOD
MipLODBias

// sampler-comparison state
ComparisonFunc
```



O lado direito de cada expressão é o valor atribuído a cada Estado. Consulte a [**estrutura \_ \_ desc de amostra D3D11**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_sampler_desc) para obter os valores de estado possíveis para o Direct3D 11. Há uma relação de 1 a 1 entre os nomes de estado e os membros da estrutura. Veja o exemplo a seguir.

</dd> </dl>

## <a name="remarks"></a>Comentários

Quando você implementa um efeito, o estado de amostra é um dos vários tipos de estado que talvez você precise configurar no pipeline para renderização. Para obter uma lista de todos os Estados possíveis que podem ser definidos em um efeito, consulte:

-   O Direct3D 10 usa [grupos de Estados](/windows/desktop/direct3d10/d3d10-effect-states).
-   O Direct3D 9 usa [Estados](/windows/desktop/direct3d9/effect-states)individuais.

## <a name="example"></a>Exemplo



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 10:<br/> Aqui está um exemplo parcial de uma amostra do Direct3D 9 do <a href="https://msdn.microsoft.com/library/Ee416223(v=VS.85).aspx">exemplo BasicHLSL</a>.<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>sampler MeshTextureSampler = 
sampler_state
{
    Texture = <g_MeshTexture>;
    MipFilter = LINEAR;
    MinFilter = LINEAR;
    MagFilter = LINEAR;
};</code></pre></td>
</tr>
</tbody>
</table>

<p>Aqui está um exemplo parcial de uma amostra do Direct3D 10 do <a href="https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx">exemplo BasicHLSL10</a>.</p>
<div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>SamplerState MeshTextureSampler
{
    Filter = MIN_MAG_MIP_LINEAR;
    AddressU = Wrap;
    AddressV = Wrap;
};</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>



 

Aqui está um exemplo parcial de declaração do estado de comparação de amostra e chamada de uma amostra de comparação no Direct3D 10.


```
SamplerComparisonState ShadowSampler
{
   // sampler state
   Filter = COMPARISON_MIN_MAG_LINEAR_MIP_POINT;
   AddressU = MIRROR;
   AddressV = MIRROR;

   // sampler comparison state
   ComparisonFunc = LESS;
};
        
float3 vModProjUV;
  ...
float fShadow = g_ShadowMap.SampleCmpLevelZero( ShadowSampler, vModProjUV.xy, vModProjUV.z);
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Tipos de dados (DirectX HLSL)](dx-graphics-hlsl-data-types.md)
</dt> </dl>

 

