---
title: /cstruct_out switch
description: A opção /cstruct_out modifica a definição C de uma interface COM que retorna estruturas para corresponder à ABI que um implementador C++ forneceria.
keywords:
- /cstruct_out com opção MIDL
topic_type:
- apiref
api_name:
- /cstruct_out
api_type:
- NA
ms.topic: reference
ms.date: 12/10/2020
ms.openlocfilehash: 212f79eaad18ba49d12a49e9a831d2b2b5365a87cb9a36c558879adf76e8bb98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118385803"
---
# <a name="cstruct_out-switch"></a>/cstruct \_ out switch

Essa opção modifica a definição C de uma interface COM que retorna estruturas para corresponder à ABI que um implementador C++ forneceria.

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a>Opções de opção

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Algumas definições de interface (notadamente aquelas em `d3d12.idl` ) contêm `__stdcall` métodos que retornam estruturas. Os ABIs C e C++ MSVC diferem em como implementam essas funções:

* C os trata como funções simples que levam um ponteiro `this` oculto como o primeiro parâmetro. O complier aplica uma pequena otimização de struct que permite que structs menores que 8 bytes (ou maiores se todos os valores são ponto flutuante) sejam retornados em registros. Somente estruturas maiores são promovidas para usar um parâmetro oculto e um valor de retorno alocado pelo chamador.
* O C++ os trata como funções de membro. O *compilador sempre* faz isso inserindo um parâmetro oculto (um ponteiro para um valor de retorno alocado pelo chamador) como o segundo parâmetro, após o `this` ponteiro. Ele também retorna o mesmo ponteiro que seu valor de retorno.

Essa opção força a definição C de interfaces no header resultante a assumir que o implementador estava usando C++, e que o código C deve usar explicitamente a ABI do C++. Isso implica que a função inclui um parâmetro oculto para o ponteiro de valor de retorno e retorna esse ponteiro em vez da estrutura diretamente.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe geral da linha de comando MIDL](general-midl-command-line-syntax.md)
</dt> </dl>
