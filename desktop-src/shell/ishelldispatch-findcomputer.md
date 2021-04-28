---
Descrição: método IShellDispatch. FindComputer-' exibe a caixa de diálogo resultados da pesquisa: computadores. A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.
MS. AssetID: 9B687A8A-BB29-49a0-8AE3-11A75FAF3257 título: IShellDispatch. FindComputer método (shldisp. h) MS. Topic: referência MS. Date: 05/31/2018 topic_type: 
- APIRef
- api_name kbSyntax: 
- IShellDispatch. FindComputer api_type: 
- Api_location COM: 
- Shell32.dll
---

# <a name="ishelldispatchfindcomputer-method"></a>Método IShellDispatch. FindComputer

Exibe a caixa de diálogo **resultados da pesquisa: computadores** . A caixa de diálogo mostra o resultado da pesquisa de um computador especificado.

## <a name="syntax"></a>Sintaxe


```JScript
IShellDispatch.FindComputer()
```


```VB

IShellDispatch.FindComputer()
```





## <a name="parameters"></a>Parâmetros

Esse método não tem parâmetros.

## <a name="return-value"></a>Valor retornado

### <a name="jscript"></a>JScript

Esse método não retorna um valor.

### <a name="vb"></a>VB

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio do método [**shell. FindComputer**](shell-findcomputer.md) .

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **FindComputer** em JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnShellFindComputerJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objshell.FindComputer();
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
        objshell.FindComputer

        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnShellFindComputerVB()
    Dim objShell As Shell

    Set objShell = New Shell
    objshell.FindComputer

    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



 

 




