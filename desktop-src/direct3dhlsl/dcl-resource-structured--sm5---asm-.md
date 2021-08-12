---
title: dcl_resource estruturada (sm5 – asm)
description: Declare uma entrada de recurso de sombreador e atribua-a a um t\ – um registro de espaço reservado para o recurso. | dcl_resource estruturada (sm5 – asm)
ms.assetid: 87FC8A56-9DB2-424B-889C-2AB59885DA13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79ec0bc0b818b345c62bb48ae6f5db68671127110ed06a85c988f8a0449fd490
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285889"
---
# <a name="dcl_resource-structured-sm5---asm"></a>dcl \_ resource structured (sm5 - asm)

Declare uma entrada de recurso de sombreador e atribua-a a um t \# – um registro de espaço reservado para o recurso.



| dcl \_ resource \_ structured dstSRV, structByteStride |
|----------------------------------------------------|



 



| Item                                                                                                                                   | Descrição                                                                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dstSRV"></span><span id="dstsrv"></span><span id="DSTSRV"></span>*dstSRV*<br/>                                         | \[em Um registro t declarado como uma referência \] \# a um ShaderResourceView de um buffer estruturado com o passo especificado que deve ser vinculado ao slot SRV na \# API. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[em \] Um uint que especifica o tamanho da estrutura em bytes no buffer que está sendo declarado. Esse valor deve ser maior que zero.<br/>                                   |



 

## <a name="remarks"></a>Comentários

O conteúdo da estrutura não tem nenhum tipo; as operações executadas na memória podem interpretar implicitamente os dados como tendo um tipo.

As instruções que referenciam um t estruturado usam um endereço 2D, em que o primeiro componente escolhe o struct e o segundo componente escolhe o deslocamento dentro do struct, vários de \# \[ \] \[ 32 \] bits.

Cs \_ 4 \_ 0 e cs \_ 4 \_ 1 são suportados por essa instrução.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





