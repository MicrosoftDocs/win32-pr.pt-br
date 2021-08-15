---
title: partial_ignore atributo
description: O atributo ACF \ partial ignore\ define uma versão especializada \_ de \ unique\ pointers que fornece semântica opcional.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore atributo MIDL
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac751e5b3bdb4a93c003e170333af8956048c9793630419fff0857d61f8c1f2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118641969"
---
# <a name="partial_ignore-attribute"></a>atributo \_ partial ignore

A ignorar **parcial \[ do \_ \]** atributo ACF define uma **\[ \]** versão especializada de ponteiros exclusivos que fornece semântica opcional.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a>Comentários

Ao criar uma função, é comum permitir que os usuários especifiquem um ponteiro não **NULL** para dados de retorno opcionais, geralmente chamados de ponteiro opcional-out. A memória apontada pelo usuário normalmente não precisa ser inicializada. Essa técnica representa um problema quando a função é usada em RPC.

Se o ponteiro opcional for válido, mas aponta para dados não reinicializados, o RPC tentará marshaling dos dados e enviá-los para o servidor, o que pode fazer com que o marshaling falhe e anula a chamada. Mesmo se o marshaling for bem-sucedido, uma quantidade potencialmente grande de dados inúteis será enviada ao servidor.

Esses problemas são resolvidos marcando o ponteiro **\[ como in, out, unique, partial \_ ignore \]**. Todos os quatro atributos devem estar presentes. Quando um **\[ ponteiro de \_ ignorar \]** parcial é marshalado no lado do cliente, os únicos dados enviados ao servidor são um indicador que mostra se o ponteiro é **NULL.** Se o ponteiro for não **NULL,** a rotina do lado do servidor receberá um ponteiro válido para um bloco de memória que foi inicializado com zeros. Se o ponteiro for **NULL,** a rotina do lado do servidor receberá um **ponteiro NULL.**

Nessa situação, o tamanho máximo do ponteiro deve ser bem definido no tempo de compilação ou com base nos parâmetros de entrada, pois o servidor precisa alocar espaço para o local de memória que está sendo apontado. Por exemplo, um ponteiro de **\[ cadeia \]** de caracteres simples não tem um tamanho bem definido porque a cadeia de caracteres é terminada implicitamente por um caractere NULL. Nesse caso, especificar o tamanho máximo da cadeia de caracteres adicionando um atributo **\[ \_ size é \]** atingiria o requisito de tamanho bem definido.

## <a name="examples"></a>Exemplos

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Único**](unique.md)
</dt> </dl>

 

 




