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
ms.openlocfilehash: ff90cfb0e0297e7d3276f00f314fce865920663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826891"
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 




