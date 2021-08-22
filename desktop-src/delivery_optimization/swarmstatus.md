---
title: Enumeração SwarmStatus (Deliveryoptimization. h)
description: Define o status de um arquivo dentro do cliente de otimização de entrega.
ms.assetid: D40ABDD3-5573-4A8D-8608-4CB0F396CCAD
keywords:
- Enumeração SwarmStatus
topic_type:
- apiref
api_name:
- SwarmStatus
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3a0f18d9e3344e05348bba0e972a18b7bf64df5edf41fde1cabc3f6a5b106d11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118541941"
---
# <a name="swarmstatus-enumeration"></a>Enumeração SwarmStatus

Define o status de um arquivo dentro do cliente de otimização de entrega.

## <a name="syntax"></a>Syntax


```C++
typedef enum _SwarmStatus { 
  SwarmStatus_Downloading  = 0,
  SwarmStatus_Complete     = 1,
  SwarmStatus_Caching      = 2,
  SwarmStatus_Paused       = 3
} SwarmStatus;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="SwarmStatus_Downloading"></span><span id="swarmstatus_downloading"></span><span id="SWARMSTATUS_DOWNLOADING"></span>**SwarmStatus_Downloading**
</dt> <dd>

O arquivo está sendo baixado.

</dd> <dt>

<span id="SwarmStatus_Complete"></span><span id="swarmstatus_complete"></span><span id="SWARMSTATUS_COMPLETE"></span>**SwarmStatus_Complete**
</dt> <dd>

O download do arquivo foi concluído.

</dd> <dt>

<span id="SwarmStatus_Caching"></span><span id="swarmstatus_caching"></span><span id="SWARMSTATUS_CACHING"></span>**SwarmStatus_Caching**
</dt> <dd>

O arquivo está sendo armazenado em cache.

</dd> <dt>

<span id="SwarmStatus_Paused"></span><span id="swarmstatus_paused"></span><span id="SWARMSTATUS_PAUSED"></span>**SwarmStatus_Paused**
</dt> <dd>

O download do arquivo está em pausa.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, \[ somente aplicativos da área de trabalho da versão 1709\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows Servidor, versão 1709 \[ aplicativos da área de trabalho\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



 

 





