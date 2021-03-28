---
description: Executa uma operação especificada em um arquivo especificado.
ms.assetid: 62E59A1C-51BD-4864-AF09-35FFD49FAB9D
title: Método Shell.ShellExecute (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.ShellExecute
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 83ab9741199bff675245f15dc2ad1ffb20592a35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104967984"
---
# <a name="shellshellexecute-method"></a>Método Shell. ShellExecute

Executa uma operação especificada em um arquivo especificado.

## <a name="syntax"></a>Syntax

JScript

```js
iRetVal = Shell.ShellExecute(
  sFile,
  [ vArguments ],
  [ vDirectory ],
  [ vOperation ],
  [ vShow ]
);
```

VBScript

```vb
iRetVal = Shell.ShellExecute( _
  sFile, _
  [ ByVal vArguments ], _
  [ ByVal vDirectory ], _
  [ ByVal vOperation ], _
  [ ByVal vShow ] _
)
```

VB:

```vb
Shell.ShellExecute( _
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
| <dl> <dt></dt> <dt>0</dt> </dl>  | Abra o aplicativo com uma janela oculta.<br/>                                                                                                    |
| <dl> <dt></dt> <dt>1</dt> </dl>  | Abra o aplicativo com uma janela normal. Se a janela for minimizada ou maximizada, o sistema a restaurará para seu tamanho e posição originais.<br/> |
| <dl> <dt></dt> <dt>2</dt> </dl>  | Abra o aplicativo com uma janela minimizada.<br/>                                                                                                 |
| <dl> <dt></dt> <dt>3</dt> </dl>  | Abra o aplicativo com uma janela maximizada.<br/>                                                                                                 |
| <dl> <dt></dt> <dt>4</dt> </dl>  | Abra o aplicativo com sua janela em seu tamanho e posição mais recentes. A janela ativa permanece ativa.<br/>                                  |
| <dl> <dt></dt><dt>5</dt> </dl>  | Abra o aplicativo com sua janela em seu tamanho e posição atuais.<br/>                                                                        |
| <dl> <dt></dt><dt>7</dt> </dl>  | Abra o aplicativo com uma janela minimizada. A janela ativa permanece ativa.<br/>                                                               |
| <dl> <dt></dt><dt>10</dt> </dl> | Abra o aplicativo com sua janela no estado padrão especificado pelo aplicativo.<br/>                                                       |



 

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse método é equivalente a iniciar um dos comandos associados ao menu de atalho de um arquivo. Cada comando é representado por uma cadeia de caracteres de verbo. O conjunto de verbos com suporte varia de arquivo para arquivo. O verbo mais comumente suportado é "Open", que também é geralmente o verbo padrão. Outros verbos podem ter suporte apenas em determinados tipos de arquivos. Para obter mais informações sobre os verbos do Shell, consulte [iniciando aplicativos](launch.md) ou [estendendo menus de atalho](context.md).

Este método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **ShellExecute** para abrir o bloco de notas. O uso é mostrado para JScript e VBScript.

JScript


```JScript
function ShellExecuteJS()
{
    var objShell = new ActiveXObject("Shell.Application");
    objShell.ShellExecute("notepad.exe", "", "", "open", 1);
}
```

VBScript

```vb
Function ShellExecuteVB()
    Dim objShell
    Set objShell = CreateObject("Shell.Application")
    Call objShell.ShellExecute("notepad.exe", "", "", "open", 1)
End Function
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 
