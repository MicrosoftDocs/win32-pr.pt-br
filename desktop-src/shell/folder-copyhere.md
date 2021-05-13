---
description: Copia um item ou itens para uma pasta.
title: Método Folder. CopyHere (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.CopyHere
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 22bf1b4c-f242-4c52-b094-c5339bb35d02
ms.openlocfilehash: 1466e5d01715c0c820cbc7cd9809c51e4963ec56
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842137"
---
# <a name="foldercopyhere-method"></a>Método Folder. CopyHere

Copia um item ou itens para uma pasta.

## <a name="syntax"></a>Sintaxe


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vItem* 
</dt> <dd>

Tipo: **variante**

O item ou itens a serem copiados. Pode ser uma cadeia de caracteres que representa um nome de arquivo, um objeto [**FolderItem**](folderitem.md) ou um objeto [**FolderItems**](folderitems.md) .

</dd> <dt>

*vOptions* \[ adicional\]
</dt> <dd>

Tipo: **variante**

Opções para a operação de cópia. Esse valor pode ser zero ou uma combinação dos valores a seguir. Esses valores se baseiam nos sinalizadores definidos para uso com o membro **fFlags** da estrutura C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) . Cada namespace de Shell deve fornecer sua própria implementação desses sinalizadores, e cada namespace pode optar por ignorar alguns ou até mesmo todos esses sinalizadores. Esses sinalizadores não são definidos pelo nome para Visual Basic, VBScript ou JScript, portanto, você deve defini-los por conta própria ou usar seus equivalentes numéricos.

> [!Note]  
> Em alguns casos, como arquivos compactados (. zip), alguns sinalizadores de opção podem ser ignorados por design.

 

<dt>



 (4)


</dt> <dd>

Não exibir uma caixa de diálogo de progresso.

</dd> <dt>



 (8)


</dt> <dd>

Dê ao arquivo operado em um novo nome em uma operação de movimentação, cópia ou renomeação se um arquivo com o nome de destino já existir.

</dd> <dt>



 (16)


</dt> <dd>

Responda com "Sim para todos" para qualquer caixa de diálogo que for exibida.

</dd> <dt>



 (64)


</dt> <dd>

Preserve as informações de desfazer, se possível.

</dd> <dt>



 (128)


</dt> <dd>

Execute a operação em arquivos somente se um nome de arquivo curinga ( \* . \* ) for especificado.

</dd> <dt>



 (256)


</dt> <dd>

Exibir uma caixa de diálogo de progresso, mas não mostrar os nomes de arquivo.

</dd> <dt>



 (512)


</dt> <dd>

Não confirme a criação de um novo diretório se a operação exigir que um seja criado.

</dd> <dt>



 (1024)


</dt> <dd>

Não exibir uma interface do usuário se ocorrer um erro.

</dd> <dt>



 (2048)


</dt> <dd>

[Versão 4.71.](versions.md) Não copie os atributos de segurança do arquivo.

</dd> <dt>



 (4096)


</dt> <dd>

Operar somente no diretório local. Não opere recursivamente em subdireários.

</dd> <dt>



 (8192)


</dt> <dd>

[Versão 5.0.](versions.md) Não copie arquivos conectados como um grupo. Copie apenas os arquivos especificados.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

Nenhuma notificação é dada ao programa de chamada para indicar que a cópia foi concluída.

> [!Note]  
> Nem todos os métodos são implementados para todas as pastas. Por exemplo, o método [**ParseName**](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL). Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.

 

## <a name="examples"></a>Exemplos

O exemplo a seguir usa **CopyHere** para copiar o arquivo de Autoexec.bat do diretório raiz para o diretório C: \\ Windows. O uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript


```JScript
<script language="JScript">
    function fnCopyHereJ()
    {
        var objShell = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.CopyHere("C:\\AUTOEXEC.BAT");
        }
    }
 </script>
```



VBScript


```VB
<script language="VBScript">
    function fnCopyHereVB()
        dim objShell
        dim objFolder
        
        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")
 
        if not objFolder is nothing then
            objFolder.CopyHere("C:\AUTOEXEC.BAT")
        end if
 
        set objShell = nothing
        set objFolder = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Sub btnCopyHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder
    
    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")
 
    If (Not objFolder Is Nothing) Then
        objFolder.CopyHere ("C:\AUTOEXEC.BAT")
    End If
 
    Set objFolder = Nothing
    Set objShell = Nothing
End Sub
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]<br/>                                         |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                           |
| Cabeçalho<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| INSERI<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (versão 4,71 ou posterior)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Pasta**](folder.md)
</dt> </dl>

 

 




