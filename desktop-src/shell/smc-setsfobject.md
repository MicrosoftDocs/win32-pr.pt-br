---
description: Notifica você para salvar o objeto passado.
title: Mensagem de SMC_SETSFOBJECT (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: f7e2cf12-7f09-45b0-97d3-eed803e57d9f
api_name:
- SMC_SETSFOBJECT
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4ac46fd69d4d91870dcd288190baac275b37a5f093b87646c17d19e479bd710e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968005"
---
# <a name="smc_setsfobject-message"></a>Mensagem do SMC \_ SETSFOBJECT

Notifica você para salvar o objeto passado.


```C++
SMC_GETOBJECT 
    wParam = (WPARAM) (REFIID) iid;
    lParam = (LPARAM) (void **) pv
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*IID* 
</dt> <dd>

O IID associado ao objeto.

</dd> <dt>

*PV* 
</dt> <dd>

Um ponteiro da interface no objeto especificado por *IID*.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar S \_ OK.

## <a name="remarks"></a>Comentários

Essa notificação é recebida pelo método [**IShellMenuCallback:: CallbackSM**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellmenucallback-callbacksm) .

A notificação do **SMC \_ SETSFOBJECT** é usada com o fluxo de IID \_ . O objeto é salvo em um formulário persistente no registro e nada é feito com a contagem de referência no objeto passado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



 

 




