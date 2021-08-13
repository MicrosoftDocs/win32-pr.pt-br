---
title: Método ActiveBasicDevice GetCachedExtraSinkProtocolInfo (PlayToDevice. h)
description: Obtém informações adicionais do protocolo de coletor armazenado em cache para o dispositivo.
ms.assetid: 97112921-1C1D-4FC9-8FE6-1381F3773351
keywords:
- API de streaming de mídia do método GetCachedExtraSinkProtocolInfo
- API de streaming de mídia do método GetCachedExtraSinkProtocolInfo, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, método GetCachedExtraSinkProtocolInfo
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedExtraSinkProtocolInfo
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf4508c40fd0abcb0df809216a9bae1d8811c8a8bd79bfb31dfbbd5062ddce1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736402"
---
# <a name="activebasicdevicegetcachedextrasinkprotocolinfo-method"></a>Método ActiveBasicDevice:: GetCachedExtraSinkProtocolInfo

Obtém informações adicionais do protocolo de coletor armazenado em cache para o dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCachedExtraSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do out, retval\]
</dt> <dd>

As informações adicionais do protocolo de coletor armazenado em cache para o dispositivo.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem sucedido, ele retornará **S \_ OK**. Caso contrário, ele retorna um código de erro **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

