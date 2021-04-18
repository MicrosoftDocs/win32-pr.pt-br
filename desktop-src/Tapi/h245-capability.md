---
description: A \_ enumeração de recursos H245 descreve o suporte a formatos de áudio e vídeo.
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: Enumeração de H245_CAPABILITY (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7a6f81f87480f221f87680d9cf086120deb2de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792629"
---
# <a name="h245_capability-enumeration"></a>\_Enumeração de recursos H245

\[**H245 \_ A funcionalidade** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A enumeração de **\_ recursos H245** descreve o suporte a formatos de áudio e vídeo.

## <a name="syntax"></a>Syntax


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="HC_G711"></span><span id="hc_g711"></span>**\_G711 HC**
</dt> <dd>

Há suporte para o protocolo de áudio G. 711.

</dd> <dt>

<span id="HC_G723"></span><span id="hc_g723"></span>**\_G723 HC**
</dt> <dd>

Há suporte para o protocolo de áudio G. 723.

</dd> <dt>

<span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**\_H263QCIF HC**
</dt> <dd>

Há suporte para o protocolo de vídeo H. 263.

</dd> <dt>

<span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**\_H261QCIF HC**
</dt> <dd>

Há suporte para o protocolo de vídeo H. 263.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>H323priv. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IH323LineEx::SetDefaultCapabilityPreferrence**](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




