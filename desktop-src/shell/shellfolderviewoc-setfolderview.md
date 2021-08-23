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
ms.openlocfilehash: 41a37d1b8f9874bdddd5a9593e0eade8bc0b5b92d30f8ada4ee9c6295af1d632
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118968395"
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

Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\***

Um objeto [**ShellFolderView**](shellfolderview.md) . Seus eventos [**EnumDone**](shellfolderviewoc-enumdone.md) e [**SelectionChanged**](shellfolderview-selectionchanged.md) serão encaminhados para o manipulador de eventos [**ShellFolderViewOC**](shellfolderviewoc-object.md) correspondente.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 
