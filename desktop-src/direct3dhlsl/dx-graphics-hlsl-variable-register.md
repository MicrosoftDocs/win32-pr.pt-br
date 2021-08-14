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



| : register ( *\[ perfil de \_ sombreador, \]* *\# \[ subcomponente tipo \]* ) |
|----------------------------------------------------------------|



 

## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="register"></span><span id="REGISTER"></span>Registrar
</dt> <dd>

Palavra-chave necessária.

</dd> <dt>

<span id="_shader_profile_"></span><span id="_SHADER_PROFILE_"></span>*\[perfil do \_ sombreador\]*
</dt> <dd>

Perfil [de sombreador opcional](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax), que pode ser um destino de sombreador ou simplesmente **ps** ou **vs**.

</dd> <dt>

<span id="Type__subcomponent_"></span><span id="type__subcomponent_"></span><span id="TYPE__SUBCOMPONENT_"></span>*\# \[ Subcomponente de tipo\]*
</dt> <dd>

Registre o tipo, o número e a declaração do subcomponente.

-   O tipo é um dos seguintes:

    

    | Tipo | Descrição do registro       |
    |------|----------------------------|
    | b    | Buffer constante            |
    | t    | Buffer de textura e textura |
    | c    | Deslocamento de buffer              |
    | s    | Exemplo                    |
    | u    | Exibição de acesso não organizado      |

    

     

-   *\#* é o número do registro, que é um número inteiro.
-   O *subcomponente* é um número inteiro opcional.

</dd> </dl>

## <a name="remarks"></a>Comentários

Você pode adicionar uma ou mais atribuições de registro à mesma declaração de variável, separadas por espaços.

Para variáveis direct3D 10 no escopo global, a palavra-chave **register** atua da mesma forma que a palavra-chave [packoffset (DirectX HLSL).](dx-graphics-hlsl-variable-packoffset.md)

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

 

 