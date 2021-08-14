---
title: imm_atomic_iadd (sm5 – asm)
description: Inteiro atômico imediato adiciona à memória. Retorna o valor na memória antes de adicionar.
ms.assetid: 24136B4C-D37C-4449-A318-57145BB8D8E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d80a24fad3731f3d55c09f232ec61f4b3b09828cc7abd698e74259efe907c6d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511411"
---
# <a name="imm_atomic_iadd-sm5---asm"></a>imm \_ atomic \_ iadd (sm5 - asm)

Inteiro atômico imediato adiciona à memória. Retorna o valor na memória antes de adicionar.



| imm \_ atomic \_ iadd dst0 \[ .single component mask , \_ \_ \] dst1, dstAddress \[ .swizzle \] , src0 \[ \_ .select component\] |
|--------------------------------------------------------------------------------------------------------------|



 



| Item                                                                                                           | Descrição                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[em \] Contém o valor em *dst1 antes* da gravação. <br/>                                                                           |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | Esse valor deve ser uma UAV (exibição de acesso não organizado) (u \# ). No sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[em \] O naddress de memória.<br/>                                                                                                      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[em \] O valor a ser acrescentado a *dst1.*<br/>                                                                                               |



 

## <a name="remarks"></a>Comentários

Essa instrução executa um único componente de 32 bits integer add of operand *src0* with *dst1* at 32-bit per component address *dstAddress*. Não é possível assinar.

Se *dst1* for um u \# , ele poderá ter sido declarado como bruto, digitado ou estruturado. Se digitado, ele deve ser declarado como UINT/SINT com o formato de recurso vinculado sendo R32 \_ \_ UINT/SINT.

Se *dst1* for g \# , ele deverá ser declarado como bruto ou estruturado.

O valor na *memória dst1* antes da adição é retornado *para dst0*.

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

 

 





