---
title: opção/cstruct_out
description: A opção/cstruct_out modifica a definição de C de uma interface COM que retorna estruturas para corresponder à ABI que um implementador do C++ forneceria.
keywords:
- /cstruct_out MIDL do comutador
topic_type:
- apiref
api_name:
- /cstruct_out
api_type:
- NA
ms.topic: reference
ms.date: 12/10/2020
ms.openlocfilehash: 535e1630046b424493e2211c29248c18bf1ed798
ms.sourcegitcommit: 9cf1ed65dfbea1ba118b63d0656f30c3685d8520
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103824875"
---
# <a name="cstruct_out-switch"></a>\_opção/cstruct out

Essa opção modifica a definição de C de uma interface COM que retorna estruturas para corresponder à ABI que um implementador do C++ forneceria.

``` syntax
midl /cstruct_out
```

## <a name="switch-options"></a>Opções de comutação

Essa opção não tem parâmetros.

## <a name="remarks"></a>Comentários

Algumas definições de interface (especialmente as contidas em `d3d12.idl` ) contêm `__stdcall` métodos que retornam estruturas. O C e C++ ABIs da MSVC diferem na forma como implementam essas funções:

* O C os trata como funções simples que usam um `this` ponteiro oculto como o primeiro parâmetro. O corparador aplica uma pequena otimização de struct que permite que structs menores que 8 bytes (ou maiores se todos os valores sejam de ponto flutuante) sejam retornados em registros. Somente estruturas maiores são promovidas para usar um parâmetro oculto e um valor de retorno alocado pelo chamador.
* O C++ os trata como funções membro. O compilador *sempre* faz isso inserindo um parâmetro oculto (um ponteiro para um valor de retorno alocado pelo chamador) como o segundo parâmetro, após o `this` ponteiro. Ele também retorna o mesmo ponteiro como seu valor de retorno.

Essa opção força a definição C de interfaces no cabeçalho resultante para assumir que o implementador estava usando C++ e que o código C deveria usar explicitamente a ABI do C++. Isso implica que a função inclui um parâmetro oculto para o ponteiro de valor de retorno e retorna esse ponteiro em vez da estrutura diretamente.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Sintaxe de linha de comando MIDL geral](general-midl-command-line-syntax.md)
</dt> </dl>
