---
title: " Diretivas ifdef e ifndef"
description: Diretivas de pré-processador que determinam se uma macro ou constante de pré-processador específico está definida.
ms.assetid: c1cc2e1d-2599-45ec-9629-56c4b42e0d0e
keywords:
- ifdef e diretivas ifndef HLSL
topic_type:
- apiref
api_name:
- ifdef and ifndef Directives
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 338308b58f1cdc68ec78984e65ffbf056a36b10b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006546"
---
# <a name="ifdef-and-ifndef-directives"></a>\#Diretivas ifdef e \# ifndef

Diretivas de pré-processador que determinam se uma macro ou constante de pré-processador específico está definida.



| \#*identificador* de ifdef...  |
|---------------------------|
| \#endif                   |
| \#*identificador* de ifndef... |
| \#endif                   |



 

## <a name="parameters"></a>Parâmetros



| Item                                                                              | Descrição                                               |
|-----------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*ID*<br/> | Identificador da constante ou macro a ser verificada. <br/> |



 

## <a name="remarks"></a>Comentários

Você pode usar as \# diretivas ifdef e \# ifndef em qualquer lugar que o [ \# se](dx-graphics-hlsl-appendix-pre-if.md) possa ser usado. A \# diretiva ifdef é equivalente a). Essas diretivas verificam apenas a presença ou a ausência de identificadores definidos usando a diretiva [ \# definir](dx-graphics-hlsl-appendix-pre-define.md) , não para identificadores declarados no código-fonte C ou C++.

Essas políticas são fornecidas somente para compatibilidade com versões anteriores da linguagem. O uso do operador [definido](dx-graphics-hlsl-appendix-pre-if.md) com a \# diretiva If é preferencial.

A \# diretiva ifndef verifica o oposto da condição verificada por \# ifdef. Se o identificador não for definido, a condição será true (diferente de zero); caso contrário, a condição será false (zero).

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



Quando compilado usando o comando a seguir, PROG. cpp será compilado no modo de teste; caso contrário, ele será compilado no modo final.


```
CL.EXE /Dtest prog.cpp
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#se,)](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





