---
description: Método ShellFolderView. SelectItem – define o estado de seleção de um item na exibição.
title: Método ShellFolderView. SelectItem (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView.SelectItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 91c39d4c-56c3-4c2b-93e8-9f782ca0aa93
ms.openlocfilehash: c8cbff0da4da55d9621bfeb01f26c5ed62fe230a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116744"
---
# <a name="shellfolderviewselectitem-method"></a>Método ShellFolderView. SelectItem

Define o estado de seleção de um item na exibição.

## <a name="syntax"></a>Sintaxe


```JScript
ShellFolderView.SelectItem(
  vItem,
  dwFlags
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vItem* \[ no\]
</dt> <dd>

Tipo: **variante \***

O objeto [**FolderItem**](folderitem.md) para o qual o estado de seleção será definido.

</dd> <dt>

*dwFlags* \[ no\]
</dt> <dd>

Tipo: **inteiro**

Um conjunto de sinalizadores que indicam o novo estado de seleção. Pode ser um ou mais dos valores a seguir.

<dt>



  acima (0)


</dt> <dd>

Desmarque o item.

</dd> <dt>



 (1)


</dt> <dd>

Selecione o item.

</dd> <dt>



 (3)


</dt> <dd>

Coloque o item no modo de edição.

</dd> <dt>



 (4)


</dt> <dd>

Anular seleção de todos, exceto o item especificado.

</dd> <dt>



 (8)


</dt> <dd>

Verifique se o item é exibido na exibição.

</dd> <dt>



 (16)


</dt> <dd>

Dê o foco ao item.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

[**FocusedItem**](shellfolderview-focuseditem.md) só pode ser chamado no sistema local. Ele não funcionará quando for executado em uma página da Web por HTTP ou UNC.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso apropriado desse método no JScript inserido em HTML.


```JScript
<html>
<head>
<title></title>

<script language="JavaScript">
    function fnShellFolderViewSelectItemJ()
    {
        var objFolder;
        
        objFolder = WebOC.Document.Folder;
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.Self;
            if (objFolderItem != null)
            {
                WebOC.Document.SelectItem(objFolderItem, 16);
                alert("item selected");
            }
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
        height=400>
</object>
<br><br>
<INPUT id=SelectItem 
       type=button 
       value=SelectItem 
       name=SelectItem 
       onclick="fnShellFolderViewSelectItemJ()">
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



 

 




