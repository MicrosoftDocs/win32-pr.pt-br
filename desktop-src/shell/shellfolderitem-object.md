---
description: Estende o objeto FolderItem. Além das propriedades e métodos com suporte do FolderItem, ShellFolderItem tem dois métodos adicionais.
title: Objeto ShellFolderItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0e2f4c91-f9f9-4daa-a801-9c7fea8af738
ms.openlocfilehash: 84e230e295a956f3f83833a577b47be1e46873a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968121"
---
# <a name="shellfolderitem-object"></a>Objeto ShellFolderItem

Estende o objeto [**FolderItem**](folderitem.md) . Além das propriedades e métodos com suporte do **FolderItem**, **ShellFolderItem** tem dois métodos adicionais.

## <a name="members"></a>Membros

O objeto **ShellFolderItem** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

O objeto **ShellFolderItem** tem esses métodos.



| Método                                                       | Descrição                                                                                                                                                                                         |
|:-------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ExtendedProperty**](shellfolderitem-extendedproperty.md) | Obtém o valor de uma propriedade do conjunto de propriedades de um item. A propriedade pode ser especificada por nome ou pelo identificador de formato do conjunto de Propriedades (FMTID) e pelo identificador de propriedade (PID).<br/> |
| [**InvokeVerbEx**](invokeverbex.md)                         | Executa um verbo em um item de Shell.<br/>                                                                                                                                                         |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 




