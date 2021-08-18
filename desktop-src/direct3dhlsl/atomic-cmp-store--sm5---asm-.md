---
title: atomic_cmp_store (sm5 – asm)
description: Comparação atômica e gravação na memória.
ms.assetid: 1B97E983-11A9-47E4-B274-E94083837C6E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dbc57b14b4279b9bd4844d89492852ae915d9d900ed04421eeeccc367979a63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118795158"
---
# <a name="atomic_cmp_store-sm5---asm"></a>atomic \_ cmp \_ store (sm5 - asm)

Comparação atômica e gravação na memória.



| atomic \_ cmp \_ store dst, dstAddress \[ .swizzle \] , src0 \[ .select component , \_ \] src1 \[ .select \_ component\] |
|--------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                           | Descrição                                                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*Dst*<br/>                                                   | \[em \] Os componentes a comparar com *src0*. Esse valor deve ser uma UAV (exibição de acesso não organizado) (u \# ). No sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[em \] O endereço de memória.<br/>                                                                                                                                                     |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[no \] valor de 32 bits a ser comparado com *dst.*<br/>                                                                                                                                 |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                                | \[em \] O valor a ser escrito na memória se os valores comparados são idênticos. <br/>                                                                                                     |



 

## <a name="remarks"></a>Comentários

Essa instrução executa uma comparação de valor de 32 bits de componente único do *operand src0* com *dst* em 32 bits por endereço de componente *dstAddress*.

Se os valores comparados são idênticos, o valor de 32 bits de componente único em *src1* é gravado na memória de destino. Caso contrário, o destino não será alterado.

Toda a operação de comparação e gravação é executada atomicamente.

Se *dst* for um u \# , ele poderá ser declarado como bruto, digitado ou estruturado. Se digitado, ele deve ser declarado como UINT/SINT com o formato de recurso vinculado sendo R32 \_ \_ UINT/SINT.

Se *dst* for g \# , ele deverá ser declarado como bruto ou estruturado.

O número de componentes retirados do endereço é determinado pela dimensionalidade de dst u \# ou g \# .

Nada é retornado para o sombreador.

Se a invocação do sombreador estiver inativa, por exemplo, se o pixel tiver sido descartado anteriormente em sua execução ou se uma instrução de pixel/exemplo não alterar a memória *dst* (silenciosamente).

O endereçamento fora dos limites em u faz com que nada seja gravado na memória, exceto se o u estiver estruturado e o deslocamento de byte no struct (segundo componente do endereço) estiver causando o acesso fora dos limites e, em seguida, todo o conteúdo do UAV se tornará \# \# indefinido.

O endereçamento fora dos limites em g (os limites desse g específico, em vez de toda a memória compartilhada) faz com que todo o conteúdo de toda a memória compartilhada se torne \# \# indefinido.

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

 

 





