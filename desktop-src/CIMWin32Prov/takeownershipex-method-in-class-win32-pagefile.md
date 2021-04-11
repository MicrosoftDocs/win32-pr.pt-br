---
description: Obtém a propriedade do arquivo de paginação lógica especificado no caminho do objeto. Esse método é uma versão estendida do método TakeOwnerShip.
ms.assetid: 6c359910-713a-441e-b2e1-949929c07e93
ms.tgt_platform: multiple
title: Método TakeOwnerShipEx da classe Win32_PageFile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PageFile.TakeOwnerShipEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5b0f4662b4884da227a64768cc29bce4c615f8f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104163908"
---
# <a name="takeownershipex-method-of-the-win32_pagefile-class"></a><span data-ttu-id="d5f5c-104">Método TakeOwnerShipEx da classe de \_ arquivo de paginação Win32</span><span class="sxs-lookup"><span data-stu-id="d5f5c-104">TakeOwnerShipEx method of the Win32\_PageFile class</span></span>

<span data-ttu-id="d5f5c-105">O método de [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **TakeOwnerShipEx** Obtém a propriedade do arquivo de paginação lógica especificado no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-105">The **TakeOwnerShipEx** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method obtains ownership of the logical paging file specified in the object path.</span></span> <span data-ttu-id="d5f5c-106">Esse método é uma versão estendida do método [**TakeOwnership**](takeownership-method-in-class-win32-directory.md) .</span><span class="sxs-lookup"><span data-stu-id="d5f5c-106">This method is an extended version of the [**TakeOwnerShip**](takeownership-method-in-class-win32-directory.md) method.</span></span> <span data-ttu-id="d5f5c-107">Se o arquivo lógico for, na verdade, um diretório, esse método agirá recursivamente, assumindo a propriedade de todos os arquivos e subdiretórios contidos no diretório.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-107">If the logical file is actually a directory, then this method acts recursively, taking ownership of all of the files and subdirectories the directory contains.</span></span>

<span data-ttu-id="d5f5c-108">Este tópico usa a sintaxe formato MOF (MOF).</span><span class="sxs-lookup"><span data-stu-id="d5f5c-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d5f5c-109">Para obter mais informações sobre como usar esse método, consulte [chamando um método](/windows/desktop/WmiSdk/calling-a-method).</span><span class="sxs-lookup"><span data-stu-id="d5f5c-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f5c-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d5f5c-110">Syntax</span></span>


```mof
uint32 TakeOwnerShipEx(
  [out]          string  StopFileName,
  [in, optional] string  StartFileName,
  [in, optional] boolean Recursive
);
```



## <a name="parameters"></a><span data-ttu-id="d5f5c-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d5f5c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5f5c-112">*StopFileName* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d5f5c-112">*StopFileName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-113">Nome do arquivo ou diretório em que o método **TakeOwnerShipEx** falhou.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-113">Name of the file or directory where the **TakeOwnerShipEx** method failed.</span></span> <span data-ttu-id="d5f5c-114">Esse parâmetro será **NULL** se o método tiver sucesso.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-114">This parameter will be **null** if the method succeeds.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-115">*StartFileName* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d5f5c-115">*StartFileName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-116">Nomeia o arquivo ou diretório filho a ser usado como ponto de partida para **TakeOwnerShipEx**. O parâmetro *StartFileName* normalmente é o parâmetro *StopFileName* que especifica o arquivo ou diretório no qual ocorreu um erro da chamada do método anterior.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-116">Names the child file or directory to use as a starting point for **TakeOwnerShipEx**.The *StartFileName* parameter is typically the *StopFileName* parameter specifying the file or directory at which an error occurred from the previous method call.</span></span> <span data-ttu-id="d5f5c-117">Se esse parâmetro for **nulo**, a operação será executada no arquivo ou diretório especificado na chamada de ExecMethod.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-117">If this parameter is **NULL**, the operation is performed on the file or directory specified in the ExecMethod call.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-118">*Recursivo* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="d5f5c-118">*Recursive* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-119">Se **for true**, a alteração de propriedade será aplicada recursivamente aos arquivos e diretórios dentro do diretório especificado pela instância de [**\_ LogicalFile do CIM**](cim-logicalfile.md) .</span><span class="sxs-lookup"><span data-stu-id="d5f5c-119">If **true**, the change of ownership will be applied recursively to the files and directories within the directory specified by the [**CIM\_LogicalFile**](cim-logicalfile.md) instance.</span></span>

> [!Note]  
> <span data-ttu-id="d5f5c-120">Para instâncias de arquivo, o parâmetro *recursivo* é ignorado.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-120">For file instances, the *Recursive* parameter is ignored.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5f5c-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d5f5c-121">Return value</span></span>

<span data-ttu-id="d5f5c-122">Retorna um valor de 0 (zero) em caso de êxito e qualquer outro número para indicar um erro.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-122">Returns a value of 0 (zero) on success, and any other number to indicate an error.</span></span>

<dl> <dt>

<span data-ttu-id="d5f5c-123">**0**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-123">**0**</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-124">A solicitação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-124">The request was successful.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-125">**2**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-125">**2**</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-126">Acesso negado.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-126">Access was denied.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-127">**8**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-127">**8**</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-128">Ocorreu uma falha não especificada.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-128">An unspecified failure occurred.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-129">**9**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-129">**9**</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-130">O nome especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-130">The name specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-131">**10**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-131">**10**</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-132">O objeto especificado já existe.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-132">The object specified already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-133">**11**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-133">**11**</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-134">O sistema de arquivos não é NTFS.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-134">The file system is not NTFS.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-135">**12**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-135">**12**</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-136">A plataforma não é o Windows.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-136">The platform is not Windows.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-137">**13**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-137">**13**</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-138">A unidade não é a mesma.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-138">The drive is not the same.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-139">**14**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-139">**14**</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-140">O diretório não está vazio.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-140">The directory is not empty.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-141">**15**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-141">**15**</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-142">Houve uma violação de compartilhamento.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-142">There has been a sharing violation.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-143">**16**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-143">**16**</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-144">O arquivo de inicialização especificado não era válido.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-144">The start file specified was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-145">**17**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-145">**17**</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-146">Um privilégio necessário para a operação não é mantido.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-146">A privilege required for the operation is not held.</span></span>

</dd> <dt>

<span data-ttu-id="d5f5c-147">**Abril**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-147">**21**</span></span>
</dt> <dd>

<span data-ttu-id="d5f5c-148">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="d5f5c-148">A parameter specified is not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d5f5c-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d5f5c-149">Requirements</span></span>



| <span data-ttu-id="d5f5c-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="d5f5c-150">Requirement</span></span> | <span data-ttu-id="d5f5c-151">Valor</span><span class="sxs-lookup"><span data-stu-id="d5f5c-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f5c-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5f5c-152">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f5c-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5f5c-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d5f5c-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d5f5c-154">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f5c-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5f5c-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d5f5c-156">Namespace</span><span class="sxs-lookup"><span data-stu-id="d5f5c-156">Namespace</span></span><br/>                | <span data-ttu-id="d5f5c-157">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d5f5c-157">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d5f5c-158">MOF</span><span class="sxs-lookup"><span data-stu-id="d5f5c-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d5f5c-159"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d5f5c-159"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d5f5c-160">DLL</span><span class="sxs-lookup"><span data-stu-id="d5f5c-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5f5c-161"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5f5c-161"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5f5c-162">Confira também</span><span class="sxs-lookup"><span data-stu-id="d5f5c-162">See also</span></span>

<dl> <dt>

<span data-ttu-id="d5f5c-163">[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d5f5c-163">[Operating System Classes](/previous-versions//aa392727(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="d5f5c-164">**\_Arquivo de paginação Win32**</span><span class="sxs-lookup"><span data-stu-id="d5f5c-164">**Win32\_PageFile**</span></span>](win32-pagefile.md)
</dt> </dl>

 

