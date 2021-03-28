---
title: dcl_uav_structured (SM5-ASM)
description: Declare um UAV (modo de exibição de acesso não ordenado) para uso por um sombreador. | dcl_uav_structured (SM5-ASM)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dc02396f4837a095506e736d81ea8c00eb0669f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172698"
---
# <a name="dcl_uav_structured-sm5---asm"></a>DCL \_ UAV \_ estruturado (SM5-ASM)

Declare um UAV (modo de exibição de acesso não ordenado) para uso por um sombreador.



| \_UAV \_ estruturada \[ \_ de DCL GLC \] dstUAV, structByteStride |
|--------------------------------------------------------|



 



| Item                                                                                                                                   | Descrição                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                                         | \[no \] UAV.<br/>                            |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[no \] tamanho da estrutura em bytes.<br/> |



 

## <a name="remarks"></a>Comentários

*dstUAV* é um \# registro u declarado como uma referência a um UnorderedAccessView de um buffer estruturado com o stride especificado que deve ser associado ao slot UAV \# na API.

O conteúdo da estrutura não tem tipo; as operações executadas na memória podem interpretar implicitamente os dados como tendo um tipo.

*structByteStride* é o tamanho da estrutura em bytes no buffer que está sendo declarado. Esse valor deve ser maior que zero. *structByteStride* é do tipo uint e deve ser um múltiplo de 4.

Instruções que fazem referência a um u estruturado \# usam um endereço 2D, em que o primeiro componente escolhe \[ struct \] e o segundo componente escolhe o \[ deslocamento dentro de struct, em bytes alinhados \] .

O \_ sinalizador GLC significa "globalmente coerente". A ausência de \_ GLC significa que o UAV está sendo declarado somente como "grupo coerente" no sombreador de computação ou "coerente localmente" em uma invocação de sombreador de pixel único.

O \_ sinalizador OPC é o contador de preservação de ordem. Isso indica que, se um UAV estiver associado ao slot \# (u \# ), ele deverá ter sido criado com o sinalizador Counter. Isso significa que as operações do [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) ou do [IMM \_ Atomic \_ consume](imm-atomic-consume--sm5---asm-.md) no sombreador manipulam um contador cujos valores podem ser usados no sombreador como uma referência permanente a um local no UAV. Os dados não podem ser reordenados depois que o sombreador terminar.

A ausência do \_ sinalizador OPC significa que se o sombreador usar as instruções de[ \_ \_ alocação atômica do IMM](imm-atomic-alloc--sm5---asm-.md) ou de [ \_ \_ consumo do IMM Atomic](imm-atomic-consume--sm5---asm-.md) e um UAV estiver associado ao slot \# (u), ele deverá ter sido criado com o sinalizador Append, que fornece um contador que não garante que a ordem seja preservada após a invocação do sombreador.

Se o \_ sinalizador OPC estiver ausente e o sombreador não contiver as instruções de contêiner [IMM \_ Atomic \_ Alloc](imm-atomic-alloc--sm5---asm-.md) ou [IMM \_ Atomic \_ consume](imm-atomic-consume--sm5---asm-.md) , um UAV associado ao slot \# (u) poderá ter sido criado com o sinalizador Counter (o contador não será usado por este sombreador), sem sinalizador (nenhum contador), mas não com o sinalizador Append.

> [!Note]  
> o cs \_ 4 \_ 0 e o cs \_ 4 \_ 1 dão suporte ao **\_ tgsm DCL \_ estruturado**, mas não ao [DCL \_ tgsm \_ RAW](dcl-tgsm-raw--sm5---asm-.md).

 

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



 

> [!Note]  
> Essa instrução tem suporte em cs \_ 4 \_ 0 e cs \_ 4 \_ 1.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





