---
title: Método WebViewFolderContents.SelectedItems (Shldisp.h)
description: Obtém um objeto FolderItems que representa todos os itens selecionados na exibição.
ms.assetid: 683acac4-f157-4a75-a3f8-c693887c1ea5
keywords:
- Método SelectedItems recursos de ambiente herdado do Windows
- Método SelectedItems herdado recursos de ambiente do Windows, objeto WebViewFolderContents
- Recursos do ambiente Windows herdado do objeto WebViewFolderContents, método SelectedItems
topic_type:
- apiref
api_name:
- WebViewFolderContents.SelectedItems
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee4b7f34cdcabec637671af79775fc1fa546790
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009677"
---
# <a name="webviewfoldercontentsselecteditems-method"></a>Método WebViewFolderContents. SelectedItems

Obtém um objeto [**FolderItems**](../shell/folderitems.md) que representa todos os itens selecionados na exibição.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = WebViewFolderContents.SelectedItems()
```



## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Retornar valor

Tipo: **[ **FolderItems**](../shell/folderitems.md)\*\***

Uma referência de objeto para o objeto [**FolderItems**](../shell/folderitems.md) .

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso correto desse método para JScript Embedded em HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectedItemsJ()
    {
        var objFolderItems;

        objFolderItems = FileList.SelectedItems();
        if (objFolderItems != null)
        {
            alert(objFolderItems.Count);
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



 

