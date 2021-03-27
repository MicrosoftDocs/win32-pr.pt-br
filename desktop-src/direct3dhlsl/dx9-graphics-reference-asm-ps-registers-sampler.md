---
title: Amostra (Direct3D 9 ASM-PS)
description: Um amostra é um pseudo registro de entrada para um sombreador de pixel, que é usado para identificar o estágio de amostragem.
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- Amostra, tipo (Direct3D 9 ASM-PS)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77875eed0827ad6bcb6d89111b13b6a31232dd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007726"
---
# <a name="sampler-direct3d-9-asm-ps"></a>Amostra (Direct3D 9 ASM-PS)

Um amostra é um pseudo registro de entrada para um sombreador de pixel, que é usado para identificar o estágio de amostragem. Existem registros de estágio de amostragem de sombreador de 16 pixels: S0 para S15. Portanto, até 16 superfícies de textura podem ser lidas em uma única passagem de sombreador. As instruções que usam um registro de amostra são texld e texldp.

A amostra deve ser declarada antes do uso com a instrução [DCL \_ SampleType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Exemplo               |      |      |      |      | x    | x     | x    | x    | x     |



 

Os exemplos são pseudo-registros porque você não pode ler ou gravar diretamente neles.

Uma unidade de amostragem corresponde ao estágio de amostragem de textura, encapsulando o estado específico de amostragem fornecido por [**Setsamplestate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate). Cada amostra identifica exclusivamente uma única superfície de textura, que é definida para a amostra correspondente usando [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). No entanto, a mesma superfície de textura pode ser definida em vários exemplos.

No momento do desenho, uma textura não pode ser definida simultaneamente como um destino de renderização e uma textura em um estágio.

Um amostra pode aparecer como o único argumento na instrução de carga de textura: [texldl-PS](texldl---ps.md).

No PS \_ 3 \_ 0, se um amostra for usado, ele precisará ser declarado no início do programa de sombreador usando a instrução [DCL \_ SampleType (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) .

A amostragem de uma textura com uma dimensão superior à do presente nas coordenadas de textura é inválida. A amostragem de uma textura com uma dimensão menor do que a presente nas coordenadas de textura ignorará as coordenadas de textura extra.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 