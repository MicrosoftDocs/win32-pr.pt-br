---
description: Copia o arquivo de entrada de diretório lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.
ms.assetid: 038e23d7-71db-4db6-8fb1-e84e972510c9
ms.tgt_platform: multiple
title: Método Copy da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Copy
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 25568167d9532303a7cbee794757bc674a378b39
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089258"
---
# <a name="copy-method-of-the-win32_directory-class"></a><span data-ttu-id="08b1e-103">Método Copy da classe do \_ diretório Win32</span><span class="sxs-lookup"><span data-stu-id="08b1e-103">Copy method of the Win32\_Directory class</span></span>

<span data-ttu-id="08b1e-104">O método **Copy** [WMI Class](/windows/desktop/WmiSdk/retrieving-a-class) copia o arquivo de entrada de diretório lógico ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="08b1e-104">The **Copy** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical directory entry file or directory specified in the object path to the location specified by the input parameter.</span></span> <span data-ttu-id="08b1e-105">Não haverá suporte para uma cópia se a substituição de um arquivo lógico existente for necessária.</span><span class="sxs-lookup"><span data-stu-id="08b1e-105">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="08b1e-106">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="08b1e-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="08b1e-107">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="08b1e-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="08b1e-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="08b1e-108">Syntax</span></span>


```mof
uint32 Copy(
   string FileName
);
```



## <a name="parameters"></a><span data-ttu-id="08b1e-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="08b1e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08b1e-110">*FileName*</span><span class="sxs-lookup"><span data-stu-id="08b1e-110">*FileName*</span></span> 
</dt> <dd>

<span data-ttu-id="08b1e-111">Nome totalmente qualificado da cópia do arquivo (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="08b1e-111">Fully qualified name of the copy of the file (or directory).</span></span> <span data-ttu-id="08b1e-112">Exemplo: c: \\ temp \\ newdirectory</span><span class="sxs-lookup"><span data-stu-id="08b1e-112">Example: c:\\temp\\newdirectory</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08b1e-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="08b1e-113">Return value</span></span>

<span data-ttu-id="08b1e-114">Retorna um valor de 0 (zero) se o arquivo foi copiado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="08b1e-114">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="08b1e-115">**0**</span><span class="sxs-lookup"><span data-stu-id="08b1e-115">**0**</span></span>
</dt> <dd>

<span data-ttu-id="08b1e-116">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="08b1e-116">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-117">**2**</span><span class="sxs-lookup"><span data-stu-id="08b1e-117">**2**</span></span>
</dt> <dd>

<span data-ttu-id="08b1e-118">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="08b1e-118">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-119">**8**</span><span class="sxs-lookup"><span data-stu-id="08b1e-119">**8**</span></span>
</dt> <dd>

<span data-ttu-id="08b1e-120">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="08b1e-120">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-121">**9**</span><span class="sxs-lookup"><span data-stu-id="08b1e-121">**9**</span></span>
</dt> <dd>

<span data-ttu-id="08b1e-122">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="08b1e-122">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-123">**10**</span><span class="sxs-lookup"><span data-stu-id="08b1e-123">**10**</span></span>
</dt> <dd>

<span data-ttu-id="08b1e-124">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="08b1e-124">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-125">**11**</span><span class="sxs-lookup"><span data-stu-id="08b1e-125">**11**</span></span>
</dt> <dd>

<span data-ttu-id="08b1e-126">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="08b1e-126">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-127">**12**</span><span class="sxs-lookup"><span data-stu-id="08b1e-127">**12**</span></span>
</dt> <dd>

<span data-ttu-id="08b1e-128">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="08b1e-128">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-129">**13**</span><span class="sxs-lookup"><span data-stu-id="08b1e-129">**13**</span></span>
</dt> <dd>

<span data-ttu-id="08b1e-130">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="08b1e-130">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-131">**14**</span><span class="sxs-lookup"><span data-stu-id="08b1e-131">**14**</span></span>
</dt> <dd>

<span data-ttu-id="08b1e-132">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="08b1e-132">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-133">**15**</span><span class="sxs-lookup"><span data-stu-id="08b1e-133">**15**</span></span>
</dt> <dd>

<span data-ttu-id="08b1e-134">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="08b1e-134">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-135">**16**</span><span class="sxs-lookup"><span data-stu-id="08b1e-135">**16**</span></span>
</dt> <dd>

<span data-ttu-id="08b1e-136">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="08b1e-136">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-137">**17**</span><span class="sxs-lookup"><span data-stu-id="08b1e-137">**17**</span></span>
</dt> <dd>

<span data-ttu-id="08b1e-138">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="08b1e-138">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="08b1e-139">**Abril**</span><span class="sxs-lookup"><span data-stu-id="08b1e-139">**21**</span></span>
</dt> <dd>

<span data-ttu-id="08b1e-140">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="08b1e-140">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="08b1e-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="08b1e-141">Remarks</span></span>

<span data-ttu-id="08b1e-142">As pastas geralmente precisam ser copiadas de um local para outro.</span><span class="sxs-lookup"><span data-stu-id="08b1e-142">Folders often need to be copied from one location to another.</span></span> <span data-ttu-id="08b1e-143">Por exemplo, você pode copiar uma pasta de um servidor para outro para criar uma cópia de backup dessa pasta.</span><span class="sxs-lookup"><span data-stu-id="08b1e-143">For example, you might copy a folder from one server to another to create a backup copy of that folder.</span></span> <span data-ttu-id="08b1e-144">Ou você pode ter uma pasta de modelos que precisa ser copiada para estações de trabalho de usuário ou uma pasta de scripts que deve ser copiada para todos os seus servidores DNS.</span><span class="sxs-lookup"><span data-stu-id="08b1e-144">Or you might have a templates folder that needs to be copied to user workstations, or a scripts folder that should be copied to all of your DNS servers.</span></span>

<span data-ttu-id="08b1e-145">O método de cópia de diretório do Win32 \_ permite que você copie uma pasta de um local para outro, no mesmo computador (por exemplo, copiando uma pasta da unidade C para a unidade D) ou em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="08b1e-145">The Win32\_Directory Copy method enables you to copy a folder from one location to another, either on the same computer (for example, copying a folder from drive C to drive D) or on a remote computer.</span></span> <span data-ttu-id="08b1e-146">Para copiar uma pasta, você retorna uma instância da pasta a ser copiada e, em seguida, chama o método Copy, passando como um parâmetro o local de destino para a nova cópia da pasta.</span><span class="sxs-lookup"><span data-stu-id="08b1e-146">To copy a folder, you return an instance of the folder to be copied and then call the Copy method, passing as a parameter the target location for the new copy of the folder.</span></span> <span data-ttu-id="08b1e-147">Por exemplo, esta linha de código copia uma pasta para a pasta scripts na unidade F:</span><span class="sxs-lookup"><span data-stu-id="08b1e-147">For example, this line of code copies a folder to the Scripts folder on drive F:</span></span>

`objFolder.Copy("F:\Scripts")`

<span data-ttu-id="08b1e-148">O WMI não substituirá uma pasta existente ao executar o método de cópia.</span><span class="sxs-lookup"><span data-stu-id="08b1e-148">WMI will not overwrite an existing folder when executing the Copy method.</span></span> <span data-ttu-id="08b1e-149">Isso significa que a operação de cópia falhará se a pasta de destino existir.</span><span class="sxs-lookup"><span data-stu-id="08b1e-149">This means that the copy operation fails if the destination folder exists.</span></span> <span data-ttu-id="08b1e-150">Por exemplo, suponha que você tenha uma pasta chamada scripts e tente copiar essa pasta para um compartilhamento remoto denominado \\ \\ ATL-FS-01 \\ Archive.</span><span class="sxs-lookup"><span data-stu-id="08b1e-150">For example, suppose you have a folder named Scripts and you attempt to copy that folder to a remote share named \\\\atl-fs-01\\archive.</span></span> <span data-ttu-id="08b1e-151">Se uma pasta denominada scripts já existir nesse compartilhamento, a operação de cópia falhará.</span><span class="sxs-lookup"><span data-stu-id="08b1e-151">If a folder named Scripts already exists on that share, the copy operation fails.</span></span>

## <a name="examples"></a><span data-ttu-id="08b1e-152">Exemplos</span><span class="sxs-lookup"><span data-stu-id="08b1e-152">Examples</span></span>

<span data-ttu-id="08b1e-153">O exemplo de código opções, extraído da [pasta Copy a usando o WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), usa o método Copy para copiar a pasta C: \\ scripts para D: \\ Archive.</span><span class="sxs-lookup"><span data-stu-id="08b1e-153">The followng code sample, taken from the [Copy a Folder Using WMI](https://Gallery.TechNet.Microsoft.Com/71b8f517-0240-42a2-be5c-e5a3921604d2), uses the Copy method to copy the folder C:\\Scripts to D:\\Archive.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colFolders = objWMIService.ExecQuery( _ 
    "Select * from Win32_Directory where Name = 'c:\\Scripts'") 
 
For Each objFolder in colFolders 
    errResults  = objFolder.Copy("D:\Archive") 
Next
```



## <a name="requirements"></a><span data-ttu-id="08b1e-154">Requisitos</span><span class="sxs-lookup"><span data-stu-id="08b1e-154">Requirements</span></span>



| <span data-ttu-id="08b1e-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="08b1e-155">Requirement</span></span> | <span data-ttu-id="08b1e-156">Valor</span><span class="sxs-lookup"><span data-stu-id="08b1e-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="08b1e-157">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08b1e-157">Minimum supported client</span></span><br/> | <span data-ttu-id="08b1e-158">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="08b1e-158">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="08b1e-159">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="08b1e-159">Minimum supported server</span></span><br/> | <span data-ttu-id="08b1e-160">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="08b1e-160">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="08b1e-161">Namespace</span><span class="sxs-lookup"><span data-stu-id="08b1e-161">Namespace</span></span><br/>                | <span data-ttu-id="08b1e-162">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="08b1e-162">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="08b1e-163">MOF</span><span class="sxs-lookup"><span data-stu-id="08b1e-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08b1e-164"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-164"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="08b1e-165">DLL</span><span class="sxs-lookup"><span data-stu-id="08b1e-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08b1e-166"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08b1e-166"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08b1e-167">Confira também</span><span class="sxs-lookup"><span data-stu-id="08b1e-167">See also</span></span>

<dl> <dt>

<span data-ttu-id="08b1e-168">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="08b1e-168">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="08b1e-169">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="08b1e-169">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> </dl>

 

