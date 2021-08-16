---
description: Representa os objetos em uma exibição e fornece propriedades e métodos usados para obter informações sobre o conteúdo da exibição.
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: Objeto ShellFolderView (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a95d57edb7992c9511e34480190580d34ad42da23c64c4297f5e4ebb75a95e73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452123"
---
# <a name="shellfolderview-object"></a>Objeto ShellFolderView

Representa os objetos em uma exibição e fornece propriedades e métodos usados para obter informações sobre o conteúdo da exibição.

## <a name="members"></a>Membros

O objeto **ShellFolderView** tem estes tipos de membros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="events"></a>Eventos

O objeto **ShellFolderView** tem esses eventos.



| Evento                                                        | Descrição                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](shellfolderview-selectionchanged.md) | Ocorre quando o estado de seleção de qualquer item ou itens na exibição é alterado.<br/> |



 

### <a name="methods"></a>Métodos

O objeto **ShellFolderView** tem esses métodos.



| Método                                                 | Descrição                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**PopupItemMenu**](shellfolderview-popupitemmenu.md) | Cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.<br/>                 |
| [**SelectedItems**](shellfolderview-selecteditems.md) | Obtém um objeto [**FolderItems**](folderitems.md) que representa todos os itens selecionados na exibição.<br/> |
| [**SelectItem**](shellfolderview-selectitem.md)       | Define o estado de seleção de um item na exibição.<br/>                                                        |



 

### <a name="properties"></a>Propriedades

O objeto **ShellFolderView** tem essas propriedades.



| Propriedade                                                      | Tipo de acesso          | Descrição                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [**Aplicativo**](shellfolderview-application.md)<br/> | Somente leitura<br/> | Contém o objeto de aplicativo do objeto.<br/>                                                         |
| [**FocusedItem**](shellfolderview-focuseditem.md)<br/> | Somente leitura<br/> | Obtém um objeto [**FolderItem**](folderitem.md) que representa o item que tem o foco de entrada.<br/> |
| [**Pasta**](shellfolderview-folder.md)<br/>           | Somente leitura<br/> | Obtém um objeto [**Folder**](folder.md) que representa a exibição.<br/>                                  |
| [**Pai**](shellfolderview-parent.md)<br/>           | Somente leitura<br/> | Não implementado.<br/>                                                                                  |
| [**Script**](shellfolderview-script.md)<br/>           | Somente leitura<br/> | Preterido.<br/>                                                                                       |
| [**Exibiroptions**](shellfolderview-viewoptions.md)<br/> | Somente leitura<br/> | Obtém um conjunto de sinalizadores que indicam as opções atuais da exibição.<br/>                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |
| IID<br/>                      | \_SHELLFOLDERVIEW CLSID<br/>                                                                              |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Sinalizadores de ShellFolderViewOptions**](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 




