---
description: Notifica sobre um novo item, conforme especificado pela estrutura SMDATA que o acompanha.
title: Mensagem de SMC_NEWITEM (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e0ccf2db-cb46-469f-bc08-4b5100a410ba
api_name:
- SMC_NEWITEM
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ebd8f1b6454a2fb592374b860811ebfc7a14f09d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968052"
---
# <a name="smc_newitem-message"></a>Mensagem do SMC \_ NEWITEM

Notifica sobre um novo item, conforme especificado pela estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) que o acompanha.


```C++
SMC_NEWITEM
            
```



## <a name="parameters"></a>Parâmetros

Esta mensagem não tem parâmetros.

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



 

 




