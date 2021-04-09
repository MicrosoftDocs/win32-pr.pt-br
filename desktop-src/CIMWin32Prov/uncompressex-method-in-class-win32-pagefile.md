---
description: Descompacta o arquivo de paginação lógica (ou diretório) especificado no caminho do objeto. Esse método é uma versão estendida do método uncompact.
ms.assetid: d4cfa42e-7f05-4d12-b629-14195fc04e77
ms.tgt_platform: multiple
title: Método UncompressEx da classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 158efe4d2390762433d66d170b774838c9e534d3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089545"
---
# <a name="uncompressex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="49db4-104">Método UncompressEx da classe de \_ arquivo de paginação Win32</span><span class="sxs-lookup"><span data-stu-id="49db4-104">UncompressEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="49db4-105">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **UncompressEx** descompacta o arquivo de paginação lógica (ou diretório) especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="49db4-105">The **UncompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uncompresses the logical paging file (or directory) specified in the object path.</span></span> <span data-ttu-id="49db4-106">Esse método é uma versão estendida do método [**uncompact**](uncompress-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="49db4-106">This method is an extended version of the [**Uncompress**](uncompress-method-in-class-win32-directory.md) method.</span></span>

<span data-ttu-id="49db4-107">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="49db4-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="49db4-108">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="49db4-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="49db4-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="49db4-109">Syntax</span></span>


```mof
uint32 UncompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="49db4-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="49db4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49db4-111">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="49db4-111">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49db4-112">Nome do arquivo ou diretório em que o método **UncompressEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="49db4-112">Name of the file or directory where the **UncompressEx** method failed.</span></span> <span data-ttu-id="49db4-113">Esse parâmetro será **NULL** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="49db4-113">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-114">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="49db4-114">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49db4-115">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **UncompressEx**.</span><span class="sxs-lookup"><span data-stu-id="49db4-115">Names the child file or directory to use as a starting point for **UncompressEx**.</span></span> <span data-ttu-id="49db4-116">O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="49db4-116">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="49db4-117">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="49db4-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-118">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="49db4-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49db4-119">Se **for true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="49db4-119">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="49db4-120">Para instâncias de arquivo, o parâmetro *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="49db4-120">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49db4-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="49db4-121">Return value</span></span>

<span data-ttu-id="49db4-122">Retorna um valor de 0 (zero) se o arquivo tiver sido descompactado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="49db4-122">Returns a value of 0 (zero) if the file was successfully decompressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="49db4-123">**0**</span><span class="sxs-lookup"><span data-stu-id="49db4-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="49db4-124">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="49db4-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-125">**2**</span><span class="sxs-lookup"><span data-stu-id="49db4-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="49db4-126">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="49db4-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-127">**8**</span><span class="sxs-lookup"><span data-stu-id="49db4-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="49db4-128">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="49db4-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-129">**9**</span><span class="sxs-lookup"><span data-stu-id="49db4-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="49db4-130">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="49db4-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-131">**10**</span><span class="sxs-lookup"><span data-stu-id="49db4-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="49db4-132">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="49db4-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-133">**11**</span><span class="sxs-lookup"><span data-stu-id="49db4-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="49db4-134">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="49db4-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-135">**12**</span><span class="sxs-lookup"><span data-stu-id="49db4-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="49db4-136">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="49db4-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-137">**13**</span><span class="sxs-lookup"><span data-stu-id="49db4-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="49db4-138">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="49db4-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-139">**14**</span><span class="sxs-lookup"><span data-stu-id="49db4-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="49db4-140">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="49db4-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-141">**15**</span><span class="sxs-lookup"><span data-stu-id="49db4-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="49db4-142">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="49db4-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-143">**16**</span><span class="sxs-lookup"><span data-stu-id="49db4-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="49db4-144">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="49db4-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-145">**17**</span><span class="sxs-lookup"><span data-stu-id="49db4-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="49db4-146">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="49db4-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="49db4-147">**Abril**</span><span class="sxs-lookup"><span data-stu-id="49db4-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="49db4-148">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="49db4-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49db4-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="49db4-149">Requirements</span></span>



| <span data-ttu-id="49db4-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="49db4-150">Requirement</span></span> | <span data-ttu-id="49db4-151">Valor</span><span class="sxs-lookup"><span data-stu-id="49db4-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49db4-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49db4-152">Minimum supported client</span></span><br/> | <span data-ttu-id="49db4-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="49db4-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="49db4-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="49db4-154">Minimum supported server</span></span><br/> | <span data-ttu-id="49db4-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="49db4-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="49db4-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="49db4-156">Namespace</span></span><br/>                | <span data-ttu-id="49db4-157">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="49db4-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="49db4-158">MOF</span><span class="sxs-lookup"><span data-stu-id="49db4-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="49db4-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="49db4-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="49db4-160">DLL</span><span class="sxs-lookup"><span data-stu-id="49db4-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="49db4-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49db4-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49db4-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="49db4-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="49db4-163">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="49db4-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="49db4-164">**\_Arquivo de paginação Win32**</span><span class="sxs-lookup"><span data-stu-id="49db4-164">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

