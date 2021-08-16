---
title: Modelos de sombreador versus perfis de sombreador
description: Modelos de sombreador versus perfis de sombreador
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d7f6a37b1d37225425a60cc42887d5e587d9522929bc78a28dbb5bf5854493f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726146"
---
# <a name="shader-models-vs-shader-profiles"></a>Modelos de sombreador versus perfis de sombreador

A Linguagem de Sombreamento de Alto Nível para DirectX implementa uma série de modelos de sombreador. Usando HLSL, você pode criar sombreadores programáveis do tipo C para o pipeline do Direct3D. Cada modelo de sombreador se baseia nos recursos do modelo antes dele, implementando mais funcionalidades com menos restrições.

O modelo 1 do sombreador começou com o DirectX 8 e incluiu instruções do tipo C e nível de assembly. Esse modelo tem muitas limitações causadas pelo hardware de sombreador programável antecipado. Os modelos de sombreador 2 e 3 foram muito expandidos no número de instruções e os sombreadores de constantes podem usar. Eles são muito mais poderosos do que o modelo de sombreador 1, mas ainda têm algumas das limitações existentes do primeiro modelo de sombreador.

Começando com Windows Vista, o modelo de sombreador 4 é uma reformulação completa. Ele permite instruções e constantes ilimitadas (dentro de restrições de hardware de seu computador), tem objetos modelados para tornar a amostragem de textura mais limpa e eficiente e tem as menores restrições de qualquer modelo de sombreador. No entanto, ele requer o Windows driver de aplicativo que só está disponível no sistema operacional Windows Vista (ou posterior).

## <a name="shader-profiles"></a>Perfis do sombreador

Um perfil de sombreador é o destino para compilar um sombreador; esta tabela lista os perfis de sombreador com suporte em cada modelo de sombreador.



| Modelo de sombreador                                                   | Perfis do sombreador                                                                                                                                                                                                                                                                                                      |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Modelo de sombreador 1](dx-graphics-hlsl-sm1.md)         | vs \_ 1 \_ 1                                                                                                                                                                                                                                                                                              |
| [Modelo de sombreador 2](dx-graphics-hlsl-sm2.md)         | ps \_ 2 \_ 0, \_ ps 2 \_ x, vs \_ \_ 2 0, vs \_ 2 \_ x, ps \_ 4 \_ 0 nível \_ \_ 9 \_ 0, ps \_ 4 \_ 0 nível \_ \_ 9 \_ 1, ps \_ 4 \_ 0 nível \_ \_ 9 3, vs \_ \_ 4 \_ 0 nível \_ \_ 9 0, vs \_ \_ 4 \_ 0 nível \_ \_ 9 1, vs \_ 4 0 nível \_ \_ \_ \_ \_ 9 3, lib \_ 4 \_ 0 nível \_ \_ 9 \_ 1, lib \_ 4 \_ 0 nível \_ \_ 9 \_ 3                                                                      |
| [Modelo de sombreador 3](dx-graphics-hlsl-sm3.md)         | ps \_ 3 \_ 0, vs \_ 3 \_ 0                                                                                                                                                                                                                                                                                    |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)         | cs \_ 4 \_ 0, gs \_ 4 \_ 0, ps \_ 4 \_ 0, \_ vs 4 \_ 0, cs \_ 4 \_ 1, gs \_ 4 \_ 1, ps \_ 4 \_ 1, \_ vs 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1                                                                                                                                                                                                  |
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) | cs \_ 5 \_ 0, ds \_ 5 \_ 0, gs \_ 5 \_ 0, hs \_ 5 \_ 0, ps \_ 5 \_ 0, \_ vs 5 \_ 0, lib \_ 5 \_ 0 (embora gs \_ 4 \_ 0, gs \_ 4 \_ 1, ps \_ 4 \_ 0, ps 4 1, vs 4 0 \_ \_ \_ \_ \_ \_ e vs 4 1 tenham sido introduzidos no modelo de sombreador 4.0, o modelo de sombreador 5 adiciona suporte a esses perfis de sombreador para buffers estruturados e buffers de endereço de byte.)<br/> |
| [Modelo de sombreador 6](shader-model-6-0.md)             | cs \_ 6 \_ 0, ds \_ 6 \_ 0, gs \_ 6 \_ 0, hs \_ 6 \_ 0, ps \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0                                                                                                                                                                                                                                 |

Diferenças entre o Direct3D 9 e o Direct3D 10:

- O Direct3D 9 introduziu os modelos de sombreador 1, 2 e 3.
- O Direct3D 10 introduziu o modelo de sombreador 4.
- O Direct3D 10.1 introduziu o modelo de sombreador 4.1.



 

## <a name="effect-profiles"></a>Perfis de efeito

Um perfil de efeito é o destino para compilar um efeito/sombreador; esta tabela lista os perfis de efeito que têm suporte em cada versão do Direct3D.

Diferenças entre o Direct3D 9 e o Direct3D 10:

- O Direct3D 9 introduziu perfis de estrutura de efeito fx \_ \_ 1 0 e fx \_ 2 \_ 0.
- O Direct3D 10 introduziu o perfil de estrutura de efeito fx \_ 4 \_ 0.
- O Direct3D 10.1 introduziu o perfil de estrutura de efeito fx \_ 4 \_ 1.
- O Direct3D 11 introduziu o perfil de estrutura de efeito fx \_ 5 \_ 0.

> [!Note]  
> Esses perfis de efeitos herdados foram preterido.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência para HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





