---
description: Obtém o tempo restante antes de uma operação de suspensão de aplicativo atrasado continuar.
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: ISuspendingOperation::D Propriedade Ora (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.Deadline
- ISuspendingOperation.get_Deadline
- ISuspendingOperation.put_Deadline
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 305610108b7a138693ccdce97e35ddbe90451806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920916"
---
# <a name="isuspendingoperationdeadline-property"></a>ISuspendingOperation: Propriedade Ora de:D

Obtém o tempo restante antes de uma operação de suspensão de aplicativo atrasado continuar.

Esta propriedade é de leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Deadline();

HRESULT get_Deadline(
  [out, retval] DateTime *value
);
```



## <a name="property-value"></a>Valor da propriedade

O tempo restante antes que uma operação de suspensão de aplicativo adiada continue.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| parâmetro<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 




