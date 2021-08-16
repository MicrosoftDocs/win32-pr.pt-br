---
description: Solicita informações sobre um item de menu normal.
title: Mensagem de SMC_GETINFO (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 07f35a64-eff0-48e8-a2fc-719ccf1eca18
api_name:
- SMC_GETINFO
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 95f27905a59fd8ce7c84cfc1166b59cb38356934b3603b0cec7f56c2365a3984
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968105"
---
# <a name="smc_getinfo-message"></a>Mensagem do SMC \_ GETinfo

Solicita informações sobre um item de menu normal.


```C++
SMC_GETINFO 
    lParam = (LPARAM) (LPSMINFO) psminfo
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*psminfo* 
</dt> <dd>

Um ponteiro para uma estrutura [**SMINFO**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-sminfo) . Preencha a estrutura com as informações apropriadas e retorne as S \_ OK.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

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



 

 




