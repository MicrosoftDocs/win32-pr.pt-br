---
title: fcall (SM5-ASM)
description: Chamada de função de interface.
ms.assetid: C21784A0-D2F4-4DDE-9AC4-4F21351BCA6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7781fc0a2fc7bbd715084d3c0e9682a433ddf16e4492724df8fdb2e31c84689
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854506"
---
# <a name="fcall-sm5---asm"></a>fcall (SM5-ASM)

Chamada de função de interface.



| fcall FP \# \[ arrayIndex \] \[ chamada\] |
|--------------------------------------|



 



| Item                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="fp_"></span><span id="FP_"></span>*FP\#*<br/>                                                  | \[no \] ponteiro de função.<br/>                                                                                                                                                                                                                                                                    |
| <span id="arrayIndex"></span><span id="arrayindex"></span><span id="ARRAYINDEX"></span>*arrayIndex*<br/> | \[em \] opcional. Especifica um deslocamento na matriz de ponteiro de função. Esse parâmetro deve ser um inteiro não assinado literal se FP \# não tiver sido declarado como indexável. Caso contrário, arrayIndex pode estar no formato literal base + offset de um registro de sombreador. Por exemplo, fcall FP1 \[ R1. w + 0 \] \[ 0 \] .<br/> |
| <span id="_callSite"></span><span id="_callsite"></span><span id="_CALLSITE"></span>*chamada*<br/>     | \[em \] opcional. Um deslocamento de inteiro não assinado literal na tabela de funções selecionada, selecionando um corpo de função FB \# a ser executado. <br/>                                                                                                                                                                |



 

## <a name="remarks"></a>Comentários

*FP \#* \[  \] \[ arrayIndex \] resolve para uma determinada tabela de funções, selecionada na API fora do sombreador das opções de tabela de funções listadas na declaração de *FP \#*.

A soma de \# em *FP \#* e *arrayIndex* selecione a tabela de funções. Por exemplo, se uma interface for declarada como FP4 \[ 4 \] \[ 3 \] (tamanho da matriz de 4), os seguintes **fcall** s serão equivalentes: fcall FP4 \[ 2 \] \[ 3 \] e FP5 \[ 1 \] \[ 3 \] , pois 4 + 2 = 5 + 1.

### <a name="restrictions"></a>Restrições

-   Se *arrayIndex* usar a indexação dinâmica, o comportamento será indefinido se *arrayIndex* divergir em invocações de sombreador adjacentes, que poderia estar em execução em atrelada. O compilador HLSL tentará não permitir esse caso.

    As invocações adjacentes podem ficar inativas devido ao controle de fluxo, pois ele não interrompe a execução de atrelada.

-   Se *FP \#*  +  *arrayIndex* especificar um índice fora dos limites, o comportamento será indefinido.
-   Para os casos indefinidos descritos aqui, isso significa que o comportamento do dispositivo D3D atual se torna indefinido, incluindo a possibilidade de perda do dispositivo. No entanto, nenhuma memória fora do dispositivo D3D atual será acessada ou executada como código.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

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

 

 





