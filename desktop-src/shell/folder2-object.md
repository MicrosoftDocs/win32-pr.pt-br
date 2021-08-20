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
ms.openlocfilehash: f5616dbace23cbca4401d9c2c38dc56eec4ff71308945ababcc758b54d3804e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118050099"
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
| [**Sincronizar**](folder2-synchronize.md)                             | Sincroniza todos os arquivos offline na pasta.<br/>                             |



 

### <a name="properties"></a>Propriedades

O objeto **Pasta2** tem essas propriedades.



| Propriedade                                                                            | Tipo de acesso          | Descrição                                                               |
|:------------------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------|
| [**HaveToShowWebViewBarricade**](folder2-havetoshowwebviewbarricade.md)<br/> | Somente leitura<br/> | Não há suporte no momento.<br/>                                       |
| [**OfflineStatus**](folder2-offlinestatus.md)<br/>                           | Somente leitura<br/> | Contém o status offline da pasta.<br/>                     |
| [**Auto-restauração**](folder2-self.md)<br/>                                             | Somente leitura<br/> | Contém o objeto [**FolderItem**](folderitem.md) da pasta.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Pasta**](folder.md)
</dt> </dl>

 

 




