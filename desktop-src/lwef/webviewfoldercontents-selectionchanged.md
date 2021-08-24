---
title: Evento WebViewFolderContents. SelectionChanged (shldisp. h)
description: Evento WebViewFolderContents. SelectionChanged – ocorre quando o estado de seleção de qualquer item ou itens na exibição é alterado.
ms.assetid: 46dfceec-aa81-4950-81e5-526a6e621271
keywords:
- recursos de ambiente herdado de Windows do evento selectionchanged
topic_type:
- apiref
api_name:
- SelectionChanged
api_location:
- Shell32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cccabe52d7370d22fa086e9e8664163771062e8828c8ab2a6d016df30f13350
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119607826"
---
# <a name="webviewfoldercontentsselectionchanged-event"></a>Evento WebViewFolderContents. SelectionChanged

Ocorre quando o estado de seleção de qualquer item ou itens na exibição é alterado.

## <a name="syntax"></a>Sintaxe


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
WebViewFolderContents.SelectionChanged = EventHandler;
```



## <a name="parameters"></a>Parâmetros

Este manipulador de eventos não tem parâmetros.

## <a name="examples"></a>Exemplos

o exemplo a seguir mostra o uso apropriado desse evento para JScript inserido em HTML.


```HTML
<html>
<head>

...

<script language="JavaScript">
    function fnWebViewFolderContentsSelectionChangedJ()
    {
        alert("SelectionChanged event was called");
    }
</script>

<script language="JavaScript" for="FileList" event="SelectionChanged">
    fnWebViewFolderContentsSelectionChangedJ();
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



 

 





