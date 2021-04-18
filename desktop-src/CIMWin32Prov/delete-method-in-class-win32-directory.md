---
description: O método excluir classe WMI excluirá o arquivo lógico (ou diretório) especificado no caminho do objeto.
ms.assetid: 5663b8a8-3089-475b-8a36-454a7315bfca
ms.tgt_platform: multiple
title: Método Delete da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Delete
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 843583698c11c1b9ad8f08e83aa6e4b894b55db8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105749092"
---
# <a name="delete-method-of-the-win32_directory-class"></a><span data-ttu-id="6471d-103">Excluir o método da \_ classe do diretório Win32</span><span class="sxs-lookup"><span data-stu-id="6471d-103">Delete method of the Win32\_Directory class</span></span>

<span data-ttu-id="6471d-104">O método **excluir** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) excluirá o arquivo lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="6471d-104">The **Delete** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method will delete the logical file (or directory) specified in the object path.</span></span>

<span data-ttu-id="6471d-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="6471d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="6471d-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="6471d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="6471d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6471d-107">Syntax</span></span>


```mof
uint32 Delete();
```



## <a name="parameters"></a><span data-ttu-id="6471d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6471d-108">Parameters</span></span>

<span data-ttu-id="6471d-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6471d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6471d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6471d-110">Return value</span></span>

<span data-ttu-id="6471d-111">Retorna um valor de 0 (zero) se o arquivo foi excluído com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="6471d-111">Returns a value of 0 (zero) if the file was successfully deleted, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="6471d-112">**0**</span><span class="sxs-lookup"><span data-stu-id="6471d-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="6471d-113">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="6471d-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="6471d-114">**2**</span><span class="sxs-lookup"><span data-stu-id="6471d-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="6471d-115">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="6471d-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="6471d-116">**8**</span><span class="sxs-lookup"><span data-stu-id="6471d-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="6471d-117">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="6471d-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="6471d-118">**9**</span><span class="sxs-lookup"><span data-stu-id="6471d-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="6471d-119">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="6471d-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6471d-120">**10**</span><span class="sxs-lookup"><span data-stu-id="6471d-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="6471d-121">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="6471d-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="6471d-122">**11**</span><span class="sxs-lookup"><span data-stu-id="6471d-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="6471d-123">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="6471d-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="6471d-124">**12**</span><span class="sxs-lookup"><span data-stu-id="6471d-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="6471d-125">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="6471d-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="6471d-126">**13**</span><span class="sxs-lookup"><span data-stu-id="6471d-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="6471d-127">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="6471d-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="6471d-128">**14**</span><span class="sxs-lookup"><span data-stu-id="6471d-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="6471d-129">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="6471d-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="6471d-130">**15**</span><span class="sxs-lookup"><span data-stu-id="6471d-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="6471d-131">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="6471d-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="6471d-132">**16**</span><span class="sxs-lookup"><span data-stu-id="6471d-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="6471d-133">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="6471d-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="6471d-134">**17**</span><span class="sxs-lookup"><span data-stu-id="6471d-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="6471d-135">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="6471d-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="6471d-136">**Abril**</span><span class="sxs-lookup"><span data-stu-id="6471d-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="6471d-137">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="6471d-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6471d-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="6471d-138">Remarks</span></span>

<span data-ttu-id="6471d-139">As pastas não são necessariamente adições permanentes a um sistema de arquivos.</span><span class="sxs-lookup"><span data-stu-id="6471d-139">Folders are not necessarily permanent additions to a file system.</span></span> <span data-ttu-id="6471d-140">Em algum momento, as pastas talvez precisem ser excluídas, talvez porque não sejam mais necessárias, porque a função do computador foi alterada ou porque as pastas foram criadas por engano.</span><span class="sxs-lookup"><span data-stu-id="6471d-140">At some point, folders might need to be deleted, perhaps because they are no longer required, because the role of the computer has changed, or because the folders were created by mistake.</span></span>

<span data-ttu-id="6471d-141">Excluir permite que você exclua pastas: basta associar-se à pasta em questão e, em seguida, chamar o método Delete.</span><span class="sxs-lookup"><span data-stu-id="6471d-141">Delete allows you to delete folders: you simply bind to the folder in question and then call the Delete method.</span></span> <span data-ttu-id="6471d-142">Depois que o método Delete é chamado, a pasta é permanentemente removida do sistema de arquivos; Ele não é enviado para a lixeira.</span><span class="sxs-lookup"><span data-stu-id="6471d-142">After the Delete method is called, the folder is permanently removed from the file system; it is not sent to the Recycle Bin.</span></span> <span data-ttu-id="6471d-143">Além disso, nenhum aviso de confirmação ("tem certeza de que deseja excluir esta pasta?") é emitido.</span><span class="sxs-lookup"><span data-stu-id="6471d-143">In addition, no confirmation notice ("Are you sure you want to delete this folder?") is issued.</span></span> <span data-ttu-id="6471d-144">Em vez disso, a pasta é removida imediatamente.</span><span class="sxs-lookup"><span data-stu-id="6471d-144">Instead, the folder is immediately removed.</span></span>

<span data-ttu-id="6471d-145">Você não pode excluir pastas somente leitura usando o FileSystemObject; no entanto, isso pode ser feito usando o WMI.</span><span class="sxs-lookup"><span data-stu-id="6471d-145">You cannot delete read-only folders using the FileSystemObject; however, this can be done using WMI.</span></span> <span data-ttu-id="6471d-146">Se o seu script usa o WMI e você não deseja remover uma pasta somente leitura, você deve usar a propriedade legível para verificar o status da pasta antes de excluí-la.</span><span class="sxs-lookup"><span data-stu-id="6471d-146">If your script uses WMI and you do not want to remove a read-only folder, you must use the Readable property to check the folder status before deleting it.</span></span>

## <a name="examples"></a><span data-ttu-id="6471d-147">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6471d-147">Examples</span></span>

<span data-ttu-id="6471d-148">O exemplo de código VBScript a seguir exclui a pasta C: \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="6471d-148">The following VBScript code sample deletes the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Delete
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="6471d-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6471d-149">Requirements</span></span>



| <span data-ttu-id="6471d-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="6471d-150">Requirement</span></span> | <span data-ttu-id="6471d-151">Valor</span><span class="sxs-lookup"><span data-stu-id="6471d-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6471d-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6471d-152">Minimum supported client</span></span><br/> | <span data-ttu-id="6471d-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6471d-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6471d-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6471d-154">Minimum supported server</span></span><br/> | <span data-ttu-id="6471d-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6471d-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6471d-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="6471d-156">Namespace</span></span><br/>                | <span data-ttu-id="6471d-157">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6471d-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6471d-158">MOF</span><span class="sxs-lookup"><span data-stu-id="6471d-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6471d-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6471d-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6471d-160">DLL</span><span class="sxs-lookup"><span data-stu-id="6471d-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6471d-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6471d-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6471d-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="6471d-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="6471d-163">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6471d-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6471d-164">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="6471d-164">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

