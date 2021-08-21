---
description: O método GetRange recupera o intervalo de valores válidos para uma determinada propriedade de dispositivo de áudio.
ms.assetid: df8985f4-8153-4f32-a90c-a5eb7c76b3c7
title: Método ITAudioDeviceControl::GetRange (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87779131dea5bb01a1575074e4f019dbfa2a62addebf5b91a7eee6e9cc041710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003443"
---
# <a name="itaudiodevicecontrolgetrange-method"></a>Método ITAudioDeviceControl::GetRange

\[Esse método não está disponível para uso no Windows Vista, Windows Server 2008 e versões subsequentes do sistema operacional. A API do Cliente RTC fornece funcionalidade semelhante.\]

O **método GetRange** recupera o intervalo de valores válidos para uma determinada propriedade [**de dispositivo de áudio**](audiodeviceproperty.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Propriedade* \[ Em\]
</dt> <dd>

Membro da [**enum AudioDeviceProperty.**](audiodeviceproperty.md)

</dd> <dt>

*plMin* \[ out\]
</dt> <dd>

Valor mínimo válido para a propriedade de entrada.

</dd> <dt>

*plMax* \[ out\]
</dt> <dd>

Valor máximo válido para a propriedade de entrada.

</dd> <dt>

*plSteppingDelta* \[ out\]
</dt> <dd>

Incremente pelo qual o valor da propriedade pode ser aumentado ou reduzido.

</dd> <dt>

*plDefault* \[ out\]
</dt> <dd>

Valor padrão para o *parâmetro* Property.

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

 

 




