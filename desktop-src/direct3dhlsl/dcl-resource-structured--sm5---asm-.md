---
title: dcl_resource estruturado (SM5-ASM)
description: Declare uma entrada de recurso de sombreador e atribua-a a um t \-um registro de espaço reservado para o recurso. | dcl_resource estruturado (SM5-ASM)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ab993e0cb260529c3419210c33f5d735a625bce
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172669"
---
# <a name="dcl_resource-structured-sm5---asm"></a>\_recurso DCL estruturado (SM5-ASM)

Declare uma entrada de recurso de sombreador e atribua-a a um \# registro de espaço reservado t-a para o recurso.



| \_recurso DCL \_ estruturado DstSRV, structByteStride |
|----------------------------------------------------|



 



| Item                                                                                                                                   | Descrição                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/>                                         | \[em \] um \# registro t declarado como uma referência a um ShaderResourceView de um buffer estruturado com o stride especificado que deve ser associado ao slot SRV \# na API. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[em \] um UINT que especifica o tamanho da estrutura em bytes no buffer que está sendo declarado. Esse valor deve ser maior que zero.<br/>                                   |



 

## <a name="remarks"></a>Comentários

O conteúdo da estrutura não tem tipo; as operações executadas na memória podem interpretar implicitamente os dados como tendo um tipo.

Instruções que fazem referência a um t estruturado \# usam um endereço 2D, em que o primeiro componente escolhe \[ struct \] e o segundo componente escolhe o \[ deslocamento dentro de struct, vários de 32 bits \] .

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

 

 





