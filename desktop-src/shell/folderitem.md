---
description: Representa um item em uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre o item.
title: Objeto FolderItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.openlocfilehash: a1c66c594a60682ad359ffbcdcd0bf045601051d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457201"
---
# <a name="folderitem-object"></a>Objeto FolderItem

Representa um item em uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre o item.

## <a name="members"></a>Membros

O objeto **FolderItem** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **FolderItem** tem esses métodos.



| Método                                      | Descrição                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InvokeVerb**](folderitem-invokeverb.md) | Executa um verbo no item.<br/>                                                                                                                     |
| [**Verbos**](folderitem-verbs.md)           | Recupera o objeto [**FolderItemVerbs**](folderitemverbs.md) do item. Esse objeto é a coleção de verbos que podem ser executados no item.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **FolderItem** tem essas propriedades.



| Propriedade                                                   | Tipo de acesso           | Description                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aplicativo**](folderitem-application.md)<br/>   | Somente leitura<br/>  | Contém o objeto de [**aplicativo**](folderitem-application.md) do item de pasta.<br/>                                                                                                                   |
| [**GetFolder**](folderitem-getfolder.md)<br/>       | Somente leitura<br/>  | Contém o objeto de [**pasta**](folder.md) do item, se o item for uma pasta.<br/>                                                                                                                           |
| [**GetLink**](folderitem-getlink.md)<br/>           | Somente leitura<br/>  | Contém o objeto [**ShellLinkObject**](shelllinkobject-object.md) do item, se o item for um atalho.<br/>                                                                                                |
| [**Isnavegável**](folderitem-isbrowsable.md)<br/>   | Somente leitura<br/>  | Indica se o item pode ser hospedado dentro de um navegador ou quadro do Windows Explorer.<br/>                                                                                                                         |
| [**Isfilesystem**](folderitem-isfilesystem.md)<br/> | Somente leitura<br/>  | Indica se o item faz parte do sistema de arquivos.<br/>                                                                                                                                                       |
| [**IsFolder**](folderitem-isfolder.md)<br/>         | Somente leitura<br/>  | Indica se o item é uma pasta.<br/>                                                                                                                                                                      |
| [**IsLink**](folderitem-islink.md)<br/>             | Somente leitura<br/>  | Indica se o item é um atalho.<br/>                                                                                                                                                               |
| [**ModifyDate**](folderitem-modifydate.md)<br/>     | Leitura/gravação<br/> | Define ou obtém a data e a hora da última modificação de um arquivo. [**ModifyDate**](folderitem-modifydate.md) pode ser usado para recuperar a data e a hora em que uma pasta foi modificada pela última vez, mas não pode defini-la.<br/> |
| [**Name**](folderitem-name.md)<br/>                 | Leitura/gravação<br/> | Define ou Obtém o nome do item.<br/>                                                                                                                                                                           |
| [**Pai**](folderitem-parent.md)<br/>             | Somente leitura<br/>  | Obtém um objeto que representa o pai do item.<br/>                                                                                                                                                  |
| [**Caminho**](folderitem-path.md)<br/>                 | Somente leitura<br/>  | Contém o caminho e o nome completos do item.<br/>                                                                                                                                                                 |
| [**Tamanho**](folderitem-size.md)<br/>                 | Somente leitura<br/>  | Contém o tamanho do item.<br/>                                                                                                                                                                               |
| [**Tipo**](folderitem-type.md)<br/>                 | Somente leitura<br/>  | Contém uma representação de cadeia de caracteres do tipo do item.<br/>                                                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 




