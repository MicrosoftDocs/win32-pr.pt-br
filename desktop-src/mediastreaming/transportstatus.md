---
title: Enumeração TransportStatus
description: Define o status de transporte disponível conforme definido pelas diretrizes de UPnP.
ms.assetid: 6fde82f0-9bc4-4abb-9d10-0000501c2b24
keywords:
- API de streaming de mídia de enumeração TransportStatus
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
ms.openlocfilehash: bb4a9de34f358db96b468dbd3329483a8e09b6b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105814533"
---
# <a name="transportstatus-enumeration"></a>Enumeração TransportStatus

Define o status de transporte disponível conforme definido pelas diretrizes de UPnP.

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

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Conhecidos**
</dt> <dd>

Status do dispositivo errôneo.

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

O status do dispositivo anterior para o status de transporte atual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| INSERI<br/> | <dl> <dt>Windows. Media. streaming. idl (referência Windows. Media. streaming. idl)</dt> </dl> |



 

 





