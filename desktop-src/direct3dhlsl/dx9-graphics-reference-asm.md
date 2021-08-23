---
title: Referência do sombreador ASM
description: Os sombreadores orientam o pipeline gráfico programável.
ms.assetid: 2c58815c-83b5-4ae8-a192-ba865b485bd6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9dbeb680b7131581b3891e59bb6bd2db0d6e5c19eb6279c47b83d22f01b5000e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119540"
---
# <a name="asm-shader-reference"></a>Referência do sombreador ASM

Os sombreadores orientam o pipeline gráfico programável.

## <a name="vertex-shader-reference"></a>Referência de sombreador de vértice

-   [vs \_ 1 \_ 1](dx9-graphics-reference-asm-vs-1-1.md)
-   [vs \_ 2 \_ 0](dx9-graphics-reference-asm-vs-2-0.md)
-   [vs \_ 2 \_ x](dx9-graphics-reference-asm-vs-2-x.md)
-   [vs \_ 3 \_ 0](dx9-graphics-reference-asm-vs-3-0.md)

[Diferenças de sombreador de vértice](dx9-graphics-reference-asm-vs-differences.md) resume as diferenças entre as versões de sombreador de vértice.

## <a name="pixel-shader-reference"></a>Referência de sombreador de pixel

-   [PS \_ 1 \_ 1, PS \_ 1 \_ 2, PS \_ 1 \_ 3, PS \_ 1 \_ 4](dx9-graphics-reference-asm-ps-1-x.md)
-   [PS \_ 2 \_ 0](dx9-graphics-reference-asm-ps-2-0.md)
-   [PS \_ 2 \_ x](dx9-graphics-reference-asm-ps-2-x.md)
-   [PS \_ 3 \_ 0](dx9-graphics-reference-asm-ps-3-0.md)

[Diferenças de sombreador de pixel](dx9-graphics-reference-asm-ps-differences.md) resume as diferenças entre versões de sombreador de pixel.

## <a name="shader-model-4-and-5-reference"></a>Referência do modelo do sombreador 4 e 5

As seções de assembly do [sombreador Model 4](dx-graphics-hlsl-sm4-asm.md) e do [sombreador Model 5](shader-model-5-assembly--directx-hlsl-.md) descrevem as instruções que dão suporte ao Shader Model 4 e 5.

## <a name="behavior-of-constant-registers-in-assembly-shaders"></a>Comportamento de registros constantes em sombreadores de assembly

Há duas maneiras de definir registros constantes em um sombreador de assembly:

-   Declare uma constante de sombreador no código do assembly usando uma das \* instruções def.
-   Use um dos métodos de \* \* \* API Set ShaderConstant \* .

### <a name="direct3d-9-shader-constants"></a>Constantes do sombreador do Direct3D 9

No Direct3D 9, o tempo de vida das constantes definidas em um determinado sombreador é restrito à execução somente desse sombreador (e não é substituível). Constantes definidas no Direct3D 9 não têm efeitos colaterais fora do sombreador.

Veja um exemplo usando o Direct3D 9:


```
Given: 
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1:
    Call Set***Shader shader1
    Call Set***ShaderConstant* to set c4
    Call Draw
    Result: The shader will see the def'd value in c4

    
Given: 
    Scenario 1 has just completed
    Create shader2 (which references c4 but does not use the def instruction
      to define it) 

Scenario 2: 
    Call Set***Shader shader2
    Call Draw
    Result: The shader will see the value last set in c4 by 
     Set***ShaderConstant* in scenario 1. This is because shader 2 
     didn't def c4.
```



No Direct3D 9, chamar get \* \* \* ShaderConstant \* recuperará apenas valores constantes definidos por meio de Set \* \* \* ShaderConstant \* .

### <a name="direct3d-8-shader-constants"></a>Constantes do sombreador do Direct3D 8

Esse comportamento é diferente no Direct3D 8. x.


```
Given:
    Create shader1 which references c4 and defines it with the def instruction

Scenario 1 (repeated with Direct3D 8):
    Call Set***Shader with shader1
    Call Set***ShaderConstant to set c4
    Call Draw
    Result: The shader will see the value in c4 from Set***ShaderConstant
```



No Direct3D 8. x Set \* \* \* ShaderConstant entra em vigor imediatamente. Considere este cenário:


```
Given:
    Create shader1 which references c4 and defines it with the def instruction
    
Scenario 3:
    Call Set***Shader with shader1
    Call Draw
    Result: The shader will see the def'd value in c4

Given:
    Scenario 3 has just completed
    Create shader2 (which references c4 but does not use the def instruction 
      to define it)     
    
Scenario 4 :    
    Call Set***Shader with shader2
    Call Draw
    Result: The shader will see the def'd value in c4 (set by def in shader 1)
```



O resultado indesejável é que a ordem na qual os sombreadores são definidos pode afetar o comportamento observado de sombreadores individuais.

## <a name="shader-driver-model-requirements"></a>Requisitos de modelo de driver do sombreador

As interfaces do Direct3D 9 são restritas a drivers de interface de driver de dispositivo (DDI) que são do nível DirectX 7 e superior. Para verificar o nível de DDI, execute a [ferramenta de diagnóstico do DirectX](https://msdn.microsoft.com/library/Ee416792(v=VS.85).aspx) e examine o arquivo de texto salvo.

Para referência, as interfaces do Direct3D 8 funcionam apenas em drivers de DDI que são de nível DirectX 6 e acima.

## <a name="shader-binary-format"></a>Formato binário do sombreador

O layout de bits bit do fluxo de instrução do sombreador é definido em D3d9types. h. Se você quiser projetar seu próprio compilador de sombreador ou ferramentas de construção e desejar obter mais informações sobre o fluxo do token do sombreador, consulte o kit de desenvolvimento de driver do Direct3D 9 (DDK).

## <a name="c-like-shader-language"></a>Linguagem de sombreador semelhante a C

Consulte a [referência do HLSL](dx-graphics-hlsl-reference.md) para ter uma linguagem de sombreador semelhante a C.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência para HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 




