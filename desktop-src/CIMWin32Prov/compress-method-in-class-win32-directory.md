---
description: Compacta o arquivo de entrada de diretório lógico (ou diretório) especificado no caminho do objeto.
ms.assetid: 4db13622-75c5-45db-8536-451059c0e477
ms.tgt_platform: multiple
title: Método compress da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Compress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea694c09e11e5801016a4ea85b9774448c542991
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088977"
---
# <a name="compress-method-of-the-win32_directory-class"></a><span data-ttu-id="e3734-103">Método compress da classe do \_ diretório Win32</span><span class="sxs-lookup"><span data-stu-id="e3734-103">Compress method of the Win32\_Directory class</span></span>

<span data-ttu-id="e3734-104">O método **compactar** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) compacta o arquivo de entrada de diretório lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="e3734-104">The **Compress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical directory entry file (or directory) specified in the object path.</span></span>

<span data-ttu-id="e3734-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="e3734-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="e3734-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="e3734-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="e3734-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e3734-107">Syntax</span></span>


```mof
uint32 Compress();
```



## <a name="parameters"></a><span data-ttu-id="e3734-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e3734-108">Parameters</span></span>

<span data-ttu-id="e3734-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e3734-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3734-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e3734-110">Return value</span></span>

<span data-ttu-id="e3734-111">Retorna um valor de 0 (zero) se o arquivo tiver sido compactado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="e3734-111">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="e3734-112">**0**</span><span class="sxs-lookup"><span data-stu-id="e3734-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="e3734-113">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="e3734-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="e3734-114">**2**</span><span class="sxs-lookup"><span data-stu-id="e3734-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="e3734-115">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="e3734-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="e3734-116">**8**</span><span class="sxs-lookup"><span data-stu-id="e3734-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="e3734-117">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="e3734-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="e3734-118">**9**</span><span class="sxs-lookup"><span data-stu-id="e3734-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="e3734-119">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="e3734-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e3734-120">**10**</span><span class="sxs-lookup"><span data-stu-id="e3734-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="e3734-121">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="e3734-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="e3734-122">**11**</span><span class="sxs-lookup"><span data-stu-id="e3734-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="e3734-123">O sistema de arquivos não é um NTFS.</span><span class="sxs-lookup"><span data-stu-id="e3734-123">The file system is not an NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="e3734-124">**12**</span><span class="sxs-lookup"><span data-stu-id="e3734-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="e3734-125">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="e3734-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="e3734-126">**13**</span><span class="sxs-lookup"><span data-stu-id="e3734-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="e3734-127">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="e3734-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="e3734-128">**14**</span><span class="sxs-lookup"><span data-stu-id="e3734-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="e3734-129">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="e3734-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="e3734-130">**15**</span><span class="sxs-lookup"><span data-stu-id="e3734-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="e3734-131">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="e3734-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="e3734-132">**16**</span><span class="sxs-lookup"><span data-stu-id="e3734-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="e3734-133">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="e3734-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e3734-134">**17**</span><span class="sxs-lookup"><span data-stu-id="e3734-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="e3734-135">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="e3734-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="e3734-136">**Abril**</span><span class="sxs-lookup"><span data-stu-id="e3734-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="e3734-137">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="e3734-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3734-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3734-138">Remarks</span></span>

<span data-ttu-id="e3734-139">A compactação fornece uma maneira de liberar espaço de armazenamento adicional em uma unidade de disco sem comprar novo hardware e sem remover arquivos ou pastas.</span><span class="sxs-lookup"><span data-stu-id="e3734-139">Compression provides a way to free additional storage space on a disk drive without purchasing new hardware and without removing files or folders.</span></span> <span data-ttu-id="e3734-140">Dependendo do tamanho do disco rígido e do tipo de arquivos armazenados nesse disco, você poderá recuperar centenas de megabytes de espaço em disco e, portanto, impedir a necessidade de comprar um novo disco rígido e colocar o computador offline até que a nova unidade seja instalada.</span><span class="sxs-lookup"><span data-stu-id="e3734-140">Depending on the size of your hard disk and the type of files stored on that disk, you might be able to recover hundreds of megabytes of disk space and thus preclude the need to purchase a new hard drive and to take the computer offline until the new drive is installed.</span></span>

<span data-ttu-id="e3734-141">O método compress compacta todos os arquivos e subpastas dentro de uma pasta especificada.</span><span class="sxs-lookup"><span data-stu-id="e3734-141">The Compress method compresses all the files and subfolders within a specified folder.</span></span> <span data-ttu-id="e3734-142">Além disso, a classe também inclui um método descompactar que remove a compactação de todos os arquivos e subpastas em uma pasta.</span><span class="sxs-lookup"><span data-stu-id="e3734-142">In addition, the class also includes an Uncompress method that removes compression from all the files and subfolders in a folder.</span></span> <span data-ttu-id="e3734-143">Métodos semelhantes também são fornecidos com a classe de DataFile do CIM \_ .</span><span class="sxs-lookup"><span data-stu-id="e3734-143">Similar methods are also provided with the CIM\_Datafile class.</span></span> <span data-ttu-id="e3734-144">Isso permite que você compacte ou Descompacte seletivamente arquivos específicos dentro de uma pasta.</span><span class="sxs-lookup"><span data-stu-id="e3734-144">This allows you to selectively compress or uncompress specific files within a folder.</span></span>

<span data-ttu-id="e3734-145">Como a compactação faz uma ligeira penalidade de desempenho, não é recomendável para arquivos ou pastas que são acessados rotineiramente; por exemplo, você provavelmente não deseja compactar arquivos de banco de dados, arquivos de log ou pastas de perfil de usuário.</span><span class="sxs-lookup"><span data-stu-id="e3734-145">Because compression imparts a slight performance penalty, it is not recommended for files or folders that are accessed on a routine basis; for example, you probably do not want to compress database files, log files, or user profile folders.</span></span> <span data-ttu-id="e3734-146">Melhores candidatos para compactação são arquivos e pastas que não são acessados com muita frequência.</span><span class="sxs-lookup"><span data-stu-id="e3734-146">Better candidates for compression are files and folders that are not accessed very often.</span></span> <span data-ttu-id="e3734-147">Por exemplo, você pode escrever um script para retornar uma coleção de pastas em uma unidade que não foi acessada por um mês ou mais e, em seguida, compactar cada uma dessas pastas.</span><span class="sxs-lookup"><span data-stu-id="e3734-147">For example, you might write a script to return a collection of folders on a drive that have not been accessed for a month or more and then compress each of those folders.</span></span>

<span data-ttu-id="e3734-148">A quantidade de espaço em disco liberada pela compactação de pastas varia dependendo do tipo de arquivos armazenados nessa pasta.</span><span class="sxs-lookup"><span data-stu-id="e3734-148">The amount of disk space freed by compressing folders varies depending on the type of files stored in that folder.</span></span> <span data-ttu-id="e3734-149">Por exemplo, arquivos. jpg já estão compactados e a compactação adicional tem pouco efeito sobre o tamanho do arquivo.</span><span class="sxs-lookup"><span data-stu-id="e3734-149">For example, .jpg files are already compressed, and further compression has little effect on the size of the file.</span></span> <span data-ttu-id="e3734-150">No entanto, com outros tipos de arquivo, a economia pode ser considerável.</span><span class="sxs-lookup"><span data-stu-id="e3734-150">With other file types, however, the savings can be considerable.</span></span> <span data-ttu-id="e3734-151">Por exemplo, uma nova pasta foi criada em um computador de teste baseado no Windows 2000 e os documentos 33 do Microsoft Word, ocupando um total de 15 megabytes (MB) de espaço em disco, foram copiados nessa pasta.</span><span class="sxs-lookup"><span data-stu-id="e3734-151">For example, a new folder was created on a Windows 2000-based test computer, and 33 Microsoft Word documents, taking up a total of 15 megabytes (MB) of disk space, were copied into that folder.</span></span> <span data-ttu-id="e3734-152">Quando os documentos foram compactados, a pasta demorou apenas 7 MB de espaço em disco.</span><span class="sxs-lookup"><span data-stu-id="e3734-152">When the documents were compressed, the folder took up only 7 MB of disk space.</span></span>

## <a name="examples"></a><span data-ttu-id="e3734-153">Exemplos</span><span class="sxs-lookup"><span data-stu-id="e3734-153">Examples</span></span>

<span data-ttu-id="e3734-154">O exemplo de VBScript a seguir compacta a pasta C: \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="e3734-154">The following VBScript sample compresses the folder C:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Compress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="e3734-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3734-155">Requirements</span></span>



| <span data-ttu-id="e3734-156">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3734-156">Requirement</span></span> | <span data-ttu-id="e3734-157">Valor</span><span class="sxs-lookup"><span data-stu-id="e3734-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3734-158">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3734-158">Minimum supported client</span></span><br/> | <span data-ttu-id="e3734-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e3734-159">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e3734-160">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e3734-160">Minimum supported server</span></span><br/> | <span data-ttu-id="e3734-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e3734-161">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e3734-162">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3734-162">Namespace</span></span><br/>                | <span data-ttu-id="e3734-163">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e3734-163">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e3734-164">MOF</span><span class="sxs-lookup"><span data-stu-id="e3734-164">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e3734-165"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e3734-165"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e3734-166">DLL</span><span class="sxs-lookup"><span data-stu-id="e3734-166">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3734-167"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3734-167"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3734-168">Confira também</span><span class="sxs-lookup"><span data-stu-id="e3734-168">See also</span></span>

<dl> <dt>

<span data-ttu-id="e3734-169">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="e3734-169">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="e3734-170">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="e3734-170">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> <dt>

[<span data-ttu-id="e3734-171">**Descompactar**</span><span class="sxs-lookup"><span data-stu-id="e3734-171">**Uncompress**</span></span>](uncompress-method-in-class-win32-directory.md)
</dt> </dl>

 

