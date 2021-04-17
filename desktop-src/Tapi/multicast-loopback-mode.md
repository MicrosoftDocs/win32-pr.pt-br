---
description: A \_ enumeração do modo de loopback multicast \_ descreve o modo de loopback multicast.
ms.assetid: bf9c3665-71cc-4cde-9ad4-1a8b62eddf9f
title: Enumeração de MULTICAST_LOOPBACK_MODE (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a15505efcd1a9e399866b104da0582ccf846689
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761951"
---
# <a name="multicast_loopback_mode-enumeration"></a>Enumeração do modo de \_ loopback multicast \_

\[**Multicast \_ O \_ modo de loopback** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A enumeração do **\_ \_ modo de loopback multicast** descreve o modo de loopback multicast.

## <a name="syntax"></a>Syntax


```C++
} MULTICAST_LOOPBACK_MODE;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="MM_NO_LOOPBACK"></span><span id="mm_no_loopback"></span>**MM \_ sem \_ loopback**
</dt> <dd>

O loopback multicast está desabilitado. Isso significa que dois aplicativos no mesmo computador que ingressam no mesmo grupo de multicast podem obter os pacotes uns dos outros.

</dd> <dt>

<span id="MM_FULL_LOOPBACK"></span><span id="mm_full_loopback"></span>**\_auto-retorno completo \_ mm**
</dt> <dd>

Todos os pacotes enviados também são reproduzidos em loop. Esse modo é útil apenas para teste.

</dd> <dt>

<span id="MM_SELECTIVE_LOOPBACK"></span><span id="mm_selective_loopback"></span>**\_loopback seletivo \_ mm**
</dt> <dd>

O loopback seletivo está habilitado. Isso significa que vários aplicativos habilitados em um computador podem ingressar no mesmo grupo de multicast sem confusão. Os pacotes são reproduzidos em loop da pilha e cada sessão RTP é responsável por filtrar pacotes indesejados.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMulticastControl:: obter \_ loopbackmode**](imulticastcontrol-get-loopbackmode.md)
</dt> <dt>

[**IMulticastControl::p UT \_ loopbackmode**](imulticastcontrol-put-loopbackmode.md)
</dt> </dl>

 

 




