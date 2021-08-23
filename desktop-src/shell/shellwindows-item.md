---
description: Recupera um objeto InternetExplorer que representa a janela shell.
ms.assetid: 32390f35-f83a-45d9-a240-282da7cb2b13
title: Método ShellWindows.Item (Exdisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellWindows.Item
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fdc64659037cbdb471d7c2142ed6c096684966cd920d4e1f6ecee046d28cce8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660577"
---
# <a name="shellwindowsitem-method"></a>Método ShellWindows.Item

Recupera um [**objeto InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa a janela shell.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = ShellWindows.Item(
  [ iIndex ]
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*iIndex* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

O índice com base em zero do item a ser recuperado. Esse valor deve ser menor que o valor da [**propriedade Count.**](shellwindows-count.md) Se esse valor for omitido, um valor padrão de 0 será usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)\*\***

Uma referência de objeto ao [**objeto InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa a janela shell.

## <a name="examples"></a>Exemplos

O exemplo a seguir usa [**Item**](folderitemverbs-item.md) para recuperar o [**objeto InternetExplorer**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752084(v=vs.85)) que representa o primeiro item de janela do Shell. O uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript:


```JavaScript
<script language="JScript">
    function fnShellWindowsItemJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objShellWindows;
        
        objShellWindows = objshell.Windows();
        if (objShellWindows != null)
        {
            var objIE;
            objIE = objShellWindows.Item();

            if (objIE != null)
            {
                alert(objIE.path());
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellWindowsItemVB()
        dim objShell
        dim objShellWindows
        
        set objShell = CreateObject("shell.application")
        set objShellWindows = objshell.Windows()

        if (not objShellWindows is nothing) then
            dim objIE
            set objIE = objShellWindows.Item

            if (not objIE is nothing) then
                Wscript.Echo objIE.path
            end if

            set objIE = nothing
        end if

        set objShellWindows = nothing
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellWindowsItemVB()
    Dim objShell        As Shell
    Dim objShellWindows As ShellWindows
    
    Set objShell = New Shell
    Set objShellWindows = objshell.Windows()

    If (Not objShellWindows Is Nothing) Then
        Dim objIE As InternetExplorer
        Set objIE = objShellWindows.Item

        If (Not objIE Is Nothing) Then
            Debug.Print objIE.Path
        End If

        Set objIE = Nothing
    End If

    Set objShellWindows = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows somente aplicativos da \[ área de trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Exdisp.h</dt> </dl>                            |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 
