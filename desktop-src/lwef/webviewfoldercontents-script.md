---
title: Propriedade WebViewFolderContents. script (shldisp. h)
description: Obtém o objeto de script para a exibição.
ms.assetid: f65246c5-3cd6-43bd-b267-ad27bdd0b41e
keywords:
- recursos de ambiente de Windows herdados da propriedade Script
- recursos de ambiente herdados de propriedade de Script Windows, objeto WebViewFolderContents
- objeto WebViewFolderContents herdado Windows recursos de ambiente, propriedade Script
topic_type:
- apiref
api_name:
- WebViewFolderContents.Script
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d214719e2e40eaa680786188cf4815623d915c1e1e70e36f94eb80b6c4a6c25b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975446"
---
# <a name="webviewfoldercontentsscript-property"></a>Propriedade WebViewFolderContents. script

Obtém o objeto de script para a exibição.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
objScript = WebViewFolderContents.Script
```



## <a name="property-value"></a>Valor da propriedade

Uma variável do tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de script.

## <a name="examples"></a>Exemplos

o exemplo a seguir mostra o uso apropriado dessa propriedade no JScript inserido em HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsScriptJ()
    {
        var objScript;

        objScript = FileList.Script;
        if (objScript != null)
        {
            alert(objScript.Name);
        }
    }
</script>

</head>
<body>

...

<object id=FileList classid="clsid:1820FED0-473E-11D0-A96C-00C04FD705A2" tabIndex=1>
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



 

