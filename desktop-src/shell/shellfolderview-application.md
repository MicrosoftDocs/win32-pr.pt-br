---
description: Propriedade ShellFolderView. Application – contém o objeto Application do objeto.
ms.assetid: 305766b1-a19f-4743-a9e3-6837b3f8ffe0
title: Propriedade ShellFolderView. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 95ef542f91235b3b068e1b1b54768b4dd453d9b3
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108083464"
---
# <a name="shellfolderviewapplication-property"></a>Propriedade ShellFolderView. Application

Contém o objeto de aplicativo do objeto.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
objApplication = ShellFolderView.Application
```



## <a name="property-value"></a>Valor da propriedade

Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de aplicativo.

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



 

 
