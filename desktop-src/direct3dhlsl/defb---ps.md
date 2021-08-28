---
title: DEFB-PS
description: Define um valor constante booliano, que deve ser carregado sempre que um sombreador for definido como um dispositivo.
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1ad823cd9932e98f919764e57666549189623986eb173ba6b4ef74cdade21f33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855352"
---
# <a name="defb---ps"></a>DEFB-PS

Define um valor constante booliano, que deve ser carregado sempre que um sombreador for definido como um dispositivo.

## <a name="syntax"></a>Syntax



| DEFB dest, boolianvalue |
|-------------------------|



 

onde

-   DST é o registro de destino.
-   boolianvalue é um único valor booliano, true ou false.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| defb                  |      |      |      |      |      | x    | x     | x    | x     |



 

A instrução DEFB define uma constante de sombreador booliana cujo valor é carregado sempre que um sombreador é definido como um dispositivo. Elas são chamadas de constantes imediatas. Constantes imediatas têm precedência sobre constantes definidas pelo método de API SetPixelShaderConstantB.

Há duas maneiras de definir um booleanconstant em um sombreador.

1.  Use DEFB para definir a constante diretamente dentro de um sombreador.
2.  Use os métodos de API para definir uma constante.
    -   Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) para definir uma constante booliana.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[def-PS](def---ps.md)
</dt> <dt>

[defi-PS](defi---ps.md)
</dt> </dl>

 

 