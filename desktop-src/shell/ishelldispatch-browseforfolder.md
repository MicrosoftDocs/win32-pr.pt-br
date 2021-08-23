---
description: Método IShellDispatch.BrowseForFolder – cria uma caixa de diálogo que permite que o usuário selecione uma pasta e, em seguida, retorne o objeto Pasta da pasta selecionada.
ms.assetid: 578C51C1-F59B-4604-A09B-62BA61225ABB
title: Método IShellDispatch.BrowseForFolder (Shldisp.h)
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
ms.openlocfilehash: e70fd50d4b08787326f93cddf7ec55a0eaacb25fa815cc2b4c8246c1934494a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119551826"
---
# <a name="ishelldispatchbrowseforfolder-method"></a>Método IShellDispatch.BrowseForFolder

Cria uma caixa de diálogo que permite que o usuário selecione uma pasta e, em seguida, retorne o objeto [**Pasta da**](folder.md) pasta selecionada.

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

A pasta raiz a ser usada na caixa de diálogo. O usuário não pode navegar mais alto na árvore do que essa pasta. Se esse valor não for especificado, a pasta raiz usada na caixa de diálogo será a área de trabalho. Esse valor pode ser uma cadeia de caracteres que especifica o caminho da pasta ou um dos [**valores ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) Observe que os nomes constantes encontrados em **ShellSpecialFolderConstants** estão disponíveis no Visual Basic, mas não no VBScript ou JScript. Nesses casos, os valores numéricos devem ser usados em seu lugar.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

### <a name="jscript"></a>JScript

Tipo: **\* \* FOLDER**

Uma referência de objeto ao objeto Pasta da [**pasta**](folder.md) selecionada.

### <a name="vb"></a>VB

Tipo: **\* \* FOLDER**

Uma referência de objeto ao objeto Pasta da [**pasta**](folder.md) selecionada.

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio [**do método Shell.BrowseForFolder.**](shell-browseforfolder.md)

## <a name="examples"></a>Exemplos

Os exemplos a seguir usam **BrowseForFolder** para exibir uma janela de navegação intitulada "Exemplo" com raiz na pasta Windows dados. O uso é mostrado para JScript, VBScript e Visual Basic.

JScript:


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



Vbscript:


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 
