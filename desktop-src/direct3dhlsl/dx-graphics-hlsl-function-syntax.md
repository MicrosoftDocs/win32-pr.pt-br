---
title: Sintaxe de declaração da função
description: As funções HLSL são declaradas com a sintaxe a seguir.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7358a59dba0096f5c8ffe58072a974ebff9a1050
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366559"
---
# <a name="function-declaration-syntax"></a>Sintaxe de declaração da função

As funções HLSL são declaradas com a sintaxe a seguir.



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| \[*StorageClass* \] \[clipplanes () \] \[ \] \_ *nome* do valor de retorno preciso ( \[ *ArgumentList* \] ) \[ : *semântica* \] { \[ *StatementBlock* \] }; |



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*
</dt> <dd>

Modificador que redefine uma declaração de função. no momento, **inline** é o único valor de modificador. O valor do modificador deve ser **embutido** porque também é o valor padrão. Portanto, uma função é embutida independentemente de você especificar **inline**, e todas as funções em HLSL são embutidas. Uma função embutida gera uma cópia do corpo da função (ao compilar) para cada chamada de função. Isso é feito para diminuir a sobrecarga de chamar a função.

</dd> <dt>

<span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*
</dt> <dd>

Lista opcional de recortes de clipes, que são até 6 planos de clipes especificados pelo usuário. Esse é um mecanismo alternativo para [ \_ ClipDistance de VA](dx-graphics-hlsl-semantics.md) que funciona no [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x e superior.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*
</dt> <dd>

Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da função de sombreador.

</dd> <dt>

<span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*
</dt> <dd>

Lista de argumentos opcional, que é uma lista separada por vírgulas de [argumentos](dx-graphics-hlsl-function-parameters.md) passados para uma função.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semântico*
</dt> <dd>

Cadeia de caracteres opcional que identifica o uso pretendido dos dados de retorno (consulte a [semântica (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

[Instruções](dx-graphics-hlsl-statement-blocks.md) opcionais que compõem o corpo da função. Uma função definida sem um corpo é chamada de protótipo de função; o corpo de uma função de protótipo deve ser definido em outro lugar antes que a função possa ser chamada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

O tipo de retorno pode ser qualquer um desses [tipos de HLSL](dx-graphics-hlsl-data-types.md).

## <a name="remarks"></a>Comentários

A sintaxe nesta página descreve quase todos os tipos de função HLSL, incluindo sombreadores de vértice, sombreadores de pixel e funções auxiliares. Embora um sombreador de geometria também seja implementado com uma função, sua sintaxe é um pouco mais complicada, portanto, há uma página separada que define uma declaração de função de sombreador de geometria (consulte o [objeto Geometry-Shader (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).

Uma função pode ser sobrecarregada desde que seja dada uma combinação exclusiva de tipos de parâmetro e/ou ordem de parâmetro. O HLSL também implementa várias funções internas ou [**intrínsecas**](dx-graphics-hlsl-intrinsic-functions.md).

Você pode especificar os planos de corte específicos do usuário com o atributo **clipplanes** . O Windows aplica esses planos de corte a todos os primitivos desenhados. O atributo **clipplanes** funciona como [VA \_ ClipDistance](dx-graphics-hlsl-semantics.md) , mas funciona em todo o [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de hardware 9 \_ x e superior. Para obter mais informações, consulte os [planos de corte do usuário no hardware nível 9 do recurso](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).

## <a name="examples"></a>Exemplos

Este exemplo é de BasicHLSL10. FX do [exemplo de BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).


```hlsl
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; 
    float4 Diffuse    : COLOR0;
    float2 TextureUV  : TEXCOORD0;
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    ...
    return Output;    
}
```



Este exemplo de AdvancedParticles. FX do [exemplo de AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)ilustra o uso de uma semântica para o tipo de retorno.


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Funções (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 