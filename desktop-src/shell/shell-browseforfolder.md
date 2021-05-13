---
description: Método Shell.BrowseForFolder – cria uma caixa de diálogo que permite que o usuário selecione uma pasta e, em seguida, retorne o objeto Pasta da pasta selecionada.
title: Método Shell.BrowseForFolder (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 4cc44e5a-3578-448b-9b19-1b71e1ae2cb9
ms.openlocfilehash: 26677173cce2b72d1a0ba6bdc941cd2407908712
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841807"
---
# <a name="shellbrowseforfolder-method"></a>Método Shell.BrowseForFolder

Cria uma caixa de diálogo que permite que o usuário selecione uma pasta e, em seguida, retorne o objeto [**Pasta da**](folder.md) pasta selecionada.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Shell.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

Shell.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Hwnd* \[ Em\]
</dt> <dd>

Tipo: **Inteiro**

O alça para a janela pai da caixa de diálogo. Esse valor pode ser zero.

</dd> <dt>

*sTitle* \[ Em\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Um **valor string** que representa o título exibido dentro da caixa de **diálogo** Procurar.

</dd> <dt>

*iOptions* \[ Em\]
</dt> <dd>

Tipo: **Inteiro**

Um **valor** Inteiro que contém as opções para o método . Isso pode ser zero ou uma combinação dos valores listados sob o **membro ulFlags** da [**estrutura BROWSEINFO.**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa)

</dd> <dt>

*vRootFolder* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

A pasta raiz a ser usada na caixa de diálogo. O usuário não pode navegar mais alto na árvore do que essa pasta. Se esse valor não for especificado, a pasta raiz usada na caixa de diálogo será a área de trabalho. Esse valor pode ser uma cadeia de caracteres que especifica o caminho da pasta ou um dos [**valores ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) Observe que os nomes de constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis em Visual Basic, mas não em VBScript ou JScript. Nesses casos, os valores numéricos devem ser usados em seu lugar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="jscript"></a>JScript

Tipo: **pasta \* \***

Uma referência de objeto para o objeto de [**pasta**](folder.md) da pasta selecionada.

### <a name="vb"></a>VB

Tipo: **pasta \* \***

Uma referência de objeto para o objeto de [**pasta**](folder.md) da pasta selecionada.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **BrowseForFolder** para exibir uma janela de procura intitulada "example" com raiz na pasta do Windows. O uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
        if (objFolder != null)
        {
            // Add code here.
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellBrowseForFolderVB()
        dim objShell
        dim ssfWINDOWS
        dim objFolder
        
        ssfWINDOWS = 36
        set objShell = CreateObject("shell.application")
            set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
                if (not objFolder is nothing) then
                    'Add code here.
                end if
            set objFolder = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellBrowseForFolderVB()
    Dim objShell   As Shell
    Dim ssfWINDOWS As Long
    Dim objFolder  As Folder
    
    ssfWINDOWS = 36
    Set objShell = New Shell
        Set objFolder = objShell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
            If (Not objFolder Is Nothing) Then
                'Add code here
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



 

 
