---
title: Registro de inteiro constante (referência de HLSL VS)
description: Os registros inteiros constantes são usados somente por loop-vs e Rep-vs.
ms.assetid: da9916d4-655b-4c98-99a4-1abfa66459b5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4cf2612eccb891ce0cffd04955e4997173e84007
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967206"
---
# <a name="constant-integer-register-hlsl-vs-reference"></a>Registro de inteiro constante (referência de HLSL VS)

Os registros inteiros constantes são usados somente por [loop-vs](loop---vs.md) e [Rep-vs](rep---vs.md).

Eles podem ser definidos usando [defi-vs](defi---vs.md) ou [**SetVertexShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti).

Quando usado como um argumento para a instrução [loop-vs](loop---vs.md) :

-   . x é a contagem de iteração. ([Rep-vs](rep---vs.md) usa apenas este componente).
-   . y é o valor inicial para o contador de loop.
-   . z é a etapa de incremento para o contador de loop.

O comportamento das constantes do sombreador foi alterado entre o Direct3D 8 e o Direct3D 9.

-   Para o Direct3D 9, as constantes definidas com defx atribuem valores ao espaço constante do sombreador. O tempo de vida de uma constante declarada com defx é restrito apenas à execução desse sombreador. Por outro lado, as constantes definidas usando as APIs SetXXXShaderConstantX inicializam constantes no espaço global. As constantes no espaço global não são copiadas para o espaço local (visível para o sombreador) até que SetxxxShaderConstants seja chamado.
-   Para o Direct3D 8, as constantes definidas com defx ou as APIs atribuem valores ao espaço constante do sombreador. Cada vez que o sombreador é executado, as constantes são usadas pelo sombreador atual, independentemente da técnica usada para defini-los.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Registros de sombreador de vértice](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 