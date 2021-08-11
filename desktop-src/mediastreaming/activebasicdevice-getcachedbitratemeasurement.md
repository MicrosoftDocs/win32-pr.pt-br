---
title: Método ActiveBasicDevice GetCachedBitrateMeasurement (PlayToDevice.h)
description: Obtém a taxa de bits armazenada em cache.
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- API de Streaming de Mídia do método GetCachedBitrateMeasurement
- Método GetCachedBitrateMeasurement API de Streaming de Mídia, interface ActiveBasicDevice
- API de Streaming de Mídia da interface ActiveBasicDevice, método GetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.GetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 031d77595298651be11c793f8fd96471808ab1aef3f5a2b6398be9c1ff10de02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236861"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a>Método ActiveBasicDevice::GetCachedBitrateMeasurement

Obtém a taxa de bits armazenada em cache.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT GetCachedBitrateMeasurement(
  [in]          GUID   physicalNetworkInterface,
  [out, retval] UINT64 *bitrate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*physicalNetworkInterface* \[ Em\]
</dt> <dd>

Especifica o interface de rede física.

</dd> <dt>

*taxa de bits* \[ out, retval\]
</dt> <dd>

Recebe o valor da taxa de bits.

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

 

