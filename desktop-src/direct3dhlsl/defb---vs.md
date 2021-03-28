---
title: DEFB-vs
description: Define um valor constante booliano, que deve ser carregado sempre que um sombreador for definido como um dispositivo.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bd5ef8ea4218890c025fdebc87154ca1224d33c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917329"
---
# <a name="defb---vs"></a>DEFB-vs

Define um valor constante booliano, que deve ser carregado sempre que um sombreador for definido como um dispositivo.

## <a name="syntax"></a>Syntax



| DEFB dest, boolianvalue |
|-------------------------|



 

onde

-   DST é o registro de destino.
-   boolianvalue é um valor booliano, true ou false.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| defb                   |      | x    | x    | x     | x    | x     |



 

A instrução DEFB-vs define uma constante de sombreador booliana cujo valor é carregado sempre que um sombreador é definido como um dispositivo. Elas são chamadas de constantes imediatas. Constantes imediatas têm precedência sobre constantes definidas pelo método de API SetVertexShaderConstantB.

Há duas maneiras de definir uma constante booliana em um sombreador.

1.  Use DEFB-vs para definir a constante diretamente dentro de um sombreador.
2.  Use os métodos de API para definir uma constante.
    -   Use [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) para definir uma constante booliana.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[def-vs](def---vs.md)
</dt> <dt>

[defi-vs](defi---vs.md)
</dt> </dl>

 

 