---
description: Solicita um ponteiro para um objeto especificado.
title: Mensagem de SMC_GETSFOBJECT (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a8478f10-77ce-4e71-a5dc-89d8a90cf513
api_name:
- SMC_GETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: c7fb57ea8e3f02ce4e773e187310530c14d65515
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170314"
---
# <a name="smc_getsfobject-message"></a>Mensagem do SMC \_ GETSFOBJECT

Solicita um ponteiro para um objeto especificado.


```C++
SMC_GETSFOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IID* 
</dt> <dd>

O IID associado ao objeto solicitado.

</dd> <dt>

*PV* 
</dt> <dd>

Um ponteiro void que recebe um ponteiro para a interface solicitada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar S \_ OK.

## <a name="remarks"></a>Comentários

Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) . É semelhante ao [**SMC \_ GetObject**](smc-getobject.md) , mas usado para itens de pasta do Shell. Crie o objeto solicitado e atribua um ponteiro à interface solicitada para *VP*.

As interfaces a seguir podem ser solicitadas.

-   [**IStream**](/windows/win32/api/objidl/nn-objidl-istream)
-   [**IShellMenu**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenu)
-   [**IShellMenuCallback**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellmenucallback)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 
