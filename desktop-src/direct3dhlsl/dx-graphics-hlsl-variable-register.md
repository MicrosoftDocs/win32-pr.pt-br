---
title: register
description: register
ms.assetid: 45149f8c-8b76-4247-98d7-d141d7268da3
keywords:
- registrar HLSL
topic_type:
- apiref
api_name:
- register
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0102716529471b3e867e17b0e9b635274cdfc28ec603f239d66c76ffb0fdaa19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119983206"
---
# <a name="register"></a>register

Palavra-chave opcional para atribuir uma variável de sombreador a um registro específico, que usa a seguinte sintaxe:



| : Register ( *\[ \_ perfil \] do sombreador*, *tipo \# \[ subcomponente \]* ) |
|----------------------------------------------------------------|



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="register"></span><span id="REGISTER"></span>Registr
</dt> <dd>

Palavra-chave required.

</dd> <dt>

<span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[perfil do sombreador \_\]*
</dt> <dd>

[Perfil de sombreador](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax)opcional, que pode ser um alvo de sombreador ou simplesmente **PS** ou **vs**.

</dd> <dt>

<span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*Subcomponente do tipo \# \[\]*
</dt> <dd>

Tipo de registro, número e declaração de subcomponente.

-   O tipo é um dos seguintes:

    

    | Tipo | Descrição do registro       |
    |------|----------------------------|
    | b    | Buffer constante            |
    | t    | Buffer de textura e texturização |
    | c    | Deslocamento do buffer              |
    | s    | Exemplo                    |
    | u    | Modo de exibição de acesso não ordenado      |

    

     

-   *\#* é o número do registro, que é um número inteiro.
-   O *subcomponente* é um número inteiro opcional.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode adicionar uma ou mais atribuições de registro à mesma declaração de variável, separadas por espaços.

Para as variáveis do Direct3D 10 no escopo global, a palavra-chave **Register** atua da mesma forma que a palavra-chave [PACKOFFSET (DirectX HLSL)](dx-graphics-hlsl-variable-packoffset.md) .

## <a name="examples"></a>Exemplos

Estes são alguns exemplos:


```
sampler myVar : register( ps_5_0, s ); 
```




```
sampler myVar : register( vs, s[8] );
```




```
sampler myVar : register( ps, s[2] ) 
              : register( ps_5_0, s[0] ) 
              : register( vs, s[8] );
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de Variável](dx-graphics-hlsl-variable-syntax.md)
</dt> <dt>

[Variáveis (DirectX HLSL)](dx-graphics-hlsl-variables.md)
</dt> </dl>

 

 