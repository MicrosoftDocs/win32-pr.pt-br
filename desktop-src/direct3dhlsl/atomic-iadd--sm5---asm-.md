---
title: atomic_iadd (SM5-ASM)
description: Inteiro atômico adicione à memória.
ms.assetid: 093C7FA5-41BF-4BDD-A35D-1AACE8CB9B5C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d582cdb4951cecc845cb868e7eee64be61b8f2d7387a0548c43e094cf308226f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287749"
---
# <a name="atomic_iadd-sm5---asm"></a>\_IAdd atômico (SM5-ASM)

Inteiro atômico adicione à memória.



| \_componente Atomic IAdd DST, dstAddress \[ . swizzle \] , src0 \[ . Select \_\] |
|----------------------------------------------------------------------|



 



| Item                                                                                                           | Descrição                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*DST*<br/>                                                   | \[nos \] componentes a serem adicionados com *src0*. Esse valor deve ser uma exibição de acesso não ordenada (UAV) (u \# ). No sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[no \] endereço de memória.<br/>                                                                                                                                                 |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[nos \] componentes a serem adicionados ao *DST*.<br/>                                                                                                                                     |



 

## <a name="remarks"></a>Comentários

Essa instrução executa um único componente de *src0* de operando de inteiro de 32 bits no *DST* em 32 bits por endereço de componente *dstAddress*, executado atomicamente. Esta instrução não diferencia a assinatura.

O número de componentes extraídos do endereço é determinado pela dimensionalidade do *DST* u \# ou g \# .

Se o *DST* for um u \# , ele poderá ser declarado como RAW, tipado ou estruturado. Se digitado, ele deve ser declarado como UINT/Santo com o formato de recurso ligado sendo R32 \_ uint/ \_ Santo.

Se o *DST* for g \# , ele deverá ser declarado como bruto ou estruturado.

Nada é retornado para o sombreador.

Se a invocação do sombreador estiver inativa, por exemplo, se o pixel tiver sido descartado anteriormente em sua execução ou se uma invocação de pixel/amostra existir apenas para servir como um auxiliar para um pixel/amostra real para derivações, essa instrução não alterará a memória de *DST* (silenciosamente).

O endereçamento fora dos limites em u não \# faz nada a ser gravado na memória, exceto se o u \# for estruturado e o deslocamento de byte na estrutura (segundo componente do endereço) estiver causando o acesso fora dos limites, todo o conteúdo do UAV se tornará indefinido.

O endereçamento fora dos limites em g \# (os limites desse g específico \# , em oposição a toda a memória compartilhada) faz com que todo o conteúdo de toda a memória compartilhada se torne indefinido.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Como UAVs estão disponíveis em todos os estágios do sombreador para o Direct3D 11,1, essa instrução se aplica a todos os estágios do sombreador para o tempo de execução do Direct3D 11,1, que está disponível a partir do Windows 8.



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





