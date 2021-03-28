---
description: Exibe a caixa de diálogo Localizar impressora.
ms.assetid: a3d1e810-f0cf-48ec-93da-5cc01117c5d4
title: Método IShellDispatch2. FindPrinter (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellDispatch2.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 81124e3f0d04244b9b81e812e090bde25971c17c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164749"
---
# <a name="ishelldispatch2findprinter-method"></a>Método IShellDispatch2. FindPrinter

Exibe a caixa de diálogo **Localizar impressora** .

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = IShellDispatch2.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

IShellDispatch2.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sname* \[ em, opcional\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **cadeia de caracteres** que contém o nome da impressora.

</dd> <dt>

*sLocation* \[ em, opcional\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **cadeia de caracteres** que contém o local da impressora.

</dd> <dt>

*sModel* \[ em, opcional\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **cadeia de caracteres** que contém o modelo de impressora.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse método é implementado e acessado por meio do método [**shell. FindPrinter**](./shell-findprinter.md) .

Se você atribuir cadeias de caracteres a um ou mais dos parâmetros opcionais, eles serão exibidos como valores padrão no controle de edição associado quando a caixa de diálogo **Localizar impressora** for exibida. O usuário pode aceitar ou substituir esses valores. Se nenhum valor for atribuído a um parâmetro, a caixa de edição associada estará vazia e o usuário deverá inserir um valor.

Este método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **FindPrinter** para exibir a caixa de diálogo **Localizar impressora** para um aplicativo específico. O uso é mostrado para JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFindPrinterVB()
        dim objShell
        dim bReturn

        set objShell = CreateObject("shell.application")
        objShell.FindPrinter()

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



 

 
