---
title: Registro de inteiro constante (referência vs HLSL)
description: Registros inteiros constantes são usados apenas por loop - vs e rep - vs.
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b46390303b2ee3aae2243f25d2a5a76385b9e9dd275c2952e8aa93e18f999e9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119949896"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a>Registro de inteiro constante (referência vs HLSL)

Registros inteiros constantes são usados apenas [por loop - vs](loop---vs.md) e rep - [vs](rep---vs.md).

Eles podem ser definidos [usando defi – vs](defi---vs.md) ou [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).

Quando usado como um argumento para o [loop – vs](loop---vs.md) instrução:

-   .x é a contagem de iteração. ([rep – vs](rep---vs.md) usa apenas este componente).
-   .y é o valor inicial do contador de loop.
-   .z é a etapa de incremento para o contador de loops.

O comportamento das constantes do sombreador foi alterado entre o Direct3D 8 e o Direct3D 9.

-   Para Direct3D 9, constantes definidas com defx atribuem valores ao espaço constante do sombreador. O tempo de vida de uma constante declarada com defx é limitado apenas à execução desse sombreador. Por outro lado, as constantes definidas usando as APIs SetXXXShaderConstantX inicializam constantes no espaço global. As constantes no espaço global não são copiadas para o espaço local (visível para o sombreador) até que SetxxxShaderConstants seja chamado.
-   Para o Direct3D 8, as constantes definidas com defx ou as APIs atribuem valores ao espaço constante do sombreador. Sempre que o sombreador é executado, as constantes são usadas pelo sombreador atual, independentemente da técnica usada para defini-las.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 