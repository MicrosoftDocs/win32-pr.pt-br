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
ms.openlocfilehash: ce8c6ec83963dac74dce32d248b23548c767192a604ddb8afbe35cf932dedee9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514601"
---
# <a name="function-declaration-syntax"></a>Sintaxe de declaração da função

As funções HLSL são declaradas com a sintaxe a seguir.

\[*StorageClass* \] \[clipplanes() \] \[ precise \] Return Value \_ *Name* ( \[ *ArgumentList* \] ) : \[ *Semantic* \] { \[ *StatementBlock* \] };



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*
</dt> <dd>

Modificador que redefine uma declaração de função. **inline** é atualmente o único valor modificador. O valor do modificador deve **ser em linha** porque também é o valor padrão. Portanto, uma função é em linha, independentemente de você especificar em **linha** e todas as funções em HLSL são em linha. Uma função em linha gera uma cópia do corpo da função (ao compilar) para cada chamada de função. Isso é feito para diminuir a sobrecarga de chamar a função.

</dd> <dt>

<span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*
</dt> <dd>

Lista opcional de planos de clipe, que é de até 6 planos de clipe especificados pelo usuário. Esse é um mecanismo alternativo para [o \_ ClipDistance SV](dx-graphics-hlsl-semantics.md) que funciona no [nível de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) recurso 9 x e \_ superior.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*
</dt> <dd>

Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da função de sombreador.

</dd> <dt>

<span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*Argumentlist*
</dt> <dd>

Lista de argumentos opcionais, que é uma lista separada por vírgulas de [argumentos passados](dx-graphics-hlsl-function-parameters.md) para uma função.

</dd> <dt>

<span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semântica*
</dt> <dd>

Cadeia de caracteres opcional que identifica o uso pretendido dos dados de retorno (consulte [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).

</dd> <dt>

<span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*
</dt> <dd>

Instruções [opcionais](dx-graphics-hlsl-statement-blocks.md) que comem o corpo da função. Uma função definida sem um corpo é chamada de protótipo de função; O corpo de uma função de protótipo deve ser definido em outro lugar antes que a função possa ser chamada.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

O tipo de retorno pode ser qualquer um desses [tipos HLSL.](dx-graphics-hlsl-data-types.md)

## <a name="remarks"></a>Comentários

A sintaxe nesta página descreve quase todos os tipos de função HLSL, isso inclui sombreadores de vértice, sombreadores de pixel e funções auxiliares. Embora um sombreador de geometria também seja implementado com uma função, sua sintaxe é um pouco mais complicada, portanto, há uma página separada que define uma declaração de função de sombreador de geometria (consulte [Objeto Geometry-Shader (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).

Uma função pode ser sobrecarregada desde que seja dada uma combinação exclusiva de tipos de parâmetro e/ou ordem de parâmetro. O HLSL também implementa um número de funções intrínsecas [**ou intrínsecas.**](dx-graphics-hlsl-intrinsic-functions.md)

Você pode especificar planos de clipe específicos do usuário com o **atributo clipplanes.** Windows aplica esses planos de clipe a todos os primitivos desenhados. O **atributo clipplanes** funciona como [SV \_ ClipDistance, mas](dx-graphics-hlsl-semantics.md) funciona em todos os recursos de hardware nível 9 x e [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) \_ superior. Para obter mais informações, consulte [Planos de clipe de usuário no hardware de nível de recurso 9.](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)

## <a name="examples"></a>Exemplos

Este exemplo é de BasicHLSL10.fx do [exemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).


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



Este exemplo de AdvancedParticles.fx da [amostra AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)ilustra o uso de uma semântica para o tipo de retorno.


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

 

 
