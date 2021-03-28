---
description: Contém o objeto de aplicativo do item de pasta.
ms.assetid: cd8d6dea-1d16-4d62-b56b-c915192f730b
title: Propriedade FolderItem. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 72816ed0c426f6ff3fa92c30a1ec31757c0a02fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501159"
---
# <a name="folderitemapplication-property"></a>Propriedade FolderItem. Application

Contém o objeto de **aplicativo** do item de pasta.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
objApplication = FolderItem.Application
```



## <a name="property-value"></a>Valor da propriedade

Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de **aplicativo** .

## <a name="remarks"></a>Comentários

A propriedade **Application** retorna o objeto Automation com suporte do aplicativo que contém o controle WebBrowser, se esse objeto estiver acessível. Caso contrário, essa propriedade retornará o objeto de automação do controle WebBrowser.

Use essa propriedade com os comandos **set** e **CreateObject** ou com o comando **GetObject** para criar e manipular uma instância do aplicativo do Windows Internet Explorer.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 
