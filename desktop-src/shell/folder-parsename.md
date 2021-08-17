---
description: Cria e retorna um objeto FolderItem que representa um item especificado.
ms.assetid: 3af7052c-fb81-4a96-9bf9-379b0365a376
title: Método Folder. ParseName (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.ParseName
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 582341c97b6373fa0c04abf69642930328a34223a7c7b0dbc7792d8c7aec4680
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119093082"
---
# <a name="folderparsename-method"></a>Método Folder. ParseName

Cria e retorna um objeto [**FolderItem**](folderitem.md) que representa um item especificado.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Folder.ParseName(
  bName
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*bName* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma cadeia de caracteres que especifica o nome do item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **FolderItem**](folderitem.md)\*\***

Uma referência de objeto para o objeto [**FolderItem**](folderitem.md) .

## <a name="remarks"></a>Comentários

**ParseName** não deve ser usado para pastas virtuais, como meus documentos.

## <a name="examples"></a>Exemplos

o exemplo a seguir usa **parsename** para criar um objeto que representa o item de pasta Clock.avi na \\ pasta C: Windows. o uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderObjectParseNameJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;
            
            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                //Add code here.
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderObjectParseNameVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem
            
            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem is nothing) then
                'Add code here.
            end if
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnParseName_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        
        Set objFolderItem = objFolder.ParseName("clock.avi")
            'Add code here.
            Debug.Print "passed"
        Set objFolderItem = Nothing
    End If

    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos de área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 
