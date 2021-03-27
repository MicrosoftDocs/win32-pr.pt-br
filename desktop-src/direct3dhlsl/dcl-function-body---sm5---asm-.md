---
title: dcl_function_body (SM5-ASM)
description: Declare um corpo de função.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33f020748ecff270311fbbc89798d82b223b1f34
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084279"
---
# <a name="dcl_function_body-sm5---asm"></a>\_corpo da função DCL \_ (SM5-ASM)

Declare um corpo de função.



| \_corpo da função DCL \_ FB\# |
|--------------------------|



 



| Item                                                          | Descrição                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="fb_"></span><span id="FB_"></span>*FB\#*<br/> | \[no \] rótulo do local onde a função será exibida.<br/> |



 

## <a name="remarks"></a>Comentários

Essa instrução declara um corpo de função exclusivo cujo código será exibido posteriormente no programa no rótulo FB \# .

Os corpos de função são usados em declarações de tabela de funções. Para obter mais informações, [consulte \_ \_ tabela de funções DCL](dcl-function-table---sm5---asm-.md).

No sombreador envoltória e no sombreador de domínio, em que há várias fases (fase de ponto de controle, fase de bifurcação e fase de junção), todos os corpos de função (rótulo FB \# ) aparecem depois de todas as fases, em vez de serem agrupados por fase.

Não há nenhum limite para quantos corpos de função podem estar presentes.

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

 

 





