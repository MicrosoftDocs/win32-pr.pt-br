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
# <a name="foldercopyhere-method"></a><span data-ttu-id="2d810-103">Método Folder. CopyHere</span><span class="sxs-lookup"><span data-stu-id="2d810-103">Folder.CopyHere method</span></span>

<span data-ttu-id="2d810-104">Copia um item ou itens para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="2d810-104">Copies an item or items to a folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d810-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2d810-105">Syntax</span></span>


```JScript
Folder.CopyHere(
  vItem,
  [ vOptions ]
)
```



## <a name="parameters"></a><span data-ttu-id="2d810-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2d810-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d810-107">*vItem*</span><span class="sxs-lookup"><span data-stu-id="2d810-107">*vItem*</span></span> 
</dt> <dd>

<span data-ttu-id="2d810-108">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="2d810-108">Type: **Variant**</span></span>

<span data-ttu-id="2d810-109">O item ou itens a serem copiados.</span><span class="sxs-lookup"><span data-stu-id="2d810-109">The item or items to copy.</span></span> <span data-ttu-id="2d810-110">Pode ser uma cadeia de caracteres que representa um nome de arquivo, um objeto [**FolderItem**](folderitem.md) ou um objeto [**FolderItems**](folderitems.md) .</span><span class="sxs-lookup"><span data-stu-id="2d810-110">This can be a string that represents a file name, a [**FolderItem**](folderitem.md) object, or a [**FolderItems**](folderitems.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="2d810-111">*vOptions* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="2d810-111">*vOptions* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="2d810-112">Tipo: **variante**</span><span class="sxs-lookup"><span data-stu-id="2d810-112">Type: **Variant**</span></span>

<span data-ttu-id="2d810-113">Opções para a operação de cópia.</span><span class="sxs-lookup"><span data-stu-id="2d810-113">Options for the copy operation.</span></span> <span data-ttu-id="2d810-114">Esse valor pode ser zero ou uma combinação dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2d810-114">This value can be zero or a combination of the following values.</span></span> <span data-ttu-id="2d810-115">Esses valores se baseiam nos sinalizadores definidos para uso com o membro **fFlags** da estrutura C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) .</span><span class="sxs-lookup"><span data-stu-id="2d810-115">These values are based upon flags defined for use with the **fFlags** member of the C++ [**SHFILEOPSTRUCT**](/windows/desktop/api/Shellapi/ns-shellapi-shfileopstructa) structure.</span></span> <span data-ttu-id="2d810-116">Cada namespace de Shell deve fornecer sua própria implementação desses sinalizadores, e cada namespace pode optar por ignorar alguns ou até mesmo todos esses sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="2d810-116">Each Shell namespace must provide its own implementation of these flags, and each namespace can choose to ignore some or even all of these flags.</span></span> <span data-ttu-id="2d810-117">Esses sinalizadores não são definidos pelo nome para Visual Basic, VBScript ou JScript, portanto, você deve defini-los por conta própria ou usar seus equivalentes numéricos.</span><span class="sxs-lookup"><span data-stu-id="2d810-117">These flags are not defined by name for Visual Basic, VBScript, or JScript, so you must define them yourself or use their numeric equivalents.</span></span>

> [!Note]  
> <span data-ttu-id="2d810-118">Em alguns casos, como arquivos compactados (. zip), alguns sinalizadores de opção podem ser ignorados por design.</span><span class="sxs-lookup"><span data-stu-id="2d810-118">In some cases, such as compressed (.zip) files, some option flags may be ignored by design.</span></span>

 

<dt>



 <span data-ttu-id="2d810-119">(4)</span><span class="sxs-lookup"><span data-stu-id="2d810-119">(4)</span></span>


</dt> <dd>

<span data-ttu-id="2d810-120">Não exibir uma caixa de diálogo de progresso.</span><span class="sxs-lookup"><span data-stu-id="2d810-120">Do not display a progress dialog box.</span></span>

</dd> <dt>



 <span data-ttu-id="2d810-121">(8)</span><span class="sxs-lookup"><span data-stu-id="2d810-121">(8)</span></span>


</dt> <dd>

<span data-ttu-id="2d810-122">Dê ao arquivo operado em um novo nome em uma operação de movimentação, cópia ou renomeação se um arquivo com o nome de destino já existir.</span><span class="sxs-lookup"><span data-stu-id="2d810-122">Give the file being operated on a new name in a move, copy, or rename operation if a file with the target name already exists.</span></span>

</dd> <dt>



 <span data-ttu-id="2d810-123">(16)</span><span class="sxs-lookup"><span data-stu-id="2d810-123">(16)</span></span>


</dt> <dd>

<span data-ttu-id="2d810-124">Responda com "Sim para todos" para qualquer caixa de diálogo que for exibida.</span><span class="sxs-lookup"><span data-stu-id="2d810-124">Respond with "Yes to All" for any dialog box that is displayed.</span></span>

</dd> <dt>



 <span data-ttu-id="2d810-125">(64)</span><span class="sxs-lookup"><span data-stu-id="2d810-125">(64)</span></span>


</dt> <dd>

<span data-ttu-id="2d810-126">Preserve as informações de desfazer, se possível.</span><span class="sxs-lookup"><span data-stu-id="2d810-126">Preserve undo information, if possible.</span></span>

</dd> <dt>



 <span data-ttu-id="2d810-127">(128)</span><span class="sxs-lookup"><span data-stu-id="2d810-127">(128)</span></span>


</dt> <dd>

<span data-ttu-id="2d810-128">Execute a operação em arquivos somente se um nome de arquivo curinga ( \* . \* ) for especificado.</span><span class="sxs-lookup"><span data-stu-id="2d810-128">Perform the operation on files only if a wildcard file name (\*.\*) is specified.</span></span>

</dd> <dt>



 <span data-ttu-id="2d810-129">(256)</span><span class="sxs-lookup"><span data-stu-id="2d810-129">(256)</span></span>


</dt> <dd>

<span data-ttu-id="2d810-130">Exibir uma caixa de diálogo de progresso, mas não mostrar os nomes de arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d810-130">Display a progress dialog box but do not show the file names.</span></span>

</dd> <dt>



 <span data-ttu-id="2d810-131">(512)</span><span class="sxs-lookup"><span data-stu-id="2d810-131">(512)</span></span>


</dt> <dd>

<span data-ttu-id="2d810-132">Não confirme a criação de um novo diretório se a operação exigir que um seja criado.</span><span class="sxs-lookup"><span data-stu-id="2d810-132">Do not confirm the creation of a new directory if the operation requires one to be created.</span></span>

</dd> <dt>



 <span data-ttu-id="2d810-133">(1024)</span><span class="sxs-lookup"><span data-stu-id="2d810-133">(1024)</span></span>


</dt> <dd>

<span data-ttu-id="2d810-134">Não exibir uma interface do usuário se ocorrer um erro.</span><span class="sxs-lookup"><span data-stu-id="2d810-134">Do not display a user interface if an error occurs.</span></span>

</dd> <dt>



 <span data-ttu-id="2d810-135">(2048)</span><span class="sxs-lookup"><span data-stu-id="2d810-135">(2048)</span></span>


</dt> <dd>

[<span data-ttu-id="2d810-136">Versão 4.71.</span><span class="sxs-lookup"><span data-stu-id="2d810-136">Version 4.71.</span></span>](versions.md) <span data-ttu-id="2d810-137">Não copie os atributos de segurança do arquivo.</span><span class="sxs-lookup"><span data-stu-id="2d810-137">Do not copy the security attributes of the file.</span></span>

</dd> <dt>



 <span data-ttu-id="2d810-138">(4096)</span><span class="sxs-lookup"><span data-stu-id="2d810-138">(4096)</span></span>


</dt> <dd>

<span data-ttu-id="2d810-139">Operar somente no diretório local.</span><span class="sxs-lookup"><span data-stu-id="2d810-139">Only operate in the local directory.</span></span> <span data-ttu-id="2d810-140">Não opere recursivamente em subdireários.</span><span class="sxs-lookup"><span data-stu-id="2d810-140">Do not operate recursively into subdirectories.</span></span>

</dd> <dt>



 <span data-ttu-id="2d810-141">(8192)</span><span class="sxs-lookup"><span data-stu-id="2d810-141">(8192)</span></span>


</dt> <dd>

[<span data-ttu-id="2d810-142">Versão 5.0.</span><span class="sxs-lookup"><span data-stu-id="2d810-142">Version 5.0.</span></span>](versions.md) <span data-ttu-id="2d810-143">Não copie arquivos conectados como um grupo.</span><span class="sxs-lookup"><span data-stu-id="2d810-143">Do not copy connected files as a group.</span></span> <span data-ttu-id="2d810-144">Copie apenas os arquivos especificados.</span><span class="sxs-lookup"><span data-stu-id="2d810-144">Only copy the specified files.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d810-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2d810-145">Return value</span></span>

<span data-ttu-id="2d810-146">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2d810-146">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2d810-147">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d810-147">Remarks</span></span>

<span data-ttu-id="2d810-148">Nenhuma notificação é dada ao programa de chamada para indicar que a cópia foi concluída.</span><span class="sxs-lookup"><span data-stu-id="2d810-148">No notification is given to the calling program to indicate that the copy has completed.</span></span>

> [!Note]  
> <span data-ttu-id="2d810-149">Nem todos os métodos são implementados para todas as pastas.</span><span class="sxs-lookup"><span data-stu-id="2d810-149">Not all methods are implemented for all folders.</span></span> <span data-ttu-id="2d810-150">Por exemplo, o método [**ParseName**](folder-parsename.md) não é implementado para a pasta do painel de controle ( \_ controles CSIDL).</span><span class="sxs-lookup"><span data-stu-id="2d810-150">For example, the [**ParseName**](folder-parsename.md) method is not implemented for the Control Panel folder (CSIDL\_CONTROLS).</span></span> <span data-ttu-id="2d810-151">Se você tentar chamar um método não implementado, um erro 0x800A01BD (decimal 445) será gerado.</span><span class="sxs-lookup"><span data-stu-id="2d810-151">If you attempt to call an unimplemented method, a 0x800A01BD (decimal 445) error is raised.</span></span>

 

## <a name="examples"></a><span data-ttu-id="2d810-152">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2d810-152">Examples</span></span>

<span data-ttu-id="2d810-153">O exemplo a seguir usa **CopyHere** para copiar o arquivo de Autoexec.bat do diretório raiz para o diretório C: \\ Windows.</span><span class="sxs-lookup"><span data-stu-id="2d810-153">The following example uses **CopyHere** to copy the Autoexec.bat file from the root directory to the C:\\Windows directory.</span></span> <span data-ttu-id="2d810-154">O uso adequado é mostrado para JScript, VBScript e Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="2d810-154">Proper usage is shown for JScript, VBScript, and Visual Basic.</span></span>

<span data-ttu-id="2d810-155">JScript</span><span class="sxs-lookup"><span data-stu-id="2d810-155">JScript:</span></span>


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



<span data-ttu-id="2d810-156">VBScript</span><span class="sxs-lookup"><span data-stu-id="2d810-156">VBScript:</span></span>


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



<span data-ttu-id="2d810-157">Visual Basic:</span><span class="sxs-lookup"><span data-stu-id="2d810-157">Visual Basic:</span></span>


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



## <a name="requirements"></a><span data-ttu-id="2d810-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d810-158">Requirements</span></span>



| <span data-ttu-id="2d810-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d810-159">Requirement</span></span> | <span data-ttu-id="2d810-160">Valor</span><span class="sxs-lookup"><span data-stu-id="2d810-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d810-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d810-161">Minimum supported client</span></span><br/> | <span data-ttu-id="2d810-162">Windows 2000 Professional, \[ somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="2d810-162">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="2d810-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d810-163">Minimum supported server</span></span><br/> | <span data-ttu-id="2d810-164">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="2d810-164">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2d810-165">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="2d810-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d810-166"><dt>Shldisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d810-166"><dt>Shldisp.h</dt></span></span> </dl>                           |
| <span data-ttu-id="2d810-167">INSERI</span><span class="sxs-lookup"><span data-stu-id="2d810-167">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2d810-168"><dt>Shldisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2d810-168"><dt>Shldisp.idl</dt></span></span> </dl>                         |
| <span data-ttu-id="2d810-169">DLL</span><span class="sxs-lookup"><span data-stu-id="2d810-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d810-170"><dt>Shell32.dll (versão 4,71 ou posterior)</dt></span><span class="sxs-lookup"><span data-stu-id="2d810-170"><dt>Shell32.dll (version 4.71 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d810-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d810-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d810-172">**Pasta**</span><span class="sxs-lookup"><span data-stu-id="2d810-172">**Folder**</span></span>](folder.md)
</dt> </dl>

 

 




