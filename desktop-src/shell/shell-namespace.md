---
description: Método Shell.NameSpace – cria e retorna um objeto Folder para a pasta especificada.
ms.assetid: c0d61bc6-6851-4b47-a62d-4c24d2958b98
title: Método Shell.NameSpace (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.NameSpace
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 41542f133961104180257b9c15b1843f3458bf6d9d2dd156fa3d97ea7b9ca87d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857735"
---
# <a name="shellnamespace-method"></a>Método Shell.NameSpace

Cria e retorna um [**objeto Folder**](folder.md) para a pasta especificada.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Shell.NameSpace(
  vDir
)
```


```VB

Shell.NameSpace( _
  ByVal vDir As Variant _
) As Folder
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vDir* \[ Em\]
</dt> <dd>

Tipo: **Variante**

A pasta para a qual criar o [**objeto**](folder.md) Pasta. Pode ser uma cadeia de caracteres que especifica o caminho da pasta ou um dos [**valores ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) Observe que os nomes constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis no Visual Basic, mas não no VBScript ou JScript. Nesses casos, os valores numéricos devem ser usados em seu lugar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="jscript"></a>JScript

Tipo: **[ **Pasta**](folder.md)\*\***

Referência de objeto ao [**objeto Pasta**](folder.md) da pasta especificada. Se a pasta não for criada com êxito, esse valor retornará **nulo.**

### <a name="vb"></a>VB

Tipo: **[ **Pasta**](folder.md)\*\***

Referência de objeto ao [**objeto Pasta**](folder.md) da pasta especificada. Se a pasta não for criada com êxito, esse valor retornará **nulo.**

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra **NameSpace** em uso. O uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellNameSpaceJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfWINDOWS = 36
        
        objFolder = objShell.NameSpace(ssfWINDOWS);
        if (objFolder != null)
        {
            alert(objFolder.Title);
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellNameSpaceVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\\")

        if (not objFolder is nothing) then
            alert(objFolder.Title)
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellNameSpaceVB()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPERSONAL)

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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 




