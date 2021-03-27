---
title: imm_atomic_exch (SM5-ASM)
description: Troca atômica imediata para memória.
ms.assetid: D06AE57E-52A4-4579-84FF-7DE9E713A5E3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb38cd696af079c5ae7dc896db619b95dd1d1d6c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084271"
---
# <a name="imm_atomic_exch-sm5---asm"></a>\_ \_ SM5-ASM (IMM Atomic Exch)

Troca atômica imediata para memória.



| \_dst0 de Exch atômico do IMM \_ \[ . \_ \_ máscara de componente único \] , dst1, dstAddress \[ . swizzle \] , \[ componente src0. Select \_\] |
|--------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                           | Descrição                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[in \] contém o valor de *dst1* antes da gravação.<br/>                                                                |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[em \] um modo de exibição de acesso não ordenado (UAV) (u \# ). No sombreador de computação, isso também pode ser memória compartilhada do grupo de threads (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[no \] endereço de memória.<br/>                                                                                             |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[no \] valor a ser gravado em *Dst1* em *dstAddress*.<br/>                                                                   |



 

## <a name="remarks"></a>Comentários

Essa instrução executa um único componente de valor de 32 bits gravação de operando *src0* para *dst1* em 32 bits por endereço de componente *dstAddress*.

Se *dst1* for u \# , ele poderá ter sido declarado como RAW, tipado ou estruturado. Se digitado, ele deve ser declarado como UINT/Santo com o formato de recurso ligado sendo R32 \_ uint/ \_ Santo.

Se *dst1* for g \# , ele deverá ser declarado como RAW ou Structured.

O número de componentes extraídos do endereço é determinado pela dimensionalidade do recurso declarado em *dst1*.

O valor de 32 bits original na memória de destino é gravado em *dst0*.

Toda a operação é executada atomicamente.

Se a invocação do sombreador estiver inativa, por exemplo, se o pixel tiver sido descartado anteriormente em sua execução, ou se uma invocação de pixel/amostra existir apenas para servir como um auxiliar para um pixel/amostra real para derivações, essa instrução não alterará a memória *dst1* e o valor retornado será indefinido.

O endereçamento fora dos limites em u não \# faz nada a ser gravado na memória, exceto se o u \# for estruturado e o deslocamento de byte na estrutura (segundo componente do endereço) estiver causando o acesso fora dos limites, todo o conteúdo do UAV se tornará indefinido.

O endereçamento fora dos limites em u \# ou g \# faz com que um resultado indefinido seja retornado ao sombreador em *dst0*.

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

 

 





