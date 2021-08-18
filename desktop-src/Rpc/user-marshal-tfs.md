---
title: Marshal do usuário
description: Marshal do usuário na RPC (Chamada de Procedimento Remoto).
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6dcc9574b49a46b6e867fc4bca314944589ccf68b9d6e3fb8695a099eb255c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010836"
---
# <a name="user-marshal"></a>Marshal do usuário

O marshal do usuário tem uma cadeia de caracteres de formato semelhante à \_ transmissão como:

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

Os sinalizadores<1> byte consistem na nibble do sinalizador superior e na nibble de alinhamento inferior.

Os 2 bits superiores da nibble de sinalizador são usados para descrever se o tipo de fio é definido como um ponteiro exclusivo, ponteiro de referência ou nenhum ponteiro (não pode ser um ptr). Os manifestos a seguir foram definidos para definir/obter os sinalizadores:

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

A nibble de alinhamento da palavra de sinalizador mantém o alinhamento de transmissão do tipo transmitido.

O índice quadruplo<2> é um índice da rotina de retorno de chamada \_ quádruplo das funções de marshal do usuário. As posições de rotina são as que se seguem: rotina de ressarqueção, marshaling, desmarque e liberação.

O tamanho de memória de tipo<2> fornece um tamanho para o tipo específico do \_ \_ \_ usuário, incluindo tipos desconhecidos.

O tamanho do buffer de tipo transmitido<2> é zero quando o tamanho é variável \_ ou o tamanho fixo \_ \_ real. Essa é uma otimização que permite que MIDL ignore retornos de chamada ao tamanho do buffer e também ao liberar.

## <a name="range"></a>Intervalo

A \[ verificação de intervalo fornece meios \] adicionais para validação de argumento na camada NDR. O \[ \] descritor de intervalo tem o seguinte formato:

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

Os sinalizadores levam a nibble superior e o tipo a nibble inferior do segundo byte. Os valores baixo e alto dependem do tipo da variável a ser verificada.

Os sinalizadores são destinados a um veículo de expansão; o compilador definiu a nibble como zero.

 

 




