---
title: dcl_function_table (SM5-ASM)
description: Declare uma tabela de funções.
ms.assetid: 3693A03F-5E4B-40E8-B436-2FE3462C8DB8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549653ee7316a664b628d5cdc692c091bdf042ad24e89b983c0fd3aac8a67ba8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119490886"
---
# <a name="dcl_function_table-sm5---asm"></a>\_ \_ tabela de funções DCL (SM5-ASM)

Declare uma tabela de funções.



| \_ \_ tabela de função DCL ft \# = {FB \# , FB \# ,...} |
|-----------------------------------------------|



 



| Item                                                      | Descrição                                   |
|-----------------------------------------------------------|-----------------------------------------------|
| <span id="ft"></span><span id="FT"></span>*ft*<br/> | \[nas \] entradas da tabela de funções.<br/> |



 

## <a name="remarks"></a>Comentários

Essa função declara uma tabela de funções como um conjunto de corpos de função que foram declarados anteriormente.

Isso é como um C++ vtable, exceto que há uma entrada por site de chamada para uma interface em vez de por método.

Não há nenhum limite para quantos corpos de função podem ser listados em uma tabela de funções.

É válido para um determinado corpo de função FB \# ser referenciado várias vezes em uma ou mais tabelas de função, como um modo de compartilhar código comum.

Essa instrução se aplica aos seguintes estágios de sombreador:



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

 

 





