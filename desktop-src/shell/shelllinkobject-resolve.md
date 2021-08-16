---
description: Procura o destino de um link do Shell, mesmo que o destino tenha sido movido ou renomeado.
ms.assetid: 60e119be-8e45-4f63-a381-cad048de0765
title: Método ShellLinkObject.Resolve (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellLinkObject.Resolve
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fdff3fd1a606b8dbec35476988497dd14892692a42e6502343716264873c184d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857489"
---
# <a name="shelllinkobjectresolve-method"></a>Método ShellLinkObject.Resolve

Procura o destino de um link do Shell, mesmo que o destino tenha sido movido ou renomeado.

## <a name="syntax"></a>Sintaxe


```JScript
iRetVal = ShellLinkObject.Resolve(
  fFlags
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*fFlags* \[ Em\]
</dt> <dd>

Tipo: **Inteiro**

Sinalizadores que especificam a ação a ser tomada. Isso pode ser uma combinação dos seguintes valores:

<dt>



 (1)


</dt> <dd>

Não exibir uma caixa de diálogo se o link não puder ser resolvido. Quando esse sinalizador é definido, a palavra de ordem alta *de fFlags* especifica uma duração de tempo-tempo, em milissegundos. O método retornará se o link não puder ser resolvido dentro da duração do tempo-out. Se a palavra de ordem alta for definida como zero, a duração do tempo-out será padrão para 3.000 milissegundos (3 segundos).

</dd> <dt>



 (4)


</dt> <dd>

Se o link tiver sido alterado, atualize o caminho e a lista de identificadores.

</dd> <dt>



 (8)


</dt> <dd>

Não atualize as informações do link.

</dd> <dt>



 (16)


</dt> <dd>

Não execute a heurística de pesquisa.

</dd> <dt>



 (32)


</dt> <dd>

Não use o acompanhamento de link distribuído.

</dd> <dt>



 (64)


</dt> <dd>

Desabilite o acompanhamento de link distribuído. Por padrão, o rastreamento de link distribuído rastreia mídia removível em vários dispositivos com base no nome do volume. Ele também usa o caminho UNC para rastrear sistemas de arquivos remotos cuja letra da unidade foi alterada. Definir esse sinalizador desabilita os dois tipos de acompanhamento.

</dd> <dt>



 (128)


</dt> <dd>

Chame o Windows Instalador.

</dd> </dl> </dd> </dl>

## <a name="remarks"></a>Comentários

Esse método é essencialmente idêntico na funcionalidade para [**Resolver**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishelllinka-resolve). Para mais discussão sobre a resolução de link, consulte a seção Comentários dessa página.

## <a name="examples"></a>Exemplos

O exemplo a seguir mostra o uso adequado desse método para JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    function fnShellLinkObjectResolveJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder;
        var ssfPROGRAMS = 2;
        
        objFolder = objShell.NameSpace(ssfPROGRAMS);
        if (objFolder != null)
        {
            var objFolderItem;
            
            objFolderItem = objFolder.ParseName("Internet Explorer.lnk");
            if (objFolderItem != null)
            {
                var objShellLink;
                
                objShellLink = objFolderItem.GetLink;
                if (objShellLink != null)
                {
                    objShellLink.Resolve(1);
                }
            }
        }
    }
</script>
```



Vbscript:


```VB
<script language="VBScript">
    function fnShellLinkObjectResolveVB()
        dim objShell
        dim objFolder
        dim ssfPROGRAMS
        
        ssfPROGRAMS = 2
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace(ssfPROGRAMS)
            if (not objFolder is nothing) then
                dim objFolderItem
                
                set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                    if (not objFolderItem is nothing) then
                        dim objShellLink
                        
                        set objShellLink = objFolderItem.GetLink
                            if (not objShellLink is nothing) then
                                objShellLink.Resolve(1)
                            end if
                        set objShellLink = nothing
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
Private Sub fnShellLinkObjectResolveVB()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace(ssfPROGRAMS)
        If (Not objFolder Is Nothing) Then
            Dim objFolderItem As FolderItem
            
            Set objFolderItem = objFolder.ParseName("Internet Explorer.lnk")
                If (Not objFolderItem Is Nothing) Then
                    Dim objShellLink As ShellLinkObject
                    
                    Set objShellLink = objFolderItem.GetLink
                        If (Not objShellLink Is Nothing) Then
                            objShellLink.Resolve (1)
                        End If
                    Set objShellLink = Nothing
                End If
            Set objFolderItem = Nothing
        End If
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional somente com aplicativos da área de trabalho SP3 \[\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                          |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                          |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                        |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 5.0 ou posterior)</dt> </dl> |



 

 
