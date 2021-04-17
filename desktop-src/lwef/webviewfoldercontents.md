---
title: Objeto WebViewFolderContents (Shldisp.h)
description: Implementado pelo shell para uso dentro de uma WebView.
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents, descritos
topic_type:
- apiref
api_name:
- WebViewFolderContents
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a9ea2020e2d9baaffbc026692faafc702db14781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812017"
---
# <a name="webviewfoldercontents-object"></a>Objeto WebViewFolderContents

Implementado pelo shell para uso dentro de uma *WebView*. **WebViewFolderContents** se inicializa automaticamente para a pasta atual da WebView. Ele cria um modo de exibição de pasta do shell que exibe o conteúdo da pasta em um dos cinco formatos: ícone pequeno, ícone grande, lista, detalhes ou miniatura. Ele não é válido fora de uma WebView.

Os métodos e as propriedades expostas por **WebViewFolderContents** são idênticos aos do objeto [**ShellFolderView**](/windows/desktop/shell/shellfolderview) .

## <a name="members"></a>Membros

O objeto **WebViewFolderContents** tem estes tipos de membros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="events"></a>Eventos

O objeto **WebViewFolderContents** tem esses eventos.



| Evento                                                              | Descrição                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](webviewfoldercontents-selectionchanged.md) | Ocorre quando o estado de seleção de qualquer item ou itens na exibição é alterado.<br/> |



 

### <a name="methods"></a>Métodos

O objeto **WebViewFolderContents** tem esses métodos.



| Método                                                       | Descrição                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**PopupItemMenu**](webviewfoldercontents-popupitemmenu.md) | Cria um menu de atalho para o item especificado e retorna a cadeia de caracteres de comando selecionada.<br/>                   |
| [**SelectedItems**](webviewfoldercontents-selecteditems.md) | Obtém um objeto [**FolderItems**](../shell/folderitems.md) que representa todos os itens selecionados na exibição.<br/> |
| [**SelectItem**](webviewfoldercontents-selectitem.md)       | Define o estado de seleção de um item na exibição.<br/>                                                          |



 

### <a name="properties"></a>Propriedades

O objeto **WebViewFolderContents** tem essas propriedades.



| Propriedade                                                            | Tipo de acesso          | Descrição                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Aplicativo**](webviewfoldercontents-application.md)<br/> | Somente leitura<br/> | Não implementado.<br/>                                                                                                              |
| [**FocusedItem**](webviewfoldercontents-focuseditem.md)<br/> | Somente leitura<br/> | Obtém um objeto [**FolderItem**](../shell/folderitem.md) que representa o item que tem o foco de entrada.<br/>                           |
| [**Pasta**](webviewfoldercontents-folder.md)<br/>           | Somente leitura<br/> | Obtém um objeto [**Folder**](../shell/folder.md) que representa a exibição.<br/>                                                            |
| [**Pai**](webviewfoldercontents-parent.md)<br/>           | Somente leitura<br/> | Não implementado.<br/>                                                                                                              |
| [**Script**](webviewfoldercontents-script.md)<br/>           | Somente leitura<br/> | Obtém o objeto de script para a exibição.<br/>                                                                                       |
| [**Exibiroptions**](webviewfoldercontents-viewoptions.md)<br/> | Somente leitura<br/> | Obtém um conjunto de sinalizadores [**ShellFolderViewOptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) que indicam as opções atuais da exibição.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

