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
ms.openlocfilehash: ea9a8090a794f23693ae4fef10556bc207f16531
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646568"
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

## <a name="return-value"></a>Retornar valor

Tipo: **[ **FolderItem**](folderitem.md)\*\***

Uma referência de objeto para o objeto [**FolderItem**](folderitem.md) .

## <a name="remarks"></a>Comentários

**ParseName** não deve ser usado para pastas virtuais, como meus documentos.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **ParseName** para criar um objeto que representa o item de pasta Clock.avi na \\ pasta C: Windows. O uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 
