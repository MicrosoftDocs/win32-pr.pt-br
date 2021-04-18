---
title: Método ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
description: Obtém as informações do protocolo de coletor em cache para o dispositivo. | Método ActiveBasicDevice GetCachedSinkProtocolInfo (PlayToDevice. h)
ms.assetid: C6A3C4B5-1883-4E71-83D2-11E378A4FBCA
keywords:
- API de streaming de mídia do método GetCachedSinkProtocolInfo
- API de streaming de mídia do método GetCachedSinkProtocolInfo, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, método GetCachedSinkProtocolInfo
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
ms.openlocfilehash: 056cc351a1ecd1c8eef07d4e994da8e895aa85f8
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105781343"
---
# <a name="activebasicdevicegetcachedsinkprotocolinfo-method"></a>Método ActiveBasicDevice:: GetCachedSinkProtocolInfo

Obtém as informações do protocolo de coletor em cache para o dispositivo.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCachedSinkProtocolInfo(
  [out, retval] HSTRING *value
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*valor* \[ do out, retval\]
</dt> <dd>

As informações do protocolo de coletor em cache para o dispositivo.

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

 

