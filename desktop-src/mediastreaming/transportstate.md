---
title: Enumeração TransportState
description: Define os estados de transporte disponíveis, conforme definido pelas Diretrizes de UPnP.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- API de Streaming de Mídia de enumeração TransportState
topic_type:
- apiref
api_name:
- TransportState
api_location:
- Windows.Media.Streaming.idl
api_type:
- IDLDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a21fc8d0f2799cfba734d605d0c4d2835744ddeb130327ea39a22090d13464f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119663086"
---
# <a name="transportstate-enumeration"></a>Enumeração TransportState

Define os estados de transporte disponíveis, conforme definido pelas Diretrizes de UPnP.

## <a name="syntax"></a>Syntax


```C++
typedef enum _TransportState { 
  Unknown         = 0,
  Stopped         = 1,
  Playing         = 2,
  Transitioning   = 3,
  Paused          = 4,
  Recording       = 5,
  NoMediaPresent  = 6,
  Last            = 7
} TransportState;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido**
</dt> <dd>

Estado do dispositivo errado.

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parou**
</dt> <dd>

O transporte do dispositivo está em um estado parado.

</dd> <dt>

<span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Jogar**
</dt> <dd>

O transporte do dispositivo está em um estado de reprodução.

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição**
</dt> <dd>

O transporte do dispositivo está em um estado de transição que resultará em outro valor de estado.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Pausado**
</dt> <dd>

O transporte do dispositivo está em um estado de pausa.

</dd> <dt>

<span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Gravação**
</dt> <dd>

O transporte do dispositivo está em um estado de gravação.

</dd> <dt>

<span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**
</dt> <dd>

O transporte do dispositivo não tem um URI definido para reprodução.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Última**
</dt> <dd>

O estado anterior do dispositivo para o estado de transporte atual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Idl<br/> | <dl> <dt>Windows. Media.Streaming.idl (referência Windows. Media.Streaming.idl)</dt> </dl> |



 

 





