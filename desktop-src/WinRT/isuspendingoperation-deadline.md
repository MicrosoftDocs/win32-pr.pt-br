---
description: Obtém o tempo restante antes que uma operação de suspensão de aplicativo atrasada continue.
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: ISuspendingOperation::D eadline (Windows. ApplicationModel.h)
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
ms.openlocfilehash: 448f4d89ec2f1b7e3f68255897b32b3f4cba2ec753ae8f6cc7751c9041b01266
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121496"
---
# <a name="isuspendingoperationdeadline-property"></a>Propriedade ISuspendingOperation::D eadline

Obtém o tempo restante antes que uma operação de suspensão de aplicativo atrasada continue.

Essa propriedade é leitura/gravação.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Deadline();

HRESULT get_Deadline(
  [out, retval] DateTime *value
);
```



## <a name="property-value"></a>Valor da propriedade

O tempo restante antes que uma operação de suspensão de aplicativo atrasada continue.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Windows. ApplicationModel.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Windows. ApplicationModel.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 




