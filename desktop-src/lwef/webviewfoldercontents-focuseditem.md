---
title: Propriedade WebViewFolderContents. FocusedItem (shldisp. h)
description: Propriedade WebViewFolderContents. FocusedItem – Obtém um objeto FolderItem que representa o item que tem o foco de entrada.
ms.assetid: 84cf92ac-dadb-4741-8383-a8ae1d35d4e0
keywords:
- Recursos do ambiente Windows herdado da propriedade FocusedItem
- Propriedade FocusedItem recursos de ambiente do Windows herdados, objeto WebViewFolderContents
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents, Propriedade FocusedItem
topic_type:
- apiref
api_name:
- WebViewFolderContents.FocusedItem
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 724743b81f605dc9ba5794a4a796b8a0c4a2a03f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102724"
---
# <a name="webviewfoldercontentsfocuseditem-property"></a>Propriedade WebViewFolderContents. FocusedItem

Obtém um objeto [**FolderItem**](../shell/folderitem.md) que representa o item que tem o foco de entrada.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
objFocusedItem = WebViewFolderContents.FocusedItem
```



## <a name="property-value"></a>Valor da propriedade

Uma variável do tipo [IDispatch](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch) que recebe o objeto de item focado.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso apropriado dessa propriedade no JScript inserido em HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsFocusedItemJ()
    {
        var objFolderItem;

        objFolderItem = FileList.FocusedItem;
        if (objFolderItem != null)
        {
            alert(objFolderItem.Name);
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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

