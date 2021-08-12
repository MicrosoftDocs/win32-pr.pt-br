---
title: atomic_imin (sm5 – asm)
description: Número inteiro com sinal atômico mínimo para memória.
ms.assetid: C30C7CDE-1024-4E69-959E-2D3122BF9AA7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a028fbca75046373e9fda13ed52e28313310de819a308fb93cd06429796695a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287739"
---
# <a name="atomic_imin-sm5---asm"></a>atomic \_ imin (sm5 - asm)

Número inteiro com sinal atômico mínimo para memória.



| atomic \_ imin dst, dstAddress \[ .swizzle \] , src0 \[ .select \_ component\] |
|----------------------------------------------------------------------|



 



| Item                                                                                                           | Descrição                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*Dst*<br/>                                                   | \[em \] Os componentes a comparar com *src0*. Esse valor deve ser uma UAV (exibição de acesso não organizado) (u \# ). No sombreador de computação, ele também pode ser a memória compartilhada do grupo de threads (g \# ). <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[em \] O endereço de memória.<br/>                                                                                                                                                   |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[em \] Os componentes a comparar com *dst*.<br/>                                                                                                                                   |



 

## <a name="remarks"></a>Comentários

Essa instrução executa um único componente com assinatura mínima de 32 bits de *src0* de operand em *dst* a 32 bits por endereço de componente *dstAddress*, executado atomicamente.

O número de componentes retirados do endereço é determinado pela dimensionalidade *de dst* u \# ou g \# .

Se *dst* for um u \# , ele poderá ser declarado como bruto, digitado ou estruturado. Se digitado, ele deve ser declarado como UINT/SINT com o formato de recurso vinculado sendo R32 \_ \_ UINT/SINT.

Se *dst* for g \# , ele deverá ser declarado como bruto ou estruturado.

Nada é retornado para o sombreador.

Se a invocação do sombreador estiver inativa, por exemplo, se o pixel tiver sido descartado anteriormente em sua execução ou se uma invocação de pixel/amostra existir apenas para servir como auxiliar em um pixel/amostra real para derivados, essa instrução não alterará a memória *dst* (silenciosamente).

O endereçamento fora dos limites em u faz com que nada seja gravado na memória, exceto se o u estiver estruturado e o deslocamento de byte no struct (segundo componente do endereço) estiver causando o acesso fora dos limites e, em seguida, todo o conteúdo do UAV se tornará \# \# indefinido.

O endereçamento fora dos limites em g (os limites desse g específico, em vez de toda a memória compartilhada) faz com que todo o conteúdo de toda a memória compartilhada se torne \# \# indefinido.

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
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





