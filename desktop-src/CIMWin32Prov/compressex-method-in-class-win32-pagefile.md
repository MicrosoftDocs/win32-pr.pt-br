---
description: Compacta o arquivo de paginação lógica (ou diretório) especificado no caminho do objeto (esse método é uma versão estendida do método compress).
ms.assetid: ea99367b-4d5e-4cd2-aa89-d250d1161f8f
ms.tgt_platform: multiple
title: Método CompressEx da classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.CompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2823d12fc474b5a5023890596a116062d94a045f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826186"
---
# <a name="compressex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="31eb3-103">Método CompressEx da classe de \_ arquivo de paginação Win32</span><span class="sxs-lookup"><span data-stu-id="31eb3-103">CompressEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="31eb3-104">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **CompressEx** compacta o arquivo de paginação lógica (ou diretório) especificado no caminho do objeto (esse método é uma versão estendida do método [**compress**](compress-method-in-class-win32-directory.md) ).</span><span class="sxs-lookup"><span data-stu-id="31eb3-104">The **CompressEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method compresses the logical paging file (or directory) specified in the object path (this method is an extended version of the [**Compress**](compress-method-in-class-win32-directory.md) method).</span></span>

<span data-ttu-id="31eb3-105">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="31eb3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="31eb3-106">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="31eb3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="31eb3-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="31eb3-107">Syntax</span></span>


```mof
uint32 CompressEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="31eb3-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="31eb3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="31eb3-109">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="31eb3-109">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-110">Nome do arquivo ou diretório em que o método **CompressEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="31eb3-110">Name of the file or directory where the **CompressEx** method failed.</span></span> <span data-ttu-id="31eb3-111">Esse parâmetro será **nulo** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="31eb3-111">This parameter is **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-112">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="31eb3-112">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-113">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **CompressEx**.</span><span class="sxs-lookup"><span data-stu-id="31eb3-113">Names the child file or directory to use as a starting point for **CompressEx**.</span></span> <span data-ttu-id="31eb3-114">O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="31eb3-114">The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="31eb3-115">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="31eb3-115">If this parameter is **NULL**, the operation is performed on the file or directory specified in the **ExecMethod** call.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-116">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="31eb3-116">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-117">Se **for true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="31eb3-117">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="31eb3-118">Para instâncias de arquivo, o parâmetro *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="31eb3-118">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="31eb3-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="31eb3-119">Return value</span></span>

<span data-ttu-id="31eb3-120">Retorna um valor de 0 (zero) se o arquivo tiver sido compactado com êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="31eb3-120">Returns a value of 0 (zero) if the file was successfully compressed, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="31eb3-121">**0**</span><span class="sxs-lookup"><span data-stu-id="31eb3-121">**0**</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-122">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="31eb3-122">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-123">**2**</span><span class="sxs-lookup"><span data-stu-id="31eb3-123">**2**</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-124">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="31eb3-124">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-125">**8**</span><span class="sxs-lookup"><span data-stu-id="31eb3-125">**8**</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-126">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="31eb3-126">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-127">**9**</span><span class="sxs-lookup"><span data-stu-id="31eb3-127">**9**</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-128">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="31eb3-128">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-129">**10**</span><span class="sxs-lookup"><span data-stu-id="31eb3-129">**10**</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-130">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="31eb3-130">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-131">**11**</span><span class="sxs-lookup"><span data-stu-id="31eb3-131">**11**</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-132">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="31eb3-132">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-133">**12**</span><span class="sxs-lookup"><span data-stu-id="31eb3-133">**12**</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-134">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="31eb3-134">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-135">**13**</span><span class="sxs-lookup"><span data-stu-id="31eb3-135">**13**</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-136">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="31eb3-136">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-137">**14**</span><span class="sxs-lookup"><span data-stu-id="31eb3-137">**14**</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-138">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="31eb3-138">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-139">**15**</span><span class="sxs-lookup"><span data-stu-id="31eb3-139">**15**</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-140">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="31eb3-140">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-141">**16**</span><span class="sxs-lookup"><span data-stu-id="31eb3-141">**16**</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-142">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="31eb3-142">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-143">**17**</span><span class="sxs-lookup"><span data-stu-id="31eb3-143">**17**</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-144">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="31eb3-144">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="31eb3-145">**Abril**</span><span class="sxs-lookup"><span data-stu-id="31eb3-145">**21**</span></span>
</dt> <dd>

<span data-ttu-id="31eb3-146">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="31eb3-146">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="31eb3-147">Requisitos</span><span class="sxs-lookup"><span data-stu-id="31eb3-147">Requirements</span></span>



| <span data-ttu-id="31eb3-148">Requisito</span><span class="sxs-lookup"><span data-stu-id="31eb3-148">Requirement</span></span> | <span data-ttu-id="31eb3-149">Valor</span><span class="sxs-lookup"><span data-stu-id="31eb3-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="31eb3-150">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31eb3-150">Minimum supported client</span></span><br/> | <span data-ttu-id="31eb3-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="31eb3-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="31eb3-152">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="31eb3-152">Minimum supported server</span></span><br/> | <span data-ttu-id="31eb3-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="31eb3-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="31eb3-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="31eb3-154">Namespace</span></span><br/>                | <span data-ttu-id="31eb3-155">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="31eb3-155">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="31eb3-156">MOF</span><span class="sxs-lookup"><span data-stu-id="31eb3-156">MOF</span></span><br/>                      | <dl> <span data-ttu-id="31eb3-157"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="31eb3-157"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="31eb3-158">DLL</span><span class="sxs-lookup"><span data-stu-id="31eb3-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="31eb3-159"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31eb3-159"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="31eb3-160">Confira também</span><span class="sxs-lookup"><span data-stu-id="31eb3-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="31eb3-161">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="31eb3-161">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="31eb3-162">**\_Arquivo de paginação Win32**</span><span class="sxs-lookup"><span data-stu-id="31eb3-162">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

