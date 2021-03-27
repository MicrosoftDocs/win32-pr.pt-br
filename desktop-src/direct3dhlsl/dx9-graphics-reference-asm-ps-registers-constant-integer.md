---
title: Registro de inteiro constante (referência do HLSL PS)
description: Os registros inteiros constantes são usados somente por loop-PS e Rep-PS.
ms.assetid: 85720ec0-b6aa-4a24-910c-3ad0468300dc
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9b03a27a95f84ae30a70147caaf5662e1949cf18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104967201"
---
# <a name="constant-integer-register-hlsl-ps-reference"></a>Registro de inteiro constante (referência do HLSL PS)

Os registros inteiros constantes são usados somente por [loop-PS](loop---ps.md) e [Rep-PS](rep---ps.md).

Eles podem ser definidos usando [defi-PS](defi---ps.md) ou [**SetPixelShaderConstantI**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti).

Quando usado como um argumento para a instrução do [loop-PS](loop---ps.md) :

-   . x é a contagem de iteração. (o[Rep-PS](rep---ps.md) usa apenas este componente).
-   . y é o valor inicial para o contador de loop.
-   . z é a etapa de incremento para o contador de loop.



| Versões do sombreador de pixel     | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|---------------------------|------|------|------|------|------|-------|------|------|-------|
| Registro de inteiro constante |      |      |      |      |      |       | x    | x    | x     |



 

O comportamento das constantes do sombreador foi alterado entre o Direct3D 8 e o Direct3D 9.

-   Para o Direct3D 9, as constantes definidas com defx atribuem valores ao espaço constante do sombreador. O tempo de vida de uma constante declarada com defx é restrito apenas à execução desse sombreador. Por outro lado, as constantes definidas usando as APIs SetXXXShaderConstantX inicializam constantes no espaço global. As constantes no espaço global não são copiadas para o espaço local (visível para o sombreador) até que SetxxxShaderConstants seja chamado.
-   Para o Direct3D 8, as constantes definidas com defx ou as APIs atribuem valores ao espaço constante do sombreador. Cada vez que o sombreador é executado, as constantes são usadas pelo sombreador atual, independentemente da técnica usada para defini-los.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 