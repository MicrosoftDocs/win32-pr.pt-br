---
title: Serialização de tipo
description: O compilador MIDL gera até três funções para cada tipo ao qual o atributo \ codifique \ ou \ decodificar \ é aplicado.
ms.assetid: 948f1dd7-c8b0-4fa0-88d8-9d122de52ba1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4674617bc98c92dbc684a29d1a3c91ac6a7429e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084695"
---
# <a name="type-serialization"></a>Serialização de tipo

O compilador MIDL gera até três funções para cada tipo ao qual o atributo de \[ [codificação](/windows/desktop/Midl/encode) \] ou \[ [decodificação](/windows/desktop/Midl/decode) \] é aplicado. Por exemplo, para um tipo definido pelo usuário chamado *com MyType*, o compilador gera código para as \_ funções com MyType Encode, com MyType \_ decodificar e com MyType \_ AlignSize. Para essas funções, o compilador grava protótipos em stub. h e código-fonte para stub \_ c.c. Geralmente, você pode codificar um objeto *com MyType* com com MyType \_ codificar e decodificar um objeto do buffer usando \_ decodificação com MyType. Com MyType \_ AlignSize será usado se você precisar saber o tamanho do buffer de marshaling antes de alocá-lo.

A função de codificação a seguir é gerada pelo compilador MIDL. Essa função serializa os dados para o objeto apontado por pObject, e o buffer é obtido de acordo com o método especificado no identificador. Depois de gravar os dados serializados no buffer, você controla o buffer. Observe que o identificador herda o status das chamadas anteriores e os buffers devem ser alinhados a 8.

Para um identificador implícito:

``` syntax
void MyType_Encode (MyType __RPC_FAR * pObject);
```

Para um identificador explícito:

``` syntax
void MyType_Encode (handle_t Handle, MyType __RPC_FAR * pObject);
```

A função a seguir desserializa os dados do armazenamento do aplicativo no objeto apontado por pObject. Você fornece um buffer de marshaling de acordo com o método especificado na alça. Observe que o identificador pode herdar o status das chamadas anteriores e os buffers devem estar alinhados a 8.

Para um identificador implícito:

``` syntax
void MyType_Decode (MyType __RPC_FAR * pObject);
```

Para um identificador explícito:

``` syntax
void MyType_Decode (handle_t Handle, MyType __RPC_FAR * pObject);
```

A função a seguir retorna um tamanho, em bytes, que inclui a instância de tipo, além de quaisquer bytes de preenchimento necessários para alinhar os dados. Isso permite a serialização de um conjunto de instâncias do mesmo tipo ou de tipos diferentes em um buffer, garantindo que os dados de cada objeto estejam alinhados adequadamente. Com MyType \_ AlignSize pressupõe que a instância apontada pelo pObject será empacotada em um buffer que começa no deslocamento alinhado a 8.

Para um identificador implícito:

``` syntax
size_t MyType_AlignSize (MyType __RPC_FAR * pObject);
```

Para um identificador explícito:

``` syntax
size_t MyType_AlignSize (handle_t Handle, MyType __RPC_FAR * pObject);
```

Observe que os procedimentos remotos com identificadores de ligação implícita e tipos serializados com identificadores de serialização implícitas usam a mesma variável de identificador global. Portanto, é aconselhável não misturar serialização de tipo e procedimentos remotos em uma interface com identificadores implícitos. Para obter detalhes, consulte [identificadores implícitos versus explícitos](implicit-versus-explicit-handles.md).

 

 