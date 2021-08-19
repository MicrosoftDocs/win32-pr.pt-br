---
description: O método Get recupera o valor de uma determinada propriedade de dispositivo de áudio.
ms.assetid: 34cb3f3e-be4a-49e0-bf7d-6915906e2368
title: Método ITAudioDeviceControl::Get (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2877b48eab2ecab6259a034c9d74f4c32b9fae9233f5ceb0a0a409f43add014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118865779"
---
# <a name="itaudiodevicecontrolget-method"></a>Método ITAudioDeviceControl::Get

\[Esse método não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método Get** recupera o valor de uma determinada propriedade de dispositivo de [**áudio**](audiodeviceproperty.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Call(
  [out] ITCallInfo **ppCall
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Propriedade* \[ Em\]
</dt> <dd>

Membro da [**enum AudioDeviceProperty.**](audiodeviceproperty.md)

</dd> <dt>

*plValue* \[ out\]
</dt> <dd>

Valor da propriedade de *entrada*.

</dd> <dt>

*plFlags* \[ out\]
</dt> <dd>

Valor da [**enum TAPIControlFlags**](tapicontrolflags.md) que indica como o *valor property* é controlado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método pode retornar um desses valores.



| Código de retorno                                                                                   | Descrição                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | O método foi bem-sucedido.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Há memória insuficiente para executar a operação.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|--------------------------------------------------------------------------------------|
| Versão do TAPI<br/> | Requer TAPI 3.1<br/>                                                         |
| Cabeçalho<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITAudioDeviceControl**](itaudiodevicecontrol.md)
</dt> <dt>

[**TAPIControlFlags**](tapicontrolflags.md)
</dt> <dt>

[**AudioDeviceProperty**](audiodeviceproperty.md)
</dt> </dl>

 

 




