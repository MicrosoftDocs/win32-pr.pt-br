---
title: Modelo de sombreador HLSL 6,4
description: Descreve os intrínsecos do Machine Learning adicionados ao modelo de sombreador HLSL 6,4.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 5e161d77439eef63547d92fcc4f47e3185ac798141d20017d7e7102ee86a38cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511830"
---
# <a name="hlsl-shader-model-64"></a>Modelo de sombreador HLSL 6,4

Descreve os intrínsecos do Machine Learning adicionados ao modelo de sombreador HLSL 6,4.

## <a name="shader-model-64"></a>Modelo do sombreador 6,4
Esses intrínsecos são um recurso necessário/com suporte do Shader Model 6,4. Consequentemente, nenhuma verificação de bit de recurso separada é necessária, além de garantir o uso do modelo de sombreador 6,4. o cliente mínimo com suporte para essas rotinas é Windows 10, versão 1903.

## <a name="shading-language-intrinsics"></a>Intrínsecos da linguagem de sombreamento

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a>Inteiro não atribuído Dot-Product de 4 elementos e acumular
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
Um ponto inteiro sem sinal de 4 dimensões-produto com adicionar. Multiplica cada par correspondente de bytes int de 8 bits não assinados nas duas DWORDs de entrada e soma os resultados no acumulador inteiro não assinado de 32 bits. Essa instrução opera em uma única rota SIMD de 32 bits. As entradas também são presumidas como quantidades de 32 bits.
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a>Inteiro assinado Dot-Product de 4 elementos e acumular
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

Um item de ponto inteiro com sinal 4-dimensional com Add. Multiplica cada par correspondente de bytes int de 8 bits assinados nos dois DWORDs de entrada e soma os resultados no acumulador inteiro com sinal de 32 bits. Essa instrução opera em uma única rota SIMD de 32 bits. As entradas também são presumidas como quantidades de 32 bits.
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a>Ponto flutuante de precisão única de dois elementos Dot-Product e acumular
```syntax
float dot2add( half2 a, half2 b, float acc );
```

Um ponto flutuante bidimensional, ponto-produto de vetores half2 com Add. Multiplica os elementos dos dois vetores de entrada float de meia precisão juntos e soma os resultados no acumulador float de 32 bits. Estas instruções operam em uma única rota SIMD de 32 bits. As entradas são quantidades de 16 bits incluídas na mesma pista.

Isso é abordado no bit de recurso de baixa precisão (indicando que a metade nativa e o suporte curto estão presentes).

### <a name="sv_shadingrate"></a>SV_ShadingRate
```syntax
uint shadingRate : SV_ShadingRate
```

Um inteiro sem sinal representando quantos pixels de destino são gravados por cada invocação do sombreador de pixel. Os valores válidos pertencem ao conjunto de valores de enumeração [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).

Esse valor de sistema está disponível em plataformas [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) ou superior. Ele pode ser gravado a partir de no máximo um vértice ou estágios de sombreador de geometria. Ele pode ser lido no estágio pixel shader. Para obter mais informações, consulte [sombreamento de taxa variável](../direct3d12/vrs.md).