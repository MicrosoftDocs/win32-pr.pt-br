---
title: Propriedade ActiveBasicDevice PhysicalNetworkInterface (PlayToDevice. h)
description: Obtém a ID da interface de rede física.
ms.assetid: F426462F-CE26-4EE1-B679-A4C80B2919A5
keywords:
- API de streaming de mídia de propriedade PhysicalNetworkInterface
- API de streaming de mídia de propriedade PhysicalNetworkInterface, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade PhysicalNetworkInterface
topic_type:
- apiref
api_name:
- ActiveBasicDevice.PhysicalNetworkInterface
- ActiveBasicDevice.get_PhysicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 479618ed4d22a3d78a351fb88fcb1108a27c618f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455363"
---
# <a name="activebasicdevicephysicalnetworkinterface-property"></a>ActiveBasicDevice: Propriedade hysicalNetworkInterface de:P

Obtém a ID da interface de rede física.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_PhysicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para um **GUID** que especifica a ID da interface de rede física.

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

 

