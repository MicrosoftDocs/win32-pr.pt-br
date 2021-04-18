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
ms.openlocfilehash: 61368a494e5bff0f6aca575380937b98f9d6b650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105793926"
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
| INSERI<br/> | <dl> <dt>Windows. Media. streaming. idl (referência Windows. Media. streaming. idl)</dt> </dl> |



 

 





