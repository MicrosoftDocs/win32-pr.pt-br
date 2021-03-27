---
description: Solicita informações sobre um item de menu de pasta do Shell.
title: Mensagem de SMC_GETSFINFO (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4459670c-f0fd-4ae8-8a1f-810e1dcac713
api_name:
- SMC_GETSFINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f3a02b61565eb08f623978900d6ce47e30eea85e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104989022"
---
# <a name="smc_getsfinfo-message"></a>Mensagem do SMC \_ GETSFINFO

Solicita informações sobre um item de menu de pasta do Shell.


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*psminfo* 
</dt> <dd>

Ponteiro para uma estrutura [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) . Preencha a estrutura com as informações apropriadas e retorne as S \_ OK.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar S \_ OK.

## <a name="remarks"></a>Comentários

Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 




