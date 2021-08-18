---
title: def – vs
description: Define constantes do sombreador de vértice.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3e5e3d5cbeb4d60f7beffd70c30ba0775863a9782cfb365a4d40bdf5552a186f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855346"
---
# <a name="def---vs"></a>def – vs

Define constantes do sombreador de vértice.

## <a name="syntax"></a>Syntax



| def dst, float1, float2, float3, float4 |
|-----------------------------------------|



 

onde

-   dst é o registro de destino.
-   float1, float2, float3, float4 são quatro números de ponto flutuante.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| def                    | x    | x    | x    | x     | x    | x     |



 

A instrução def define uma constante de sombreador cujo valor é carregado sempre que um sombreador é definido como um dispositivo. Elas são chamadas constantes imediatas. Constantes imediatas têm precedência sobre constantes definidas pelos métodos de API SetVertexShaderConstantF.

Há duas maneiras de definir uma constante em um sombreador.

1.  Use def – vs para definir a constante diretamente dentro de um sombreador.

    def - vs só pode definir constantes de ponto flutuante.

2.  Use os métodos de API para definir uma constante.
    -   Use [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) para definir uma constante de ponto flutuante.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[defi – vs](defi---vs.md)
</dt> <dt>

[defb – vs](defb---vs.md)
</dt> </dl>

 

 