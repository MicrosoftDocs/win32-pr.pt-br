---
description: Contém o título da pasta.
ms.assetid: 95c064ff-4504-4e9c-80ac-47beca443ad4
title: Propriedade Folder. Title (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.Title
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a1b449caa1a1447b292a982522e30b9172168f09098d5e4dee0647c0ae6dc14e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860253"
---
# <a name="foldertitle-property"></a>Propriedade Folder. title

Contém o título da pasta.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
strTitle = Folder.Title
```



## <a name="property-value"></a>Valor da propriedade

Uma cadeia de caracteres que contém o título do objeto.

## <a name="remarks"></a>Comentários

> [!Note]  
> Nem todos os métodos são implementados para todas as pastas. Por exemplo, o método [**ParseName**](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL). Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **título** para recuperar o título da pasta que contém os grupos de programas do usuário (geralmente "programas"). o uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderTitleJ()
    {
        var objShell    = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderTitleVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfPROGRAMS
            
            ssfPROGRAMS = 2
            set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                alert(objFolder.Title)
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnFolderTitleVB()
    Dim objShell    As Shell
    Dim objFolder   As Folder
    Dim ssfPROGRAMS As Long
            
    ssfPROGRAMS = 2
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
    If (Not objFolder Is Nothing) Then
        Debug.Print objFolder.Title
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



 

 




