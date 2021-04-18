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
ms.openlocfilehash: 2be369b34355b199cd47518065724242b9a422e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105766467"
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
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>PlayToDevice. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>PlayToDevice. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

