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
ms.openlocfilehash: c2c630ef36f6e4b2b58f3902c3d5728a31ad1f0d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842057"
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



| Propriedade                                                                            | Tipo de acesso          | Descrição                                                               |
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
| INSERI<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Pasta**](folder.md)
</dt> </dl>

 

 




