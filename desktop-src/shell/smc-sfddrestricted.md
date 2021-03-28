---
description: Solicita se é aceitável descartar um objeto de dados no item especificado pela estrutura SMDATA que o acompanha.
ms.assetid: 777bbc7e-6b0f-4627-9d92-4aa8209082ca
title: Mensagem de SMC_SFDDRESTRICTED (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77ae6a852fd342e67edf42429f31eb7e1ba3b566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968049"
---
# <a name="smc_sfddrestricted-message"></a>Mensagem do SMC \_ SFDDRESTRICTED

Solicita se é aceitável descartar um objeto de dados no item especificado pela estrutura [**SMDATA**](/windows/win32/api/shobjidl_core/ns-shobjidl_core-smdata) que o acompanha.


```C++
SMC_SFDDRESTRICTED 
    wParam = (WPARAM) (void **) pDropTarget
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*pDropTarget* 
</dt> <dd>

O endereço de um ponteiro void que recebe um ponteiro para a interface [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) . Defina esse valor como **NULL** se você não quiser aceitar o objeto de dados.

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



 

 
