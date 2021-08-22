---
title: imm_atomic_consume (SM5-ASM)
description: Decrementar atomicamente o contador de 32 bits oculto armazenado com uma contagem ou acréscimo de UAV (exibição de acesso não ordenado), retornando o novo valor.
ms.assetid: 1115C318-2F86-4161-AC5C-2A61A262DC28
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0244b885d9d2c46b734994d5e101f79147839d0cf76e2bab5669e52700cf59e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119310"
---
# <a name="imm_atomic_consume-sm5---asm"></a>\_consume atômico \_ do IMM (SM5-ASM)

Decrementar atomicamente o contador de 32 bits oculto armazenado com uma contagem ou acréscimo de UAV (exibição de acesso não ordenado), retornando o novo valor.



| o IMM \_ Atomic \_ consume dst0 \[ . \_ máscara de componente único \_ \] , dstUAV |
|---------------------------------------------------------------|



 



| Item                                                                                           | Descrição                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[in \] contém o valor do contador original retornado.<br/>           |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[em \] um buffer estruturado UAV com o sinalizador Count ou Append. <br/> |



 

## <a name="remarks"></a>Comentários

Consulte [a \_ \_ alocação atômica do IMM](imm-atomic-alloc--sm5---asm-.md) para obter uma discussão sobre a validade do valor da contagem retornada, dependendo se o UAV é Count ou Append. O mesmo se aplica **ao \_ \_ consumo atômico do IMM**.

o **IMM \_ Atomic \_ consume** faz um decréscimo atômico do valor do contador, retornando o novo valor para *dst0*.

Não há nenhum fixação MSS da contagem, portanto, ele encapsula em estouro negativo.

O mesmo sombreador não pode tentar a **\_ \_ alocação do IMM Atomic** e o **IMM \_ Atomic \_ consume** no mesmo UAV. Além disso, a GPU não pode permitir que várias invocações de sombreador misturem a **\_ \_ alocação atômica do IMM** e o **IMM \_ Atomic \_ consume** no mesmo UAV.

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
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





