---
description: Representa um item em uma pasta shell. Esse objeto contém propriedades e métodos que permitem recuperar informações sobre o item.
title: Objeto FolderItem (Shldisp.h)
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
ms.openlocfilehash: f6744441c051d65bd24f2db888f9bc8d71e66cedcf50c097094beee8ae5a96a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715366"
---
# <a name="folderitem-object"></a>Objeto FolderItem

Representa um item em uma pasta shell. Esse objeto contém propriedades e métodos que permitem recuperar informações sobre o item.

## <a name="members"></a>Membros

O **objeto FolderItem** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto FolderItem** tem esses métodos.



| Método                                      | Descrição                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InvokeVerb**](folderitem-invokeverb.md) | Executa um verbo no item.<br/>                                                                                                                     |
| [**Verbos**](folderitem-verbs.md)           | Recupera o objeto [**FolderItemVerbs do**](folderitemverbs.md) item. Esse objeto é a coleção de verbos que podem ser executados no item.<br/> |



 

### <a name="properties"></a>Propriedades

O **objeto FolderItem** tem essas propriedades.



| Propriedade                                                   | Tipo de acesso           | Descrição                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aplicativo**](folderitem-application.md)<br/>   | Somente leitura<br/>  | Contém o [**objeto**](folderitem-application.md) Application do item de pasta.<br/>                                                                                                                   |
| [**Getfolder**](folderitem-getfolder.md)<br/>       | Somente leitura<br/>  | Contém o objeto [**Pasta do**](folder.md) item, se o item for uma pasta.<br/>                                                                                                                           |
| [**GetLink**](folderitem-getlink.md)<br/>           | Somente leitura<br/>  | Contém o objeto [**ShellLinkObject**](shelllinkobject-object.md) do item, se o item for um atalho.<br/>                                                                                                |
| [**IsBrowsable**](folderitem-isbrowsable.md)<br/>   | Somente leitura<br/>  | Indica se o item pode ser hospedado dentro de um navegador ou Windows Explorer quadro.<br/>                                                                                                                         |
| [**IsFileSystem**](folderitem-isfilesystem.md)<br/> | Somente leitura<br/>  | Indica se o item faz parte do sistema de arquivos.<br/>                                                                                                                                                       |
| [**IsFolder**](folderitem-isfolder.md)<br/>         | Somente leitura<br/>  | Indica se o item é uma pasta.<br/>                                                                                                                                                                      |
| [**Islink**](folderitem-islink.md)<br/>             | Somente leitura<br/>  | Indica se o item é um atalho.<br/>                                                                                                                                                               |
| [**ModifyDate**](folderitem-modifydate.md)<br/>     | Leitura/gravação<br/> | Define ou obtém a data e a hora em que um arquivo foi modificado pela última vez. [**ModifyDate**](folderitem-modifydate.md) pode ser usado para recuperar a data e a hora em que uma pasta foi modificada pela última vez, mas não pode defini-la.<br/> |
| [**Nome**](folderitem-name.md)<br/>                 | Leitura/gravação<br/> | Define ou obtém o nome do item.<br/>                                                                                                                                                                           |
| [**Pai**](folderitem-parent.md)<br/>             | Somente leitura<br/>  | Obtém um objeto que representa o pai do item.<br/>                                                                                                                                                  |
| [**Caminho**](folderitem-path.md)<br/>                 | Somente leitura<br/>  | Contém o caminho e o nome completos do item.<br/>                                                                                                                                                                 |
| [**Tamanho**](folderitem-size.md)<br/>                 | Somente leitura<br/>  | Contém o tamanho do item.<br/>                                                                                                                                                                               |
| [**Tipo**](folderitem-type.md)<br/>                 | Somente leitura<br/>  | Contém uma representação de cadeia de caracteres do tipo do item.<br/>                                                                                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 




