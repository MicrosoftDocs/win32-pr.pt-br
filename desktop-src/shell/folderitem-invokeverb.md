---
description: Executa um verbo no item.
ms.assetid: 569bdc88-15ef-4d08-923c-4f41e5ae5a38
title: Método FolderItem.InvokeVerb (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem.InvokeVerb
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1f6c45c67bd8863b6cf1169670a4d087f29e4441c48592f850a683af5ef0bc1d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111786"
---
# <a name="folderiteminvokeverb-method"></a>Método FolderItem.InvokeVerb

Executa um verbo no item.

## <a name="syntax"></a>Sintaxe


```JScript
FolderItem.InvokeVerb(
  [ vVerb ]
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vVerb* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

Uma cadeia de caracteres que especifica o verbo a ser executado. Ele deve ser um dos valores retornados pela propriedade FolderItemVerb.Name [**item.**](folderitemverb-name.md) Se nenhum verbo for especificado, o verbo padrão será invocado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Um verbo é uma cadeia de caracteres usada para especificar uma ação específica à qual um item dá suporte. Invocar um verbo é equivalente a selecionar um comando no menu de atalho de um item. Normalmente, invocar um verbo inicia um aplicativo relacionado. Por exemplo, invocar o verbo "abrir" em um arquivo .txt abre o arquivo com um editor de texto, geralmente Microsoft Bloco de notas. Consulte [Iniciando aplicativos](launch.md) para uma discussão mais sobre verbos.

O [**objeto FolderItemVerbs**](folderitemverbs.md) representa a coleção de verbos associados ao item. O verbo padrão pode variar para itens diferentes, mas normalmente é "aberto".

## <a name="examples"></a>Exemplos

O exemplo a seguir **usa InvokeVerb** para invocar o verbo padrão ("open" nesse caso) na pasta Windows dados. O uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderItemInvokeVerbJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder2;
        var ssfWINDOWS = 36;
        
        objFolder2 = objShell.NameSpace(ssfWINDOWS);
        if (objFolder2 != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder2.Self;
            if (objFolderItem != null)
            {
                var szReturn;
                
                objFolderItem.InvokeVerb();
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFolderItemInvokeVerbVB()
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
                    dim szReturn
                                
                    objFolderItem.InvokeVerb()
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
Private Sub fnFolderItemInvokeVerbVB()
    Dim objShell   As Shell
    Dim objFolder2 As Folder2
    Dim ssfWINDOWS As Long
    
    ssfWINDOWS = 36
    Set objShell = New Shell
    Set objFolder2 = objShell.NameSpace(ssfWINDOWS)
        If (Not objFolder2 Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder2.Self
                If (Not objFolderItem Is Nothing) Then
                    Dim szReturn As String
                    
                    objFolderItem.InvokeVerb
                Else
                    'FolderItem object returned nothing.
                End If
            Set objFolderItem = Nothing
        Else
            'Folder object returned nothing.
        End If
    Set objFolder2 = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FolderItem**](folderitem.md)
</dt> <dt>

[**Verbos**](folderitem-verbs.md)
</dt> <dt>

[**Doit**](folderitemverb-doit.md)
</dt> </dl>

 

 




