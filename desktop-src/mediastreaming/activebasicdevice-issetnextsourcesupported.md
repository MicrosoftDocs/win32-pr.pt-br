---
title: Propriedade ActiveBasicDevice IsSetNextSourceSupported (PlayToDevice. h)
description: Obtém um valor que indica se há suporte para a configuração da próxima fonte.
ms.assetid: 0888A737-D2CC-4259-BC60-9D2B8E8302A0
keywords:
- API de streaming de mídia de propriedade IsSetNextSourceSupported
- API de streaming de mídia de propriedade IsSetNextSourceSupported, interface ActiveBasicDevice
- API de streaming de mídia da interface ActiveBasicDevice, Propriedade IsSetNextSourceSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSetNextSourceSupported
- ActiveBasicDevice.get_IsSetNextSourceSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b84190336678e677ad3f0436d7233a49d4587574
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812334"
---
# <a name="activebasicdeviceissetnextsourcesupported-property"></a>Propriedade ActiveBasicDevice:: IsSetNextSourceSupported

Obtém um valor que indica se há suporte para a configuração da próxima fonte.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_IsSetNextSourceSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para um **booliano** que indica se há suporte para a configuração da próxima fonte.

**true** se a configuração da próxima fonte for suportada; caso contrário, **false**.

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

 

