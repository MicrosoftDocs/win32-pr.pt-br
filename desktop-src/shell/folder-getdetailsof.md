---
description: Recupera detalhes sobre um item em uma pasta. Por exemplo, seu tamanho, tipo ou a hora de sua última modificação.
ms.assetid: d2fe4550-f171-40d9-8bce-065b61826997
title: Método Folder.GetDetailsOf (Shlobj \_ core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.GetDetailsOf
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c703150069bc839f2d20024c0de8f3197fba09c5c3571e3de818dec3f3d6737c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860324"
---
# <a name="foldergetdetailsof-method"></a>Método Folder.GetDetailsOf

Recupera detalhes sobre um item em uma pasta. Por exemplo, seu tamanho, tipo ou a hora de sua última modificação.

## <a name="syntax"></a>Sintaxe


```JScript
retVal = Folder.GetDetailsOf(
  vItem,
  iColumn
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Vitem* 
</dt> <dd>

Tipo: **Variante**

O item para o qual recuperar as informações. Deve ser um [**objeto FolderItem.**](folderitem.md)

</dd> <dt>

*Icolumn* 
</dt> <dd>

Tipo: **Inteiro**

Um **valor** inteiro que especifica as informações a serem recuperadas. As informações disponíveis para um item dependem da pasta na qual ele é exibido. Esse valor corresponde ao número de coluna baseado em zero que é exibido em uma exibição shell. Para um item no sistema de arquivos, esse pode ser um dos seguintes valores:

<dt>



  acima (0)


</dt> <dd>

Recupera o nome do item.

</dd> <dt>



 (1)


</dt> <dd>

Recupera o tamanho do item.

</dd> <dt>



 (2)


</dt> <dd>

Recupera o tipo do item.

</dd> <dt>



 (3)


</dt> <dd>

Recupera a data e a hora em que o item foi modificado pela última vez.

</dd> <dt>



 (4)


</dt> <dd>

Recupera os atributos do item.

</dd> <dt>



 (-1)


</dt> <dd>

Recupera as informações de dica de informações para o item.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)\***

Cadeia de caracteres que contém os detalhes recuperados.

## <a name="remarks"></a>Comentários

> [!Note]  
> Nem todos os métodos são implementados para todas as pastas. Por exemplo, o [**método ParseName**](folder-parsename.md) não é implementado para a pasta Painel de Controle (CSIDL \_ CONTROLS). Se você tentar chamar um método não simplificado, um erro 0x800A01BD (decimal 445) será gerado.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir **usa GetDetailsOf** para recuperar o tipo do arquivo chamado Clock.avi. O uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnGetDetailsOfJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            var objFolderItem = new Object;

            objFolderItem = objFolder.ParseName("clock.avi");
            if (objFolderItem != null)
            {
                var objInfo = new Object;

                objInfo = objFolder.GetDetailsOf(objFolderItem, 2);
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnGetDetailsOfVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            dim objFolderItem

            set objFolderItem = objFolder.ParseName("clock.avi")

            if (not objFolderItem Is Nothing) then
                dim objInfo
                        
                objInfo = objFolder.GetDetailsOf(objFolderItem, 2)
            end if
            
            set objFolderItem = nothing
        end if
        
        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnGetDetailsOf_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
    
    If (Not objFolder Is Nothing) Then
        Dim objFolderItem As FolderItem
        Set objFolderItem = objFolder.ParseName("clock.avi")
   
        If (Not objFolderItem Is Nothing) Then
            Dim szItem As String
            szItem = objFolder.GetDetailsOf(objFolderItem, 2)
        End If
        
        Set objFolderItem = Nothing
    End If
    
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, Windows aplicativos da área de \[ trabalho XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shlobj \_ core.h (inclua Shldisp.h)</dt> </dl>  |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4.71 ou posterior)</dt> </dl> |



 

 
