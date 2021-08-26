---
title: " Diretivas ifdef e ifndef"
description: Diretivas de pré-processador que determinam se uma constante ou macro de pré-processador específica está definida.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- Diretivas ifdef e ifndef HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 584cde8856c48aeafed5665016a71146f8c2ffb341b837faa6bf35d627152c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068316"
---
# <a name="ifdef-and-ifndef-directives"></a>\#Diretivas \# ifdef e ifndef

Diretivas de pré-processador que determinam se uma constante ou macro de pré-processador específica está definida.



| \#Identificador  ifdef ...  |
|---------------------------|
| \#endif                   |
| \#identificador  ifndef ... |
| \#endif                   |



 

## <a name="parameters"></a>Parâmetros



| Item                                                                              | Descrição                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*Identificador*<br/> | Identificador da constante ou macro a ser verificada. <br/> |



 

## <a name="remarks"></a>Comentários

Você pode usar as \# diretivas ifdef \# e ifndef em qualquer lugar em que [ \# o se](dx-graphics-hlsl-appendix-pre-if.md) possa ser usado. A \# instrução ifdef é equivalente à diretiva ). Essas diretivas verificam apenas a presença ou ausência de identificadores definidos usando a diretiva [ \# define,](dx-graphics-hlsl-appendix-pre-define.md) não para identificadores declarados no código-fonte C ou C++.

Essas políticas são fornecidas somente para compatibilidade com versões anteriores da linguagem. O uso do operador [definido](dx-graphics-hlsl-appendix-pre-if.md) com a \# diretiva if é preferencial.

A \# diretiva ifndef verifica o oposto da condição verificada por \# ifdef. Se o identificador não estiver definido, a condição será verdadeira (não zero); caso contrário, a condição será false (zero).

## <a name="examples"></a>Exemplos

O identificador pode ser passado da linha de comando usando a opção /D. Até 30 macros podem ser especificadas com /D. Isso é útil para verificar se uma definição existe, uma vez que uma definição pode ser passada da linha de comando. O exemplo a seguir usa esse comportamento para determinar se um aplicativo deve ser executado no modo de teste.


```
// PROG.CPP
#ifndef test
  #define final
#endif
int main()
{
}
```



Quando compilado usando o comando a seguir, prog.cpp será compilado no modo de teste; caso contrário, ele será compilado no modo final.


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#if, )](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





