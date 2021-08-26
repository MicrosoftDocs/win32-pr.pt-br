---
title: Serialização de procedimento
description: Quando você usa a serialização de procedimento, um procedimento é rotulado com o atributo \ encode\ ou \ decode\. Em vez de gerar o stub remoto normal, o compilador gera um stub de serialização para a rotina.
ms.assetid: 98367b00-696b-44c4-a747-92ecac34ba1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023b514aa5a2e5be1b937a3989c3446bcc6e61c76f885381ce257286b5c625b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120018946"
---
# <a name="procedure-serialization"></a>Serialização de procedimento

Quando você usa a serialização de procedimento, um procedimento é rotulado com o atributo \[ [**de codificação**](/windows/desktop/Midl/encode) \] ou \[ [**decodificar.**](/windows/desktop/Midl/decode) \] Em vez de gerar o stub remoto normal, o compilador gera um stub de serialização para a rotina.

Assim como um procedimento remoto deve usar um alça de associação para fazer uma chamada remota, um procedimento de serialização deve usar um alça de serialização para usar serviços de serialização. Se um alça de serialização não for especificado, um handle implícito padrão será usado para direcionar a chamada. Por outro lado, se o alça de serialização for especificado, como um argumento t de handle [**\_ explícito**](/windows/desktop/Midl/handle-t) da rotina ou usando o atributo de alça explícito, você deverá passar um alça válido como um argumento da \[ [**\_**](/windows/desktop/Midl/explicit-handle) \] chamada. Para obter informações adicionais sobre como criar um alça de serialização válido, consulte [Serialization Handles](serialization-handles.md), [Examples of Fixed Buffer ENcoding](fixed-buffer-serialization.md)e [Examples of Incremental Encoding](examples-of-incremental-encoding.md).

> [!Note]
> O Microsoft RPC permite que procedimentos remotos e de serialização sejam mistos em uma interface. No entanto, use cuidado ao fazer isso.
> 
> Para procedimentos remotos com identificador de associação implícito, o compilador MIDL gera uma variável de identificador global do tipo [**\_ identificador t**](/windows/desktop/Midl/handle-t). Procedimentos e tipos com alças de serialização implícita usam essa mesma variável de alça global.
> 
> Para alças implícitas, o handle implícito global deve ser definido como um alça de associação válido antes de uma chamada remota. O alça implícito deve ser definido como um alça de serialização válido antes de uma chamada de serialização. Portanto, um procedimento não pode ser remoto e serializado. Ele deve ser um ou outro.

 

 

 