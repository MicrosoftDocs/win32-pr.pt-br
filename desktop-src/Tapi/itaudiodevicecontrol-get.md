---
description: O método Get recupera o valor de uma determinada propriedade de dispositivo de áudio.
ms.assetid: 34cb3f3e-be4a-49e0-bf7d-6915906e2368
title: 'Método ITAudioDeviceControl:: Get (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4311dc18291fcfbbe533dbe17042e6ba19c1122
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779906"
---
# <a name="itaudiodevicecontrolget-method"></a>Método ITAudioDeviceControl:: Get

\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **Get** recupera o valor de uma determinada [**propriedade de dispositivo de áudio**](audiodeviceproperty.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Propriedade* \[ no\]
</dt> <dd>

Membro da enumeração [**AudioDeviceProperty**](audiodeviceproperty.md) .

</dd> <dt>

*plValue* \[ fora\]
</dt> <dd>

Valor da *Propriedade* de entrada.

</dd> <dt>

*plFlags* \[ fora\]
</dt> <dd>

Valor da enumeração [**TAPIControlFlags**](tapicontrolflags.md) indicando como o valor da *Propriedade* é controlado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,1<br/>                                                         |
| parâmetro<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITAudioDeviceControl**](itaudiodevicecontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**AudioDeviceProperty**](audiodeviceproperty.md)
</dt> </dl>

 

 




