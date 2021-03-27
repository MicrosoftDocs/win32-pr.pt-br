---
title: Modelos de sombreador vs. perfis de sombreador
description: Modelos de sombreador vs. perfis de sombreador
ms.assetid: 6224f05e-20b1-42ea-96fb-63dd0edb720e
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93a8d5c02662bff285c13461e8d716b03b8553b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822898"
---
# <a name="shader-models-vs-shader-profiles"></a>Modelos de sombreador vs. perfis de sombreador

A linguagem de sombreamento de alto nível do DirectX implementa uma série de modelos de sombreador. Usando o HLSL, você pode criar sombreadores programáveis C para o pipeline do Direct3D. Cada modelo de sombreador se baseia nos recursos do modelo antes dele, implementando mais funcionalidade com menos restrições.

O modelo de sombreador 1 foi iniciado com DirectX 8 e instruções do tipo assembly e C-like incluídas. Esse modelo tem muitas limitações causadas pelo hardware de sombreador programável antecipado. O Shader Model 2 e 3 expandiu muito o número de instruções e os sombreadores constantes podem usar. Eles são muito mais eficientes do que o Shader Model 1, mas ainda têm algumas das limitações existentes do primeiro modelo de sombreador.

A partir do Windows Vista, o Shader Model 4 é uma reformulação completa. Ele permite instruções e constantes ilimitadas (dentro das restrições de hardware da sua máquina), tem objetos modelados para tornar a amostragem de textura mais limpa e mais eficiente e tem as menores restrições de qualquer modelo de sombreador. No entanto, ele requer o Windows Driver Model que só está disponível no sistema operacional Windows Vista (ou posterior).

## <a name="shader-profiles"></a>Perfis de sombreador

Um perfil de sombreador é o destino para a compilação de um sombreador; Esta tabela lista os perfis de sombreador que têm suporte em cada modelo de sombreador.



|                                                    |                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Modelo de Sombreador                                       | Perfis de sombreador                                                                                                                                                                                                                                                                                       |
| [Modelo de sombreador 1](dx-graphics-hlsl-sm1.md)         | vs \_ 1 \_ 1                                                                                                                                                                                                                                                                                              |
| [Modelo de sombreador 2](dx-graphics-hlsl-sm2.md)         | PS \_ 2 \_ 0, PS \_ 2 \_ x, vs \_ 2 \_ 0, vs \_ 2 \_ x, PS \_ 4 \_ 0 \_ nível \_ 9 0 \_ , PS \_ 4 \_ 0 \_ nível \_ 9 \_ 1, PS \_ 4 \_ 0 \_ nível \_ 9 \_ 3, vs \_ 4 \_ 0 \_ nível \_ 9 \_ 0, vs \_ 4 \_ 0 \_ nível \_ 9 \_ 1, vs \_ 4 \_ 0 \_ nível \_ 9 \_ 3, lib \_ 4 \_ 0 \_ nível \_ 9 \_ 1, lib \_ 4 \_ 0 \_ nível \_ 9 \_ 3                                                                      |
| [Modelo de sombreador 3](dx-graphics-hlsl-sm3.md)         | PS \_ 3 \_ 0, vs \_ 3 \_ 0                                                                                                                                                                                                                                                                                    |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)         | cs \_ 4 \_ 0, GS \_ 4 \_ 0, PS \_ 4 \_ 0, vs \_ 4 \_ 0, cs \_ 4 \_ 1, GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1, lib \_ 4 \_ 0, lib \_ 4 \_ 1                                                                                                                                                                                                  |
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) | cs \_ 5 \_ 0, DS \_ 5 0 \_ , GS \_ 5 \_ 0, HS \_ 5 \_ 0, PS \_ 5 \_ 0, vs \_ 5 \_ 0, lib \_ 5 \_ 0 (embora GS \_ 4 \_ 0, GS \_ 4 \_ 1, PS \_ 4 \_ 0, PS \_ 4 \_ 1, vs \_ 4 \_ 0 e vs \_ 4 \_ 1 foram introduzidos no Shader Model 4,0, o Shader Model 5 adiciona suporte a esses perfis de sombreador para buffers estruturados e buffers de endereço de byte<br/> |
| [Modelo do sombreador 6](shader-model-6-0.md)             | cs \_ 6 \_ 0, DS \_ 6 \_ 0, GS \_ 6 \_ 0, HS \_ 6 \_ 0, PS \_ 6 \_ 0, vs \_ 6 \_ 0, lib \_ 6 \_ 0                                                                                                                                                                                                                                 |



 



|                                                                                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D 9 e o Direct3D 10:<br/> O Direct3D 9 introduziu os modelos de sombreador 1, 2 e 3.<br/> O Direct3D 10 introduziu o modelo de sombreador 4.<br/> O Direct3D 10,1 introduziu o modelo de sombreador 4,1.<br/> |



 

## <a name="effect-profiles"></a>Perfis de efeito

Um perfil de efeito é o destino da compilação de um efeito/sombreador; Esta tabela lista os perfis de efeito que são suportados por cada versão do Direct3D.



|                                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Diferenças entre o Direct3D 9 e o Direct3D 10:<br/> O Direct3D 9 introduziu os perfis de estrutura de efeito FX \_ 1 \_ 0 e FX \_ 2 \_ 0.<br/> O Direct3D 10 introduziu o perfil de estrutura de efeito FX \_ 4 \_ 0.<br/> O Direct3D 10,1 introduziu o perfil de estrutura de efeito FX \_ 4 \_ 1.<br/> O Direct3D 11 introduziu o perfil de estrutura de efeito FX \_ 5 \_ 0.<br/> |



 

> [!Note]  
> Esses perfis de efeitos herdados são preteridos.

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência para HLSL](dx-graphics-hlsl-reference.md)
</dt> </dl>

 

 





