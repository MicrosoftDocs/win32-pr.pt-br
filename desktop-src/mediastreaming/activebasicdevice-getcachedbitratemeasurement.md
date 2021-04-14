---
title: Método ActiveBasicDevice GetCachedBitrateMeasurement (PlayToDevice. h)
description: Obtém a taxa de bits armazenada em cache.
ms.assetid: 78C3C5D7-C46B-413D-BC18-C3861E5FDAA5
keywords:
- API de streaming de mídia do método GetCachedBitrateMeasurement
- API de streaming de mídia do método GetCachedBitrateMeasurement, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, método GetCachedBitrateMeasurement
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
ms.openlocfilehash: d15b38ba2730d2023b09c2fa0352ade1f1532724
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499682"
---
# <a name="activebasicdevicegetcachedbitratemeasurement-method"></a>Método ActiveBasicDevice:: GetCachedBitrateMeasurement

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

*physicalNetworkInterface* \[ no\]
</dt> <dd>

Especifica a interface de rede física.

</dd> <dt>

*taxa de bits* \[ out, retval\]
</dt> <dd>

Recebe o valor de taxa de bits.

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

 

