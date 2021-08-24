---
title: Enumeração ConnectionStatus
description: Representa o estado do dispositivo na rede como visto pela última vez.
ms.assetid: e1893a59-ce7d-4e9c-a013-02ac916d4ee8
keywords:
- API de streaming de mídia de enumeração ConnectionStatus
topic_type:
- apiref
api_name:
- ConnectionStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8617012abe75d213e0de7be70811152315a888693c7336ef58cd34ceb98eba55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721246"
---
# <a name="connectionstatus-enumeration"></a>Enumeração ConnectionStatus

Representa o estado do dispositivo na rede como visto pela última vez.

## <a name="syntax"></a>Syntax


```C++
typedef enum ConnectionStatus { 
  Online    = 0,
  Offline   = 1,
  Sleeping  = 2
} ConnectionStatus;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="Online"></span><span id="online"></span><span id="ONLINE"></span>**Conectar**
</dt> <dd>

O dispositivo está online e ativo na rede.

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Está**
</dt> <dd>

O dispositivo está offline.

</dd> <dt>

<span id="Sleeping"></span><span id="sleeping"></span><span id="SLEEPING"></span>**Dormindo**
</dt> <dd>

O dispositivo está offline no momento, mas pode ser ativado automaticamente quando for feita uma tentativa de comunicação com ele.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| INSERI<br/> | <dl> <dt>Windows. Media. streaming. idl (Windows de referência. Media. streaming. idl)</dt> </dl> |



 

 





