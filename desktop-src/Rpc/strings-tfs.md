---
title: Cadeias de caracteres (RPC)
description: Três tipos de cadeia de caracteres e RPC (chamada de procedimento remoto).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207e20b1c343ded17b5d62db2321bee380463f20
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294368"
---
# <a name="strings-rpc"></a>Cadeias de caracteres (RPC)

Há três tipos de cadeias de caracteres denotados pelas seguintes subcadeias de caracteres finais no caractere de formato.



| Tipo                  | Subcadeia de caracteres |
|-----------------------|-----------|
| Cadeia de caracteres      | CSTRING   |
| Cadeia de caracteres largo | WSTRING   |
| Estrutura habilitada para cadeia de caracteres | SSTRING   |



 

### <a name="nonconformant-strings"></a>Cadeias de caracteres não compatíveis

Um exemplo de cadeia de caracteres não compatível é uma **\[ cadeia de caracteres \]** em uma matriz de tamanho fixo.

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a>Cadeias de caracteres de conformidade

``` syntax
FC_C_CSTRING | FC_C_WSTRING
FC_PAD 
```

–ou–

``` syntax
FC_C_CSTRING | FC_C_WSTRING 
FC_STRING_SIZED 
conformance_description<> 
```

O primeiro formato descreve cadeias de caracteres comuns, como um argumento Char **\[ \] String** \* . Uma cadeia de caracteres de acordo com o tamanho tem a última descrição.

A descrição de conformidade \_<> é um descritor de correlação e tem 4 ou 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.

### <a name="structure-strings"></a>Cadeias de caracteres de estrutura

A seguir está uma estrutura habilitada para cadeia de caracteres não compatível:

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

Estrutura compatível com cadeia de caracteres em conformidade:

``` syntax
FC_C_SSTRING 
element_size<1>
```

or

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

A última descrição é para uma estrutura com capacidade de cadeia de caracteres dimensionada.

 

 