---
title: Enumeração TransportStatus
description: Define o status de transporte disponível conforme definido pelas Diretrizes de UPnP.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- API de Streaming de Mídia de enumeração TransportStatus
topic_type:
- apiref
api_name:
- TransportStatus
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96b7d3892d0344b166665426c66313da370aed1abbdb80c17037ea6aeb44e46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472992"
---
# <a name="transportstatus-enumeration"></a>Enumeração TransportStatus

Define o status de transporte disponível conforme definido pelas Diretrizes de UPnP.

## <a name="syntax"></a>Syntax


```C++
typedef enum TransportStatus { 
  Unknown        = 0,
  Ok             = 1,
  ErrorOccurred  = 2,
  Last           = 3
} TransportStatus;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido**
</dt> <dd>

Status do dispositivo errado.

</dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>**Okey**
</dt> <dd>

O dispositivo está em um bom status.

</dd> <dt>

<span id="ErrorOccurred"></span><span id="erroroccurred"></span><span id="ERROROCCURRED"></span>**ErrorOccurred**
</dt> <dd>

Ocorreu um erro no dispositivo.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Última**
</dt> <dd>

O status anterior do dispositivo para o status de transporte atual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Windows. Media.Streaming.idl (referência Windows. Media.Streaming.idl)</dt> </dl> |



 

 





