---
title: Sampler (Direct3D 9 asm-vs)
description: Um exemplo é um pseudo-registro de entrada para um sombreador de vértice, que é usado para identificar o estágio de amostragem. Há quatro amostras de sombreador de vértice s0 a s3. Quatro superfícies de textura podem ser lidas em uma única passagem de sombreador.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Sampler, Type (Direct3D 9 asm-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3bd822dc085243adeb97a4baaedce35b150db311ab6b98c531a3e33731635666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789076"
---
# <a name="sampler-direct3d-9-asm-vs"></a>Sampler (Direct3D 9 asm-vs)

Um exemplo é um pseudo-registro de entrada para um sombreador de vértice, que é usado para identificar o estágio de amostragem. Há quatro exemplos de sombreador de vértice: s0 a s3. Quatro superfícies de textura podem ser lidas em uma única passagem de sombreador.

Sampler (Direct3D 9 asm-vs)s são pseudo-registros porque você não pode ler ou gravar diretamente neles.

Uma unidade de amostragem corresponde ao estágio de amostragem de textura, encapsulando o estado específico da amostragem fornecido por [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate). Cada amostra identifica exclusivamente uma única superfície de textura, que é definida como o sampler correspondente usando [**o SetTexture.**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) No entanto, a mesma superfície de textura pode ser definida em vários exemplos.

Em tempo de desenho, uma textura não pode ser definida simultaneamente como um destino de renderização e uma textura em um estágio.

Como há quatro amostras, até quatro superfícies de textura podem ser lidas em uma única passagem de sombreador. Um exemplo pode aparecer como o único argumento na instrução de carregamento de textura: [texldl - vs](texldl---vs.md).

Em versus 3 0, se um exemplo for usado, ele precisará ser declarado no início do programa de sombreador usando \_ \_ a [instrução dcl \_ samplerType (sm3 - vs asm).](dcl-samplertype---vs.md)



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Exemplo                |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[Texturas de vértice \_ em \_ versus 3 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 