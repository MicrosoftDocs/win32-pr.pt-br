---
title: dcl_function_body (sm5 – asm)
description: Declare um corpo de função.
ms.assetid: 3A651107-BEA6-4D79-938F-8E0243C874C3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339e7f5d7edb91f4f3405b328286a9ae32a8108efdaafaba1f212870be7ff8b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117727230"
---
# <a name="dcl_function_body-sm5---asm"></a>corpo da função dcl \_ \_ (sm5 – asm)

Declare um corpo de função.



| dcl \_ function \_ body fb\# |
|--------------------------|



 



| Item                                                          | Descrição                                                              |
|---------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="fb_"></span><span id="FB_"></span>*Fb\#*<br/> | \[em \] O rótulo do local em que a função será exibida.<br/> |



 

## <a name="remarks"></a>Comentários

Essa instrução declara um corpo de função exclusivo cujo código será exibido posteriormente no programa no rótulo fb \# .

Os corpos de função são usados em declarações da tabela de funções. Para obter mais informações, consulte [tabela de funções \_ \_ dcl](dcl-function-table---sm5---asm-.md).

No sombreador de chassi e sombreador de domínio, em que há várias fases (fase do ponto de controle, fase de bifurcação e fase de junção), todos os corpos de função (rótulo fb ) aparecem após todas as fases, em vez de serem \# agrupados por fase.

Não há limite para quantos corpos de função podem estar presentes.

Essa instrução se aplica aos seguintes estágios do sombreador:



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

 

 





