---
description: Executa um verbo em um item de Shell.
ms.assetid: aac3f338-6074-4b1f-9b2f-e6206db52419
title: Método ShellFolderItem. InvokeVerbEx (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 627c2b40869ac9c509dcd645ec259de7db118235
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967552"
---
# <a name="shellfolderiteminvokeverbex-method"></a>Método ShellFolderItem. InvokeVerbEx

Executa um verbo em um item de Shell.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = ShellFolderItem.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vVerb* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

Uma **variante** que contém a cadeia de caracteres de verbo que corresponde ao comando a ser executado. Deve ser um dos valores retornados pela propriedade [**Name**](folderitemverb-name.md) do item. Se nenhum verbo for especificado, o verbo padrão será executado.

</dd> <dt>

*vArgs* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

Uma **variante** que consiste em uma cadeia de caracteres com um ou mais argumentos para o comando especificado por *vVerb*. O formato dessa cadeia de caracteres depende do verbo específico.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um verbo é uma cadeia de caracteres usada para especificar uma ação específica à qual um item dá suporte. Normalmente, chamar um verbo inicia um aplicativo relacionado. Por exemplo, chamar o verbo **Open** em um arquivo. txt normalmente abre o arquivo com um editor de texto, geralmente o bloco de notas da Microsoft. O objeto [**FolderItemVerbs**](folderitemverbs.md) representa a coleção de verbos associados ao item. Para obter mais informações sobre verbos, consulte [iniciando aplicativos](launch.md).

Esse método é semelhante a [**InvokeVerb**](folderitem-invokeverb.md), mas permite que você especifique argumentos para o comando, bem como o próprio comando.

## <a name="examples"></a>Exemplos

Os exemplos a seguir mostram o uso apropriado desse método no JScript, no VBScript e no Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnFolderItem2InvokeVerbExJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.ParseName("NOTEPAD.EXE");
            if (objFolderItem != null)
            {
                objFolderItem.InvokeVerbEx("open", "c:\\autoexec.bat");
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder2
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder2 = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder2 is nothing) then
                dim objFolderItem
                        
                set objFolderItem = objFolder2.Self
                if (not objFolderItem is nothing) then
                    objFolderItem.InvokeVerbEx()
                end if
                set objFolderItem = nothing
            end if
            set objFolder2 = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnFolderItem2InvokeVerbExVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem2 As Object
            
            Set objFolderItem2 = objFolder2.ParseName("NOTEPAD.EXE")
                If (Not objFolderItem2 Is Nothing) Then
                    objFolderItem2.InvokeVerbEx ("open")
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem2 = Nothing
        Else
            'Folder object returned nothing.
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

[**ShellFolderItem**](shellfolderitem-object.md)
</dt> <dt>

[**InvokeVerb**](folderitem-invokeverb.md)
</dt> </dl>

 

 




