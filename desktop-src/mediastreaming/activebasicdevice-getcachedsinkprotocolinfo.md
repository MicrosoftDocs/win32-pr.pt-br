---
title: Método ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice.h)
description: Obtém as informações de protocolo do sink armazenado em cache para o dispositivo. | Método ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice.h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- API de Streaming de Mídia do método GetCachedSinkProtocolInfo
- Método GetCachedSinkProtocolInfo API de Streaming de Mídia, interface ActiveBasicDevice
- API de Streaming de Mídia da interface ActiveBasicDevice, método GetCachedSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1a9ebda71f59dc4bd887479b5ff9e763844b32985736f8cf224ed4981f04b34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736392"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a>Método ActiveBasicDevice::GetCachedSinkProtocolInfo

Obtém as informações de protocolo do sink armazenado em cache para o dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*value* \[ out, retval\]
</dt> <dd>

As informações de protocolo do sink armazenado em cache para o dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

