---
description: Propriedade FolderItemVerbs. Count – contém o número de itens na coleção.
ms.assetid: a676593b-ea78-433d-a622-221028245c3a
title: Propriedade FolderItemVerbs. Count (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs.Count
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 985ab6eb9508d57a7dd38616108bb0fdb58e7244623d90db435ca0a7022a570c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090586"
---
# <a name="folderitemverbscount-property"></a>Propriedade FolderItemVerbs. Count

Contém o número de itens na coleção.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```JScript
iCount = FolderItemVerbs.Count
```



## <a name="property-value"></a>Valor da propriedade

Um **inteiro** que recebe a propriedade **Count** .

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **Count** para recuperar a contagem de verbos disponíveis para a pasta do painel de controle. o uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderItemVerbsCountJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfCONTROLS = 3;
        
        objFolder2 = objShell.NameSpace(ssfCONTROLS);
        if (objFolder2 != null)
        {
            var objVerbs;
            
            objVerbs = objFolder2.Self.Verbs();

            if (objVerbs != null)
            {
                var nCount;
                nCount = objVerbs.Count;

                alert(nCount);
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemsCountVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfWINDOWS
                
            ssfWINDOWS = 36
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems
                        
                set objFolderItems = objFolder.Items()
                if (not objFolderItems is nothing) then
                    dim nCount
                    
                    nCount = objFolderItems.Count
                    alert(nCount)
                end if
                set objFolderItems = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
 </script>
```



Visual Basic:


```VB
Private Sub fnFolderItemsCountVB()
    Dim objShell   As Shell
    Dim objFolder  As Folder
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems As FolderItems
            
            Set objFolderItems = objFolder.Items
                If (Not objFolderItems Is Nothing) Then
                    Dim nCount As Integer
                    
                    nCount = objFolderItems.Count
                    Debug.Print nCount
                End If
            Set objFolderItems = Nothing
        End If
    Set objFolder = Nothing
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



 

 




