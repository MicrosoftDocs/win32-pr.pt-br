---
title: Serialização de procedimento
description: Quando você usa a serialização de procedimento, um procedimento é rotulado com o atributo \ Encode \ ou \ decodificar \. Em vez de gerar o stub remoto usual, o compilador gera um stub de serialização para a rotina.
ms.assetid: 98367b00-696b-44c4-a747-92ecac34ba1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77696761a9aa5fe1471e9ebf24a57303b15d0ff3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "104370829"
---
# <a name="procedure-serialization"></a>Serialização de procedimento

Quando você usa a serialização de procedimento, um procedimento é rotulado com o atributo de \[ [**codificação**](/windows/desktop/Midl/encode) \] ou \[ [**decodificação**](/windows/desktop/Midl/decode) \] . Em vez de gerar o stub remoto usual, o compilador gera um stub de serialização para a rotina.

Assim como um procedimento remoto deve usar um identificador de associação para fazer uma chamada remota, um procedimento de serialização deve usar um identificador de serialização para usar serviços de serialização. Se um identificador de serialização não for especificado, um identificador implícito padrão será usado para direcionar a chamada. Por outro lado, se o identificador de serialização for especificado, como um argumento de [**identificador \_ t**](/windows/desktop/Midl/handle-t) explícito da rotina ou usando o \[ atributo [**\_ identificador explícito**](/windows/desktop/Midl/explicit-handle) \] , você deverá passar um identificador válido como um argumento da chamada. Para obter informações adicionais sobre como criar um identificador de serialização válido, consulte [identificadores de serialização](serialization-handles.md), [exemplos de codificação de buffer fixo](fixed-buffer-serialization.md)e [exemplos de codificação incremental](examples-of-incremental-encoding.md).

> [!Note]
> O Microsoft RPC permite que os procedimentos remotos e de serialização sejam misturados em uma interface. No entanto, tome cuidado ao fazer isso.
> 
> Para procedimentos remotos com identificadores de associação implícitos, o compilador MIDL gera uma variável de identificador global do tipo [**Handle \_ t**](/windows/desktop/Midl/handle-t). Os procedimentos e os tipos com identificadores de serialização implícitas usam essa mesma variável de identificador global.
> 
> Para identificadores implícitos, o identificador implícito global deve ser definido como um identificador de associação válido antes de uma chamada remota. O identificador implícito deve ser definido como um identificador de serialização válido antes de uma chamada de serialização. Portanto, um procedimento não pode ser remoto e serializado. Ele deve ser um ou outro.

 

 

 