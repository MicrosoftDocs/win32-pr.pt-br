---
title: Propriedade ActiveBasicDevice IsVideoSupported (PlayToDevice. h)
description: Obtém um valor que indica se o dispositivo dá suporte a vídeo.
ms.assetid: E8D33A04-748D-42F8-878F-35D973A6B559
keywords:
- API de streaming de mídia de propriedade IsVideoSupported
- API de streaming de mídia de propriedade IsVideoSupported, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade IsVideoSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsVideoSupported
- ActiveBasicDevice.get_IsVideoSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bb115aad422546746a44824c847bd0ae80c188264e8539e569a26e16eefa93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972515"
---
# <a name="activebasicdeviceisvideosupported-property"></a>Propriedade ActiveBasicDevice:: IsVideoSupported

Obtém um valor que indica se o dispositivo dá suporte a vídeo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_IsVideoSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para um **booliano** que indica se o dispositivo dá suporte a vídeo.

**true** se o dispositivo der suporte a vídeo; caso contrário, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[Somente aplicativos da área de trabalho R2\]<br/>                                     |
| Cabeçalho<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

