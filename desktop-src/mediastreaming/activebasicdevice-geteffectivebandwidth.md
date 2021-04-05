---
title: Método ActiveBasicDevice GetEffectiveBandwidth (PlayToDevice. h)
description: Obtém a largura de banda efetiva atual do dispositivo.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- API de streaming de mídia do método GetEffectiveBandwidth
- API de streaming de mídia do método GetEffectiveBandwidth, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, método GetEffectiveBandwidth
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetEffectiveBandwidth
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05a97e9f1dc77040d4f55bc8997e553e0cdc5239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009719"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a>Método ActiveBasicDevice:: GetEffectiveBandwidth

Obtém a largura de banda efetiva atual do dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*transmitSpeed* \[ no, retval\]
</dt> <dd>

Especifica se a velocidade de transmissão é recuperada ou se a velocidade de recebimento é recuperada.

**true** para recuperar a velocidade de transmissão. **false** para recuperar a velocidade de recebimento.

</dd> <dt>

*currentSpeed* \[ fora\]
</dt> <dd>

Recebe a largura de banda efetiva atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

