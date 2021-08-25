---
Descrição: método Shell. FindComputer-' exibe a caixa de diálogo resultados da pesquisa: computadores. A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.
MS. AssetID: 0304b955-AFde-4de4-824a-9ec9c9530360 título: Shell. FindComputer método (shldisp. h) MS. Topic: referência MS. Date: 05/31/2018 topic_type: 
- APIRef
- api_name kbSyntax: 
- Api_type do Shell. FindComputer: 
- Api_location COM: 
- Shell32.dll
---

# <a name="shellfindcomputer-method"></a>Método Shell. FindComputer

Exibe a caixa de diálogo **resultados da pesquisa: computadores** . A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.

## <a name="syntax"></a>Sintaxe


```JScript
Shell.FindComputer()
```


```VB

Shell.FindComputer()
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

### <a name="jscript"></a>JScript

Esse método não retorna um valor.

### <a name="vb"></a>VB

Esse método não retorna um valor.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra **FindComputer** em uso. O resultado desse código é o mesmo que pressionar o botão **Iniciar** , clicar em **Pesquisar**, clicar na opção **impressoras, computadores ou pessoas** e clicar em **um computador na rede**. o uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindComputer();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellFindComputerVB()
        dim objShell
        dim ssfWINDOWS
        ssfWINDOWS = 36

        set objShell = CreateObject("shell.application")
        objShell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objShell.FindComputer

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



 

 




