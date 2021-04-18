---
description: Obtém o valor de uma propriedade do conjunto de propriedades de um item. A propriedade pode ser especificada por nome ou pelo identificador de formato do conjunto de Propriedades (FMTID) e pelo identificador de propriedade (PID).
ms.assetid: ca787d7b-d95a-45b9-9627-fd505f99f868
title: Método ShellFolderItem. Extended (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderItem.ExtendedProperty
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 614e42512b17a0d8a6950ac96914128b8746c685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968122"
---
# <a name="shellfolderitemextendedproperty-method"></a>Método ShellFolderItem. Extended

Obtém o valor de uma propriedade do conjunto de propriedades de um item. A propriedade pode ser especificada por nome ou pelo identificador de formato do conjunto de Propriedades (FMTID) e pelo identificador de propriedade (PID).

## <a name="syntax"></a>Sintaxe


```JScript
retVal = ShellFolderItem.ExtendedProperty(
  sPropName
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*sPropName* \[ no\]
</dt> <dd>

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Um valor de **cadeia de caracteres** que especifica a propriedade. Consulte a seção comentários para obter detalhes.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **Variant \** _

Quando esse método retornar, conterá o valor da propriedade, se existir para o item especificado. O valor terá uma digitação completa — por exemplo, datas são retornadas como datas, não cadeias de caracteres.

Esse método retornará uma cadeia de caracteres de comprimento zero se a propriedade for válida, mas não existir para o item especificado, ou então um código de erro.

## <a name="remarks"></a>Comentários

Há duas maneiras de especificar uma propriedade. A primeira é atribuir o nome conhecido da propriedade, como "autor" ou "data", a _sPropName *. No entanto, cada propriedade é um membro de um conjunto de propriedades de Component Object Model (COM) e também pode ser identificada especificando sua ID de formato (FMTID) e ID de propriedade (PID). Um [**FMTID**](../stg/structured-storage-serialized-property-set-format.md) é um GUID que identifica o conjunto de propriedades e um [**pid**](../stg/structured-storage-serialized-property-set-format.md) é um inteiro que identifica uma propriedade específica dentro do conjunto de propriedades.

Especificar uma propriedade por seus valores FMTID/PID é geralmente mais eficiente do que usar seu nome. Para usar os valores de FMTID/PID de uma propriedade com **Extendeproperty**, eles devem ser combinados em um scid. Um SCID é uma cadeia de caracteres que contém os valores FMTID/PID no formato "*FMTID * * PID*", em que FMTID é a forma de cadeia de caracteres do GUID do conjunto de propriedades. Por exemplo, o SCID da propriedade autor do conjunto de propriedades de informações de resumo é "{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 4".

Para obter uma lista de FMTIDs e PIDs que atualmente têm suporte no Shell, consulte [**SHCOLUMNID**](./objects.md).

## <a name="examples"></a>Exemplos

Este código de exemplo ilustra como usar o **Extended** para recuperar as propriedades "title" e "Author" de um documento do Word. Depois que você tiver o objeto [**ShellFolderItem**](shellfolderitem-object.md) associado ao arquivo, *fiWordDoc* neste exemplo, recupere o valor da propriedade, passando seu nome para **Extended**.


```none
...
Doc_Title=fiWordDoc.ExtendedProperty("DocTitle")
Doc_Author=fiWordDoc.ExtendedProperty("Author")
...
```



Uma abordagem mais rápida e eficiente é passar um scid para o **Extended**.


```none
...
FMTID_SummaryInfo="{F29F85E0-4FF9-1068-AB91-08002B27B3D9}"
PID_TITLE="2"
PID_AUTHOR="4"
SCID_TITLE=FMTID_SummaryInfo+" "+PID_TITLE
SCID_AUTHOR=FMTID_SummaryInfo+" "+PID_AUTHOR
Doc_Title=fiWordDoc.ExtendedProperty(SCID_TITLE)
Doc_Author=fiWordDoc.ExtendedProperty(SCID_AUTHOR)
...
```



Os exemplos a seguir mostram o uso apropriado desse método para JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnFolderItem2ExtendedPropertyJ()
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
                var szReturn = "";
                
                szReturn = objFolderItem.ExtendedProperty("infotip");
                alert(szReturn);
            }
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    function fnFolderItemExtendedPropertyVB()
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
                    
                    szReturn = objFolderItem.ExtendedProperty("type")
                    alert(szReturn)
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
Private Sub fnFolderItem2ExtendedPropertyVB()
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
                    Dim szReturn As String
                    
                    szReturn = objFolderItem2.ExtendedProperty("size")
                    Debug.Print szReturn
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
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                                    |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                          |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5,0 ou posterior)</dt> </dl> |



 

 
