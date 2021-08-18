---
title: Proteção de buffer MCCP
description: a partir do Windows Vista, o mecanismo de marshalling de RPC executa outras etapas para tentar evitar saturações de buffer do lado do cliente devido a dados retornados. Esse recurso é chamado de proteção de conformidade de mini computação (MCCP).
ms.assetid: 37fe743b-c64e-469d-b8f4-abab9f05c813
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b95234eed76c3d8f0fdc34b0b53e9cf02bcae2fd6db62694e1a3aadd602076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928402"
---
# <a name="mccp-buffer-protection"></a>Proteção de buffer MCCP

a partir do Windows Vista, o mecanismo de marshalling de RPC executa outras etapas para tentar evitar saturações de buffer do lado do cliente devido a dados retornados. Esse recurso é chamado de proteção de conformidade de mini computação (MCCP).

Quando o cliente passa um ponteiro para um buffer existente para um \[ parâmetro [**out**](/windows/desktop/Midl/out-idl) \] ou \[ [**in**](/windows/desktop/Midl/in),**out** , \] os dados retornados para esse parâmetro são copiados para o buffer existente. Se os dados retornados forem maiores que o buffer passado, uma saturação de buffer poderá ocorrer quando o RPC copiar os dados retornados para o buffer muito pequeno. Consulte [ponteiros de nível superior e inseridos](top-level-and-embedded-pointers.md).

Com o MCCP, o RPC tenta detectar essa condição e rejeitar a chamada se ela for detectada. Para buffers com um valor de correlação, como \[ [**tamanho \_**](/windows/desktop/Midl/size-is) \] , se os dados retornados não couberem no tamanho do buffer especificado, a chamada será rejeitada e a \_ \_ exceção de dados stub inválidos RPC X \_ \_ será gerada. Para cadeias de caracteres sem tamanho, a chamada será rejeitada se o tamanho da cadeia de caracteres existente (comprimento até o terminador **NULL** ) não for suficiente para manter a cadeia de caracteres retornada, a chamada será rejeitada. O RPC não pode detectar estouros de buffer em todas as condições, portanto, é aconselhável que o desenvolvedor continue a tomar precauções normais contra estouros de buffer.

Se o cliente não passar um buffer existente para um parâmetro \[ [**out**](/windows/desktop/Midl/out-idl) \] , mas, em vez disso, passar um ponteiro de referência para **NULL**, o RPC seguirá as regras normais para alocar um novo buffer em nome do cliente. Esse buffer será alocado com espaço suficiente para manter os dados retornados.

Uma segunda proteção é que, para parâmetros correlacionados, o RPC irá impor que um buffer não **nulo** seja passado quando a variável de contagem de correlação for não **nula**.

``` syntax
HRESULT PassString( [in] DWORD Length, [in, unique, string, size_is( Length )]LPWSTR MyString );
```

Se *MyString* for **NULL**, o RPC rejeitará a chamada, a menos que *Length* esteja definido como 0. Observe que o RPC permitirá que o *comprimento* seja 0 enquanto o *MyString* não for **nulo** e o RPC tratará *MyString* como uma alocação de buffer de comprimento 0.

 

 