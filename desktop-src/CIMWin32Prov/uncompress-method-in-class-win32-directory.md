---
description: Descompacta o arquivo de entrada de diretório lógico (ou diretório) especificado no caminho do objeto.
ms.assetid: dd39aae3-7c88-48fc-93ed-5225d2f1491c
ms.tgt_platform: multiple
title: Descompactar método da classe Win32_Directory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Directory.Uncompress
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c46a6bb90d43c1b793350bb96822a1aaed8dd9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089552"
---
# <a name="uncompress-method-of-the-win32_directory-class"></a><span data-ttu-id="c5512-103">Descompactar o método da \_ classe do diretório Win32</span><span class="sxs-lookup"><span data-stu-id="c5512-103">Uncompress method of the Win32\_Directory class</span></span>

<span data-ttu-id="c5512-104">O método **uncompactar** [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) descompacta o arquivo de entrada de diretório lógico (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="c5512-104">The **Uncompress** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical directory entry file (or directory) specified in the object path.</span></span>

<span data-ttu-id="c5512-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="c5512-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c5512-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="c5512-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5512-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c5512-107">Syntax</span></span>


```mof
uint32 Uncompress();
```



## <a name="parameters"></a><span data-ttu-id="c5512-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c5512-108">Parameters</span></span>

<span data-ttu-id="c5512-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c5512-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c5512-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c5512-110">Return value</span></span>

<span data-ttu-id="c5512-111">Retorna um valor inteiro de 0 (zero) se o arquivo tiver sido descompactado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="c5512-111">Returns an integer value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="c5512-112">**0**</span><span class="sxs-lookup"><span data-stu-id="c5512-112">**0**</span></span>
</dt> <dd>

<span data-ttu-id="c5512-113">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="c5512-113">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="c5512-114">**2**</span><span class="sxs-lookup"><span data-stu-id="c5512-114">**2**</span></span>
</dt> <dd>

<span data-ttu-id="c5512-115">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="c5512-115">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="c5512-116">**8**</span><span class="sxs-lookup"><span data-stu-id="c5512-116">**8**</span></span>
</dt> <dd>

<span data-ttu-id="c5512-117">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="c5512-117">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c5512-118">**9**</span><span class="sxs-lookup"><span data-stu-id="c5512-118">**9**</span></span>
</dt> <dd>

<span data-ttu-id="c5512-119">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="c5512-119">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c5512-120">**10**</span><span class="sxs-lookup"><span data-stu-id="c5512-120">**10**</span></span>
</dt> <dd>

<span data-ttu-id="c5512-121">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="c5512-121">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c5512-122">**11**</span><span class="sxs-lookup"><span data-stu-id="c5512-122">**11**</span></span>
</dt> <dd>

<span data-ttu-id="c5512-123">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="c5512-123">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="c5512-124">**12**</span><span class="sxs-lookup"><span data-stu-id="c5512-124">**12**</span></span>
</dt> <dd>

<span data-ttu-id="c5512-125">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="c5512-125">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="c5512-126">**13**</span><span class="sxs-lookup"><span data-stu-id="c5512-126">**13**</span></span>
</dt> <dd>

<span data-ttu-id="c5512-127">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="c5512-127">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="c5512-128">**14**</span><span class="sxs-lookup"><span data-stu-id="c5512-128">**14**</span></span>
</dt> <dd>

<span data-ttu-id="c5512-129">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="c5512-129">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="c5512-130">**15**</span><span class="sxs-lookup"><span data-stu-id="c5512-130">**15**</span></span>
</dt> <dd>

<span data-ttu-id="c5512-131">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="c5512-131">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="c5512-132">**16**</span><span class="sxs-lookup"><span data-stu-id="c5512-132">**16**</span></span>
</dt> <dd>

<span data-ttu-id="c5512-133">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="c5512-133">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c5512-134">**17**</span><span class="sxs-lookup"><span data-stu-id="c5512-134">**17**</span></span>
</dt> <dd>

<span data-ttu-id="c5512-135">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="c5512-135">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="c5512-136">**Abril**</span><span class="sxs-lookup"><span data-stu-id="c5512-136">**21**</span></span>
</dt> <dd>

<span data-ttu-id="c5512-137">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="c5512-137">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="c5512-138">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c5512-138">Examples</span></span>

<span data-ttu-id="c5512-139">O exemplo de VBScript a seguir descompacta a pasta c: \\ scripts.</span><span class="sxs-lookup"><span data-stu-id="c5512-139">The following VBScript sample uncompresses the folder c:\\Scripts.</span></span>


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
 & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colFolders = objWMIService.ExecQuery _
 ("SELECT * FROM Win32_Directory WHERE Name = 'c:\\Scripts'")
For Each objFolder in colFolders
 errResults = objFolder.Uncompress
 Wscript.Echo errResults
Next
```



## <a name="requirements"></a><span data-ttu-id="c5512-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5512-140">Requirements</span></span>



| <span data-ttu-id="c5512-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5512-141">Requirement</span></span> | <span data-ttu-id="c5512-142">Valor</span><span class="sxs-lookup"><span data-stu-id="c5512-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5512-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5512-143">Minimum supported client</span></span><br/> | <span data-ttu-id="c5512-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5512-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c5512-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5512-145">Minimum supported server</span></span><br/> | <span data-ttu-id="c5512-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5512-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c5512-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="c5512-147">Namespace</span></span><br/>                | <span data-ttu-id="c5512-148">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c5512-148">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c5512-149">MOF</span><span class="sxs-lookup"><span data-stu-id="c5512-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5512-150"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5512-150"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5512-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c5512-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5512-152"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5512-152"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5512-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5512-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="c5512-154">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="c5512-154">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="c5512-155">**\_Diretório Win32**</span><span class="sxs-lookup"><span data-stu-id="c5512-155">**Win32\_Directory**</span></span>](win32-directory.md)
</dt> <dt>

[<span data-ttu-id="c5512-156">**Compactar**</span><span class="sxs-lookup"><span data-stu-id="c5512-156">**Compress**</span></span>](compress-method-in-class-win32-directory.md)
</dt> </dl>

 

