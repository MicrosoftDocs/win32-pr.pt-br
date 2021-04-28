---
description: Método IShellDispatch2. ShellExecute-executa uma operação especificada em um arquivo especificado.
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: Método IShellDispatch2. ShellExecute (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 5c058275948d5d96805ae24a76389321d7c69b8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117014"
---
# <a name="ishelldispatch2shellexecute-method"></a>Método IShellDispatch2. ShellExecute

Executa uma operação especificada em um arquivo especificado.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = IShellDispatch2.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
)
```


```VB

IShellDispatch2.ShellExecute( _
  ByVal sFile As BSTR, _
  [ ByVal vArguments As Variant ], _
  [ ByVal vDirectory As Variant ], _
  [ ByVal vOperation As Variant ], _
  [ ByVal vShow As Variant ] _
) As Integer
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sfile* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **cadeia de caracteres** que contém o nome do arquivo no qual **ShellExecute** executará a ação especificada por *vOperation*.

</dd> <dt>

*vArguments* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

Uma cadeia de caracteres que contém valores de parâmetro para a operação.

</dd> <dt>

*vDirectory* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

O caminho totalmente qualificado do diretório que contém o arquivo especificado por *sfile*. Se esse parâmetro não for especificado, o diretório de trabalho atual será usado.

</dd> <dt>

*vOperation* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

A operação a ser executada. Esse valor é definido como uma das cadeias de caracteres de verbo com suporte no arquivo. Para obter uma discussão sobre verbos, consulte a seção comentários. Se esse parâmetro não for especificado, a operação padrão será executada.

</dd> <dt>

*vShow* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

Uma recomendação sobre como a janela do aplicativo deve ser exibida inicialmente. O aplicativo pode ignorar essa recomendação. Esse parâmetro pode usar um dos valores a seguir. Se esse parâmetro não for especificado, o aplicativo usará seu valor padrão.



| Valor                                                                                                                               | Significado                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt></dt><dt>0</dt> </dl>  | Abra o aplicativo com uma janela oculta.<br/>                                                                                                    |
| <dl> <dt></dt> <dt>1</dt> </dl>  | Abra o aplicativo com uma janela normal. Se a janela for minimizada ou maximizada, o sistema a restaurará para seu tamanho e posição originais.<br/> |
| <dl> <dt></dt> <dt>2</dt> </dl>  | Abra o aplicativo com uma janela minimizada.<br/>                                                                                                 |
| <dl> <dt></dt> <dt>3</dt> </dl>  | Abra o aplicativo com uma janela maximizada.<br/>                                                                                                 |
| <dl> <dt></dt><dt>4</dt> </dl>  | Abra o aplicativo com sua janela em seu tamanho e posição mais recentes. A janela ativa permanece ativa.<br/>                                  |
| <dl> <dt></dt><dt>5</dt> </dl>  | Abra o aplicativo com sua janela em seu tamanho e posição atuais.<br/>                                                                        |
| <dl> <dt></dt><dt>7</dt> </dl>  | Abra o aplicativo com uma janela minimizada. A janela ativa permanece ativa.<br/>                                                               |
| <dl> <dt></dt><dt>10</dt> </dl> | Abra o aplicativo com sua janela no estado padrão especificado pelo aplicativo.<br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio do método [**shell. ShellExecute**](./shell-shellexecute.md) .

Esse método é equivalente a iniciar um dos comandos associados ao menu de atalho de um arquivo. Cada comando é representado por uma cadeia de caracteres de verbo. O conjunto de verbos com suporte varia de arquivo para arquivo. O verbo mais comumente suportado é "Open", que também é geralmente o verbo padrão. Outros verbos podem ter suporte apenas em determinados tipos de arquivos. Para obter mais informações sobre os verbos do Shell, consulte [iniciando aplicativos](launch.md) ou [estendendo menus de atalho](context.md).

Este método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **ShellExecute** para abrir o bloco de notas. O uso é mostrado para JScript e VBScript.

JScript


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnShellExecuteVB()
        dim objShell

        set objShell = CreateObject("shell.application")

        objShell.ShellExecute "notepad.exe", "", "", "open", 1

        set objShell = nothing
    end function
</script>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 
