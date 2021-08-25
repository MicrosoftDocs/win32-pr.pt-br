---
description: Método Shell.FindPrinter – exibe a caixa de diálogo Encontrar Impressora.
ms.assetid: 61C700CF-623B-4c99-A211-AC26A1E4AE85
title: Método Shell.FindPrinter (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Shell.FindPrinter
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3c3208d001f501371245e578ca691267604be691076f858b0a9f8bb7eeb36279
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111146"
---
# <a name="shellfindprinter-method"></a>Método Shell.FindPrinter

Exibe a caixa **de diálogo** Encontrar Impressora.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = Shell.FindPrinter(
  [ sName ],
  [ sLocation ],
  [ sModel ]
)
```


```VB

Shell.FindPrinter( _
  [ ByVal sName As BSTR ], _
  [ ByVal sLocation As BSTR ], _
  [ ByVal sModel As BSTR ] _
) As Integer
```





## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sName* \[ in, opcional\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **Cadeia de** caracteres que contém o nome da impressora.

</dd> <dt>

*sLocation* \[ in, opcional\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **Cadeia de** caracteres que contém o local da impressora.

</dd> <dt>

*sModel* \[ in, opcional\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Uma **Cadeia de** caracteres que contém o modelo de impressora.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se você atribuir cadeias de caracteres a um ou mais dos parâmetros opcionais, eles serão exibidos como valores padrão no controle de edição associado quando a caixa de diálogo Encontrar Impressora for exibida.  O usuário pode aceitar ou substituir esses valores. Se nenhum valor for atribuído a um parâmetro, a caixa de edição associada será vazia e o usuário deverá inserir um valor.

Esse método não está disponível atualmente no Microsoft Visual Basic.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso de **FindPrinter** para exibir a caixa de diálogo Encontrar **Impressora** para um aplicativo específico. O uso é mostrado para JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFindPrinterJ()
    {
        var objShell = new ActiveXObject("shell.application");
        
        objShell.FindPrinter();
    }
</script>
```



Vbscript:


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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



 

 
