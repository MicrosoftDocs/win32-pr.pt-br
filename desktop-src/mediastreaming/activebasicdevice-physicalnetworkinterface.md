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
ms.openlocfilehash: 5bd9eb004607d93b92d502d22b253258bf39e501969e6b3952a58b0a03a1eec1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736202"
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
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

