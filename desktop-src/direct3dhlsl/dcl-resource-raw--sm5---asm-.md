---
title: dcl_resource bruto (SM5-ASM)
description: Declare uma entrada de recurso de sombreador e atribua-a a um t \-um registro de espaço reservado para o recurso. | dcl_resource bruto (SM5-ASM)
ms.assetid: ECBA9DAB-F217-47FB-9588-F35866004E72
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8dd6ccc5990e34990772a072086d9e080cde67b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172732"
---
# <a name="dcl_resource-raw-sm5---asm"></a>\_recurso DCL bruto (SM5-ASM)

Declare uma entrada de recurso de sombreador e atribua-a a um \# registro de espaço reservado t-a para o recurso.



| \_dstSRV de recursos \_ brutos de DCL |
|---------------------------|



 



| Item                                                                                           | Descrição                                                                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/> | \[em \] um \# registro t declarado como uma referência a um ShaderResourceView de um buffer bruto.<br/> |



 

## <a name="remarks"></a>Comentários

O conteúdo da estrutura não tem tipo; as operações executadas na memória podem interpretar implicitamente os dados como tendo um tipo.

Instruções que fazem referência a um t bruto \# usam um endereço 1D, um valor de 32 bits sem sinal especificando o deslocamento de byte para um local alinhado de 32 bits no buffer. O endereço deve ser um múltiplo de 4 (bytes).

Exibições associadas a t \# declaradas como RAW devem ter RAW especificado em sua criação; caso contrário, o comportamento quando acessado de um sombreador é indefinido.

cs \_ 4 \_ 0 e cs \_ 4 \_ 1 dão suporte a essa instrução.

Essa instrução se aplica aos seguintes estágios de sombreador:



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

 

 





