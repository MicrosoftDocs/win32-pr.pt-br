---
description: Propriedade ShellFolderView. Folder – Obtém um objeto Folder que representa a exibição.
ms.assetid: 8f3e7827-f2a0-4ce9-b3e9-e6316ec58863
title: Propriedade ShellFolderView. Folder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.Folder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 40ff2dbed37aa8ceb80072870c78cee4e63cba3656550081be2c655cb6f6ddf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857705"
---
# <a name="shellfolderviewfolder-property"></a>Propriedade ShellFolderView. Folder

Obtém um objeto [**Folder**](folder.md) que representa a exibição.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
Folder = ShellFolderView.Folder
```



## <a name="property-value"></a>Valor da propriedade

Objeto que recebe o objeto de [**pasta**](folder.md) .

## <a name="remarks"></a>Comentários

A **pasta** só pode ser chamada no sistema local. Ele não funcionará quando for executado em uma página da Web por HTTP ou UNC.

## <a name="examples"></a>Exemplos

o exemplo a seguir mostra o uso apropriado dessa propriedade para JScript inserido em HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewFolderJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            alert("Got Folder object");
        }
    }
    
    function fnLoad()
    {
        var webOC;
        
        webOC = document.all("WebOC");
        webOC.Navigate("C:\\");
    }
</script>

</head>
<body onload="fnLoad()">
<object id="WebOC" 
        classid="clsid:8856F961-340A-11D0-A96B-00C04FD705A2"
        width=400
        height=400 VIEWASTEXT>
</object>
<br><br>
<INPUT id=Folder 
       type=button 
       value=Folder 
       name=Folder 
       onclick="fnShellFolderViewFolderJ()">
</body>
</html>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 




