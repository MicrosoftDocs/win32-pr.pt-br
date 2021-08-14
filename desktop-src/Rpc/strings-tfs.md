---
title: Cadeias de caracteres (RPC)
description: Três tipos de cadeias de caracteres e RPC (Chamada de Procedimento Remoto).
ms.assetid: 186cabeb-ea3f-4213-ba71-53afe91e6e14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b15467ed5a1425443cbc5a53cf35aba71725c5db68c542c292af38eb0d238cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924832"
---
# <a name="strings-rpc"></a>Cadeias de caracteres (RPC)

Há três tipos de cadeias de caracteres anotados pelas seguintes sub-cadeias de caracteres finais no caractere de formato.



| Tipo                  | Subcadeia de caracteres |
|-----------------------|-----------|
| Cadeia de caracteres      | Cstring   |
| Cadeia de caracteres largos | Wstring   |
| Estrutura capaz de cadeia de caracteres | SSTRING   |



 

### <a name="nonconformant-strings"></a>Cadeias de caracteres não conformantes

Um exemplo de cadeia de caracteres não conformante é uma **\[ cadeia de caracteres \]** em uma matriz de tamanho fixo.

``` syntax
FC_CSTRING | FC _WSTRING 
FC_PAD 
string_size<2>
```

### <a name="conformant-strings"></a>Cadeias de caracteres compatíveis

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

O primeiro formato descreve cadeias de caracteres comuns, como um argumento **\[ char de cadeia \]** de \* caracteres. Uma cadeia de caracteres compatível dimensionada tem a última descrição.

A descrição de conformidade<> é um descritor de correlação e tem 4 ou \_ 6 bytes, dependendo se [**/robust**](/windows/desktop/Midl/-robust) é usado.

### <a name="structure-strings"></a>Cadeias de caracteres de estrutura

Veja a seguir uma estrutura não conformente capaz de cadeia de caracteres:

``` syntax
FC_SSTRING 
element_size<1> 
number_of_elements<2>
```

Estrutura compatível com cadeia de caracteres:

``` syntax
FC_C_SSTRING 
element_size<1>
```

–ou –

``` syntax
FC_C_SSTRING 
elements_size<1> 
FC_STRING_SIZED FC_PAD 
conformance_description<>
```

A última descrição é para uma estrutura dimensionada capaz de cadeia de caracteres.

 

 