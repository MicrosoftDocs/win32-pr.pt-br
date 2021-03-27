---
title: imm_atomic_alloc (SM5-ASM)
description: Incrementar atomicamente o contador de 32 bits oculto armazenado com uma contagem ou acréscimo de UAV (exibição de acesso não ordenado), retornando o valor original.
ms.assetid: 534FA3C3-6FAC-41DC-AC07-0E53FEED000C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28a97709629497bae9af0298789453ef1d1172b7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638877"
---
# <a name="imm_atomic_alloc-sm5---asm"></a>\_alocação atômica \_ do IMM (SM5-ASM)

Incrementar atomicamente o contador de 32 bits oculto armazenado com uma contagem ou acréscimo de UAV (exibição de acesso não ordenado), retornando o valor original.



| \_ \_ dst0 de alocação atômica do IMM \[ . \_ \_ máscara de componente único \] , dstUAV |
|-------------------------------------------------------------|



 



| Item                                                                                           | Descrição                                                               |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                | \[in \] contém o valor do contador retornado.<br/>                    |
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[em \] um buffer estruturado UAV com o sinalizador Count ou Append. <br/> |



 

## <a name="remarks"></a>Comentários

Há um valor de contador inteiro de 32 bits sem sinal oculto associado a uma exibição de buffer de contagem ou acréscimo que é inicializada quando a exibição é associada ao pipeline, incluindo a opção de manter o valor anterior.

Essa instrução faz um incremento atômico do valor do contador, retornando o original para *dst0*.

Para um UAV de acréscimo, o valor retornado é válido somente para a duração da invocação do sombreador. Depois disso, a implementação pode reorganizar o layout da memória. Qualquer endereçamento de memória com base no valor retornado deve ser limitado à invocação do sombreador.

Para um Append UAV, na invocação do sombreador, o compilador HLSL pode usar o valor retornado como o índice de struct a ser usado para acessar o buffer estruturado. Acessar qualquer índice de struct diferente daqueles locais retornados por chamada (s) para **a \_ \_ alocação atômica do IMM** ou [ \_ consumir](imm-atomic-consume--sm5---asm-.md) produzir resultados indefinidos, pois exatamente qual local de memória dentro do UAV está sendo acessado é aleatório e é corrigido somente pelo tempo de vida da invocação do sombreador.

Para um UAV de contagem, o valor retornado pode ser salvo pelo aplicativo como uma referência a um local fixo dentro do UAV que é significativo após a invocação do sombreador. Qualquer local em um UAV de contagem sempre pode ser acessado independentemente do que é o valor de contagem.

Não há nenhum fixação MSS da contagem, portanto, ele encapsula o estouro.

O mesmo sombreador não pode tentar a **\_ \_ alocação do IMM Atomic** e o **IMM \_ Atomic \_ consume** no mesmo UAV. Além disso, a GPU não pode permitir que várias invocações de sombreador misturem a **\_ \_ alocação atômica do IMM** e o **IMM \_ Atomic \_ consume** no mesmo UAV.

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

 

 





