---
title: Enumeração DeviceTypes
description: Descreve os tipos de dispositivo DLNA que são suportados pela API de streaming de mídia.
ms.assetid: ec6bbc1f-653a-414c-b458-1a5e1b101781
keywords:
- API de streaming de mídia de enumeração DeviceTypes
topic_type:
- apiref
api_name:
- DeviceTypes
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9caf60fa5736f9db442da5787746a49f71c61c89
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105798047"
---
# <a name="devicetypes-enumeration"></a>Enumeração DeviceTypes

Descreve os tipos de dispositivo DLNA que são suportados pela API de streaming de mídia.

## <a name="syntax"></a>Syntax


```C++
typedef enum DeviceTypes { 
  Unknown               = 0x0,
  DigitalMediaRenderer  = 0x1,
  DigitalMediaServer    = 0x2,
  DigitalMediaPlayer    = 0x4
} DeviceTypes;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Conhecidos**
</dt> <dd>

Tipo de dispositivo desconhecido.

</dd> <dt>

<span id="DigitalMediaRenderer"></span><span id="digitalmediarenderer"></span><span id="DIGITALMEDIARENDERER"></span>**DigitalMediaRenderer**
</dt> <dd>

DMR (processador de mídia digital DLNA). O valor é equivalente ao tipo de dispositivo **urn: schemas-UPnP-org: Device: MediaRenderer: 1**.

</dd> <dt>

<span id="DigitalMediaServer"></span><span id="digitalmediaserver"></span><span id="DIGITALMEDIASERVER"></span>**DigitalMediaServer**
</dt> <dd>

Servidor de mídia digital DLNA (DMS). O valor é equivalente ao tipo de dispositivo **urn: schemas-UPnP-org: Device: MediaServer: 1**.

</dd> <dt>

<span id="DigitalMediaPlayer"></span><span id="digitalmediaplayer"></span><span id="DIGITALMEDIAPLAYER"></span>**DigitalMediaPlayer**
</dt> <dd>

Player de mídia digital DLNA

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| INSERI<br/> | <dl> <dt>Windows. Media. streaming. idl (referência Windows. Media. streaming. idl)</dt> </dl> |



 

 





