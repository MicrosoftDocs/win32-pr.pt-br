---
title: Enumeração de TransportState
description: Define os Estados de transporte disponíveis, conforme definido pelas diretrizes de UPnP.
ms.assetid: 2F942EAC-514B-4E65-A12F-85558E9A96A0
keywords:
- API de streaming de mídia de enumeração de transportestate
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
ms.openlocfilehash: 865d7e0f6a96727915833bb402860cde661162f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771460"
---
# <a name="transportstate-enumeration"></a>Enumeração de TransportState

Define os Estados de transporte disponíveis, conforme definido pelas diretrizes de UPnP.

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

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Conhecidos**
</dt> <dd>

Estado do dispositivo errado.

</dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Interrompido**
</dt> <dd>

O transporte do dispositivo s está em um estado parado.

</dd> <dt>

<span id="Playing"></span><span id="playing"></span><span id="PLAYING"></span>**Jogando**
</dt> <dd>

O transporte do dispositivo está em estado de execução.

</dd> <dt>

<span id="Transitioning"></span><span id="transitioning"></span><span id="TRANSITIONING"></span>**Transição**
</dt> <dd>

O transporte do dispositivo s está em um estado de transição, o que resultará em outro valor de estado.

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Em pausa**
</dt> <dd>

O transporte do dispositivo s está em um estado de pausa.

</dd> <dt>

<span id="Recording"></span><span id="recording"></span><span id="RECORDING"></span>**Registra**
</dt> <dd>

O transporte do dispositivo s está em um estado de gravação.

</dd> <dt>

<span id="NoMediaPresent"></span><span id="nomediapresent"></span><span id="NOMEDIAPRESENT"></span>**NoMediaPresent**
</dt> <dd>

O transporte do dispositivo s não tem um URI definido para reprodução.

</dd> <dt>

<span id="Last"></span><span id="last"></span><span id="LAST"></span>**Última**
</dt> <dd>

O estado anterior do dispositivo para o estado de transporte atual.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| INSERI<br/> | <dl> <dt>Windows. Media. streaming. idl (referência Windows. Media. streaming. idl)</dt> </dl> |



 

 





