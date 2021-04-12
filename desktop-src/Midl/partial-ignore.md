---
title: partial_ignore atributo
description: O atributo ACF \ \_ ignore parcial \ define uma versão especializada de \ Unique \ ponteiros que fornece semântica opcional de saída.
ms.assetid: 8a8f88b0-4a12-496d-bf77-ee57241b577b
keywords:
- partial_ignore do atributo MIDL
topic_type:
- apiref
api_name:
- partial_ignore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82d133275ca77032341d160b51b95b20235c8f2a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104364971"
---
# <a name="partial_ignore-attribute"></a>\_atributo de ignorar parcial

O atributo de ACF **\[ \_ ignorar \] parcial** define uma versão especializada de ponteiros **\[ exclusivos \]** que fornece semântica de saída opcional.

``` syntax
[ [function-attribute-list <>] ] type-specifier <> [pointer- <>declarator <>] function-name <>( [ partial_ignore [ , parameter-attribute-list <> ] ] type-specifier <> [declarator <>] , ...);
```

## <a name="remarks"></a>Comentários

Ao criar uma função, é comum permitir que os usuários especifiquem um ponteiro não **nulo** para dados de retorno opcionais, geralmente chamados de ponteiros opcionais. Normalmente, a memória apontada pelo usuário não precisa ser inicializada. Essa técnica representa um problema quando a função é usada no RPC.

Se o ponteiro de saída opcional for válido, mas apontar para dados não inicializados, o RPC tentará realizar marshaling desses dados e enviá-los para o servidor, o que pode fazer com que o marshaling falhe e anule a chamada. Mesmo que o marshaling seja executado com sucesso, uma quantidade potencialmente grande de dados inúteis é enviada ao servidor.

Esses problemas são resolvidos marcando o ponteiro como **\[ in, out, Unique e \_ parcial \] ignore**. Todos os quatro atributos devem estar presentes. Quando um ponteiro de **\[ \_ ignorar \] parcial** é empacotado no lado do cliente, os únicos dados enviados ao servidor são um indicador mostrando se o ponteiro é **nulo**. Se o ponteiro não for **nulo**, a rotina do lado do servidor receberá um ponteiro válido para um bloco de memória que foi inicializado com zeros. Se o ponteiro for **nulo**, a rotina do lado do servidor receberá um ponteiro **nulo** .

Nessa situação, o tamanho máximo do ponteiro deve ser bem definido no momento da compilação ou com base nos parâmetros de entrada, pois o servidor precisa alocar espaço para o local da memória que está sendo apontado. Por exemplo, um ponteiro de **\[ cadeia de caracteres \]** simples não tem um tamanho bem definido porque a cadeia de caracteres é terminada implicitamente por um caractere nulo. Nesse caso, a especificação do tamanho máximo da cadeia de caracteres com a adição de um **\[ tamanho \_ é \]** o atributo atingiria o requisito de tamanho bem definido.

## <a name="examples"></a>Exemplos

``` syntax
/* The MoveLeft function will move one position to the left and optionally return the previous position */
void MoveLeft([in, out, unique, partial_ignore] long *pPrevPosition);
```

## <a name="see-also"></a>Confira também

<dl> <dt>

[**diferente**](unique.md)
</dt> </dl>

 

 




