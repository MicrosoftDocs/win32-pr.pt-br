---
title: atomic_or (SM5-ASM)
description: OR-bit atômica para memória.
ms.assetid: 5AFB96AA-267B-454E-9526-BA61A876ED42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 245f1b02edd74712471206b095f0c8a9040962b6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104498948"
---
# <a name="atomic_or-sm5---asm"></a>atômico \_ ou (SM5-ASM)

OR-bit atômica para memória.



| \_componente Atomic ou DST, dstAddress \[ . swizzle \] , src0 \[ . Select \_\] |
|--------------------------------------------------------------------|



 



| Item                                                                                                           | Descrição                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*DST*<br/>                                                   | \[nos \] componentes para ou com *src0*. Esse valor deve ser uma exibição de acesso não ordenada (UAV) (u \# ). No sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[no \] endereço de memória.<br/>                                                                                                                                                |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[nos \] componentes do para o ou com o *DST*.<br/>                                                                                                                                   |



 

## <a name="remarks"></a>Comentários

Essa instrução executa um único componente de 32 bits de bit a bit ou do operando *src0* no *DST* em 32 bits por endereço de componente *dstAddress*, executado atomicamente.

O número de componentes extraídos do endereço é determinado pela dimensionalidade do *DST* u \# ou g \# .

Se o *DST* for um u \# , ele poderá ser declarado como RAW, tipado ou estruturado. Se digitado, ele deve ser declarado como UINT/Santo com o formato de recurso ligado sendo R32 \_ uint/ \_ Santo.

Se o *DST* for g \# , ele deverá ser declarado como bruto ou estruturado.

Nada é retornado para o sombreador.

Se a invocação do sombreador estiver inativa, por exemplo, se o pixel tiver sido descartado anteriormente em sua execução ou se uma invocação de pixel/amostra existir apenas para servir como um auxiliar para um pixel/amostra real para derivações, essa instrução não alterará a memória de *DST* (silenciosamente).

O endereçamento fora dos limites em u não \# faz nada a ser gravado na memória, exceto se o u \# for estruturado e o deslocamento de bytes na estrutura (segundo componente do endereço) estiver causando o acesso fora dos limites, o conteúdo inteiro do UAV se tornará indefinido.

O endereçamento fora dos limites em g \# (os limites desse g específico \# , em oposição a toda a memória compartilhada) faz com que todo o conteúdo de toda a memória compartilhada se torne indefinido.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





