---
title: saída de dcl_usage (SM1, SM2, SM3-vs ASM)
description: Os vários tipos de registros de saída foram recolhidos em doze registros de saída (dois para cor, oito para textura, um para posição e outro para sombra e tamanho de ponto).
ms.assetid: 500ca6b3-0f8a-446e-b1b9-edc51f006ad4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9ee5f444cbf145957ad93db00160d812e75e4a624019ad9f578b5dc960e84f59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726713"
---
# <a name="dcl_usage-output-sm1-sm2-sm3---vs-asm"></a>\_saída de uso de DCL (SM1, SM2, SM3-vs ASM)

Os vários tipos de registros de saída foram recolhidos em doze registros de saída (dois para cor, oito para textura, um para posição e outro para sombra e tamanho de ponto). Eles podem ser usados para qualquer coisa que o usuário queira interpolar para o sombreador de pixel: coordenadas de textura, cores, neblina e assim por diante.

Os registros de saída exigem declarações que incluem semânticas. Por exemplo, os registros de posição antiga e de tamanho de ponto são substituídos por meio da declaração de um registro de saída com uma semântica de posição ou de tamanho de ponto.

Dos doze registros de saída, quaisquer dez (não necessariamente o0 a O9) têm quatro componentes (xyzw), outro deve ser declarado como posição (e também deve incluir todos os quatro componentes) e, opcionalmente, mais um pode ser um tamanho de ponto escalar.

## <a name="syntax"></a>Syntax

A sintaxe para declarar registros de saída é semelhante às declarações para o registro de entrada:



|                                  |
|----------------------------------|
| a semântica de DCL a \_ \[ . Write \_ Mask\] |



 

Em que:

-   a \_ semântica de DCL pode usar o mesmo conjunto de semânticas para a declaração de entrada. Os nomes semânticos vêm de [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (e são emparelhados com um índice, como position3). Sempre deve haver um registro de saída com a semântica positiont0 quando não for usado para processar vértices. A semântica positiont0 e a semântica pointsize0 são as únicas que têm significado além de simplesmente permitir a vinculação de vértice a sombreadores de pixel. Para sombreadores com controle de fluxo, supõe-se que a pior saída de caso seja declarada. Não haverá padrões se um sombreador não gerar realmente o que ele declara (devido ao controle de fluxo).
-   o é um registro de saída. Consulte [ \_ registros de saída](dx9-graphics-reference-asm-vs-registers-vs-3-0.md).
-   \_a máscara de gravação indica o mesmo registro de saída que pode ser declarado várias vezes (portanto, uma semântica diferente pode ser aplicada a componentes individuais), cada vez com uma máscara de gravação exclusiva. No entanto, a mesma semântica não pode ser usada várias vezes em uma declaração. Isso significa que os vetores devem ter quatro componentes ou menos, e não podem passar pelos limites de registro de quatro componentes (registros individuais). Quando a semântica de tamanho de ponto é usada, ela deve ter uma máscara de gravação completa porque é considerada uma escalar. Quando a semântica de posição é usada, ela deve ter uma máscara de gravação completa porque todos os quatro componentes precisam ser escritos.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 3 \_ 0 | 3 \_ SW |
|------------------------|------|-------|
| uso de DCL \_             | x    | x     |



 

Todas as instruções de [ \_ uso de DCL](dcl-usage-input-register---vs.md) devem aparecer antes da primeira instrução executável.

## <a name="declaration-examples"></a>Exemplos de declaração


```
vs_3_0
dcl_color4     o3.x    // color4 is a semantic name.
dcl_texcoord3  o3.yz   // Different semantics can be packed into one register.
dcl_fog        o3.w 
dcl_tangent    o4.xyz
dcl_position   o7.xyzw // position must be declared to some unique register 
                       //   in a vertex shader, with all 4 components.

dcl_psize      o6      // Pointsize cannot have a mask 
                       //   (that is, mask is full .xyzw)
                       // This is an implied scalar register. 
                       // No other semantics can be assigned to any components
                       //   of this register.
                       // If pointsize declaration is not used (typical),
                       //   only 11 "out" registers are available, not 12.
                       // Pixel shaders cannot see this value.

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
