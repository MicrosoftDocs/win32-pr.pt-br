---
title: dcl_samplerType (SM3-vs ASM)
description: Declare uma amostra de sombreador de vértice.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 556655d793e94b9290fcd1a4a40fdf7f797e80ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988614"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>\_SampleType de DCL (SM3-vs ASM)

Declare uma amostra de sombreador de vértice.

## <a name="syntax"></a>Syntax



|                      |
|----------------------|
| \_amostrador DCL s\# |



 

em que:

-   \_SampleType define o tipo de dados de amostra. Isso determina quantas coordenadas são exigidas por cada coordenada de textura durante a amostragem. As dimensões de coordenadas de textura a seguir são definidas.
    -   \_Dimensiona
    -   \_simples
    -   \_volume
-   s \# identifica um amostra em que s é uma abreviação para a amostra e \# é o número de amostra. As [amostras (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s são superregistradas porque você não pode ler ou gravar diretamente nelas.

## <a name="remarks"></a>Comentários



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| \_classificador de DCL       |      |      |      |       | x    | x     |



 

Todas as \_ instruções de SampleType de DCL devem aparecer antes da primeira instrução executável.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de vértice](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




