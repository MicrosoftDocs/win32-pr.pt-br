---
description: O método GetRange recupera o intervalo de valores válidos para uma determinada propriedade de dispositivo de áudio.
ms.assetid: df8985f4-8153-4f32-a90c-a5eb7c76b3c7
title: 'Método ITAudioDeviceControl:: GetRange (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cbf5bf36d4ec754440e1612f2e228c495d165c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811929"
---
# <a name="itaudiodevicecontrolgetrange-method"></a>Método ITAudioDeviceControl:: GetRange

\[ Esse método não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

O método **GetRange** recupera o intervalo de valores válidos para uma determinada [**propriedade de dispositivo de áudio**](audiodeviceproperty.md).

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_Terminal(
  [out] ITTerminal **ppTerminal
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Propriedade* \[ no\]
</dt> <dd>

Membro da enumeração [**AudioDeviceProperty**](audiodeviceproperty.md) .

</dd> <dt>

*plMin* \[ fora\]
</dt> <dd>

Valor mínimo válido para a propriedade de entrada.

</dd> <dt>

*plMax* \[ fora\]
</dt> <dd>

Valor máximo válido para a propriedade de entrada.

</dd> <dt>

*plSteppingDelta* \[ fora\]
</dt> <dd>

Incremento pelo qual o valor da propriedade pode ser aumentado ou diminuído.

</dd> <dt>

*plDefault* \[ fora\]
</dt> <dd>

Valor padrão para o parâmetro *Property* .

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

 

 




