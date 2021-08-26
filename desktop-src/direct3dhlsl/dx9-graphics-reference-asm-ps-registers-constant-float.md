---
title: Registro float de constante (referência do HLSL PS)
description: Registro de entrada do sombreador de pixel para uma constante de ponto flutuante de 4D.
ms.assetid: e4f46a48-c81e-4105-901b-332b92fa6195
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 025c7e7609e7e0d19c15dfa24e27b9f174114e9287a9e09d01d2436b4ef2ef8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982846"
---
# <a name="constant-float-register-hlsl-ps-reference"></a>Registro float de constante (referência do HLSL PS)

Registro de entrada do sombreador de pixel para uma constante de ponto flutuante de 4D.

Eles podem ser definidos usando [def-PS](def---ps.md) ou [**SetPixelShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantf).

O comportamento das constantes do sombreador foi alterado entre o Direct3D 8 e o Direct3D 9.

-   Para o Direct3D 9, as constantes definidas com defx atribuem valores ao espaço constante do sombreador. O tempo de vida de uma constante declarada com defx é restrito apenas à execução desse sombreador. Por outro lado, as constantes definidas usando as APIs SetXXXShaderConstantX inicializam constantes no espaço global. As constantes no espaço global não são copiadas para o espaço local (visível para o sombreador) até que SetxxxShaderConstants seja chamado.
-   Para o Direct3D 8, as constantes definidas com defx ou as APIs atribuem valores ao espaço constante do sombreador. Cada vez que o sombreador é executado, as constantes são usadas pelo sombreador atual, independentemente da técnica usada para defini-los.

## <a name="examples"></a>Exemplos

Aqui está um exemplo declarando duas constantes de ponto flutuante em um sombreador.


```
def c40, 0.0f,0.0f,0.0f,0.0f;
```



Essas constantes são carregadas toda vez que [**SetPixelShader**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader) é chamado.

Se você estiver definindo valores constantes com a API, não haverá nenhuma declaração de sombreador necessária.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 