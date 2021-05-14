---
description: Representa a coleção de itens em uma pasta shell. Esse objeto contém propriedades e métodos que permitem recuperar informações sobre a coleção.
title: Objeto FolderItems (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b99201b3-95e8-4ddd-b338-dee8d107d0a0
ms.openlocfilehash: 2b6e9506d6c2354018a41ae7a15ca6e8e1900857
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840647"
---
# <a name="folderitems-object"></a>Objeto FolderItems

Representa a coleção de itens em uma pasta shell. Esse objeto contém propriedades e métodos que permitem recuperar informações sobre a coleção.

## <a name="members"></a>Membros

O **objeto FolderItems** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O **objeto FolderItems** tem esses métodos.



| Método                                    | Descrição                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](folderitems--newenum.md) | Não implementado.<br/>                                                                              |
| [**Item**](folderitems-item.md)          | Recupera o [**objeto FolderItem**](folderitem.md) para um item especificado na coleção.<br/> |



 

### <a name="properties"></a>Propriedades

O **objeto FolderItems** tem essas propriedades.



| Propriedade                                                  | Tipo de acesso          | Descrição                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**Aplicativo**](folderitems-application.md)<br/> | Somente leitura<br/> | Contém o [**objeto Application**](folderitems-application.md) da coleção de itens de pasta.<br/> |
| [**Contagem**](folderitems-count.md)<br/>             | Somente leitura<br/> | Contém o número de itens na coleção.<br/>                                                    |
| [**Pai**](folderitems-parent.md)<br/>           | Somente leitura<br/> | Não implementado.<br/>                                                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, somente aplicativos da área de trabalho do Windows XP \[\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 




