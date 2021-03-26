---
description: Contém o status offline da pasta.
ms.assetid: b50b130d-0675-49b5-b730-f67ea1c71d8c
title: Propriedade Pasta2. OfflineStatus (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder2.OfflineStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: d456eae826e8a2e173b92fac4be716fb24bcb92d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967280"
---
# <a name="folder2offlinestatus-property"></a>Propriedade Pasta2. OfflineStatus

Contém o status offline da pasta.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
iOfflineStatus = Folder2.OfflineStatus
```



## <a name="property-value"></a>Valor da propriedade

Um **inteiro** que é definido como um dos valores a seguir.

<dt>



 (OFS \_ DIRTYCACHE)


</dt> <dd>

O servidor está online com alterações não sincronizadas.

</dd> <dt>



 (OFS \_ INATIVO


</dt> <dd>

O cache offline não está habilitado para esta pasta.

</dd> <dt>



 (OFS \_ ESTÁ


</dt> <dd>

O servidor está offline.

</dd> <dt>



 (OFS \_ CONECTAR


</dt> <dd>

O servidor está online.

</dd> <dt>



 (OFS \_ SERVERBACK)


</dt> <dd>

O servidor está offline, mas pode ser acessado.

</dd> </dl>

## <a name="remarks"></a>Comentários

> [!Note]  
> Arquivos Offline deve ser habilitado por meio de opções de pasta para que o **OfflineStatus** funcione corretamente. Se a opção Arquivos Offline não estiver habilitada, a propriedade retornará **OFS \_ inativa**.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso apropriado de **OfflineStatus** para JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnOfflineStatusJ()
    {
        var objShell   = new ActiveXObject("shell.application");
        var objFolder2 = new Object;
        
        objFolder2 = objShell.NameSpace("\\\\server\\share\\folder");
        if (objFolder2 != null)
        {
            var nReturn;

            nReturn = objFolder2.OfflineStatus;
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnOfflineStatusVB()
        dim objShell
        dim objFolder2
       
        set objShell = CreateObject("shell.application")
        set objFolder2 = objShell.NameSpace("\\server\share\folder")

        if (not objFolder2 is nothing) then
            dim nReturn

            nReturn = objFolder2.OfflineStatus
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnOfflineStatusVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace("\\server\share\folder")

    If (Not objFolder2 Is Nothing) Then
        Dim nReturn As Integer
        
        nReturn = objFolder2.OfflineStatus()
    End If

    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                          |
| parâmetro<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Pasta2**](folder2-object.md)
</dt> <dt>

[**Pasta**](folder.md)
</dt> </dl>

 

 




