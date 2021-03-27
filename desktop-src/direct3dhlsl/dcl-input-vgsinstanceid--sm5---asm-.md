---
title: dcl_input vGSInstanceID (SM5-ASM)
description: Habilitar a instanciação do sombreador de geometria.
ms.assetid: 47B9BAD5-0FFF-4DB7-B34A-7811B8A4F792
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3134a9d372f1fde5457f26235fe9a6a5439c58c1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293600"
---
# <a name="dcl_input-vgsinstanceid-sm5---asm"></a>\_vGSInstanceID de entrada DCL (SM5-ASM)

Habilitar a instanciação do sombreador de geometria.



| \_vGSInstanceID de entrada DCL, instanceCount |
|-----------------------------------------|



 



| Item                                                                                                                       | Descrição                           |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="vGSInstanceID"></span><span id="vgsinstanceid"></span><span id="VGSINSTANCEID"></span>*vGSInstanceID*<br/> | \[na \] ID da instância.<br/>    |
| <span id="instanceCount"></span><span id="instancecount"></span><span id="INSTANCECOUNT"></span>*instanceCount*<br/> | \[na \] contagem de instâncias.<br/> |



 

## <a name="remarks"></a>Comentários

O parâmetro *instanceCount* da declaração especifica quantas instâncias o sombreador de geometria deve executar para cada primitiva de entrada. O valor máximo para *instanceCount* é 32.

O número máximo de vértices declarados para saída, via [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), aplica-se individualmente a cada instância.

A contagem de instâncias nessa declaração, multiplicada pela contagem máxima de vértices por instância via [**DCL \_ maxOutputVertexCount**](dcl-maxoutputvertexcount.md), deve ser <= 1024.

A quantidade de dados que uma determinada instância de sombreador de geometria pode emitir é de 1024 escalares máximos, validadas contando todos os escalares declarados para entrada e multiplicando pela contagem de vértices de saída declarada.

O uso da instanciação do sombreador de geometria aumenta efetivamente a quantidade total de dados que podem ser emitidos por primitivo de entrada. 1024 escalares para uma única instância gera até 1024 \* 32 escalares de dados de saída em todas as instâncias de sombreador de geometria para um único primitivo de entrada. No entanto, quanto mais instâncias, menor é o número de vértices que cada instância pode emitir. Uma única instância (sem instanciação) pode emitir 1024 vértices. Se você declarar \* instâncias de 32, isso significa que cada instância só poderá produzir uma saída de 1024/32 = 32 vértices.

A declaração de instanciação do sombreador de geometria torna disponível para o programa um registro de entrada de inteiro de 32 bits autônomo, *vGSInstanceID*. Cada instância de sombreador de geometria é identificada pelo valor contido em *vGSInstanceID* \[ 0, 1, 2... \] .

*vGSInstanceID* não faz parte da matriz de vértice de entrada do sombreador de geometria (por exemplo, 3 vértices ao inserir um triângulo). O registro de *vGSInstanceID* permanece por conta própria, como vPrimitiveID.

Quando cada instância de sombreador de geometria termina, há um corte implícito na topologia de saída, portanto, as instâncias consecutivas não dependem umas das outras.

Embora o hardware possa executar cada instância de sombreador de geometria em paralelo, a saída de todas as instâncias no final é serializada como se todas as invocações de sombreador de geometria em instância executassem sequencialmente em um loop Iterando *vGSInstanceID* de 0 a *instanceCount*-1, com a topologia de saída implícita recorta no final de cada instância.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





