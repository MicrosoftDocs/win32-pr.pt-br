---
title: Amostra (Direct3D 9 ASM-vs)
description: Um amostra é um pseudo registro de entrada para um sombreador de vértice, que é usado para identificar o estágio de amostragem. Há quatro exemplos de sombreadores de vértice S0 para S3. Quatro superfícies de textura podem ser lidas em uma única passagem de sombreador.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Amostra, tipo (Direct3D 9 ASM-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 685f261da9d56dc29c0632d01cabbf29cd13a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366653"
---
# <a name="sampler-direct3d-9-asm-vs"></a>Amostra (Direct3D 9 ASM-vs)

Um amostra é um pseudo registro de entrada para um sombreador de vértice, que é usado para identificar o estágio de amostragem. Há quatro exemplos de sombreador de vértice: S0 para S3. Quatro superfícies de textura podem ser lidas em uma única passagem de sombreador.

As amostras (Direct3D 9 ASM-vs) s são superregistradas porque você não pode ler ou gravar diretamente nelas.

Uma unidade de amostragem corresponde ao estágio de amostragem de textura, encapsulando o estado específico de amostragem fornecido por [**Setsamplestate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate). Cada amostra identifica exclusivamente uma única superfície de textura, que é definida para a amostra correspondente usando [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture). No entanto, a mesma superfície de textura pode ser definida em vários exemplos.

No momento do desenho, uma textura não pode ser definida simultaneamente como um destino de renderização e uma textura em um estágio.

Como há quatro amostras, até quatro superfícies de textura podem ser lidas em uma única passagem de sombreador. Um amostra pode aparecer como o único argumento na instrução de carga de textura: [texldl-vs](texldl---vs.md).

No vs \_ 3 \_ 0, se um amostra for usado, ele precisará ser declarado no início do programa de sombreador usando a instrução [DCL \_ SampleType (SM3-vs ASM)](dcl-samplertype---vs.md) .



| Versões do sombreador de vértice | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Exemplo                |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[Texturas de vértice no vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 