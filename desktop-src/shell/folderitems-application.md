---
description: Contém o objeto Application da coleção de itens de pasta.
ms.assetid: 2cd4243e-a5a6-4de4-b310-f74558ac0fbe
title: Propriedade FolderItems.Application (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3809d76576b69c53f6fc5f8a11ab954242e3a89c9a369ada2f4fa47c460f523f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032604"
---
# <a name="folderitemsapplication-property"></a>Propriedade FolderItems.Application

Contém o **objeto Application** da coleção de itens de pasta.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
objApplication = FolderItems.Application
```



## <a name="property-value"></a>Valor da propriedade

Uma referência de objeto ao objeto Application.

## <a name="remarks"></a>Comentários

A **propriedade** Application retorna o objeto de automação com suporte pelo aplicativo que contém o controle WebBrowser, se esse objeto estiver acessível. Caso contrário, essa propriedade retornará o objeto de automação do controle WebBrowser.

Use essa propriedade com os **comandos Set** e **CreateObject** ou com o comando **GetObject** para criar e manipular uma instância do Windows Internet Explorer aplicativo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 




