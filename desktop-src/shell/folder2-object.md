---
description: Estende o objeto Folder para dar suporte a pastas offline.
title: Objeto Pasta2 (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b52b141-ced3-4d38-8584-7dfcfe12ab56
ms.openlocfilehash: 8db899fc52cc3511d1af82013fc6c4c87544f1cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967931"
---
# <a name="folder2-object"></a>Objeto Pasta2

Estende o objeto [**Folder**](folder.md) para dar suporte a pastas offline.

## <a name="members"></a>Membros

O objeto **Pasta2** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **Pasta2** tem esses métodos.



| Método                                                                 | Descrição                                                                          |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**DismissedWebViewBarricade**](folder2-dismissedwebviewbarricade.md) | Chamado em resposta à exibição da Web Barricade sendo Descartado pelo usuário.<br/> |
| [**Novamente**](folder2-synchronize.md)                             | Sincroniza todos os arquivos offline na pasta.<br/>                             |



 

### <a name="properties"></a>Propriedades

O objeto **Pasta2** tem essas propriedades.



| Propriedade                                                                            | Tipo de acesso          | Description                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [**HaveToShowWebViewBarricade**](folder2-havetoshowwebviewbarricade.md)<br/> | Somente leitura<br/> | Não há suporte no momento.<br/>                                       |
| [**OfflineStatus**](folder2-offlinestatus.md)<br/>                           | Somente leitura<br/> | Contém o status offline da pasta.<br/>                     |
| [**Auto-restauração**](folder2-self.md)<br/>                                             | Somente leitura<br/> | Contém o objeto [**FolderItem**](folderitem.md) da pasta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Pasta**](folder.md)
</dt> </dl>

 

 




