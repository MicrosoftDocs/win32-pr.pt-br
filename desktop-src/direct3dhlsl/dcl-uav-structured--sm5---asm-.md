---
title: dcl_uav_structured (sm5 – asm)
description: Declare uma UAV (exibição de acesso não organizado) para uso por um sombreador. | dcl_uav_structured (sm5 – asm)
ms.assetid: 40D6B8F7-8A41-4EFE-A8A3-44A646B4D43B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b398dc8b59db6d8fc3a64effdf3cd93b56664881c4c7024a185ad6a212b9fb4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726794"
---
# <a name="dcl_uav_structured-sm5---asm"></a>dcl \_ uav \_ estruturado (sm5 - asm)

Declare uma UAV (exibição de acesso não organizado) para uso por um sombreador.



| dcl \_ uav \_ structured \[ \_ glc \] dstUAV, structByteStride |
|--------------------------------------------------------|



 



| Item                                                                                                                                   | Descrição                                           |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                                         | \[no \] UAV.<br/>                            |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[em \] O tamanho da estrutura em bytes.<br/> |



 

## <a name="remarks"></a>Comentários

*dstUAV* é um registro u declarado como uma referência \# a um UnorderedAccessView de um buffer estruturado com o passo especificado que deve ser vinculado ao slot UAV na \# API.

O conteúdo da estrutura não tem nenhum tipo; as operações executadas na memória podem interpretar implicitamente os dados como tendo um tipo.

*structByteStride* é o tamanho da estrutura em bytes no buffer que está sendo declarado. Esse valor deve ser maior que zero. *structByteStride* é do tipo uint e deve ser um múltiplo de 4.

As instruções que referenciam um u estruturado levam um endereço 2D, em que o primeiro componente escolhe o struct e o segundo componente escolhe o deslocamento dentro \# \[ do \] \[ struct, em bytes alinhados. \]

O \_ sinalizador glc significa "globalmente coerente". A ausência de glc significa que o UAV está sendo declarado apenas como "coerente de grupo" no sombreador de computação ou "localmente coerente" em uma invocação de sombreador de \_ pixel único.

O \_ sinalizador opc é o contador de preservação de ordem. Indica que, se um UAV estiver vinculado ao slot \# (u \# ), ele deverá ter sido criado com o sinalizador COUNTER. Isso significa que as operações [imm \_ atomic \_ alloc](imm-atomic-alloc--sm5---asm-.md) ou [imm \_ atomic \_ consume](imm-atomic-consume--sm5---asm-.md) no sombreador manipulam um contador cujos valores podem ser usados no sombreador como uma referência permanente a um local no UAV. Os dados não podem ser reordenados após o fim do sombreador.

A ausência do sinalizador opc significa que, se o sombreador usar instruções \_ [imm \_ atomic \_ alloc](imm-atomic-alloc--sm5---asm-.md) ou [imm \_ atomic \_ consume](imm-atomic-consume--sm5---asm-.md) e um UAV estiver vinculado ao slot (u), ele deverá ter sido criado com o sinalizador APPEND, que fornece um contador que não garante que a ordem seja preservada após a invocação do \# sombreador.

Se o sinalizador opc estiver ausente e o sombreador não contém instruções \_ [imm \_ atomic \_ alloc](imm-atomic-alloc--sm5---asm-.md) ou [imm \_ atomic \_ consume,](imm-atomic-consume--sm5---asm-.md) um UAV vinculado ao slot (u) terá permissão para ter sido criado com o sinalizador COUNTER (o contador não seráusado por esse sombreador), nenhum sinalizador (sem contador), mas não com o sinalizador \# APPEND.

> [!Note]  
> Cs \_ 4 \_ 0 e cs 4 1 dá suporte \_ a \_ **dcl \_ tgsm \_** estruturado, mas não [dcl \_ tgsm \_ bruto.](dcl-tgsm-raw--sm5---asm-.md)

 

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



 

> [!Note]  
> Essa instrução tem suporte nos cs \_ 4 \_ 0 e cs \_ 4 \_ 1.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





