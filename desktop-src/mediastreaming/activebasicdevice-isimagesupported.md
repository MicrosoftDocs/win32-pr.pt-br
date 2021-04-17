---
title: Propriedade ActiveBasicDevice IsImageSupported (PlayToDevice. h)
description: Obtém um valor que indica se o dispositivo dá suporte a imagens.
ms.assetid: FC53B87C-D739-4AD4-9DD3-415AC8692224
keywords:
- API de streaming de mídia de propriedade IsImageSupported
- API de streaming de mídia de propriedade IsImageSupported, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade IsImageSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsImageSupported
- ActiveBasicDevice.get_IsImageSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2e90f51d2dd59ffec8221787b9ee7c247536abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105797524"
---
# <a name="activebasicdeviceisimagesupported-property"></a>Propriedade ActiveBasicDevice:: IsImageSupported

Obtém um valor que indica se o dispositivo dá suporte a imagens.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_IsImageSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para um **booliano** que indica se o dispositivo dá suporte a imagens.

**true** se o dispositivo der suporte a imagens; caso contrário, **false**.

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

 

