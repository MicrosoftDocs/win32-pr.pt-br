---
title: Marshal do usuário
description: Marshaling do usuário na chamada de procedimento remoto (RPC).
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c901fd8c75137b4657322a89692ff8a3afb5408
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822630"
---
# <a name="user-marshal"></a>Marshal do usuário

O marshaling do usuário tem uma cadeia de caracteres de formato semelhante a transmitir \_ como:

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

Os sinalizadores<1> byte consiste no Nibble superior do sinalizador e no Nibble inferior do alinhamento.

Os dois bits superiores do demarcador Nibble são usados para descrever se o tipo de conexão é definido como um ponteiro exclusivo, um ponteiro de referência ou nenhum ponteiro (não pode ser um PTR). Os seguintes manifestos foram definidos para definir/obter os sinalizadores:

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

O Nibble de alinhamento da palavra de sinalizador mantém o alinhamento de fios do tipo transmitido.

O índice quádruplo \_<2> é um índice da rotina de retorno de chamada quádruplo das funções de marshaling do usuário. As posições de rotina são as seguintes: dimensionamento, empacotamento, desempacotamento e rotina de liberação.

O tamanho da memória do tipo de usuário \_ \_ \_<2> fornece um tamanho para o tipo específico do usuário, incluindo tipos desconhecidos.

O tamanho do buffer de tipo transmitido \_ \_ \_<2> é zero quando o tamanho é variável ou o tamanho fixo real. Essa é uma otimização que permite ao MIDL ignorar retornos de chamada ao dimensionar o buffer e também ao liberar.

## <a name="range"></a>Intervalo

A \[ verificação de intervalo \] fornece meios adicionais para validação de argumento na camada de NDR. O \[ \] descritor de intervalo tem o seguinte formato:

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

Os sinalizadores assumem o Nibble superior e o tipo o Nibble inferior do segundo byte. Os valores baixos e altos dependem do tipo da variável a ser verificada.

Os sinalizadores são destinados a um veículo de expansão; o compilador tem definido o Nibble para zero.

 

 




