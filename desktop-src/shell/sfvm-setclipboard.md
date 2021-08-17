---
description: Notifica o IShellView quando um de seus objetos é colocado na área de transferência como resultado de um comando de menu. Usado pela \_ mensagem SHShellFolderView.
title: Mensagem de SFVM_SETCLIPBOARD (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6a4cf0c5-2349-4e1e-b6c5-ee9b5430456e
api_name:
- SFVM_SETCLIPBOARD
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 99548be90c7f4fb9b840e4d4c6f816710c6e02cc1a888ce0c1c774f73c58f668
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117858208"
---
# <a name="sfvm_setclipboard-message"></a>SFVM \_ mensagem da área de transferência

Notifica o [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) quando um de seus objetos é colocado na área de transferência como resultado de um comando de menu. Usado pela [**\_ mensagem SHShellFolderView**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_SETCLIPBOARD 

    lParam = (DWORD) dwEffect;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*dwEffect* \[ no\]
</dt> <dd>

Use (WPARAM)-2 se o item estiver sendo recortado para a área de transferência ou (WPARAM)-3 se o item estiver sendo copiado para a área de transferência.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




