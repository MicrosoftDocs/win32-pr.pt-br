---
title: Método ActiveBasicDevice SetCachedBitrateMeasurement (PlayToDevice. h)
description: Define a taxa de bits armazenada em cache.
ms.assetid: 53530217-CFF7-4376-B155-E11044621E2D
keywords:
- API de streaming de mídia do método SetCachedBitrateMeasurement
- API de streaming de mídia do método SetCachedBitrateMeasurement, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, método SetCachedBitrateMeasurement
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
ms.openlocfilehash: c681776b00eb9d911a4fa75a9d360b39a3d2b8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455899"
---
# <a name="activebasicdevicesetcachedbitratemeasurement-method"></a>Método ActiveBasicDevice:: SetCachedBitrateMeasurement

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

*physicalNetworkInterface* \[ no\]
</dt> <dd>

Especifica a interface de rede física.

</dd> <dt>

*taxa de bits* \[ no\]
</dt> <dd>

O valor para o qual definir a taxa de bits.

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

 

