---
description: Copia o arquivo de paginação lógica ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro FileName. Esse método é uma versão estendida do método Copy.
ms.assetid: a8376dc8-eb73-4097-b84c-839432ac3a25
ms.tgt_platform: multiple
title: Método CopyEx da classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.CopyEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 810f1d3bcf878d33756930f6bd3b6799c3513dc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826707"
---
# <a name="copyex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="b7596-104">Método CopyEx da classe de \_ arquivo de paginação Win32</span><span class="sxs-lookup"><span data-stu-id="b7596-104">CopyEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="b7596-105">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CopyEx** copia o arquivo de paginação lógica ou o diretório especificado no caminho do objeto para o local especificado pelo parâmetro *filename* .</span><span class="sxs-lookup"><span data-stu-id="b7596-105">The **CopyEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method copies the logical paging file or directory specified in the object path to the location specified by the *FileName* parameter.</span></span> <span data-ttu-id="b7596-106">Esse método é uma versão estendida do método [**Copy**](copy-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="b7596-106">This method is an extended version of the [**Copy**](copy-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="b7596-107">Não haverá suporte para uma cópia se a substituição de um arquivo lógico existente for necessária.</span><span class="sxs-lookup"><span data-stu-id="b7596-107">A copy is not supported if overwriting an existing logical file is required.</span></span>

<span data-ttu-id="b7596-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="b7596-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="b7596-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="b7596-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="b7596-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7596-110">Syntax</span></span>


```mof
uint32 CopyEx(
  [in]           string  FileName,
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="b7596-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7596-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7596-112">*Nome do arquivo* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b7596-112">*FileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b7596-113">Nome totalmente qualificado da cópia do arquivo (ou diretório).</span><span class="sxs-lookup"><span data-stu-id="b7596-113">Fully qualified name of the copy of the file (or directory).</span></span>

<span data-ttu-id="b7596-114">Exemplo: c: \\ temp \\ newdirectory</span><span class="sxs-lookup"><span data-stu-id="b7596-114">Example: c:\\temp\\newdirectory</span></span>

</dd> <dt>

<span data-ttu-id="b7596-115">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b7596-115">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b7596-116">Nome do arquivo ou diretório em que o método **CopyEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="b7596-116">Name of the file or directory where the **CopyEx** method failed.</span></span> <span data-ttu-id="b7596-117">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="b7596-117">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-118">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7596-118">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7596-119">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **CopyEx**.</span><span class="sxs-lookup"><span data-stu-id="b7596-119">Names the child file or directory to use as a starting point for **CopyEx**.</span></span> <span data-ttu-id="b7596-120">O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="b7596-120">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="b7596-121">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="b7596-121">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-122">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="b7596-122">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="b7596-123">Se **for true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="b7596-123">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="b7596-124">Para instâncias de arquivo, o parâmetro *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="b7596-124">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7596-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7596-125">Return value</span></span>

<span data-ttu-id="b7596-126">Retorna um valor de 0 (zero) se o arquivo foi copiado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="b7596-126">Returns a value of 0 (zero) if the file was successfully copied, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="b7596-127">**0**</span><span class="sxs-lookup"><span data-stu-id="b7596-127">**0**</span></span>
</dt> <dd>

<span data-ttu-id="b7596-128">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="b7596-128">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-129">**2**</span><span class="sxs-lookup"><span data-stu-id="b7596-129">**2**</span></span>
</dt> <dd>

<span data-ttu-id="b7596-130">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="b7596-130">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-131">**8**</span><span class="sxs-lookup"><span data-stu-id="b7596-131">**8**</span></span>
</dt> <dd>

<span data-ttu-id="b7596-132">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="b7596-132">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-133">**9**</span><span class="sxs-lookup"><span data-stu-id="b7596-133">**9**</span></span>
</dt> <dd>

<span data-ttu-id="b7596-134">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="b7596-134">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-135">**10**</span><span class="sxs-lookup"><span data-stu-id="b7596-135">**10**</span></span>
</dt> <dd>

<span data-ttu-id="b7596-136">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="b7596-136">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-137">**11**</span><span class="sxs-lookup"><span data-stu-id="b7596-137">**11**</span></span>
</dt> <dd>

<span data-ttu-id="b7596-138">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="b7596-138">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-139">**12**</span><span class="sxs-lookup"><span data-stu-id="b7596-139">**12**</span></span>
</dt> <dd>

<span data-ttu-id="b7596-140">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="b7596-140">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-141">**13**</span><span class="sxs-lookup"><span data-stu-id="b7596-141">**13**</span></span>
</dt> <dd>

<span data-ttu-id="b7596-142">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="b7596-142">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-143">**14**</span><span class="sxs-lookup"><span data-stu-id="b7596-143">**14**</span></span>
</dt> <dd>

<span data-ttu-id="b7596-144">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="b7596-144">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-145">**15**</span><span class="sxs-lookup"><span data-stu-id="b7596-145">**15**</span></span>
</dt> <dd>

<span data-ttu-id="b7596-146">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="b7596-146">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-147">**16**</span><span class="sxs-lookup"><span data-stu-id="b7596-147">**16**</span></span>
</dt> <dd>

<span data-ttu-id="b7596-148">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="b7596-148">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-149">**17**</span><span class="sxs-lookup"><span data-stu-id="b7596-149">**17**</span></span>
</dt> <dd>

<span data-ttu-id="b7596-150">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="b7596-150">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="b7596-151">**Abril**</span><span class="sxs-lookup"><span data-stu-id="b7596-151">**21**</span></span>
</dt> <dd>

<span data-ttu-id="b7596-152">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="b7596-152">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7596-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7596-153">Requirements</span></span>



| <span data-ttu-id="b7596-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7596-154">Requirement</span></span> | <span data-ttu-id="b7596-155">Valor</span><span class="sxs-lookup"><span data-stu-id="b7596-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7596-156">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7596-156">Minimum supported client</span></span><br/> | <span data-ttu-id="b7596-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b7596-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b7596-158">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b7596-158">Minimum supported server</span></span><br/> | <span data-ttu-id="b7596-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b7596-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b7596-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="b7596-160">Namespace</span></span><br/>                | <span data-ttu-id="b7596-161">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b7596-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b7596-162">MOF</span><span class="sxs-lookup"><span data-stu-id="b7596-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7596-163"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7596-163"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b7596-164">DLL</span><span class="sxs-lookup"><span data-stu-id="b7596-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7596-165"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7596-165"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7596-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7596-166">See also</span></span>

<dl> <dt>

<span data-ttu-id="b7596-167">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="b7596-167">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="b7596-168">**\_Arquivo de paginação Win32**</span><span class="sxs-lookup"><span data-stu-id="b7596-168">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

