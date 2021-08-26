---
title: Método ActiveBasicDevice SetCachedBitrateMeasurement (PlayToDevice.h)
description: Define a taxa de bits armazenada em cache.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- Api de Streaming de Mídia do método SetCachedBitrateMeasurement
- Método SetCachedBitrateMeasurement API de Streaming de Mídia , interface ActiveBasicDevice
- API de Streaming de Mídia da interface ActiveBasicDevice, método SetCachedBitrateMeasurement
topic_type:
- apiref
api_name:
- ActiveBasicDevice.SetCachedBitrateMeasurement
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adf79b7e9066aacfcce1f82c998463d6d620f5061fef4af788104a0c01a44ee8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952766"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a>Método ActiveBasicDevice::SetCachedBitrateMeasurement

Define a taxa de bits armazenada em cache.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT SetCachedBitrateMeasurement(
  [in] GUID   physicalNetworkInterface,
  [in] UINT64 bitrate
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*physicalNetworkInterface* \[ Em\]
</dt> <dd>

Especifica o interface de rede física.

</dd> <dt>

*taxa de bits* \[ Em\]
</dt> <dd>

O valor para o que definir a taxa de bits.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se esse método for bem-sucedido, ele **retornará S \_ OK.** Caso contrário, ele retornará um **código de erro HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

