---
description: SMC_GETOBJECT mensagem – solicita um ponteiro para um objeto especificado.
title: SMC_GETOBJECT mensagem (Shobjidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 36e8f304-a92a-485f-8413-b9c416087ec9
api_name:
- SMC_GETOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 693159f44d3b8878e2b70b9878ced5234c51e79110de8771d57a1c59a22feb32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047078"
---
# <a name="smc_getobject-message"></a>Mensagem \_ GETOBJECT do SMC

Solicita um ponteiro para um objeto especificado.


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Iid* 
</dt> <dd>

O IID associado ao objeto solicitado.

</dd> <dt>

*Pv* 
</dt> <dd>

Um ponteiro nulo que recebe um ponteiro para a interface solicitada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar S \_ OK.

## <a name="remarks"></a>Comentários

Essa notificação é recebida pelo [**método IShellMenuCallback::CallbackSM.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) Crie o objeto solicitado e atribua um ponteiro à interface solicitada para *pv.*

As interfaces a seguir podem ser solicitadas.

-   [**IShellMenu**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [**Icontextmenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
-   [**IShellMenuCallback**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)
-   [**Idroptarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Shobjidl.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shobjidl.idl</dt> </dl> |



 

 
