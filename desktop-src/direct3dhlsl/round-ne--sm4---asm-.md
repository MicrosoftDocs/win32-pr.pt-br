---
title: round_ne (sm4 – asm)
description: Float de ponto flutuante para float integral. | round_ne (sm4 – asm)
ms.assetid: 2D1A0786-F7DB-4D69-9F56-82ECD1EE7ABA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fe7088d9a6b577366fdaf169e21075188597ad4b761bb6fd3c555c809e91c41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853656"
---
# <a name="round_ne-sm4---asm"></a>round \_ ne (sm4 - asm)

Float de ponto flutuante para float integral.



| round \_ ne \[ \_ sat \] dest \[ .mask , \] \[ - \] src0 \[ \_ abs \] \[ .swizzle\] |
|------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O endereço dos resultados da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] Os componentes na operação.<br/>             |



 

## <a name="remarks"></a>Comentários

Essa instrução executa uma rodada de ponto flutuante por componente dos valores em *src0,* escrevendo valores integrais de ponto flutuante para *dest.* **\_ arredonda ne** arredonda para a mais próxima.

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.

F significa número finito real.



| **src**  | **-inf** | **-F** | **-denorm** | **-0** | **+0** | **+denorm** | **+F** | **+inf** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **Dest** | -inf     | -F     | -0          | -0     | +0     | +0          | +F     | +inf     | NaN     |



 

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





