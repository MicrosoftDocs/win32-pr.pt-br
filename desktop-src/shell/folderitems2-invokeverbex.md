---
description: Executa um verbo em uma coleção de objetos FolderItem. Esse método é uma extensão do método InvokeVerb, permitindo o controle adicional da operação por meio de um conjunto de sinalizadores.
ms.assetid: 2c02985d-8877-4a02-a232-6aeb1716928c
title: Método FolderItems2.InvokeVerbEx (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems2.InvokeVerbEx
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 94d62de132a61bb357acac77aea41d2278ba1eb4453afa826ac32be90095ab25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860145"
---
# <a name="folderitems2invokeverbex-method"></a>Método FolderItems2.InvokeVerbEx

Executa um verbo em uma coleção de [**objetos FolderItem.**](folderitem.md) Esse método é uma extensão do método [**InvokeVerb,**](folderitem-invokeverb.md) permitindo o controle adicional da operação por meio de um conjunto de sinalizadores.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = FolderItems2.InvokeVerbEx(
  [ vVerb ],
  [ vArgs ]
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vVerb* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

Uma **Variante** com a cadeia de caracteres de verbo que corresponde ao comando a ser executado. Se nenhum verbo for especificado, o verbo padrão será executado.

</dd> <dt>

*vArgs* \[ in, opcional\]
</dt> <dd>

Tipo: **Variante**

Uma **Variante** que consiste em uma cadeia de caracteres com um ou mais argumentos para o comando especificado por *vVerb*. O formato dessa cadeia de caracteres depende do verbo específico.

</dd> </dl>

## <a name="remarks"></a>Comentários

Um verbo é uma cadeia de caracteres usada para especificar uma ação específica associada a um item ou coleção de itens. Normalmente, chamar um verbo inicia um aplicativo relacionado. Por exemplo, chamar o **verbo aberto** em um arquivo .txt normalmente abre o arquivo com um editor de texto, geralmente Microsoft Bloco de notas. Para mais discussão sobre verbos, consulte [Iniciando aplicativos](launch.md).

## <a name="examples"></a>Exemplos

O exemplo a seguir **usa InvokeVerbEx** para invocar o verbo padrão ("open") no **Meu Computador**. O uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnFolderItems2InvokeVerbExJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder;
        var ssfDRIVES = 17;
        
        objFolder = objShell.NameSpace(ssfDRIVES);
        if (objFolder != null)
        {
            var objFolderItems2;
            
            objFolderItems2 = objFolder.Items();
            if (objFolderItems2 != null)
            {
                objFolderItems2.InvokeVerbEx();
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnFolderItems2InvokeVerbExVB()
        dim objShell
        
        set objShell = CreateObject("shell.application")
        if (not objShell is nothing) then
            dim objFolder
            dim ssfDRIVES
                
            ssfWINDOWS = 17
            set objFolder = objShell.NameSpace(ssfWINDOWS)
            if (not objFolder is nothing) then
                dim objFolderItems2
                        
                set objFolderItems2 = objFolder.Items()
                if (not objFolderItems2 is nothing) then
                    objFolderItems2.InvokeVerbEx
                end if
                set objFolderItems2 = nothing
            end if
            set objFolder = nothing
        end if
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub fnFolderItems2InvokeVerbExVB()
    Dim objShell      As Shell
    Dim objFolder     As Folder2
    Dim ssfDRIVES     As Long
    
    ssfDRIVES = 17
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfDRIVES)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItems2 As FolderItems
            
            Set objFolderItems2 = objFolder.Items
                If (Not objFolderItems2 Is Nothing) Then
                    objFolderItems2.InvokeVerbEx
                End If
            Set objFolderItems2 = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**FolderItems2**](folderitems2-object.md)
</dt> <dt>

[**InvokeVerb**](folderitem-invokeverb.md)
</dt> </dl>

 

 




