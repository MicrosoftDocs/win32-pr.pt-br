---
title: dcl_samplerType (sm2, sm3 – ps asm)
description: Declare um exemplo de sombreador de pixel.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7a6da220e50b43ce990c090c61d1caf84afec653
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129663"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a>dcl \_ samplerType (sm2, sm3 - ps asm)

Declare um exemplo de sombreador de pixel.

## <a name="syntax"></a>Sintaxe

dcl \_ samplerType s\#



 

em que:

-   \_samplerType define o tipo de dados sampler. Isso determina quantas coordenadas são necessárias para cada coordenada de textura durante a amostragem. As dimensões de coordenada de textura a seguir são definidas.
    -   \_2d
    -   \_Cubo
    -   \_Volume
-   s identifica um exemplo em que s é uma abreviação para o \# exemplo e é o número do \# exemplo. Os exemplos são pseudo-registros porque você não pode ler ou gravar diretamente neles.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dcl \_ samplerType      |      |      |      |      | x    | x    | x     | x    | x     |



 

Todas as instruções dcl \_ samplerType devem aparecer antes da primeira instrução executável.

## <a name="example"></a>Exemplo


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




