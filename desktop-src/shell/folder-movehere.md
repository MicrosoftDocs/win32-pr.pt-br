---
description: Move um item ou itens para esta pasta.
ms.assetid: 07723dc1-5d9d-4f32-ab18-52617b0988c4
title: Método Folder. MoveHere (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder.MoveHere
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: eb826d23a168d81d838341e96fa5e613f8b6f5261a3cda548a2be320acebbde8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118458914"
---
# <a name="foldermovehere-method"></a>Método Folder. MoveHere

Move um item ou itens para esta pasta.

## <a name="syntax"></a>Sintaxe


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*vItem* \[ no\]
</dt> <dd>

Tipo: **variante**

O item ou os itens a serem movidos. Pode ser uma cadeia de caracteres que representa um nome de arquivo, um objeto [**FolderItem**](folderitem.md) ou um objeto [**FolderItems**](folderitems.md) .

</dd> <dt>

*vOptions* \[ em, opcional\]
</dt> <dd>

Tipo: **variante**

Opções para a operação de movimentação. Esse valor pode ser zero ou uma combinação dos valores a seguir. Esses valores se baseiam nos sinalizadores definidos para uso com o membro **fFlags** da estrutura C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) . esses sinalizadores não são definidos como tal para Visual Basic, VBScript ou JScript, portanto, você deve defini-los por conta própria ou usar seus equivalentes numéricos.

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

Exibir uma caixa de diálogo de progresso, mas não mostrar os nomes dos arquivos.

</dd> <dt>



 (512)


</dt> <dd>

Não confirme a criação de um novo diretório se a operação exigir a criação de um.

</dd> <dt>



 (1024)


</dt> <dd>

Não exibir uma interface do usuário se ocorrer um erro.

</dd> <dt>



 (2048)


</dt> <dd>

[Versão 4,71.](versions.md) Não copie os atributos de segurança do arquivo.

</dd> <dt>



 (4096)


</dt> <dd>

Operar somente no diretório local. Não opere recursivamente em subdiretórios.

</dd> <dt>



 (9182)


</dt> <dd>

[Versão 5,0.](versions.md) Não mova os arquivos conectados como um grupo. Mover apenas os arquivos especificados.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método não retorna um valor.

## <a name="remarks"></a>Comentários

> [!Note]  
> Nem todos os métodos são implementados para todas as pastas. Por exemplo, o método [**ParseName**](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL). Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.

 

## <a name="examples"></a>Exemplos

o exemplo a seguir usa **MoveHere** para mover o arquivo Temp.txt do diretório raiz da unidade c para a pasta c: \\ Windows. o uso adequado é mostrado para JScript, VBScript e Visual Basic.

JScript:


```JScript
<script language="JScript">
    var FOF_NOCONFIRMATION = 16;

    function fnFolderObjectMoveHereJ()
    {
        var objShell  = new ActiveXObject("shell.application");
        var objFolder = new Object;
        
        objFolder = objShell.NameSpace("C:\\WINDOWS");
        if (objFolder != null)
        {
            objFolder.MoveHere ("C:\\temp.txt", FOF_NOCONFIRMATION);
        }
    }
</script>
```



VBScript


```VB
<script language="VBScript">
    private const FOF_NOCONFIRMATION = 16
    
    function fnFolderObjectMoveHereVB()
        dim objShell
        dim objFolder

        set objShell = CreateObject("shell.application")
        set objFolder = objShell.NameSpace("C:\WINDOWS")

        if (not objFolder is nothing) then
            objFolder.MoveHere "C:\temp.txt", FOF_NOCONFIRMATION
        end if

        set objFolder = nothing
        set objShell = nothing
    end function
</script>
```



Visual Basic:


```VB
Private Const FOF_NOCONFIRMATION = &H10

Private Sub btnMoveHere_Click()
    Dim objShell  As Shell
    Dim objFolder As Folder

    Set objShell = New Shell
    Set objFolder = objShell.NameSpace("C:\WINDOWS")

    If (Not objFolder Is Nothing) Then
        objFolder.MoveHere "c:\temp.txt", FOF_NOCONFIRMATION
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



 

 




