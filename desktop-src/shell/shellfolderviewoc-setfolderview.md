---
description: Encaminha os eventos do objeto ShellFolderView especificado para o manipulador de eventos ShellFolderViewOC correspondente.
ms.assetid: 44a2a0a5-aa87-43ae-b4ea-0d301fcb8464
title: Método ShellFolderViewOC. SetFolderView (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderViewOC.SetFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7d331fadbd8abae62ee896caec772d84d079f88d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968118"
---
# <a name="shellfolderviewocsetfolderview-method"></a>Método ShellFolderViewOC. SetFolderView

Encaminha os eventos do objeto [**ShellFolderView**](shellfolderview.md) especificado para o manipulador de eventos [**ShellFolderViewOC**](shellfolderviewoc-object.md) correspondente.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = ShellFolderViewOC.SetFolderView(
  oShellFolderView
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*oShellFolderView* \[ no\]
</dt> <dd>

Tipo: **[**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) \** _

Um objeto [_ *ShellFolderView* *](shellfolderview.md) . Seus eventos [**EnumDone**](shellfolderviewoc-enumdone.md) e [**SelectionChanged**](shellfolderview-selectionchanged.md) serão encaminhados para o manipulador de eventos [**ShellFolderViewOC**](shellfolderviewoc-object.md) correspondente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 
