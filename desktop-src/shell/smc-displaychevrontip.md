---
description: Notifica você de que uma infotip está prestes a ser exibida para a divisa associada ao item especificado pela estrutura SMDATA que o acompanha.
title: SMC_DISPLAYCHEVRONTIP mensagem (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: e4ec4839-e49a-4563-9bc9-79f9d4d54658
api_name:
- SMC_DISPLAYCHEVRONTIP
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f1107af5cd621bafbc1e463101cee2ea57236b9d29844d6183963134b50ce3ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968165"
---
# <a name="smc_displaychevrontip-message"></a>Mensagem SMC \_ DISPLAY LTDRONTIP

Notifica você de que uma infotip está prestes a ser exibida para a divisa associada ao item especificado pela estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) que o acompanha.


```C++
SMC_DISPLAYCHEVRONTIP
            
```



## <a name="parameters"></a>Parâmetros

Essa mensagem não tem parâmetros.

## <a name="return-value"></a>Valor retornado

Retorne S \_ OK para exibir a infotip. Retornar S \_ FALSE para impedir que o infotip seja exibido.

## <a name="remarks"></a>Comentários

Essa notificação é recebida pelo [**método IShellMenuCallback::CallbackSM.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 




