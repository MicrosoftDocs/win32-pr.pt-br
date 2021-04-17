---
description: Renomeia o arquivo de entrada de diretório especificado no caminho do objeto.
ms.assetid: 8bfe1b69-5f93-4408-a742-f03a9cb16bfe
ms.tgt_platform: multiple
title: Método Rename da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Rename
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 874151e1ff8c9feca375df3eb441665863d1070d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753583"
---
# <a name="rename-method-of-the-win32_directory-class"></a><span data-ttu-id="5c9c3-103">Método Rename da classe do \_ diretório Win32</span><span class="sxs-lookup"><span data-stu-id="5c9c3-103">Rename method of the Win32\_Directory class</span></span>

<span data-ttu-id="5c9c3-104">O método **renomear** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) renomeia o arquivo de entrada de diretório especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-104">The **Rename** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renames the directory entry file specified in the object path.</span></span> <span data-ttu-id="5c9c3-105">Não haverá suporte para renomear se o destino estiver em outra unidade ou se for necessário substituir um arquivo lógico existente.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-105">A rename is not supported if the destination is on another drive or if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="5c9c3-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="5c9c3-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5c9c3-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="5c9c3-107">For more information about using this method see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5c9c3-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5c9c3-108">Syntax</span></span>


```mof
uint32 Rename(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="5c9c3-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5c9c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c9c3-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="5c9c3-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="5c9c3-111">Novo nome totalmente qualificado do arquivo (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="5c9c3-111">Fully qualified new name of the file (or directory).</span></span> <span data-ttu-id="5c9c3-112">Exemplo: c: \\ temp \\newfile.txt.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-112">Example: c:\\temp\\newfile.txt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c9c3-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5c9c3-113">Return value</span></span>

<span data-ttu-id="5c9c3-114">Retorna um valor de 0 (zero) se o arquivo tiver sido renomeado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-114">Returns a value of 0 (zero) if the file was successfully renamed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="5c9c3-115">**0**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="5c9c3-116">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="5c9c3-117">**2**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="5c9c3-118">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="5c9c3-119">**8**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="5c9c3-120">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="5c9c3-121">**9**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="5c9c3-122">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5c9c3-123">**10**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="5c9c3-124">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5c9c3-125">**11**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="5c9c3-126">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="5c9c3-127">**12**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="5c9c3-128">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="5c9c3-129">**13**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="5c9c3-130">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="5c9c3-131">**14**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="5c9c3-132">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="5c9c3-133">**15**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="5c9c3-134">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="5c9c3-135">**16**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="5c9c3-136">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="5c9c3-137">**17**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="5c9c3-138">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="5c9c3-139">**Abril**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="5c9c3-140">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c9c3-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="5c9c3-141">Remarks</span></span>

<span data-ttu-id="5c9c3-142">Para renomear uma pasta, primeiro associe-se à pasta em questão e, em seguida, chame o método Rename.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-142">To rename a folder, first bind to the folder in question and then call the Rename method.</span></span> <span data-ttu-id="5c9c3-143">Como o único parâmetro para o método, passe o novo nome da pasta como um nome de caminho completo.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-143">As the sole parameter to the method, pass the new name for the folder as a complete path name.</span></span> <span data-ttu-id="5c9c3-144">Por exemplo, se a pasta no backup de logs de scripts C: \\ \\ \\ for renomeada como c: \\ script \\ arquivo, você deverá passar \\ o arquivo c: scripts \\ como o nome de pasta completo.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-144">For example, if the folder in the C:\\Scripts\\Logs\\Backup is to be renamed C:\\Scripts\\Archive, you must pass C:\\Scripts\\Archive as the complete folder name.</span></span> <span data-ttu-id="5c9c3-145">Passar somente o nome da pasta-arquivo-resulta em um erro de caminho inválido.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-145">Passing only the folder name - Archive - results in an Invalid path error.</span></span>

<span data-ttu-id="5c9c3-146">A classe de diretório Win32 não \_ fornece um método de uma etapa para mover pastas.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-146">The Win32\_Directory class does not provide a one-step method for moving folders.</span></span> <span data-ttu-id="5c9c3-147">Em vez disso, mover uma pasta geralmente envolve duas etapas:</span><span class="sxs-lookup"><span data-stu-id="5c9c3-147">Instead, moving a folder generally involves two steps:</span></span>

<dl> 1. <span data-ttu-id="5c9c3-148">Copiando a pasta para seu novo local</span><span class="sxs-lookup"><span data-stu-id="5c9c3-148">Copying the folder to its new location</span></span>  
2. <span data-ttu-id="5c9c3-149">Excluindo a pasta original</span><span class="sxs-lookup"><span data-stu-id="5c9c3-149">Deleting the original folder</span></span>  
</dl>

<span data-ttu-id="5c9c3-150">A única exceção para esse processo de duas etapas envolve mover uma pasta para um novo local na mesma unidade.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-150">The one exception to this two-step process involves moving a folder to a new location on the same drive.</span></span> <span data-ttu-id="5c9c3-151">Por exemplo, suponha que você deseja mover C: \\ Temp para c: \\ scripts \\ arquivos temporários \\ arquivo morto.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-151">For example, suppose you want to move C:\\Temp to C:\\Scripts\\Temporary Files\\Archive.</span></span> <span data-ttu-id="5c9c3-152">Desde que o local atual e o novo local estejam na mesma unidade, você pode mover a pasta simplesmente chamando o método Rename e passando o novo local como o parâmetro Method.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-152">As long as the current location and the new location are on the same drive, you can move the folder by simply calling the Rename method and passing the new location as the method parameter.</span></span> <span data-ttu-id="5c9c3-153">Essa abordagem permite efetivamente que você mova a pasta em uma única etapa.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-153">This approach effectively allows you to move the folder in a single step.</span></span> <span data-ttu-id="5c9c3-154">No entanto, o script falhará se a unidade atual e a nova unidade forem diferentes.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-154">However, the script fails if the current drive and the new drive are different.</span></span> <span data-ttu-id="5c9c3-155">Uma tentativa de Renomear C: \\ Temp para D: \\ Temp falha com um erro "a unidade não é o mesmo".</span><span class="sxs-lookup"><span data-stu-id="5c9c3-155">An attempt to rename C:\\Temp to D:\\Temp fails with a "Drive not the same" error.</span></span>

## <a name="examples"></a><span data-ttu-id="5c9c3-156">Exemplos</span><span class="sxs-lookup"><span data-stu-id="5c9c3-156">Examples</span></span>

<span data-ttu-id="5c9c3-157">O código a seguir, a partir da amostra [mover uma pasta usando o WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript na galeria do TechNet, usa o método Rename para mover a pasta c: \\ scripts para C: \\ Admins \\ documentam o \\ \\ VBScript.</span><span class="sxs-lookup"><span data-stu-id="5c9c3-157">The following code, from the [Move a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/f4f9643c-d7ed-4f54-b155-c6515396431f) VBScript sample on TechNet Gallery, uses the Rename method to move the folder C:\\Scripts to C:\\Admins\\Documents\\Archive\\VBScript.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery _ 
    ("Select * from Win32_Directory where name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults = objFolder.Rename("C:\Admins\Documents\Archive\VBScript") 
Next
```



## <a name="requirements"></a><span data-ttu-id="5c9c3-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5c9c3-158">Requirements</span></span>



| <span data-ttu-id="5c9c3-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c9c3-159">Requirement</span></span> | <span data-ttu-id="5c9c3-160">Valor</span><span class="sxs-lookup"><span data-stu-id="5c9c3-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5c9c3-161">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c9c3-161">Minimum supported client</span></span><br/> | <span data-ttu-id="5c9c3-162">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c9c3-162">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="5c9c3-163">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="5c9c3-163">Minimum supported server</span></span><br/> | <span data-ttu-id="5c9c3-164">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c9c3-164">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="5c9c3-165">Namespace</span><span class="sxs-lookup"><span data-stu-id="5c9c3-165">Namespace</span></span><br/>                | <span data-ttu-id="5c9c3-166">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="5c9c3-166">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5c9c3-167">MOF</span><span class="sxs-lookup"><span data-stu-id="5c9c3-167">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5c9c3-168"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5c9c3-168"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5c9c3-169">DLL</span><span class="sxs-lookup"><span data-stu-id="5c9c3-169">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c9c3-170"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c9c3-170"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c9c3-171">Confira também</span><span class="sxs-lookup"><span data-stu-id="5c9c3-171">See also</span></span>

<dl> <dt>

<span data-ttu-id="5c9c3-172">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5c9c3-172">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="5c9c3-173">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="5c9c3-173">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

