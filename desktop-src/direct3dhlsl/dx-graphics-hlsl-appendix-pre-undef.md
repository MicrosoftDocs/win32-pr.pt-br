---
title: " Diretiva undef"
description: Diretiva de pré-processador que remove a definição atual de uma constante ou macro que foi definida anteriormente usando a diretiva \ define.
ms.assetid: ba6bbe6b-ecfa-40cb-887f-e42b6e22c7bd
keywords:
- Diretiva de undef HLSL
topic_type:
- apiref
api_name:
- undef Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7358dc60d002e784394f64773934a18f7413e493
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293197"
---
# <a name="undef-directive"></a>\#Diretiva undef

Diretiva de pré-processador que remove a definição atual de uma constante ou macro que foi definida anteriormente usando a diretiva de [ \# definição](dx-graphics-hlsl-appendix-pre-define.md) .



| \#*identificador* de undef |
|----------------------|



 

## <a name="parameters"></a>Parâmetros



| Item                                                                              | Descrição                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="identifier"></span><span id="IDENTIFIER"></span>*ID*<br/> | Identificador da constante ou da macro para remover a definição de. Se você estiver desdefinindo uma macro, forneça apenas o identificador, não a lista de parâmetros. <br/> |



 

## <a name="remarks"></a>Comentários

Você pode aplicar a \# diretiva undef a um identificador que não tem nenhuma definição anterior; isso garante que o identificador seja indefinido. A substituição de macro não é executada em \# instruções undef.

A \# diretiva undef normalmente é emparelhada com uma diretiva de [ \# definição](dx-graphics-hlsl-appendix-pre-define.md) para criar uma região em um programa de origem no qual um identificador tem um significado especial. Por exemplo, uma função específica do programa de origem pode usar constantes manifestas para definir os valores específicos que não afetam o restante do programa. A \# diretiva undef também funciona com a diretiva [) para controlar a compilação condicional do programa de origem.

Constantes e macros podem ser indefinidas na linha de comando usando a opção/U, seguida pelos identificadores para serem indefinidos. Isso é equivalente a adicionar uma sequência de \# diretivas undef no início do arquivo de origem.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra como usar a \# diretiva undef para remover definições de uma constante simbólica e uma macro.


```
#define WIDTH           80
#define ADD( X, Y )     (X) + (Y)

#undef WIDTH
#undef ADD
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Diretivas de pré-processador (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#definir diretiva (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-define.md)
</dt> <dt>

[\#se,)](dx-graphics-hlsl-appendix-pre-if.md)
</dt> </dl>

 

 





