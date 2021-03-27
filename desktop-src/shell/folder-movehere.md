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
ms.openlocfilehash: da6590d63f4a3c79252e25f3625c0ee75b146b6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646569"
---
# <a name="foldermovehere-method"></a><span data-ttu-id="8c07f-103">Método Folder. MoveHere</span><span class="sxs-lookup"><span data-stu-id="8c07f-103">Folder.MoveHere method</span></span>

<span data-ttu-id="8c07f-104">Move um item ou itens para esta pasta.</span><span class="sxs-lookup"><span data-stu-id="8c07f-104">Moves an item or items to this folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c07f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c07f-105">Syntax</span></span>


```JScript
Folder.MoveHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="8c07f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c07f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c07f-107">*vItem* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c07f-107">*vItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c07f-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="8c07f-108">Type: **Variant**</span></span>

<span data-ttu-id="8c07f-109">O item ou os itens a serem movidos.</span><span class="sxs-lookup"><span data-stu-id="8c07f-109">The item or items to move.</span></span> <span data-ttu-id="8c07f-110">Pode ser uma cadeia de caracteres que representa um nome de arquivo, um objeto [**FolderItem**](folderitem.md) ou um objeto [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="8c07f-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="8c07f-111">*vOptions* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8c07f-111">*vOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8c07f-112">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="8c07f-112">Type: **Variant**</span></span>

<span data-ttu-id="8c07f-113">Opções para a operação de movimentação.</span><span class="sxs-lookup"><span data-stu-id="8c07f-113">Options for the move operation.</span></span> <span data-ttu-id="8c07f-114">Esse valor pode ser zero ou uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8c07f-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="8c07f-115">Esses valores se baseiam nos sinalizadores definidos para uso com o membro **fFlags** da estrutura C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="8c07f-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="8c07f-116">Esses sinalizadores não são definidos como tal para Visual Basic, VBScript ou JScript, portanto, você deve defini-los por conta própria ou usar seus equivalentes numéricos.</span><span class="sxs-lookup"><span data-stu-id="8c07f-116">These flags are not defined as such for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

<dt>



 <span data-ttu-id="8c07f-117">(4)</span><span class="sxs-lookup"><span data-stu-id="8c07f-117">(4)</span></span>


</dt> <dd>

<span data-ttu-id="8c07f-118">Não exibir uma caixa de diálogo de progresso.</span><span class="sxs-lookup"><span data-stu-id="8c07f-118">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="8c07f-119">(8)</span><span class="sxs-lookup"><span data-stu-id="8c07f-119">(8)</span></span>


</dt> <dd>

<span data-ttu-id="8c07f-120">Dê ao arquivo operado em um novo nome em uma operação de movimentação, cópia ou renomeação se um arquivo com o nome de destino já existir.</span><span class="sxs-lookup"><span data-stu-id="8c07f-120">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="8c07f-121">(16)</span><span class="sxs-lookup"><span data-stu-id="8c07f-121">(16)</span></span>


</dt> <dd>

<span data-ttu-id="8c07f-122">Responda com "Sim para todos" para qualquer caixa de diálogo que for exibida.</span><span class="sxs-lookup"><span data-stu-id="8c07f-122">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="8c07f-123">(64)</span><span class="sxs-lookup"><span data-stu-id="8c07f-123">(64)</span></span>


</dt> <dd>

<span data-ttu-id="8c07f-124">Preserve as informações de desfazer, se possível.</span><span class="sxs-lookup"><span data-stu-id="8c07f-124">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="8c07f-125">(128)</span><span class="sxs-lookup"><span data-stu-id="8c07f-125">(128)</span></span>


</dt> <dd>

<span data-ttu-id="8c07f-126">Execute a operação em arquivos somente se um nome de arquivo curinga ( \* . \* ) for especificado.</span><span class="sxs-lookup"><span data-stu-id="8c07f-126">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="8c07f-127">(256)</span><span class="sxs-lookup"><span data-stu-id="8c07f-127">(256)</span></span>


</dt> <dd>

<span data-ttu-id="8c07f-128">Exibir uma caixa de diálogo de progresso, mas não mostrar os nomes dos arquivos.</span><span class="sxs-lookup"><span data-stu-id="8c07f-128">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="8c07f-129">(512)</span><span class="sxs-lookup"><span data-stu-id="8c07f-129">(512)</span></span>


</dt> <dd>

<span data-ttu-id="8c07f-130">Não confirme a criação de um novo diretório se a operação exigir a criação de um.</span><span class="sxs-lookup"><span data-stu-id="8c07f-130">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="8c07f-131">(1024)</span><span class="sxs-lookup"><span data-stu-id="8c07f-131">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="8c07f-132">Não exibir uma interface do usuário se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="8c07f-132">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="8c07f-133">(2048)</span><span class="sxs-lookup"><span data-stu-id="8c07f-133">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="8c07f-134">Versão 4,71.</span><span class="sxs-lookup"><span data-stu-id="8c07f-134">Version 4.71.</span></span>](versions.md) <span data-ttu-id="8c07f-135">Não copie os atributos de segurança do arquivo.</span><span class="sxs-lookup"><span data-stu-id="8c07f-135">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="8c07f-136">(4096)</span><span class="sxs-lookup"><span data-stu-id="8c07f-136">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="8c07f-137">Operar somente no diretório local.</span><span class="sxs-lookup"><span data-stu-id="8c07f-137">Only operate in the local directory.</span></span> <span data-ttu-id="8c07f-138">Não opere recursivamente em subdiretórios.</span><span class="sxs-lookup"><span data-stu-id="8c07f-138">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="8c07f-139">(9182)</span><span class="sxs-lookup"><span data-stu-id="8c07f-139">(9182)</span></span>


</dt> <dd>

[<span data-ttu-id="8c07f-140">Versão 5,0.</span><span class="sxs-lookup"><span data-stu-id="8c07f-140">Version 5.0.</span></span>](versions.md) <span data-ttu-id="8c07f-141">Não mova os arquivos conectados como um grupo.</span><span class="sxs-lookup"><span data-stu-id="8c07f-141">Do not move connected files as a group.</span></span> <span data-ttu-id="8c07f-142">Mover apenas os arquivos especificados.</span><span class="sxs-lookup"><span data-stu-id="8c07f-142">Only move the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c07f-143">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c07f-143">Return value</span></span>

<span data-ttu-id="8c07f-144">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8c07f-144">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c07f-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c07f-145">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8c07f-146">Nem todos os métodos são implementados para todas as pastas.</span><span class="sxs-lookup"><span data-stu-id="8c07f-146">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="8c07f-147">Por exemplo, o método [**ParseName**](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="8c07f-147">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="8c07f-148">Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.</span><span class="sxs-lookup"><span data-stu-id="8c07f-148">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="8c07f-149">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8c07f-149">Examples</span></span>

<span data-ttu-id="8c07f-150">O exemplo a seguir usa **MoveHere** para mover o arquivo Temp.txt do diretório raiz da unidade c para a pasta c: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="8c07f-150">The following example uses **MoveHere** to move the file Temp.txt from the root directory of the C drive to the C:\\Windows folder.</span></span> <span data-ttu-id="8c07f-151">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="8c07f-151">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="8c07f-152">JScript</span><span class="sxs-lookup"><span data-stu-id="8c07f-152">JScript:</span></span>


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



<span data-ttu-id="8c07f-153">VBScript</span><span class="sxs-lookup"><span data-stu-id="8c07f-153">VBScript:</span></span>


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



<span data-ttu-id="8c07f-154">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="8c07f-154">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="8c07f-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8c07f-155">Requirements</span></span>



| <span data-ttu-id="8c07f-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="8c07f-156">Requirement</span></span> | <span data-ttu-id="8c07f-157">Valor</span><span class="sxs-lookup"><span data-stu-id="8c07f-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c07f-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c07f-158">Minimum supported client</span></span><br/> | <span data-ttu-id="8c07f-159">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="8c07f-159">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="8c07f-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8c07f-160">Minimum supported server</span></span><br/> | <span data-ttu-id="8c07f-161">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="8c07f-161">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="8c07f-162">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8c07f-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c07f-163"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8c07f-163"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="8c07f-164">INSERI</span><span class="sxs-lookup"><span data-stu-id="8c07f-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8c07f-165"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8c07f-165"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="8c07f-166">DLL</span><span class="sxs-lookup"><span data-stu-id="8c07f-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8c07f-167"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="8c07f-167"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



 

 




