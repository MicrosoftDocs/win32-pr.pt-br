---
description: Contém um objeto que representa um aplicativo.
ms.assetid: 61B85691-399D-41c1-9901-825345A38E5A
title: Propriedade IShellDispatch. Application (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.Application
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5adeb5663220309310c7cccb323be877de909516
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502090"
---
# <a name="ishelldispatchapplication-property"></a>Propriedade IShellDispatch. Application

Contém um objeto que representa um aplicativo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
objApplication = IShellDispatch.Application
```


```VB

Property Application As Object
```





## <a name="property-value"></a>Valor da propriedade

Uma variável do tipo [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de aplicativo.

## <a name="remarks"></a>Comentários

Essa propriedade é implementada e acessada por meio da propriedade [**shell. EjectPC**](shell-ejectpc.md) .

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



 

 
