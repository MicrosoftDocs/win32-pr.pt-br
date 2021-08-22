---
title: Carregar (objeto de textura DirectX HLSL)
description: Lê dados do Texel sem nenhuma filtragem ou amostragem.
ms.assetid: a2fbda88-29c7-4d28-bd3e-df1d9aa36ee8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ba394fb13fd98793401b29e6343ef4fa9ff0194b7a86f22dda1e58439737b34b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119860"
---
# <a name="load-directx-hlsl-texture-object"></a>Carregar (objeto de textura DirectX HLSL)

Lê dados do Texel sem nenhuma filtragem ou amostragem.



<table>
<tbody>
<tr class="odd">
<td>Objeto Ret. Load (<dl> Local typeX,<br />
[typeX SampleIndex,]<br />
[deslocamento de typeX]<br />
</dl>);</td>
</tr>
</tbody>
</table>

typeX denota que há quatro tipos possíveis: **int**, **Int2**, **Int3** ou **INT4**.

 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*
</dt> <dd>

Um tipo de [objeto de textura](dx-graphics-hlsl-to-type.md) (exceto TextureCube ou TextureCubeArray).

</dd> <dt>

<span id="Location"></span><span id="location"></span><span id="LOCATION"></span>*Local*
</dt> <dd>

\[nas \] coordenadas de textura, o último componente especifica o nível de mipmap. Esse método usa um sistema de coordenadas baseado em 0 e não um sistema UV de 0,0-1,0. O tipo de argumento é dependente do tipo de objeto Texture.



| Tipo de objeto                                  | Tipo de parâmetro |
|----------------------------------------------|----------------|
| Buffer                                       | INT            |
| Texture1D, Texture2DMS                       | int2           |
| Texture1DArray, 2D de textura, Texture2DMSArray | Int3           |
| Texture2DArray, Texture3D                    | int4           |



 

Por exemplo, para acessar uma textura 2D, forneça coordenadas UV para os dois primeiros componentes e um nível de mipmap para o terceiro componente.

> [!Note]  
> Quando uma ou mais das coordenadas no *local* excedem as dimensões de nível u, v ou w mipmap da textura, **Load** retorna zero em todos os componentes. O Direct3D garante para retornar zero para qualquer recurso que seja acessado fora dos limites.

 

</dd> <dt>

<span id="SampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*SampleIndex*
</dt> <dd>

\[em \] um índice de amostragem opcional.



| Tipo de textura                                                                                                   | Tipo de parâmetro |
|----------------------------------------------------------------------------------------------------------------|----------------|
| Texture1D, Texture1DArray, Texture2D, Texture2DArray, Texture3D, Texture2DArray, TextureCube, TextureCubeArray | sem suporte  |
| Texture2DMS, Texture2DMSArray ¹                                                                                 | INT            |



 

> [!Note]  
> *SampleIndex* só está disponível para texturas com várias amostras.

 

</dd> <dt>

<span id="Offset"></span><span id="offset"></span><span id="OFFSET"></span>*Desvio*
</dt> <dd>

\[em \] um deslocamento opcional aplicado às coordenadas de textura antes da amostragem. O tipo de deslocamento depende do tipo de objeto de textura e deve ser estático.



| Tipo de textura                                             | Tipo de parâmetro |
|----------------------------------------------------------|----------------|
| Texture1D, Texture1DArray                                | INT            |
| Texture2D, Texture2DArray, Texture2DMS, Texture2DMSArray | int2           |
| Texture3D, Texture2DArray                                | Int3           |



 

> [!Note]  
> Se você usar o *deslocamento* com texturas com várias amostras, também deverá especificar *SampleIndex*.

 

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

O tipo de retorno corresponde ao tipo na declaração de *objeto* . Por exemplo, um objeto Texture2D que foi declarado como "Texture2d <uint4> MyTexture;" tem um valor de retorno do tipo **uint4**.

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1 ¹ | PS \_ 4 \_ 0 | PS \_ 4 \_ 1 ¹ | GS \_ 4 \_ 0 | GS \_ 4 \_ 1 ¹ |
|----------|-----------|----------|-----------|----------|-----------|
| x        | x         | x        | x         | x        | x         |



 

-   O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.

## <a name="example"></a>Exemplo

este exemplo de código parcial é do arquivo Paint. fx no [exemplo AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx).


```
// Object Declarations
Buffer<float4> g_ParticleBuffer;

// Shader body calling the intrinsic function
float4 PSPaint(PSQuadIn input) : SV_Target
{       
    ... 
    for( int i=g_ParticleStart; i<g_NumParticles; i+=g_ParticleStep )
    {
        ... 
        // load the particle
        float4 particlePos = g_ParticleBuffer.Load( i*4 );
        float4 particleColor = g_ParticleBuffer.Load( (i*4) + 2 );
        ...     
    }
    ...
}   
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Textura-objeto](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 




