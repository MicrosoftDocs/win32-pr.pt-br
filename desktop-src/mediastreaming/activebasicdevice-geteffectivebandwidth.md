---
title: Método ActiveBasicDevice GetEffectiveBandwidth (PlayToDevice.h)
description: Obtém a largura de banda efetiva atual para o dispositivo.
ms.assetid: 88CE03AB-6F87-4E43-B673-2C693D351F10
keywords:
- API de Streaming de Mídia do método GetEffectiveBandwidth
- Método GetEffectiveBandwidth API de Streaming de Mídia, interface ActiveBasicDevice
- API de Streaming de Mídia da interface ActiveBasicDevice, método GetEffectiveBandwidth
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
ms.openlocfilehash: 7ac51318997e80c043e36dc87b052a5e21bf9933f93e34f2e5071fb20d4bb75b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236778"
---
# <a name="activebasicdevicegeteffectivebandwidth-method"></a>Método ActiveBasicDevice::GetEffectiveBandwidth

Obtém a largura de banda efetiva atual para o dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetEffectiveBandwidth(
  [in, retval] boolean transmitSpeed,
  [out]        ULONG64 *currentSpeed
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*transmitSpeed* \[ in, retval\]
</dt> <dd>

Especifica se a velocidade de transmissão é recuperada ou se a velocidade de recebimento é recuperada.

**true** para recuperar a velocidade de transmissão. **false** para recuperar a velocidade de recebimento.

</dd> <dt>

*currentSpeed* \[ out\]
</dt> <dd>

Recebe a largura de banda efetiva atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Veja também

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

