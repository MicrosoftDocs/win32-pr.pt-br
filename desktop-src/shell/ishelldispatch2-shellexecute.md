---
description: Método IShellDispatch2.ShellExecute – executa uma operação especificada em um arquivo especificado.
ms.assetid: a55e804c-ed7c-4b22-b86f-8e5653976654
title: Método IShellDispatch2.ShellExecute (Shldisp.h)
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
ms.openlocfilehash: 8e524ea4a4422e92068d432a91165dfeb97155cfba1d5e6bd9a06ed75b7550cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118721031"
---
# <a name="ishelldispatch2shellexecute-method"></a>Método IShellDispatch2.ShellExecute

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

*sFile* \[ Em\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **Cadeia de** Caracteres que contém o nome do arquivo no qual **ShellExecute** executará a ação especificada por *vOperation*.

</dd> <dt>

*vArguments* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

Uma cadeia de caracteres que contém valores de parâmetro para a operação.

</dd> <dt>

*vDirectory* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

O caminho totalmente qualificado do diretório que contém o arquivo especificado por *sFile*. Se esse parâmetro não for especificado, o diretório de trabalho atual será usado.

</dd> <dt>

*vOperation* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

A operação a ser executada. Esse valor é definido como uma das cadeias de caracteres verbais com suporte no arquivo. Para uma discussão sobre verbos, consulte a seção Comentários. Se esse parâmetro não for especificado, a operação padrão será executada.

</dd> <dt>

*vShow* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

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

Esse método é implementado e acessado por meio do [**método Shell.ShellExecute.**](./shell-shellexecute.md)

Esse método é equivalente a iniciar um dos comandos associados ao menu de atalho de um arquivo. Cada comando é representado por uma cadeia de caracteres de verbo. O conjunto de verbos com suporte varia de arquivo para arquivo. O verbo com suporte mais comum é "open", que também é geralmente o verbo padrão. Outros verbos podem ser suportados apenas por determinados tipos de arquivos. Para mais discussão sobre verbos do Shell, consulte [Iniciando aplicativos](launch.md) ou [Estendendo menus de atalho.](context.md)

Esse método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **ShellExecute para** abrir Bloco de notas. O uso é mostrado para JScript e VBScript.

JScript:


```JScript
<script language="JScript">
    function fnShellExecuteJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.ShellExecute("notepad.exe", "", "", "open", 1);
    }
</script>
```



Vbscript:


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



 

 
