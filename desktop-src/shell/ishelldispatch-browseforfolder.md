---
description: Cria uma caixa de diálogo que permite ao usuário selecionar uma pasta e, em seguida, retorna o objeto de pasta da pasta selecionada.
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
title: Método IShellDispatch. BrowseForFolder (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch.BrowseForFolder
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e603bb08b4b98ba4008aa4ea162c9b59e5d42da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090847"
---
# <a name="ishelldispatchbrowseforfolder-method"></a>Método IShellDispatch. BrowseForFolder

Cria uma caixa de diálogo que permite ao usuário selecionar uma pasta e, em seguida, retorna o objeto de [**pasta**](folder.md) da pasta selecionada.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = IShellDispatch.BrowseForFolder(
  Hwnd,
  sTitle,
  iOptions,
  [ vRootFolder ]
)
```


```VB

IShellDispatch.BrowseForFolder( _
  ByVal Hwnd As Integer, _
  ByVal sTitle As BSTR, _
  ByVal iOptions As Integer, _
  [ ByVal vRootFolder As Variant ] _
) As FOLDER
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*HWND* \[ no\]
</dt> <dd>

Tipo: **inteiro**

O identificador para a janela pai da caixa de diálogo. Esse valor pode ser zero.

</dd> <dt>

*sTitle* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Um valor de **cadeia de caracteres** que representa o título exibido dentro da caixa de diálogo de **procura** .

</dd> <dt>

*iOptions* \[ no\]
</dt> <dd>

Tipo: **inteiro**

Um valor **inteiro** que contém as opções para o método. Isso pode ser zero ou uma combinação dos valores listados no membro **ulFlags** da estrutura [**BROWSEINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-browseinfoa) .

</dd> <dt>

*vRootFolder* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

A pasta raiz a ser usada na caixa de diálogo. O usuário não pode navegar mais para cima na árvore do que essa pasta. Se esse valor não for especificado, a pasta raiz usada na caixa de diálogo será a área de trabalho. Esse valor pode ser uma cadeia de caracteres que especifica o caminho da pasta ou um dos valores de [**ShellSpecialFolderConstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) . Observe que os nomes de constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis em Visual Basic, mas não em VBScript ou JScript. Nesses casos, os valores numéricos devem ser usados em seu lugar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

### <a name="jscript"></a>JScript

Tipo: **pasta \* \***

Uma referência de objeto para o objeto de [**pasta**](folder.md) da pasta selecionada.

### <a name="vb"></a>VB

Tipo: **pasta \* \***

Uma referência de objeto para o objeto de [**pasta**](folder.md) da pasta selecionada.

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio do método [**shell. BrowseForFolder**](shell-browseforfolder.md) .

## <a name="examples"></a>Exemplos

Os exemplos a seguir usam **BrowseForFolder** para exibir uma janela de procura intitulada "example" com raiz na pasta do Windows. O uso é mostrado para JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellBrowseForFolderJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var ssfWINDOWS = 36;
        var objFolder;
        
        objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS);
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
            set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
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
        Set objFolder = objshell.BrowseForFolder(0, "Example", 0, ssfWINDOWS)
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



 

 
