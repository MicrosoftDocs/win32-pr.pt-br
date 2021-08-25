---
description: Notifica o IShellView para reorganizar seus itens. Usado pela mensagem SHShellFolderView. \_
title: SFVM_REARRANGE mensagem (Shlobj.h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d745bafc-f2f5-40a1-b7e8-e16e4cf0153d
api_name:
- SFVM_REARRANGE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 03bb5b8d39a85d8ce4fb6e76b75967a642361f502ce3bcb20ca49f276a5221de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941976"
---
# <a name="sfvm_rearrange-message"></a>Mensagem SFVM \_ REORGANIZAR

Notifica o [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) para reorganizar seus itens. Usado pela [**mensagem SHShellFolderView \_**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).


```C++
SFVM_REARRANGE 

    lParam = (LPARAM) lparam;

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* \[ Em\]
</dt> <dd>

Passado para [**IShellFolder::CompareIDs.**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) Consulte [**IShellFolder::CompareIDs para**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) obter mais informações sobre esse parâmetro.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                          |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj.h</dt> </dl> |



 

 




