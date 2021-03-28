---
description: Representa uma coleção das janelas abertas que pertencem ao shell. Os métodos associados a esses objetos podem controlar e executar comandos no Shell e obter outros objetos relacionados ao shell.
ms.assetid: cad1f961-7fb4-4ba1-be48-b664d3de2c60
title: Objeto ShellWindows (exdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 6a3a782dd4e29d56f5edc7a869004ac7b3fb7ccd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967965"
---
# <a name="shellwindows-object"></a>Objeto ShellWindows

Representa uma coleção das janelas abertas que pertencem ao shell. Os métodos associados a esses objetos podem controlar e executar comandos no Shell e obter outros objetos relacionados ao shell.

## <a name="members"></a>Membros

O objeto **ShellWindows** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

O objeto **ShellWindows** tem esses métodos.



| Método                                                 | Descrição                                                                                                         |
|:-------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](shellwindows--newenum-method-7ral.md) | Cria e retorna um novo objeto **ShellWindows** que é uma cópia desse objeto **ShellWindows** .<br/>        |
| [**Item**](shellwindows-item.md)                      | Recupera um objeto [**InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa a janela do Shell.<br/> |



 

### <a name="properties"></a>Propriedades

O objeto **ShellWindows** tem essas propriedades.



| Propriedade                                       | Tipo de acesso          | Description                                                |
|:-----------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Contar**](shellwindows-count.md)<br/> | Somente leitura<br/> | Contém o número de itens na coleção.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>O textdisp. h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 
