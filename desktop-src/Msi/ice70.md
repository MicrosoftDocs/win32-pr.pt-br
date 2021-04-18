---
description: ICE70 verifica se os valores inteiros das entradas do registro estão especificados corretamente.
ms.assetid: f8493622-867b-42e1-9fda-a7c3229bbb4e
title: ICE70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616592a772dec6f95d81b92f03f0bffea6ce7bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758956"
---
# <a name="ice70"></a>ICE70

ICE70 verifica se os valores inteiros das entradas do registro estão especificados corretamente. Os valores do formato \# \# Str, \# % unexpanded Str não são validados. Os valores do formato \# xhex, \# xhex, \# Integer e \# \[ Property \] são validados. A tabela a seguir fornece uma breve visão geral.



| Valor                 | Validação                                                                    |
|-----------------------|-------------------------------------------------------------------------------|
| \#\#Str               | válido                                                                         |
| \#% de str não expandido     | válido                                                                         |
| \#xHex, \# xHex         | Valide os caracteres hexadecimais válidos (0-9, a-f, A-F). As propriedades são permitidas aqui. |
| \#+ int, \# -int, \# int | Validar para caracteres numéricos válidos (0-9). As propriedades são permitidas aqui.     |



 

A sintaxe para um valor inteiro a ser inserido no registro é \# Integer, em que Integer é numérico.

## <a name="result"></a>Resultado

ICE70 relatará um erro se os valores inteiros das entradas do registro não forem especificados corretamente.

## <a name="example"></a>Exemplo

ICE70 relata os erros a seguir para o exemplo fornecido.

``` syntax
The value #12xz34 is an invalid numeric value for registry entry Reg1. If you meant to use a string, then the string value entry must be preceded by ## not #.
```

Para corrigir este erro: se você quiser que o valor seja numérico, altere o valor para usar todos os caracteres numéricos. Se você quiser que o valor seja uma cadeia de caracteres, ele deverá ser precedido por dois ' \# ' ( \# \# ) em vez de apenas um.

``` syntax
The value #xz34 is an invalid hexadecimal value for registry entry Reg2.
```

Para corrigir esse erro: os caracteres hexadecimais válidos são 0-9, A-F e a-f. Somente esses caracteres podem seguir o \# x (ou \# x).

[Tabela do registro](registry-table.md) (parcial)



| Registro | Valor    |
|----------|----------|
| Reg1     | \#12xz34 |
| Reg2     | \#xz34   |



 

## <a name="remarks"></a>Comentários

-   \#\[MyProperty \] é válido.
-   \#\[MyProperty não é válido (colchete de fechamento ausente).
-   \#\[myprop1 \] \[ myprop2 é válido. (Mesmo que o último esteja faltando o colchete final, myprop1 poderia avaliar como \# str para que você tivesse \# \# myprop2 Str \[ , que é válido
-   \#\]MyProperty \[ não é válido
-   Qualquer propriedade inserida em uma cadeia de caracteres de valor não pode estar no \[ \] formulário $compkey, \[ \# FileKey \] ou \[ ! FileKey \] porque elas não são numéricas. No entanto, há uma exceção, \# \[ MyProperty \] \[ $compkey \] (ou \[ \# FileKey \] ou \[ ! FileKey \] ) é válida porque, como no anterior, \[ MyProperty \] pode avaliar como \# Str.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de ICE](ice-reference.md)
</dt> </dl>

 

 



