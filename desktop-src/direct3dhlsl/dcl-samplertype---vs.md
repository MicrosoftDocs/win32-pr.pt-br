---
title: dcl_samplerType (sm3 – vs asm)
description: Declare um exemplo de sombreador de vértice.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2fbcb934ad591274d743f09c810de2db42278261
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129864"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>dcl \_ samplerType (sm3 – vs asm)

Declare um exemplo de sombreador de vértice.

## <a name="syntax"></a>Sintaxe

dcl \_ samplerType s\#



 

em que:

-   \_samplerType define o tipo de dados sampler. Isso determina quantas coordenadas são necessárias para cada coordenada de textura durante a amostragem. As dimensões de coordenada de textura a seguir são definidas.
    -   \_2d
    -   \_Cubo
    -   \_Volume
-   s identifica um exemplo em que s é uma abreviação para o \# exemplo e é o número do \# exemplo. [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s são pseudo-registros porque você não pode ler ou gravar diretamente neles.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dcl \_ samplerType       |      |      |      |       | x    | x     |



 

Todas as instruções dcl \_ samplerType devem aparecer antes da primeira instrução executável.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




