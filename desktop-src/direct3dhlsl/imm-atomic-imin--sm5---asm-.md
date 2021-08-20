---
title: imm_atomic_imin (sm5 – asm)
description: Mínimo atômico com assinatura imediata na memória. Retorna o valor na memória antes da operação máxima.
ms.assetid: 8E104FFA-D086-49FD-9063-B950B6B1548B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f41e616e8dd2727b994854eb0b9239ab7ef0eb62559500d72e1f654be25a2db5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089417"
---
# <a name="imm_atomic_imin-sm5---asm"></a>imm \_ atomic \_ imin (sm5 - asm)

Mínimo atômico com assinatura imediata na memória. Retorna o valor na memória antes da operação máxima.



| imm \_ atomic \_ imin dst0 \[ .single component mask , \_ \_ \] dst1, dstAddress \[ .swizzle \] , src0 \[ \_ .select component\] |
|--------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                           | Descrição                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[em \] Contém o valor de *dst1 antes* desta instrução.<br/>                                                         |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[em Uma exibição de acesso não organizado \] (UAV) (u \# ). No sombreador de computação, isso também pode ser memória compartilhada do grupo de threads (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[em \] O endereço de memória.<br/>                                                                                             |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[em \] O valor a ser comparado a *dst1* em *dstAddress*.<br/>                                                                 |



 

## <a name="remarks"></a>Comentários

A instrução Thisi executa um único componente com assinatura mínima de 32 bits de *src0* de operand com *dst1* a 32 bits por endereço de componente *dstAddress*.

Se *dst1* for um u \# , ele poderá ter sido declarado como bruto, digitado ou estruturado. Se digitado, ele deve ser declarado como UINT/SINT com o formato de recurso vinculado sendo R32 \_ \_ UINT/SINT.

Se *dst1* for g \# , ele deverá ser declarado como bruto ou estruturado.

O valor na *memória dst1* antes de min é retornado para *dst0*.

O número de componentes retirados do endereço é determinado pela dimensionalidade *de dst1*.

Toda a operação é executada atomicamente.

Se a invocação do sombreador estiver inativa, por exemplo, se o pixel tiver sido descartado anteriormente em sua execução ou se uma invocação de pixel/exemplo existir apenas para servir como auxiliar em um pixel/amostra real para derivados, essa instrução não alterará a memória *dst1* e o valor retornado será indefinido.

O endereçamento fora dos limites em u faz com que nada seja gravado na memória, exceto se o u estiver estruturado e o deslocamento de byte no struct (segundo componente do endereço) estiver causando o acesso fora dos limites e, em seguida, todo o conteúdo do UAV se tornará \# \# indefinido.

O endereçamento fora dos limites em u ou g faz com que um resultado indefinido seja retornado ao \# \# sombreador *em dst0*.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Como os UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11.1, essa instrução se aplica a todos os estágios do sombreador para o runtime do Direct3D 11.1, que está disponível a partir do Windows 8.



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





