---
title: Propriedade ActiveBasicDevice LogicalNetworkInterface (PlayToDevice. h)
description: Obtém a ID da interface de rede lógica.
ms.assetid: 47C2E0BE-D3E3-4A9F-9FC6-873882811506
keywords:
- API de streaming de mídia de propriedade LogicalNetworkInterface
- API de streaming de mídia de propriedade LogicalNetworkInterface, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade LogicalNetworkInterface
topic_type:
- apiref
api_name:
- ActiveBasicDevice.LogicalNetworkInterface
- ActiveBasicDevice.get_LogicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95a87f2951ea09a0bba3d56da50b8f77a9d4a980
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369541"
---
# <a name="activebasicdevicelogicalnetworkinterface-property"></a>Propriedade ActiveBasicDevice:: LogicalNetworkInterface

Obtém a ID da interface de rede lógica.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_LogicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para um **GUID** que especifica a ID da interface de rede lógica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

