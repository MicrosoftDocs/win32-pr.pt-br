---
title: dcl_immediateConstantBuffer (sm4 – asm)
description: dcl \_ immediateConstantBuffer (sm4 - asm)
ms.assetid: 55e21ab1-0749-4200-8e68-bb098e935dac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 781a792257b23a3d89cfa432ccc1ead9e5d756159beb428defc3404ba32df47c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024796"
---
# <a name="dcl_immediateconstantbuffer-sm4---asm"></a>dcl \_ immediateConstantBuffer (sm4 - asm)

Declara um buffer de constante imediata do sombreador.



| dcl \_ immediateConstantBuffer *value(s)* |
|-----------------------------------------|



 

<dl> <dt>

<span id="value_s_"></span><span id="VALUE_S_"></span>*value(s)*
</dt> <dd>

\[em \] O buffer deve conter pelo menos um valor, mas não mais de 4096 valores.

</dd> </dl>

### <a name="remarks"></a>Comentários

Um sombreador tem permissão para um buffer de constante imediata. Um buffer constante imediato é acessado como um buffer constante com indexação dinâmica.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Essa instrução é incluída para auxiliar na depuração de um sombreador no assembly; não é possível autor de um sombreador na linguagem de assembly usando o Modelo de Sombreador 4.

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

 

 




