---
description: Executa o item de pasta do Shell especificado na estrutura SMDATA acompanhada.
title: Mensagem de SMC_SFEXEC (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bb8f6434-0936-460f-b7dc-39be58bb70ce
api_name:
- SMC_SFEXEC
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b4e414cd7dab9968882272b19b9b21b95da0f1d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968048"
---
# <a name="smc_sfexec-message"></a>Mensagem do SMC \_ SFEXEC

Executa o item de pasta do Shell especificado na estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) acompanhada.


```C++
SMC_SFEXEC
            
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



 

 




