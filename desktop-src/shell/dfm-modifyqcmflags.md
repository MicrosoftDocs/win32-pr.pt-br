---
description: 'Permite que o retorno de chamada modifique os valores do CFM \_ xxx passados para IContextMenu:: QueryContextMenu.'
title: Mensagem de DFM_MODIFYQCMFLAGS (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 62ce86426b31abfb6dec67d7ee45b01a8bc47ba10c40ce9ed00051dd414a0ffd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119223586"
---
# <a name="dfm_modifyqcmflags-message"></a>\_Mensagem DFM MODIFYQCMFLAGS

Permite que o retorno de chamada modifique os valores do CFM \_ xxx passados para [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*puNewFlags* \[ no\]
</dt> <dd>

Um ponteiro para os novos valores de sinalizador.

</dd> <dt>

*uFlags* \[ no\]
</dt> <dd>

Sinalizadores que especificam como o menu de contexto pode ser alterado. Esse parâmetro usa os valores de CMF \_ xxx descritos em [**IContextMenu:: QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




