---
description: Representa a coleção de verbos de um item em uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a coleção.
title: Objeto FolderItemVerbs (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 31badb4b-b89e-4294-9dd7-bda716e163b2
ms.openlocfilehash: 651f439ea34a55203da852f2907a27ba87bdd275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103828301"
---
# <a name="folderitemverbs-object"></a>Objeto FolderItemVerbs

Representa a coleção de verbos de um item em uma pasta do Shell. Este objeto contém propriedades e métodos que permitem que você recupere informações sobre a coleção.

## <a name="members"></a>Membros

O objeto **FolderItemVerbs** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **FolderItemVerbs** tem esses métodos.



| Método                                        | Descrição                                                                                                      |
|:----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](folderitemverbs--newenum.md) | Cria e retorna um novo objeto **FolderItemVerbs** que é uma cópia desse objeto FolderItemVerbs.<br/>   |
| [**Item**](folderitemverbs-item.md)          | Recupera o objeto [**FolderItemVerb**](folderitemverb.md) para um item especificado na coleção.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **FolderItemVerbs** tem essas propriedades.



| Propriedade                                                      | Tipo de acesso          | Description                                                |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Aplicativo**](folderitemverbs-application.md)<br/> | Somente leitura<br/> | Não implementado.<br/>                                |
| [**Contar**](folderitemverbs-count.md)<br/>             | Somente leitura<br/> | Contém o número de itens na coleção.<br/> |
| [**Pai**](folderitemverbs-parent.md)<br/>           | Somente leitura<br/> | Não implementado.<br/>                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 




